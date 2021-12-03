---
layout: essay
type: essay
title: "Instructions for Dummies, My journey with Design Patterns"
date: 2021-12-01
labels:
  - Design Patterns 
  - Meteor
  - MVC
---


After many years of copying solutions and looking towards other people for answers, design patterns have given me a way to do that, but in a proffesional manner. 


## Respect your elders  

The idea of design patterns is simple:

1. Find a problem, hopefully a common one, that many software developers have encountered
2. Create a description of the solution, containing the relationships of the classes/objects involved in the problem
3. Describe the consequences of using this design patterns 
4. Lastly find a cool name the encapsulates the problem

I mean 


## Patterns in my own work? Impossible 

In our group's final project Bow-Bites, I have spotted a few relationships that are similar to design patterns that I have learned. These design patterns include MVC (Model-View-Controller), Singleton, and Observers. 


### Singleton

Our code does have the pattern of Singleton. In Bow-Bites, there is a VendorCollection, which creates the mongo collection and has the schema for a vendor. The last line of our VendorCollection code: [here](https://github.com/bow-bites/bow-bites/blob/main/app/imports/api/vendor/Vendor.js#L44), is exporting a singleton instance of the VendorCollection called "Vendors". 

"Vendors" is now a "Global Variable" of sorts. We can import "Vendors" into any page/component by doing:

```meteor
import { Vendors } from '../../api/vendor/Vendor';
```

Once "Vendors" is imported we can access and edit the data in Vendors, from any page/component.

