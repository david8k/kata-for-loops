# Basic Programming Kata

## Introduction

This kata is intended to be coded in an iterative way. Follow each requirement by their own solely taking into account previous requirements. **Not** future ones.

As a prerequisite. The user that makes this Kata is expected to have at least slim knowledge about Java. To relief knowledge about testing, all the tests will be commented out of the code and can be added as soon as the requirements allow it.

In the end of this Kata. The user should have more knowledge on object oriented programming (polymorphism), looping, conditions and basic programming techniques.

## How to do this Kata

Get use to the code first. Run the tests by doing:

```./gradlew test```

If the tests are green, you can proceed to the first requirement.

### Doing the requirements

For each requirement it is really important that you look for the test's prefix `requirement_X` where X is the number of the requirement that you are intending to solve.

After you've identified that, delete the line `@skip` from those tests and run the tests by using `./gradlew test`.

You will notice that some tests are failing. It is your job to fix them, normally. The tests will pass again if the requirement is fully completed.

**Get to the next requirement if and only if all the tests are green**

##Requirements

### Problem statement

The TGB company (The Great Bill) has contacted us to solve an issue with their systems. As you may know, TGB is a great place to have something to dinner. However, lately, they've been trying to spice things up and make the customers do crazy stuff when paying their bills to enhance the user experience on the sites.

As so, they would like to standardize their bills from real numbers with two decimal points (such as *3.95*) to integer numbers representing the number with two decimal points (such as 395). And, with this in mind, create a set of rules based on the multiples of those numbers. For example, one rule can be that if the bill is multiple of 5, the client must jump. If it does, the client will be given a free round of beverages when they pay!

As TGB is huge and the bills can seemingly be infinite, we would like to solve this kata without using any sort of structure to handle memory (no lists, no maps)

### Requirement 1:

Given a number with two decimal points, return the string representation of that number with its decimal point to integers. (e.g. *3.95* is expected to become *"395"*)

### Requirement 2:

Given a number that is multiple of 10, return "Jump" instead of the number.

### Requirement 3:

Given a number that is multiple of 3, return "Scream" instead of the number.

### Requirement 4:

Given a number that is **both** multiple of 10 and 3, return "Scream and Jump" instead of the number.

### Requirement 5:

Given a number that has multiples of 3, 7 and 10, return "Scream, Stand Up and Jump" instead of the number.

### Requirement 6:

We would like to add new rules to the system without having to update it.

Go to the class `BillGame` and define a method `prepare` that will return an instance of a BillGame with the number set. Then, implement the method `rule` that will take a number and a string, we would like to consider that number as a multiple that, if successful, will create a new activity with the string name in it. After that, a method `apply` shall be called to apply those rules into the number fed.