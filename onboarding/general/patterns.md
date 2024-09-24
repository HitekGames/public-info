# Design Patterns in Software Engineering

Design patterns are standard solutions to common problems in software design and system architecture. They are not ready-made code snippets but rather templates for solving problems during development. Design patterns help developers create cleaner, more efficient, and optimized code. They are categorized into three main groups:

## 1. Creational Patterns
These patterns abstract the instantiation process. They help make a system independent of how its objects are created, composed, and represented.

- **Singleton**: Ensures a class has only one instance and provides a global point of access to it.
- **Factory Method**: Defines an interface for creating an object, but lets subclasses decide which class to instantiate.
- **Abstract Factory**: Provides an interface for creating families of related or dependent objects without specifying their concrete classes.
- **Builder**: Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.
- **Prototype**: Allows cloning objects without being coupled to their concrete classes.

## 2. Structural Patterns
These patterns deal with object and class composition. They help structure larger structures by combining objects.

- **Adapter (or Wrapper)**: Allows objects with incompatible interfaces to collaborate.
- **Bridge**: Decouples an abstraction from its implementation so that the two can vary independently.
- **Composite**: Allows clients to treat individual objects and compositions of objects uniformly.
- **Decorator**: Dynamically adds alternative behavior to objects.
- **Facade**: Provides a unified interface to a set of interfaces in a system.
- **Flyweight**: Minimizes memory use by sharing as much data as possible with other similar objects.
- **Proxy**: Provides a placeholder or surrogate for another object to control access to it.

## 3. Behavioral Patterns
These patterns are concerned with algorithms and the assignment of responsibilities between objects.

- **Chain of Responsibility**: Avoids coupling the sender of a request to its receiver by giving more than one object a chance to handle the request.
- **Command**: Encapsulates a request as an object, thereby allowing for the parameterization of clients with different requests, and support for undoable operations.
- **Interpreter**: Provides a way to evaluate language grammar or expression.
- **Iterator**: Provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation.
- **Mediator**: Defines an object that encapsulates how a set of objects interact.
- **Memento**: Without violating encapsulation, capture and externalize an object's internal state so that the object can be restored to this state later.
- **Observer**: Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.
- **State**: Allows an object to alter its behavior when its internal state changes.
- **Strategy**: Allows selecting an algorithm at runtime.
- **Template Method**: Defines the skeleton of an algorithm in an operation, deferring some steps to subclasses.
- **Visitor**: Lets a new operation be defined without changing the classes of the elements on which it operates.

Understanding and implementing these design patterns correctly can significantly enhance the scalability, maintainability, and performance of software applications.
