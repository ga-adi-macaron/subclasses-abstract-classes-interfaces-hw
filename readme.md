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

The difference between them is the static keyword which defines the class level. Static determines whether the method can be called and accessed within the Class or without creating a new instance. ex. Class.method(); vs. Class method = new Class();

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?

No because the public access modifiers allows programmers to change and modify the member variable, if it was private the getters and setters are needed because it cannot be modified outside the Class.

3. What are some benefits of making member variables `private`?

A beneift of making private member variables is that it can not be changed nor accessed by anyone since the access modifier is private and not public.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?

Classs B is the super class and Class A is the subclass. Class B is the parent and Class A is the child

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?

It means that all methods and member variable under the parent can be called and defined under the child class.

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?

It will cause an error because the method is not inside the parent class which is being called from Appliance. If it was called from the Refrigerator class it would solve this problem.

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?

In a Normal class it can simply be declared and defined from the class that it is impleting which is the abstract class.

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?

Yes, can implement methods and those methods are declared int a concrete class.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.

final keyword means that the method should not be change and are usually in capital letters

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?

It gets the method from the abstract clasee even if it hasn't define and can be defined in the child class.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/subclassing-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/interfaces-and-abstract-classes).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!

---

## Licensing
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact [legal@ga.co](mailto:legal@ga.co).
