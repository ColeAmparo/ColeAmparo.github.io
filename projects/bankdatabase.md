---
layout: project
type: project
image: images/bank.png
title: Bank Record Database
permalink: projects/bankrecorddatabase
date: 2020-12-05
labels:
  - C
  - C++
  - Pointers
summary: A database of bank records in a linked list, that are able to be added, deleted, or printed by a user.
---


<img class="ui medium left floated image" src="../images/bankPrint.png">

Summary
-----------------

When you start the program there is a prompt asking the user if they
want to add, delete or find a bank record in the database, or print all
the records in the database (Picture to the left). The user interface was simple enough. The
hard part was that each record was an object, that had a start pointer,
an account number, a name and an address. There are also functions that
can take in a textfile of an already created record database, and then
when the program is over print out the record database.

### Pointers and Linked Lists

In the database there is a linked list where the record with the
highest account number was pointing to the start, while the record with
the second highest account number was pointing to the first record, and this
continues until the list ends. When a new record is added to the
database, the pointer dereferences the account numbers and compares
them, and when the record has found its place in the linked list, the
record before it has to now point to the new record. 

## Contribution

I did all the work in this program, as well as converting it from C to
C++.

What I learned
----------------------------

One thing I learned from this project is the importance of **Knowing what
your code is doing.** Especially when it comes to pointers, if you make
a mistake on the syntax, the linked list will not function, and the
function addRecord might be comparing a records account number to a
different records name. Because I knew how the pointers worked it was
easier to translate this program into C++.

Link to the source code, in a GitHub Repository
[Here](https://github.com/ColeAmparo/CppLinkedListRecordDatabase).


