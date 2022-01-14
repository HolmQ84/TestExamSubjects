## 1.3 - Test without code
Explain what kinds of tests can be carried out without running any code. 
Explain how it can be used on non-code documents as well.
***
### Reviews

Formelle reviews:

- Aftalt møde.
- Alle får materiale på forhånd, for at være forberedte.
- Der findes løsninger, som vedtages og nedskrives.

Informelle reviews:

- Kaffemaskine møder.
- Impulsive
- Ingen nedskrevne løsninger. 

***
### Technical reviews

A Technical review er en 'statisk white-box testing' teknik.

- Bruges til at finde/løse fejl i koden.
- Nå til konsensus.
- Tekniske specialister deltager.
- Ledelsen deltager ikke nødvendigvis.
- Ledes normal af en moderator (Må ikke være ham der har skrevet koden).
- Dokumenteres med fundne fejl og løsninger på problemerne.

***
### Management reviews

Systematisk evaluering af udviklingen.

- Ledelsen står for den, sammen med en erfaren programmer (Moderator, Senior Dev, Architect)
- Undersøger om tidsplanen holder i forhold til deadlinen.
- Ser på allokeringen af developers.
- Gennemgår de forskellige programmørers arbejde.
- Hvis nødvendigt kan der ændres i 'scopet' på projektet.
- Dokumenteres med:
  - Project under review.
  - Review team members to check their skills and technical know-how
  - Defects in the system.

***
### Audit

Uafhængig undersøgelse af et software produkt.

- Vurderer produktets overensstemmelse med kravsspecifikationerne (FURPS).
- Tjekker for kode standarder.
- Kontraktmæssige forhold og aftaler.

Relaterer til Quality Assurance (QA)

Formålet er at lave en uafhængig undersøgelse af:
- Projektet som helhed
- Aftalte standarder

***
### Static analysis
####What is Static analysis?
Analysing code without running it.

- Manual code review


- Automatic code review
  - Analysis
  - Contracts
  - Proofs
  
    
####Why Static analysis?
Prevent bugs instead of fixing them.

####Manuel code reviews

WTF's per minute.

####Automated Approaches - Model
- Cyclomatic Complexity (CC)
  - A metric used to indicate the complexity of a program
  - Higher number = More complex code = Bad.

Flow graphs are used to calculate CC within a software program.

Formula for calculating code complexity:

    V(G) = E - N + 2
V(G) = the maximum number of independent paths in the graph.\
E = Number of edges.\
N = Number of nodes.

    V (G) = P + 1
P = predicate nodes. (Nodes that contain conditions)

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
### Linters

Linters er et analyserings værktøj - del af Statisk Analyse.

Automatisk værktøj - køre sideløbende med kodning - modsat fx. QAPlug.

Fordele:

- Færre fejl efter programmet er sat i produktion.

- Tjekker for 'code smell'.

- Tjekker for syntaks fejl og strukturelle fejl.

- Tjekker for afvigelser fra kode standarder.

Vi har brugt SonarLint.