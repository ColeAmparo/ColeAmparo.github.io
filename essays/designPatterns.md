---
layout: essay
type: essay
title: "Design Patterns are a Legal Way to Cheat"
date: 2021-12-01
labels:
  - Design Patterns 
  - Meteor
  - MVC
---


Sometimes I think I'm a masochist for frustration, I like playing difficult video games and I'm a Computer Science major. If I am trying to beat a difficult boss, and I can't do anything by myself, I'll scour the internet for solutions... and the responses vary:

>> Get better lol
>> Uninstall.
>> The boss has a pattern of attacking overhead with a sword and then dashing back immediately, if you want to approach you have to dodge the sword and run at him while he dashes back. 

Most of the time bosses do have patterns that you can learn and exploit for your own advantage, and the same thing goes for coding! 

When coming up with solution for how to approach a problem, there's a good change that multiple people have had 



## Respect your elders  

The idea of design patterns is simple:

1. Find a problem, hopefully a common one, that many software developers have encountered
2. Create a description of the solution, containing the relationships of the classes/objects involved in the problem
3. Describe the consequences of using this design patterns 
4. Lastly find a cool name the encapsulates the problem

I mean 


## Patterns in my own work? Impossible.

In our group's final project [Bow-Bites](https://github.com/bow-bites), I have spotted a few relationships that are similar to design patterns that I have learned. These design patterns include MVC (Model-View-Controller), Singleton, and Observers. 


### Singleton

Our code does have the pattern of Singleton. In Bow-Bites, there is a VendorCollection, which creates the mongo collection and has the schema for a vendor. The last line of our VendorCollection code: [here](https://github.com/bow-bites/bow-bites/blob/main/app/imports/api/vendor/Vendor.js#L44), is exporting a singleton instance of the VendorCollection called "Vendors". 

"Vendors" is now a "Global Variable" of sorts. We can import "Vendors" into any page/component by doing:

```meteor
import { Vendors } from '../../api/vendor/Vendor';
```

Once "Vendors" is imported we can access and edit the data in Vendors, from any page/component.

<img class="ui tiny image" src="../images/vendors-singleton.png">

> For example we can map through vendors, making each one a vendor item, and then displaying them as a list. 

### MVC 

I was excited to play some Marvel vs. Capcom, but the design pattern of Model-View-Controller (MVC) is exciting in it's own way. After learning about MVC, I was suprised to see how much of that design pattern I can see when it comes to meteor. In our final project 

