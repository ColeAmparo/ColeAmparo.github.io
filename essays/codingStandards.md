---
layout: essay
type: essay
title: Coding Standards are the Best Adhesive for Inefficient Programming
date: 2021-09-22
labels:
  - ESLint 
  - Javascript
---

Why are coding standards necessary? For every language that I learned throughout my academic journey in coding, there were always different coding standards that I had to adhere to. For Java we used CheckStyle, for C we adhered to the ANSI C standard, and in ICS 314 we are using ESLint for Javascript. 

One might say: 

> Coding standards are unnecessary because if my code works it doesn't matter what it looks like."

To that person I would say: 

> Sure, but good luck finding people that want to work with you!

Learning how to adhere to coding standards will not only make it easier to work in a group, but will also improve your own understanding of a programming language. Using linters like ESLint will also make programming more efficient.


## The benefits of Coding Standards

Unless you are some freak of nature hacker-man, there will always be times where group work is necessary for software engineering. When working in a group it can be hard if every programmer has their own way of programming, and a solution to that problem is coding standards. When the whole group is adhering to the same coding standard, there will be less time-waste on trying to understand each other's code. Having to spend less time going over code quality and coding style leads to a more efficient workflow on a project. Overall coding standards make it easy to maintain a program and detect errors when working with multiple programmers


## ESLint and IntelliJ

My experience with ESLint has been positive thus far. ESLint is a linter, which means that it flags various syntax errors and makes sure that the code adheres to the coding standard. One nice thing about ESLint is that you can see errors before execution, which streamlines the coding process. Instead of being stuck in the tedious loop of: 

> executing --> checking for syntax errors --> executing --> etc

Instead, when the error is made it's highlighted and ready to be fixed. 

### The cons of ESLint

One element of ESLint that I didn't like was the "Quick-Fix" that ESLint gives when it flags an error. The "Quick-fix" is a suggested solution by ESLint to fix the errors of your code, but when abused it enables lazy code writing. I wrote a badExample function with a lot of syntax errors, unsafe equality operators, and usage of 'var' instead of 'const' or 'let'.


```javascript
var number = 3;
function badExample  (num  ) {
  if  (num == 1) {
    return true
  } else if (num == 2  ) {
    return true
     } else {
    return false
  }
}



badExample(number )
```

Instead of looking at the ESLint error flags and understanding what I did wrong, I simply pressed "ESLint: Fix current file" and it formatted the code to adhere to the coding standard: 

```javascript
const number = 3;
function badExample(num) {
  if (num === 1) {
    return true;
  } if (num === 2) {
    return true;
  }
  return false;
}

badExample(number);
```

There were 18 errors highlighted by ESLint in badExample and with the press of a button the code is correct. Having suggested solutions is great for when you look at the code and understand the error. However when quick fixes are being abused by programmers who don't understand the errors not only is it a detriment to the program, but also a detriment to the user themselves. There is no ESLint when you are in a technical interview so bad habits won't automatically get fixed for you. Of course, the errors in badExample are obvious and you could invoke "ESLint: Fix current file" to save time, but when you do that with larger programs it will be harder to find what was fixed, and if it was even fixed correctly.

## Conclusion 

In conclusion, researching coding standards has made me realize why I was forced to use them while learning to program. First, coding standards are a staple in software engineering because coding standards can make the code from different programmers consistent with one another. Secondly, coding standards can help improve a programmer's efficiency, especially when using linters like ESLint. Using linters can have downsides but overall coding standards are necessary for both group work and solo work.
