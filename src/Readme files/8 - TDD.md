# 1.8 - Test Driven Development
Explain test driven development, and how it affects the development process and code quality.

****
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
****