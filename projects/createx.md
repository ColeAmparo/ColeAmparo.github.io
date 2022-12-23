---
layout: project
type: project
image: images/createxThumbnail.png
title: Developing for Create-x
permalink: projects/createx
date: 2022-10-08
labels:
  - Unity 
  - C#
  - Kinect
summary: I created a game where a player has to physically move around to dodge oncoming projectiles. 
---



## Overview 

Create-X is a kit that uses two Kinect cameras to track the joint positions of a human player, an show it on the screen as a skeleton. Using that kit I created a game where a player has to physically move around to dodge oncoming projectiles. 

## Video:

[Link to the video](https://youtu.be/DqAXcq1dW00)


## Methods 

The Create-X kit included the skeleton model and the joint tracking. To create the missiles I made two scripts “Shooter” and “Bullet”. 


Shooter class 

```cs
public class Shooter : MonoBehaviour
{
 
   public GameObject addBullet;
   private GameObject player;
   private float lastTimeShooted = 0;
   private int shoot;
 
   public static int currHealth;
 
   // Start is called before the first frame update
   void Start()
   {
       this.player = GameObject.FindGameObjectWithTag("Player");
       currHealth = 100;
       shoot = Random.Range(3, 15);
   }
 
   // Update is called once per frame
   void Update()
   {
       //shoot = Random.Range(3, 15);
 
       if((lastTimeShooted + shoot) < Time.time) {
           GameObject newInstance = Instantiate(addBullet);
           newInstance.transform.position = this.transform.position;
           // Bullet bullet = newInstance.GetComponent<Bullet>();
           // newInstance.Target = this.player;
           lastTimeShooted = Time.time;
       }
   }
}
```

The shooter script creates an instance of an object every 3 - 15 seconds. This object it creates is a bullet object with the bullet script. The shooter script instantiates the bullet object, sets its position to be by the shooter, and then aims at the target (which is the player). 


Bullet Class: 

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
 
public class Bullet : MonoBehaviour
{
 
   private float Speed = 3.5f;
   public GameObject Target;
   public HealthBar healthBar;
   Rigidbody m_Rigidbody;
 
 
   // Start is called before the first frame update
 
   void Awake()
   {
       Target = GameObject.FindGameObjectWithTag("Player");
   }
 
   void Start()
   {
       if (Target != null) {
  
 
           m_Rigidbody = GetComponent<Rigidbody>();
 
           m_Rigidbody.AddForce(Vector3.forward * Speed);
 
       }
   }
 
   // Update is called once per frame
   void FixedUpdate()
   {
       if (Target != null) {
           /*float step = Random.Range(1,5) * Time.deltaTime;
           this.transform.position = Vector3.MoveTowards(this.transform.position, Target.transform.position + new Vector3(0,0.5f,0), step);
 
           Vector3 relativePos = Target.transform.position - this.transform.position;
           var halfWayVector = (Vector3.up + Vector3.right).normalized;
           Quaternion bulletRotation = Quaternion.LookRotation(relativePos, halfWayVector);
           this.transform.rotation = bulletRotation;*/
 
           m_Rigidbody.AddForce(Vector3.forward * Speed);
       }
   }
 
   public void OnTriggerEnter(Collider other)
   {
      
       if (other.gameObject.tag == "targetBox") {
           Debug.Log("skeleton hit");
           Shooter.currHealth--;
           int sendHealth = Shooter.currHealth;
           healthBar.setHealth(sendHealth);
       }
 
       if (other.gameObject.tag != "ShootBox") {
           GameObject.Destroy(this.gameObject);
       }
 
   }
 
}
```

Every Bullet spawned from the shooter class has this script attached to it. Originally the trajectory of the bullet was updated every second to track the player. It turned out to be too difficult to dodge, so instead, I made the bullet shoot forward. This script also shows the OnTriggerEnter function that decrements the health bar every time the player hits a bullet. 

