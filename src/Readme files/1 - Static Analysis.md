## 1.1 - Static Analysis

We have looked at some static analysis tools like StyleCop, PMD, FindBugs and SonarLint. 
Explain how static analysis can improve code quality. 
Explain how it helped you or could have helped you in your project.

***

### Static Analysis generally

Static Analysis is the automated analysis of source code without executing the application.

When the analysis is performed during program execution then it is known as Dynamic Analysis.

Static Analysis is often used to detect:

- Security vulnerabilities (Such as security risks of SQL injections)
- Performance issues (Cyclomatic Complexity - Duplicated Code - Unused functions, variables or classes)
- Non-compliance with standards.
- Use of out of date programming constructs (Deprecated libraries and classes)

All the above will create vulnerabilities in a program, wheither it's related to potential security breaches, 
performance issues or future disabled functions which results in a non-functional code.

Therefore, using a static analysis tool will greatly increase your chances of improving the code, 
which will result in a better product in the end.

Another useful usage for static analysis tools are for junior developers to get a better understanding 
of where to focus on improving their skills and thus creating better code.

#### Automated Approaches - Model
- Cyclomatic Complexity (CC)
    - A metric used to indicate the complexity of a program
    - Higher number = More complex code = Bad.

Flow graphs are used to calculate CC within a software program.
![img_1.png](Images/img_1.png)

Formula for calculating code complexity:

    V(G) = E - N + 2
V(G) = the maximum number of independent paths in the graph.\
E = Number of edges.\
N = Number of nodes.

    V (G) = P + 1
P = predicate nodes. (Nodes that contain conditions)

Example:

    i = 0;
    n=4; //N-Number of nodes
    
    while (i<n-1) do
    j = i + 1;
    
    while (j<n) do
    
    if A[i]<A[j] then
    swap(A[i], A[j]);
    
    end do;
    i=i+1;
    
    end do;
![img_2.png](Images/img_2.png)


    V(G) = 9 – 7 + 2 = 4
    V(G) = 3 + 1 = 4 (Condition nodes are 1,2 and 3 nodes)
    Basis Set – A set of possible execution path of a program
    1, 7
    1, 2, 6, 1, 7
    1, 2, 3, 4, 5, 2, 6, 1, 7
    1, 2, 3, 5, 2, 6, 1, 7


Basis Path testing is one of White box technique, and it guarantees to execute at least one statement during testing.
It checks each linearly independent path through the program, which means number test cases, will be equivalent
to the cyclomatic complexity of the program.

This metric is useful because of properties of Cyclomatic complexity (CC) –

1. CC can be number of test cases to achieve branch coverage (Upper Bound)
2. CC can be number of paths through the graphs. (Lower Bound)


    If (Condition 1)
    Statement 1
    
    Else
    Statement 2
    
    If (Condition 2)
    Statement 3
    
    Else
    Statement 4

Cyclomatic Complexity for this program will be 8-7+2=3.

| Complexity number | Meaning                                                                          |
|-------------------|----------------------------------------------------------------------------------|
| 1 - 10            | Structured and well written code<br>High Testability <br>Cost and Effort is less |
| 10 - 20           | Complex Code <br>Medium Testibility <br>Cost and effort is minimum               |
| 20 - 40           | Very complex code <br>Low testability <br>Cost and efforts are High              |
| >40               | Not at all testable <br>Very high Cost and Effort                                |


Other tools for static analysis:
- Checkstyle
    - Coding standards and conventions.
- FindBugs
    - Finds bugs and potential future bugs
- PMD
    - Warns about bad practices

***

#### Security



#### Code smell



#### Technical debt

Technical debt (also known as tech debt or code debt)
describes what results when development teams take actions to expedite the delivery of a piece of
functionality or a project which later needs to be refactored. \
In other words, it's the result of prioritizing speedy delivery over perfect code.

### Programs and plugins for static analysis

#### FindBugs



#### SonarLint



#### PMD



#### Checkstyle
