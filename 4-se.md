Design Patterns
===

If you have THIS situation, then THIS programming technique might help.

System Modelling
---

Better to design first, then implement

* abstractions: what classes will I have
* relationship between classes

Formal technique: UML(Unified Modelling Language)

A UML class is a box

name of class | Vec
--- | ---
<ul><li>fields(optional)</li><li>-private +public</li></ul> | <ul><li>- x:integer</li><li>- y:integer</li></ul>
method | <ul><li>- getX</li><li>+ getY</li></ul>

Coupling and Cohesion
---
Coupling: Degree to which modules depend on each other

Low Coupling: desirable

* Program to an interface
* Do no care about implementation details

High Coupling: depend on low level implementation

* friends
* public fields

Cohesion: how related are components within a module

* High Cohesion: desirable
* Low Cohesion: no separation of concerns

Singleton Pattern
---

We have a class C and we want only one instance (object) to be created (throughout life of the program)
Example: database connection, error log

See provided example code

Observer Pattern
---

Publish-Subscribe model

Some entities which publishes/generates data: The Subject

Other entities which subscribe to data to react/consume it: The Observer

See provided example code

Decorator Pattern
---

See provided example code

Factory Method Pattern
---

Enemies: Turtle, Bullet, Boss (singleton)
Level: Normal, Castle

```C++
while(Game not end) Enemy *e = l->createEnemy();
```

* Compartmentalizes enemy creation logic inside levels
* Ability to have different logic based on levels

Singleton and factory method pattern often work together. Imagine a Boss enemy, there is only one Boss.

```C++
while(Game not end) Enemy *e = e->createEnemy();
```

See wiki

Template Pattern
---

Put same code in a superclass. No subclass can override non-virtual private methods.

See provided example code

Visitor Pattern
---

Double Dispatch: make a decision on which method to call based on the type of tweet objects.

See provided sample code
