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

A: Member variables can have different copies and variations while class variables are usually initialized inside its' own class and have only one instance across the program. Class variables can be accessed without creating an instance of the class.

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?

A:It doesn't if getter and setter methods are created for public member variable because it is accessible and can be modified anywhere. Private variables however is required to have getter and setter because user can't access or modify the variable directly. 

3. What are some benefits of making member variables `private`?

A: This is to prevent the users from tempering the values and giving the developers more control of what the values should be passed along.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?

A: Class B is the parents/super class. Class A is the child/sub class.

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?

A: Inheriting the parent class means the sub class can access the parent's method or variable, provided that it is public.

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?

A: It is because myAppliance is declared as myAPpliance class(despite being created as "new Refrigerator()"). Also getTemperature() is not declared in Appliance. Therefore, when the compiler is running it is treated as Appliance. 
By Casting it in (Refrigerator), myAppliance will be treated as Refrigerator class before calling the getTemperature method.

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?

A: In a normal class, you only need to declare some methods but it is required to implements all abstract methods. In abstract class, you only need to declare those methods that are abstract.

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?

A: You can only declare methods in interface but not implementation. 

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.

A: An abstract class cannot be created as an instance on its own because it basically served as a blueprint for the developer to add on. The reason why a class can't be both final and abstract is because 'final' put a final initialization onto the variable while abstract has been implemented into other classes and override. 

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?

A: When you @Override a method, the new method will be the one being execute. The method from the child class will be executed. 

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?

A: LinkedList and ArrayList implement List Interface. A method is polymorphic when it ignores which class is calling it and changes  and acts according to the concrete class that is calling it. 

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/subclassing-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/interfaces-and-abstract-classes).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!

---

## Licensing
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact [legal@ga.co](mailto:legal@ga.co).
