# 1.8 - Test Driven Development
Means driving the design development of the code using tests as specifications
****
###Red, Green, Refactor
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
****
### Maintainable code
****
### Equivalence partitions
****
###Positive, negative tests
****