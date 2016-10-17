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
    }}--->> Member variables are initiated when an object is instantiated, and are variables for just that instance. Static class variables are the same for every object created in that class.

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?
    }}--->> Doesn't make sense for public mVariables because you can already access them in other classes. For private, that is the sole reason you'd make a getter and a setter, so yes it does make sense.

3. What are some benefits of making member variables `private`?
    }}--->> It prevents people from changing the variable to something that it shouldn't be.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?
    }}--->> B is the parent && super class, A is the child && sub class.

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?
    }}--->> It means that any public method written within a parent class can be accessed by an object instantiated with the class of the child. 

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?
    }}--->> myAppliance has the attributes of an Appliance. Casting it as a Refrigerator will give it the methods available to Refrigerator.
  

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?
    }}--->> An abstract class has at least one method that is just declared. In a concrete class, all of the methods must be implemented.

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?
    }}--->> An interface only has declared methods, no implemented methods.


9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.
    }}--->> An abstract class must be extended to another class. A final cannot be extended. So something can't be abstract AND final. 

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?
    }}--->> If a parent and a child have methods with the same name, you must tag the child class to @Override so that it executes the child's method instead of the parent's method of the same name.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?
    }}--->> List is an interface to LinkedList and ArrayList. A method is polymorphic if it can take multiple data types and figure out which one you're trying to input. Like, if it's a list of ints and you put a double in, it won't read an error, but instead turn the double into an int or all the ints into a double, etc. Maybe, I'm not sure about this one exactly. 

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/subclassing-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-macaron/Course-Materials/tree/master/lessons/programming-fundamentals-in-java/interfaces-and-abstract-classes).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!

---

## Licensing
1. All content is licensed under a CC­BY­NC­SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact [legal@ga.co](mailto:legal@ga.co).
