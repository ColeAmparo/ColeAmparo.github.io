---
layout: essay
type: essay
title: I thought Java WAS Javascript
date: 2021-08-31
labels:
  - Javascript
  - Learning
---

Even though I am in my third year of the ICS program, I am embarrassed
to admit that I thought Java and Javascript were the same thing. I
didn’t have time to think about the difference because it has been a year
since I have touched Java, due to mainly programming in C for ICS 212. So when I
started doing the “intro to Javascript” exercises I thought I was already
familiar with the language. Boy was I wrong.

## Benefits of Javascript

First of all Javascript feels easier to use compared to C or Java because of small changes. Not
having to specify your variable, being able to access characters in a
string by using array notation, the list goes on. Secondly there is a
much wider *array* of things that you can do in Java.

### Variable type doesn’t matter, put it in an Array!

Being able to put any data type: integers, arrays, functions, strings,
all in one array -as well as being able to access them- is nothing short
of useful. In Javascript, functions are first class so not only can you
put them in an array, you can use a function as a variable for another
function which gives a lot of options to the user, and I can realize
that even if I don’t know how to make use of it.

### Quick and simple objects

Creating objects in Javascript is also easy as well, for example:

```
const dog = {

“breed” : “Golden Retriever”;

“name” : “Harley”;

}
```

You have an object with two properties just like that. To be honest
learning object oriented programming in C was such a pain that I didn’t
want to do it anymore, but with how easy it seems to make complex
objects in Javascript and manipulate them, it makes me want to give it a
second chance.


Lets talk about WODs
--------------------

To be honest I was dreading WODs (Workout of the day), which are timed
exercises worth 100 points that are pass/fail. Now that I have had some
time to practice WODs I realize that they are preparing me for
technical interviews. It does matter if you understand a concept, but it
is useless if you can’t apply it. WODs force you to apply the concept
that you are learning into actual programming, and at first it will be
ugly, you will make syntax mistakes, and you will fail, but that is part
of the process.


### An example

```
function eulerProjectOne(max) {
  let result = 0;
  for (let i = 0; i < max; i++) {
    if ((i % 3 === 0) || (i % 5 === 0)) {
       result += i;
    }  
  }  
  console.log(result);
}
eulerProjectOne(1000);
```

The first practice WOD that I did was a function that took a number as a parameter and returned the sum of all multiples of 3 and 5 under this number, which in this example was 1000. The first time I attempted this WOD I did not finish it under a passable time, which was frustrating. It was because I was so nervous about the WOD being timed that I forgot about the mod function. When doing WODs failure is part of the process but I tried again and again until I got a good time.



## Conclusion: Practice and Failure

It’s easy when you have a couple hours to work on a trivial
program (like the example above), you could even look it up on google you will probably find code that
you can copy. However when it is a timed exercise and you only have the
information in your brain. Not only do WODs convince you to study the
material, they also show that failure is a part of the computer science
process. I am sure that I will get a DNF in one or two WODs this
semester, but if I can learn from the mistakes not only will I improve
in the WODs, I will become a better programmer overall.
