Tips for memorizing:
    - Slow down. Stop and think.
    - Do the excercises
    - Read there are no dumb questions
    - DESIGN SOMETHING!

### Chapter 1: Intro

disadvantages of using inheritance to provide duck behaviour
    <!-- - Code is duplicated across subclasses -->
    - hard to gain knowledge of all duck behaviours
    - changes can unintentionally affect other ducks

Inheritance
    - Inheritance isn't the answer when not all subclasses have the same behaviour
    - have no implementation details so no code reuse. Will need to change functionality in all class that implement the interface

###### Design Principle 1
- Identify aspects of your application that vary and seperate them from what stays the same
- Take what varies and encapsulate it so you can extend later

Over time application will grow and change
    - customer or user decide they want something else
    - company using new vendor/tech
    - management want to new feature
    - competitor created a new feature and now your boss wants the same feature


###### Design Principle 2
- Program to interface, not to an implementation

```Java
// Programming to an implementation
Dog d = new Dog()
d.bark()

// Programming to an interface
Animal dog = new Animal()
animal.makeSound()

```

Duck behaviours live in a seperate class
- Make a class to represent behaviour

Integrating duck behaviour
    - duck will now *delegate* its' flying and quacking behaviour

    - Add two instance variables to Duck class called FlyBehaviour and QuackBehaviour
    - replace fly() and quack() method on Duck class with performFly() and performQuack()

###### Design Principle 3
- Favour composition over inheritance

Composition gives much more flexibility, allows to change behaviour at runtime

#### Strategy Pattern
- The Strategy Pattern defines a family of algorithms,
encapsulates each one, and makes them interchangeable. Strategy
lets the algorithm vary independently from clients that use it.
