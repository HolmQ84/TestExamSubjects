## 1.4 - Test Activities
Explain test activities, and how they are related to each other.\
Then explain the test activities you carried out in your project.
***
### Unit testing
####What?
The goal of unit testing is to test each unit in isolation. \
We test the smallest units possible.\
Examining each unit.

- It's a piece of the code.
- Must test a unit of work.
- Must be automated.
- Must communicate errors found. (Expected vs actual result)\


<b>Class</b>

    public class Calculator {
        public int add(int a, int b) { return a+b; }
    }
<b>Test for the class</b>

    public class AddTest{
    
        @Test
        public void zeroPlusOneMustGiveOne() {
    
        // Arrange
        Calculator c = new Calculator();
    
        // Act
        var result = c.add(0,1);

        // Assert
        Assert.equals(1, result);
        }
    }
####Why?
The claims are:\
- It helps to fix bugs early in development.
![img.png](Images/unitTest1.png)

![img.png](Images/UnitTest2.png)

- It helps developers understand the code base.
  - By reading unit tests, you can see how the unit is used.
  - By writing unit tests, you have to think about use cases, edge cases, fault scenarios.
  

- It serves at documentation
  - Reading unit tests gives an understanding of the intentions / expectations.
  - Keeping unit tests is like keeping a log of requirements.

- It helps write code re-use 
  - Used in TDD, refactoring is an essential step, where code is used again.

####Purity
- Pure functions are easier to test
  - Returns the same value, when same argument(s) are given.
  - Has no side effects

Makes the function deterministic, meaning it is easier to test as it acts more like a mathematical function.
####Naming
Test names should be as descriptive as possible and consistent. (Camel case / SnakeCase)

Makes it easier to identify test that fails, and documents the intended behaviour.
***
### Integration testing
![img.png](Images/IntegrationTest.png)

Integration testing is defines as a type of testing where software modules are integrated logically and tested as a group

Integration testing focuses on checking data communication amongst modules.

This type of test focuses mainly on the interface and flow of data/information between modules, where priority is given\
to the integration link rather than the unit test, which has already been tested.

The integration could be with another system, which makes it a black-box testing.

Approches:
- Big Bang
- Top Down
- Buttom Up
- Sandwitch - combination of Top down and Buttom up
***
### Refactoring

***
### Maintenance

***
### Continuous Integration

***
### Code reviews

