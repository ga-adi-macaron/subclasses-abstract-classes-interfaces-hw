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

	A class variable is shared amongst all instances of the class. If it changes, it affects all instances.
	However, member variable is unique to each Instance. Each instance can potentially hold a different value becuase they all have their own versions of the variable;

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?

	For a public member variable, no. It can already be accessed directly by other classes.
	Private member variables cannot be accessed by other classes. UNLESS they go through a public getter and or setter.

3. What are some benefits of making member variables `private`?

	It forces foreign classes to access them through getters or setters.
	For setters, this allows a programmer to put some filters in place as to prevent invalid/unwanted values for member variables.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?

	Class B is the super or parent class. Class A is the sub or child class.

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?

	It means the child class, too, has these methods and variables (Although not in the same file).
	What the programmer is declaring is "the objects that belong to this child class ALSO belong to this parent class".

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?


	Even though at run-time, myAppliance is actually a Refrigerator, the compiler only looks to the left of the assignment operator.
	The compiler thinks myAppliance is just an Appliance. Since the Appliance class does not contain the getTemperature() method, it says
	"Hey man, I don't see that method in this class. You can't run this."

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?

	Concrete classes must implement ALL of their methods (inherited or not).
	Abstract classes by definition don't need to be concrete. They may have methods that are declared but not implemented.

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?

	You can declare as many methods as you'd like. But you cannot implement any of them.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.

	No, you cannot create an instance of an abstract class.
	A final class cannot be extended. An abstract class MUST be extended in order for its methods to ever be implemented. The two conflict one another.

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?

	When a method is overridden, it is changing the method for that class and all of it's subclasses.
	Once overridden, a method called through an instance of the child class will run the overridden version instead of the super class' version.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?

	LinkedList and ArrayList are both child classes of the List class.
	I assume polymorphic means 'many forms'. It allows us to hold variables with the type of an object's super class.
	This technique allows for maximun flexability and generalzation when desired.

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/subclassing-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/interfaces-and-abstract-classes).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!

---

## Licensing
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact [legal@ga.co](mailto:legal@ga.co).
