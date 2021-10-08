---
layout: essay
type: essay
title: Dear Semantic UI, U & I will go great together!
date: 2021-10-06
labels:
  - Semantic UI
  - CSS Frameworks
  - HTML5
---

Dear Semantic UI, I know we had a rocky start, there was many a time that I didn't understand how to use you fully to the extent of your ability and to be honest I'm sure I have only dipped my toes into the vast amount potential you hold. I love the way that you already have built in classes that I can use and manpulate to make proffesional looking websites. I love learning about the new things I can do with you: use ui containers to make sure the margins of my wepbages are aligned, using menus and dropdowns, placing my information into columns and rows, and touching all your buttons. Semantic UI you are an *ICON* to me in many ways. This letter is a recap of the start of our relationship, the struggles, the victories, and the hope for our future together.

##Semantic UI and CSS Frameworks

At first I didn't really know what you were. I had learned the basics of you from my ex, CSS, and heard you were a UI Framework but I didn't know what that meant. After I did some research I found out that a UI Framework is a collection of pre-existing style classes that you can use right away! In simpler terms Semantic UI contains a bunch of elements like menus, buttons, icons, labels, etc,. that look polished. For example, once you load Semantic UI into the  html file you can create a menu section on your website by typing:

```html
<div class="ui menu"></div>
```
The code above create a div that is a menu and no matter if you put **a**, **div**, **img** in that div, if they have "item" included in their class that they will become part of the menu.

Example:

```html
<div class="ui menu">
<a class="item"></a>
<button class="ui button item"></a>
<img class="item"></a>
</div>
```

Just like that you have a menu with a link, a button, and an image! If you weren't using Semantic UI you would manually have to create a menu in the linked CSS style sheet. To be honest I had a hard time changing a list to a nav bar so when I found out that that there was an easy way to make elements that looked nicer than basic CSS it piqued my interest. In the code above the class for the button was "ui button item", since Semantic UI already has a style class for buttons (ui button) you can add that infront of "item" and the button will be aligned with the other items, as well as having the same padding and margins.

##Struggles

After the honeymoon phase of using Semantic UI, it was time to make a copy of a website I choose in E36, I realized that I only knew a little bit about Semantic UI. Until this point, all the WODS we have done had clear directions of how to make the website with Semantic UI. When I started on this WOD I stared at my computer for 30 mins, it wasn't because I had a lack of options using Semantic UI, it was because I had *too* many options. I spent hours playing around with containers, simple dropdown, menus, lists, buttons. I would add one word to the class and then check to see if it looked similar to the orginal. At this point it was more guessing and checking, rather than looking up the documentation and finding the correct class name. Even worse than that is when I tried to copy the code for a button from the Semantic UI website, and added it to my menu/list. One would think that it would work as promised on the website, but when it doesn't it's hard to find out what is wrong because you did not create the classes.

##A small victory

After a couple hours I made my version of the website using semantic UI and it turned out like this:

    <img  style="width: 300px" src="../images/Original.png">

    
    <img style="width: 300px" src="../images/SemanticUI.png">



