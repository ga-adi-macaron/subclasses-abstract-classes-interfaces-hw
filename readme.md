---
title: Subclassing and Interfaces
type: Homework
duration: "1:00"
creator:
    name: Charlie Drews
    city: NYC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Subclassing, Abstract Classes, and Interfaces

> ***Note:*** _You can discuss with classmates, but everyone must submit their own answers_

## Exercise

#### Requirements

- Fork this repo, then add your answers direcly to this **readme.md** file
  - After forking, you can clone, edit the readme in the text editor of your choice, and push back to Github...
  - Or, you can edit the readme [right from the browser](https://help.github.com/articles/editing-files-in-your-repository/)
- After adding your answers, submit a **pull request**

#### Questions

1. What is the difference between *member variables* (also called *instance variables*) and *class variables* (w/ keyword `static`)? Which can be accessed without creating an instance of the class?

Typically, member variables are unique to each object of a given class. A class variable is a variable shared with all objects that belong to that class. 
An example could be if you have a Commodity class, you can set a supply variable that increments with each new Commodity object that is created. When calling a getSupply() on any object of that Commodity class, you will get the same value depicting the total supply of that Commodity.


2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?

There is nothing stopping you from writing a getter/setter method for public member variables, but you can interact with them without the need for those methods. Ex. Object.mVariable=newValue; x= Object.mVariable;
For private member variables, since you can't interact with them outside of the class you need to use getter/setter methods.

3. What are some benefits of making member variables `private`?

It prevents users from editing the member variables from outside classes and possibly breaking your program, it prevents colission if there's other variables with the same name in another class.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?

Class B would be the super class, class A is the sub class. The parent is the super class(class B) and child is the sub class(class A).

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?

A child class inherently has all of the methods and/or variables that it's parent class has; the child class is an appendment of the parent class.

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigerator*, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?

Calling "getTemperature()" causes an error because that method is not defined in the superclass "Appliance" since many appliances don't worry with temperature.
By casting "myAppliance" to a Refrigerator you give it access to the methods that are exclusive to the Refrigerator subclass. 


7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?

In a concrete class methods must be declared & implemented. In an abstract class you can choose to only declare your methods.


8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?

For an interface you can only declare methods. There is no implementation of methods in an interface. If a class is a blueprint for an object, an interface is a blueprint of a blueprint.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.

The "final" keyword is a declaration that the following variable is in it's final form and can't be edited. Inherently abstract objects can't be final because they are not complete objects.

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?

When a method overrides another method it tells java: "Even though this method exists in a super class I want you to run the one in the child class instead with these instructions." So if you call an override method that has the same name in parent and child, the implementation in the child class is the one that will be executed.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?

List is the parent class for LinkedList and ArrayList. It is called polymorphic because it has multiple types and can be cast into a multitude of other types, meaning an Arraylist can be cast as either a List or an ArrayList. It is useful because it gives us flexibility in what type of data we are passing as an argument.

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/subclassing-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/interfaces-and-abstract-classes).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!

---

## Licensing
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact [legal@ga.co](mailto:legal@ga.co).
