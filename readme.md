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
Member variables are not directly accessible outside of the class and can only be accessed in the main method by creating an instance of the class and calling a getter.

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?
Only for a private member variable, since a public variable can be accessed from any class.

3. What are some benefits of making member variables `private`?
You can control how it can be changed by a user, or even a developer implementing the class.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?
super/parent class: B
sub/child class: A

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?
The child class can use the methods and variables of its parent class

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?
  getTemperature() only exists in the Refrigerator class. Casting myAppliance with (Refrigerator)my.Appliance will declare this instance of the Appliance class as a Refrigerator.

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?
A normal class can have method declarations or implementations, while an abstract class's abstract methods cannot be directly implemented

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?
An interface must be implemented by a class and can only contain method declarations.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.
You can't create an instance of an abstract class, but can use a subclass. A final abstract class would have no value and would be immutable, so it cannot exists.

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?
A subclass can override a method to create a different outcome from calling that method. When you call the child class, the '@Override' method will be executed.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?
List is an interface implemented by LinkedList and ArratList. A method is polymorphic because it behaves differently depending on the type of List it is being called from.

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/subclassing-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/interfaces-and-abstract-classes).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!

---

## Licensing
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact [legal@ga.co](mailto:legal@ga.co).
