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

Every object of a class has its own version of the member variables when they are initialised. However, regardless of the object number; a static variable is only created one per class and shared between all objects of that class. Static variables can be accessed without creating an instance of that class.

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?

It doesn't make sense to write a getter and setter method for public member variables as they can be accessed directly from other classes. However, for private member variables it is mandatory to have getter and setter methods if we want to access or modify those variables.

3. What are some benefits of making member variables `private`?

It lets you to manage the complexity easier. Because it can only be accessed from within the class it is defined; when we have a problem with it; we know exactly where to look for.
It also prevents from other programmers to access and modify it; in case we don't want to.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?

B is super, parent. A is sub, child.

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?

It means that the child class can use the variables and/or methods from the parent class as if they were declared within the child class.

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = ((Refrigerator(myAppliance)).getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?

  It would cause and error. I have corrected it on the code.

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?

In a normal class you have to implement all the methods. However in an abstract class you just need to declare them.

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?

In an interface you just declare methods; you cannot implement any methods.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.

No, you cannot create an instance of an abstract class. A final class can't be extended, an abstract class needs to be extended in order to be instantiated. Therefore, a final abstract class would be a logical contradiction.

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed? 

When a method overrides another method; it essentially changes the way the other method runs. We get @Override as an indicator to show us that the method in the parent class has been overridden. If a parent and child class have methods with the same name; child class's implementation will be executed.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?

List in an interface; so LinkedList and ArrayList implement List. It is useful; because it allows you to switch between different implementations of the List interface with ease. For instance; let's say that I've started a code with "List list = new LinkedList();" but then I realised that LinkedList was inappropriate for my situation and an ArrayList was better. By changing the code to "List list = new ArrayList();" I can change list type I use without worrying if I the rest of my code will have any problems.


#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/subclassing-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/interfaces-and-abstract-classes).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!

---

## Licensing
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact [legal@ga.co](mailto:legal@ga.co).
