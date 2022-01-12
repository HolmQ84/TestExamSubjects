## 1.12 - Test Automation 
Explain problems in test automation, and how a continuous integration tool can help.
***
### What is Continuous Integration?
When deploying code, we can hit "Merge hell" when pushing to the cloud, if we don't push often enough.

When we use Continuous Integration, we push everytime we have built a small piece that is tested and works. It doesn't
have to be a full functioning program.
In GitHub when we push, we can add automation which always keeps an eye on the code. When code is pushed, it
automatically builds the code and tests it. then it pushes the code to the others in the team.

if a conflict occurs, an email is sends to the team, telling where the conflict is, and who has been working on the code.
this makes sure that we always have a testable build.

***
### How can a CI help regarding tests?

CI helps in 2 ways.

1. CI allows automation of regression test

_"Automated tests are great at handling regressions, making sure new changes don’t break the application. But it can only cover the areas that have test scenarios written for them."_

2. CI Run a complete set of tests and, on success, automatically deploy the latest code changes to production.


Continuous integration can provide the entire team with better insight into the project’s health by generating reports and valuable metrics. Developers can receive feedback as soon as they commit new changes, saving tons of effort in correcting the inevitable issues that arise during development. Testers will have more time to work on high-value tasks. Finally, CI services can handle almost all of your workflows automatically.

***
### What is a regression?

The purpose of regression testing is to establish whether changes to the system have broken existing functionality or caused old defects to resurface

**As sson as a test is added to an automated suite of tests, it becomes a regression test**

***
### What test levels can be covered by a CI system?

1. Unit testing ✅

2. Integration testing ✅

3. System testing⛔
   
Så vidt jeg kan se er det ikke muligt at system teste

3. Acceptance test ✅
