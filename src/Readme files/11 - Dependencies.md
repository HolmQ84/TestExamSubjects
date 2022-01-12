## 1.11 - Dependencies 
Elaborate on dependencies in software, and how it’s related to the subject of the test.
***
### Dependencies between layers
Most applications are layered. Each layer has responsibility for some specific functionality,
like presentation or business logic.

Dependencies between layers is just dependencies between program elements.

Although layered architecture enforces strict separation between the layers and dependencies
in **one** direction, typically in the majority of cases, such architectures become more "flexible"
and contains some bypasses.

Layers become challenging when they are violated and bypassed.

A good way of writing layers together that often ensures testability is using **dependency inversion** and 
**dependency injection** frameworks.


***
### System resources

***
### Relations between objects

***
### Dependency inversion, Inversion of Control, Dependency Injection

Dependency inversion principles (DIP) states that **High level modules should not depend on low level module;
Both should depend on abstractions. Abstractions should not depend on details. Details should depend upon abstractions**

DIP is one of the SOLID principles and part of Inversion of Control to obtain loose coupling.

The general idea is to ensure that the business Logic Layer doesn't have direct access to the data access layer.

This is done by implementing abstraction in form of an interface between the two layers, which insures that the method 
calls goes through the interface, instead of the data layer.

####When this is done we have not obtained loose coupling yet, only that the classes are loosely coupled.

**Dependency injection and strategy patterns** is used to move the dependency object creation completely out
of the classes.

Dependency injection pattern involves 3 types of classes.
1. **Client class:** The client class (dependent class) is a class which depends on the service class.
2. **Service class:** The service class (dependency) is a class that provides service to the client.
3. **Injector class:** The injector class injects the service class object into the client class.
![img.png](Images/DependencyInjection.png)

**Three types of injections**
- Constructor injection
- Property injection
  - Method injection


      public class CustomerService {
          CustomerBusinessLogic _customerBL;
    
          public CustomerService(){

              _customerBL = new CustomerBusinessLogic(new CustomerDataAccess());
          }
    
          public string GetCustomerName(int id) {
              return _customerBL.ProcessCustomerData(id);
          }
      }

In the example above, CustomerDataAccess() in injected into CustomerBusinessLogic() in the service class.

#### These principles lead to Inversion of control.
Ioc is basically to obtain loose coupling in our program and by that make the code more maintainable.

The IoC principle suggests inverting the control, meaning that instead of driving the car yourself, you hire a 
cab, where another person will drive the car.



***
### Mocks
