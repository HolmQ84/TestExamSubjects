# 1.5 - Code Quality
Testing is related to ensuring higher code quality. 
Elaborate on what characterizes high code quality, and what makes code testable.
***
## Testable code

To create testable code, it's important to follow a set of principles.

### SOLID principles.

#### S - Single Responsibility Principle.

Each module should only have one responsibility.

*Example*\
Imagine that you write a program that calls an external REST API endpoint, 
does some kind of processing with the received data and writes it to a CSV file.\
A naive approach might be to have everything in the same class.

With this approach, it will be very difficult to test - thus you should split each responsibility into its own class.

#### O - Open/Closed Principle.

Your classes should be open for extensions, but closed to modifications.

#### L - Liskov Substitution Principle.

Objects of a superclass should be replaceable with objects of its subclasses without breaking the application.

#### I - Integration Segregation Principle.

No client should be forced to depend on methods it does not use.

#### D - Dependency Inversion Principle.

High-level modules should not depend on low-level modules; both should depend on abstractions.\
Abstractions should not depend on details. Details should depend upon abstractions.

***
### Names of tests



***
### “sufficient” tests of a method or class



***
### Assertions, defensive programming



***
### Dependency injection

