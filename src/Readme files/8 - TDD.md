# 1.8 - Test Driven Development
Explain test driven development, and how it affects the development process and code quality.

****
Means driving the design development of the code using tests as specifications
****
###Red, Green, Refactor
Red, Green, refactor is the TDD mantra.

1. Write a test that fails.
2. Simplest thing we can think of, to get our test to pass.
3. Refactor the code, so when going forward, the code will be as easy to change as possible


- In TDD we don't Declare our classes, but writes a test that uses a class, where the test forces us to declare the class.
  In essence, through our tests, we are making design decisions, - a few in each test -
  neither do we declare the methods.


- This is not only about writing failing tests, and then making them pass. We also need to refactor code if necessary.
  So make sure to do code review, duplicated code, similar tests.


- After refactoring first time, I remove some duplicated knowledge of how to create a shopping basket,
  which decouples my test code from the API's that I am testing. If useful the following tests should be easier to write.

****
### Testable code
To create testable code, it's important to follow a set of principles.

###### Observability

First of all, we need to make sure that the SUT (System under Test) is observable.
Without the possibility to check wheither or not our tests have made the impact we wanted, the test will be useless.

Observability should be thought about very early in the development phase, to make sure the SUD is programmed correctly for later testing.

The different ways of observing a SUT, can include:

- Debugging
- System Outputs
- Loggers

###### Controllability

Controllability is the ability to change the states of something in a SUT.

It is both neccesary to test functionality, but also leads to reproducibility.

A state means the possibility to change fields, variables or parameters to produce different outputs.

###### - Deployability

Deployability is a measure of the amount of work needed to deploy a given system.

To get a rough feeling - ask yourself:

"How long does it take to get a change that affects one line of code into production."

###### - Isolability

Isolability is, as the name suggests, the focus on isolating code parts as much as possible.

In many ways, it is similar to low coupling - and therefore desirable for both developers and testers.

The lower coupling a programs modules have, the easier it is to test and reuse the modules.

###### Smallness

The smaller the software, the better testability - because there's less to test.

###### Singularity

If something is singular, there's only one instance of it.

In systems with high singularity, every behavior and piece of data have a single source of truth.
Whenever we want to make a change, we make it in one place.

###### Level of Abstraction

Level of Abstraction is determined by the choice of programming language as well as the IDE.

With modern languages and frameworks, they tend to do a lot of things 'under the hood', which means that there's less code to test.

###### Efficiency

Efficiency refers to the ability to use the given programming language's functionality to keep the code expressive and concise.

###### Reusability

Reusability means using third-party components to avoid reinventing the wheel.
When using components from previous systems or from external source codes, we can make sure that the SUD is as
small as possible, which again means fewer tests needed to be done.

****
### Maintainable code
To write maintainable bode, we have to keep the following in mind when we write our program:

- Low coupling, high cohesion
Is how easy the code is to work on for another developer and maintain.
This suggests that we through our code keep a low coupling and high cohesion.

- Static Analysis
We have to be aware of our code complexity through static analysis, where we use tools such as 
Cyclomatic Complexity, findBugs (To chek for present and future bugs), checkStyle (Keep coding standards and conventions)
and PMD. (Warns about bad practices)


- Continuous Integration
Is so that we always keep a tested and new build running. 
It also insures that when frequently pushes of code, merge conflicts won't cause too much refactoring.


****
### Equivalence partitions

A software technique that divides the input data of a software unit input into partitions of
equivalent data from which test cases can be derived.\
It can be seen as a sort of black box testing technique.

- It divides input data of software into different equivalence data classes.
- You can apply this technique, where there is a range in the input field.

###

If you are to make a calculator that adds two sums together, is it then necessary to check if it calculates 5+5 correctly when you have testet for 4+4 and 3+3?
Equivalence partitions is a grouping of the same datatype.

Some equivalence partitions(classes) could be:

Males/females
* Those aged 0 to 17, 18 to 28, 29 to 44 and so on.
* those registered in the system before the year 2000 and those after.
* Prospects, regular, or premium customers.
* Those who pay with Visa, Mastercard, or PayPal.
* Those who have returned some merchandise and those who haven't.

****
###Positive, negative tests

Two test strategies in software testing are positive testing and negative testing.

**Positive Testing**
Determins that your application works as expected. If an error occurs during positive testing, the test fails.

**Negative Testing**
Ensures that your application handle invalid inputs or unexpected user behaviour. - For example if a user tries to
type letters in a numeric field, the correct behaviour in this case would be to display "Incorrect data input".
****
