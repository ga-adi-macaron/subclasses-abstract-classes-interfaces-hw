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
	*class variables hold a value for all instances in the code while member variables are very similar but do not hold their value through the entirety of the code but only in the instance they are in
	*class variables

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?
	*yes because they are able to be accessed throughout the code so to get the variable it is easier to use a getter method.
	*no because private variables are only available in the class they are in, if you want to access them elsewhere you need to make a new public variable that calls the private one and then a new getter/setter to easily access it

3. What are some benefits of making member variables `private`?
	*keeps code a bit cleaner and avoids using variables you don’t want used

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?
	*Super/Parent=classB
	*subclass/Child=classA

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?
	*it means that all methods/variables defined in the parent class are in effect in the subclass.
	ParentClassA - holds 2 variables (A,B)
	ChildSubclassB - adds 2 variables (C,D) all variables active are A,B,C,D
	ChildSubclassC - adds 2 other variables (E,F) all var active are A,B,E,F

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?
	*an error will occur because there is no getTemperature method in Appliance so Java doesn’t know what you are trying to call
	*casting by changing Appliance to Refrigerator would fix the error because then it knows that there is a getTemp method inside Refrigerator class and can access it from there

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?
	*you need to implement all of the methods or make the concrete class into an abstract class
	*in an abstract class you just need to declare the methods

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?
	*only if you need to later on in a project, the new ‘default implementations’ help your program from breaking if you add a method after the interface has been implemented
	*you can declare an abstract method because the whole interface is considered an abstract object

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.
	*yesss? kind of.. you can create a subclass with no changes that calls the methods and variables from the abstract class
	User(abstract)
	V	     V
   Admin	  GeneralUser
the Admin subclass adds certain permissions to the user but the GeneralUser subclass has no new values and is essentially an ‘instance’ of the user class.
	*it cannot be both because a ‘final’ class cannot be changed and is the final instance of that class. if it is abstract it will be used and values can/will be changed still

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?
	*@Override indicates that this method declaration is intended to override a method from a superclass, the method with the override tag will be used

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?
	*List = parent class / LinkedList & ArrayList = child class
	*It is polymorphic because the List class is a very complex class and can reference its child classes within itself
#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/subclassing-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/interfaces-and-abstract-classes).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!

---

## Licensing
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact [legal@ga.co](mailto:legal@ga.co).
