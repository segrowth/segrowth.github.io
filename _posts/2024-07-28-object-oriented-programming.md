---
title: Object-Oriented Programming
authors: [imyrta, kjodlows]
date: 2024-07-28 00:00:00 +0200
categories: [Software Engineering, Junior]
tags: [Technical Skills, Programming Paradigms, Object-Oriented Programming]
image:
  path:  /commons/post-img-people.png
---

> This is part 3 of our Programming Paradigms series, [click here]({{ site.baseurl }}{% link _posts/2024-05-12-declarative-programming.md %}) 
to see the previous part if you missed it!
{: .prompt-info }

## The Most Common Paradigm: Object-Oriented Programming

### What kind of programming style is it?

The most common, potentially the most used subset of an Imperative Style is Object-Oriented Programming (OOP).

OOP is a style of organizing software design and development around <b>objects</b>, which are <b>instances</b> of 
<b>classes</b> containing their <b>state</b> and <b>behavior</b>. It emphasizes the concept of an object as a 
fundamental building block of a given program, allowing data and behavior to be encapsulated. OOP facilitates a modular 
approach and promotes code reuse. It also enhances software design by modeling real-world entities or abstract concepts
using objects and their characteristics, based on <b>inheritance</b>, <b>polymorphism</b>, <b>encapsulation</b>, and
<b>abstraction</b> itself. It's a very logical concept, and even if seems to be very abstract, it's rather an easy one
to understand for humans. 

> There's a lot of programming languages that support OOP, e.g. Java, Python, C++, Go, and JavaScript.
{: .prompt-info }

### What's so unique about OOP?

There is a set of different characteristics specific to object-oriented programming:

<details>
<summary><b>Encapsulation</b> - Data and methods are bundled, and details are carefully managed.</summary>
<ul>
The way this can be achieved is by using access modifiers like <i>public</i>, <i>private</i>, <i>protected</i>, 
<i>getters</i>, and <i>setters</i>, which can either hide or expose values, essentially hiding the intricate details of
the implementation.
</ul>
</details>

<details>
<summary><b>Inheritance</b> - When classes are allowed to inherit attributes or methods from other classes.</summary>
<ul>
This establishes a relationship, in which we have base classes, commonly known as <b>superclasses</b>, and then 
<b>subclasses</b> or what are differently known as derived classes. Inheritance can be expressed through keywords like 
<i>extends</i> or <i>inherit</i>, and having inheritance allows us to achieve things like polymorphism. 
</ul>
</details>

<details>
<summary><b>Polymorphism</b> - When objects of different classes are treated as if they are objects of a common 
superclass.</summary>
<ul>
This allows the objects to take a variety of forms. This can be achieved by methods such as <b>overriding</b> (runtime
polymorphism) or <b>overloading</b> (compile time polymorphism)). 
</ul>
</details>

<details>
<summary><b>Abstraction</b> - A simplified representation of a complex system, hiding the implementation details.</summary>
<ul>
You don't see what is underneath but only what was exposed by the implementer. This can be done through <b>abstract
classes</b>, <b>interfaces</b>, <b>templates</b>, or different generics in some languages. 
</ul>
</details>

<details>
<summary><b>Classes and Objects</b> - Basic code blocks definition and their instantiation.</summary>
<ul>
A class is used to define the structure and behavior of an object, which is an <b>instance</b> of a <b>class</b>. This 
is achieved through class <b>definitions</b>, object <b>instantiation</b>, <b>constructors</b>, and <b>destructors</b>.
</ul>
</details>

<details>
<summary><b>Message Passing</b> - Objects communicate and interact with each other by sending messages.</summary>
<ul>
This "communication" is done through the <b>method invocation</b>, <b>method calls</b>, passing <b>arguments</b>, and 
<b>returning</b> values.
</ul>
</details>

<details>
<summary><b>Object relationships</b> - Define how the objects depend on each other.</summary>
<ul>
These relations can be of different types:
<ul>
<li><b>associacion</b>: there can be one-to-one, one-to-many, or many-to-many relationships</li>
<li><b>composition</b>: one object is composed of another object (object containment or a complex object using simpler
objects)</li>
<li><b>aggregation</b>: objects that have relationships are grouped together and put, however, the objects themselves
still exist independently (through the forming of larger structures and shared ownership)</li>
<li><b>dependency</b>: an object depends on another object, typically due to the method parameters or association
(object and method dependencies, or dependency injection)</li>
</ul>
</ul>
</details>

<details>
<summary><b>Design Patterns</b> - Solutions to common software design problems.</summary>
<ul>
These already-designed and proven effective patterns are categorized into groups like <b>creational</b>, 
<b>structural</b>, and <b>behavioral</b>. Some notable examples are the <b>Singleton pattern</b>, 
<b>Observer pattern</b>, and <b>Strategy pattern</b>. When having a specific problem, one might find that there are a
few patterns that can be applied to solve it. Once a pattern is identified, it can be reused over and over.
</ul>
</details>
\
All of the above characteristics are somehow connected, because they emphasize the relationships inside and between the
objects. First of them (encapsulation, inheritance, polymorphism, and abstraction) are even called as the <b>Four
Pillars of Object-Oriented Programming</b>, an absolute must know when it comes to this paradigm. Objects can implement
different functions/methods or have the same structure as other objects, in the same time relations between those
objects can be addressed with the design patterns.

### Code examples

It's time to take a look at Object-Oriented programming code examples. It's hard to go through all the mentioned OOP
concepts, but let's talk about - what we believe are - the most important ones. We picked four of them:

#### Encapsulation

A simple example illustrating encapsulation might look like this:
```java
public class Circle {
    private double radius;

    public double getRadius() {
        return radius;
    }

    public void setRadius(double radius) {
        if (radius > 0) {
            this.radius = radius;
        }
    }
}
```

Encapsulation in object-oriented programming is demonstrated through the use of access modifiers and methods to expose
or hide class internals. The example provided, a `Circle` class, utilizes a <i>private</i> <b>access modifier</b> for
the `radius` attribute to encapsulate its details:
```java
    private double radius;
```
This restricts its access solely to the internal methods of the class. This restriction is a core aspect of
encapsulation, ensuring that the internal state of an object is shielded from direct external modification or access.

Interaction with the `radius` is mediated through <i>public</i> <b>getter</b> and <b>setter</b> methods:
```java
    public double getRadius() {
        return radius;
    }

    public void setRadius(double radius) {
        if (radius > 0) {
            this.radius = radius;
        }
    }
```
The getter method, `getRadius`, allows external entities to access the value of the `radius`. Being public, it
facilitates reading the radius without altering it. On the other hand, the setter method, `setRadius`, incorporates
logic to check the validity of the `radius` value (it must be greater than zero). This ensures that the object maintains
a valid state at all times, demonstrating encapsulation's capability to enforce data integrity and constraints.

As can be seen above, there's a a significant aspect of encapsulation: <b>control over data exposure</b>. If it were
necessary to make the radius inaccessible, removing the getter method would effectively hide the radius entirely from
outside access. This selective exposure is a strategic decision in encapsulation, reflecting on why certain data should
be hidden or exposed.

Encapsulation supports <b>clean coding</b> principles by confining data manipulation logic within the class, thus
preventing its spread across the codebase. This confinement simplifies maintenance and understanding of the code. It
also raises points on potential complications if the radius were <i>public</i>, emphasizing that such an approach, while
doable, complicates external code and is generally not recommended.

Through encapsulation, the `Circle` class maintains a clean and controlled <b>interface</b> for interacting with its
internal state, illustrating encapsulation's pivotal role in building robust and maintainable software.

#### Inheritance

Inheritance is a cornerstone concept in object-oriented programming that facilitates the reuse of code by allowing
classes to inherit properties and methods from other classes. The mechanism for this is the `extends` keyword in Java:
```java
public class Vehicle {
    protected String brand;

    public void drive() {
        System.out.println("Driving the vehicle");
    }
}

public class Car extends Vehicle {
    private int numberOfDoors;

    public void honk() {
        System.out.println("Honking the car horn");
    }
}
```

The `Vehicle` class serves as the base class with a <i>protected</i> attribute `brand` and a method `drive()`:
```java
public class Vehicle {
    protected String brand;

    public void drive() {
        System.out.println("Driving the vehicle");
    }
}
```

The `protected` <b>access modifier</b> ensures that these members are accessible to subclasses, unlike <i>private</i> 
members, which are not accessible.

The `Car` class illustrates a subclass of `Vehicle`:
```java
public class Car extends Vehicle {
    private int numberOfDoors;

    public void honk() {
        System.out.println("Honking the car horn");
    }
}
```

It inherits the `drive()` method from its superclass and adds its own attributes and methods, such as the <i>private</i> `numberOfDoors` and the <i>public</i> method `honk()`. The honk method, when called, outputs a specific message, 
demonstrating how subclasses can have different functionalities from their base classes.

When a `Car` object is <b>instantiated</b>, it inherits both the behavior of the superclass (`drive()`) and integrates
its unique behavior (`honk()`). This ability to incorporate and extend superclass behavior is fundamental to
inheritance. Moreover, subclasses like `Car` can further manipulate inherited properties if they are accessible (i.e.,
not <i>private</i> in the superclass), and can add additional methods to utilize these properties, such as manipulating
the `brand`.

> <b>Instantiation</b> is one of the fundamental principles in object-oriented programming. It involves creating an
instance of a class, which is akin to forming an object from a blueprint. By instantiating a class, you create an object
ready for use within your program.
{: .prompt-info }

Inheritance enables classes to build upon existing code, promoting code reusability and reducing redundancy. The 
<i>extends</i> keyword is pivotal, enabling subclasses to access and extend the functionalities of their superclasses,
provided the <b>access levels</b> <i>protected</i> or <i>public</i>. This hierarchy not only streamlines the development
process but also enhances the logical grouping and scalability of applications.

#### Polymorphism

Once you understand encapsulation and inheritance, it's impossible not to mention polymorphism. Here is a slightly more
extensive example:
```java
public interface Shape {
    double calculateArea();
}

public class Circle implements Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}

public class Rectangle implements Shape {
    private double length;
    private double width;

    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }

    @Override
    public double calculateArea() {
        return length * width;
    }
}
```

The `Shape` <b>interface</b> defines a method `calculateArea()`, that must be implemented by any class that implements
that interface:
```java
public interface Shape {
    double calculateArea();
}
```
This setup facilitates polymorphism where different geometric figures such as circles and rectangles
implement this method to compute the area specific to their shape.

> In OOP, an <b>interface</b>, or protocol type, serves as a data type that abstracts a class. It specifies a collection
of <b>method signatures</b>, which can be implemented by various classes that may not be related to each other. When a
class supplies the methods outlined in it, it's considered to have adopted the protocol or <b>implemented the
interface</b>.
{: .prompt-info }

Each class (`Circle` and `Rectangle`) implements the `calculateArea()` method differently:

- The `Circle` calculates area using the formula for the area of a circle, which requires the `radius`:
```java
public class Circle implements Shape {
    ...
    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}
```

- The `Rectangle` calculates area based on the formula for the area of a rectangle, requiring 
`length` and `width`:
```java
public class Rectangle implements Shape {
    ...
    @Override
    public double calculateArea() {
        return length * width;
    }
}
```

<b>Constructors</b> play a critical role in defining how objects of a class are instantiated. For instance:

- A `Circle` object is instantiated with a mandatory `radius` parameter, essential for later area calculations:
```java
public class Circle implements Shape {
    ...
    public Circle(double radius) {
        this.radius = radius;
    }
    ...
}
```

- Similarly, a `Rectangle` requires `length` and `width` at instantiation, underscoring the dependency of the area 
calculation on these parameters:
```java
public class Rectangle implements Shape {
    ...
    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }
    ...
}
```

> A <b>constructor</b> is a special method designed to create an object, named the same way as the class. It initializes
the new object, typically taking arguments that help set essential member variables for immediate use. 
{: .prompt-info }

The constructors not only define how objects are instantiated but also - by letting the parameters be passed only when
the object is initialized - to encapsulate the necessary parameters. Both classes encapsulate their respective
dimensions (`radius`, `length`, and `width`) by making them <i>private</i>, thereby restricting direct access from
outside the class:
```java
public class Circle implements Shape {
    private double radius;
    ...
}

public class Rectangle implements Shape {
    private double length;
    private double width;
    ...
}
```
This encapsulation ensures that the dimensions are set only during object creation and used internally for calculations
without further modification. The encapsulation extends to behaviors (methods) as well. Classes implementing the `Shape`
interface encapsulate the logic for area calculation within the `calculateArea()` method, exposing only the result, not
the internal calculation logic:
```java
public class Circle implements Shape {
    ...
    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}

public class Rectangle implements Shape {
    ...
    @Override
    public double calculateArea() {
        return length * width;
    }
}
```

Polymorphism allows the creation of flexible systems where components can be easily interchanged. It simplifies code
management and increases the system's extensibility. In the context of the example provided:

- Objects of both `Circle` and `Rectangle` can be treated as `Shape` objects.
- This ability allows for writing more general and reusable code that can interact with any `Shape` object, leveraging
the polymorphic behavior of the `calculateArea()` method.

Polymorphism, through the use of interfaces and abstract classes, provides a powerful tool for creating flexible and
easily manageable code. It promotes a clear separation of behaviors and an abstraction layer that allows different
objects to implement standardized behaviors in their unique ways. By understanding and applying polymorphism, developers
can enhance both the functionality and scalability of their software designs.

#### Composition

Composition is the last foundational design principle in object-oriented programming we want to investigate. It models a
"has-a" relationship between objects. This principle allows the creation of complex objects by combining simpler and 
constituent objects. The following Java example demonstrates composition through a `Car` class that contains an
`Engine`:

```java
public class Engine {
    public void start() {
        System.out.println("Engine started");
    }
}

public class Car {
    private Engine engine;

    public Car() {
        this.engine = new Engine();
    }

    public void startCar() {
        engine.start();
        System.out.println("Car started");
    }
}
```

In this example, the `Engine` class represents a real-life engine with a basic functionality to start, encapsulated in 
the `start()` method. This simple method prints "Engine started" to indicate the engine's operation:
```java
public class Engine {
    public void start() {
        System.out.println("Engine started");
    }
}
```

The `Car` class illustrates composition by incorporating an `Engine` object as a <i>private</i> field:
```java
public class Car {
    private Engine engine;
    ...
}
```

This design reflects the real-world scenario where a car inherently possesses an engine. The `Car` class does not
require an external engine to be passed at its creation; instead, it internally constructs an `Engine`:
```java
public class Car {
    ...
    public Car() {
        this.engine = new Engine();
    }
    ...
}
```
The constructor of the `Car` class initializes a new `Engine` when a `Car` object is instantiated. This design choice
implies that the engine is integral to the car, mirroring real-life situations where a car is typically sold with an
engine already installed. The encapsulated engine is a permanent component of the car, showcasing how composition binds
objects together.

When the `Car` starts, it activates its engine through the `startCar()` method, which in turn calls the `start()` method
of the `Engine`:
```java
public class Car {
    ...
    public void startCar() {
        engine.start();
        System.out.println("Car started");
    }
}
```
This sequence of method calls ("Engine started" followed by "Car started") illustrates how real-life actions (starting
a car) are simulated in programming through composition. The method `startCar()` effectively delegates part of its
responsibility to the `Engine` class, maintaining a clear division of roles and responsibilities.

Composition offers several advantages in object-oriented design:

- Modularity: It keeps the system modular by allowing separate classes to manage their responsibilities.
- Reusability: It enhances reusability through independent and interchangeable components.
- Maintainability: It simplifies maintenance by localizing functionality and limiting external dependencies.

Composition allows developers to create complex systems that are modular, easy to manage, and maintain. By embedding
objects within other objects, programmers can closely mimic real-life relationships and behaviors, providing a clear and
effective framework for building software applications.

### What can OOP be used for?

Each programming paradigm, including the subsets, shines in particular cases. For the Object-Oriented Programming,
these areas are: 

<details>
<summary><b>Modeling Real-World Entities</b> - OOP is well suited for modeling real-world entities and their
interfaces.</summary>
It can be used for solving problems in simulations, games, physical systems, financial systems, or any other type of
domain that depends on objects.
</details>

<details>
<summary><b>Software Development</b> - OOP provides a structured approach to software development.</summary>
It allows for modularity and reusable code and facilitates the organization and management of large codebases. It also
promotes maintainability, extensibility, and code reusability, which is why it's very common and one of the most popular
styles used out there (in about 80-90% of companies, OOP is used to solve problems).
</details>

<details>
<summary><b>Graphical User Interfaces (GUIs)</b> - Objects represent visual components like windows, buttons, menus.</summary>
OOP allows for the encapsulation of the behavior and the state of these components while handling user interactions. For
example, when a button is clicked, we can close a window, or we can have a dropdown menu, and then we can pick one of
the items from the menu, and another window can pop up.
</details>

<details>
<summary><b>Database Applications</b> - Objects can represent database tables, records, entities, and their relations.</summary>
There are a lot of libraries and frameworks based on object-oriented languages that provide interaction with databases.
E.g. in the SQL case, the database itself can be implemented through object-oriented programming, and evenn accessing
the data within the database or just making the connection can be represented through objects.
</details>

<details>
<summary><b>Web Development</b> - OOP is used for developing web frameworks and applications.</summary>
Many languages like Java, Ruby, or PHP, have their own object-oriented frameworks dedicated to web development. E.g. in
the case of Ruby, we have Rails; in the case of Python, we have Django; and in the case of PHP, we have Laravel. OOP
allows for modeling web entities such as users, articles, and products. It handles interactions within those objects, 
for example a user ordering a product or a user looking at an article.
</details>

<details>
<summary><b>Software Design Patterns</b> - Ability to solve problems with already-crafted solutions.</summary>
Object-oriented programming is closely associated with design patterns because it provides solutions to common design
problems. We strongly recommend visiting <a href="https://refactoring.guru/design-patterns">this website</a> to get
familiar with this important topic (also, we'll certainly take a closer look at them in the future;).
</details>


<details>
<summary><b>Collaborative Development</b> - A common language and structure to communicate between developers.</summary>
OOP allows the team to divide responsibilities and work on different modules independently and integrate their code much
more easily. This facilitates parallel development, speeding up the work, and then integrating everything at the end to
have a final product. Example: in the case of the engine and the car, one person can work on the engine basics and
another person on the car's characteristics, and they can merge their code together later.
</details>

<details>
<summary><b>Extensibility and Maintenance</b> - New features and code modification without affecting other parts of the 
system.</summary>
Encapsulation and inheritance allow developers to extend and modify code in a more controlled and maintainable manner,
making it easier to build software through object-oriented programming.
</details>

### Quick summary

While the Object-Oriented Programming may not be the optimal choice for every type of problem, it is undoubtedly the
most frequently used one. However, various other styles are available for solving different problems, with the selection
depending on factors such as problem complexity, requirements, team expertise, and performance considerations. Sill, OOP
broad applicability explains its popularity.

## Live discussion

Want to see a live discussion on the topic? Check out our YouTube recording:

{% include embed/youtube.html id='v7k9LVEdWJA' %}

## Stay tuned!

Guess what - we're not done yet with all we have for Programming Paradigms! We have already traveled through the most
general division which is Imperative and Declarative style and met the most famous Imperative style which is OOP. Next
time we’ll discuss an important Declarative style representative: Structured Query Language (SQL). We'll also make
a quick summary of the Programming Paradigms topic.
