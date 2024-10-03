# COT 3100 Discrete Structures - Exam 1 Review

<ins>Textbook</ins>: *Discrete Mathematics with Applications (5th ed.)* by Susanna Epp

<!-- The following tEx escapes do not render in GFM: \R, \Z, \empty                         -->
<!-- To render correctly, inline tEx blocks must not have characters directly after them    -->
<!-- There is no way to insert single tilde (~) in GFM tEx                                  -->

### Logic Symbols and their Meanings
| Symbol        | Pronunciation         |
|---------------|-----------------------|
| T             | *true*                |
| F             | *false*               |
| $\therefore$  | *therefore*           |
| $\in$         | *in*                  |
| $\supseteq$   | *is a superset of*    |
| $\subseteq$   | *is a subset of*      |
| \|, :         | *such that*           |
| $\forall$     | *for all*             |
| $\exists$     | *there exists a*      |
| *iff*         | *if, and only if*     |

## 1. Set Theory

- A *set* is some collection collection of elements
    - Can contain other sets
    - Typically denoted by a capital letter

>**Example:** Sets cannot be created from ambiguous conditions.
>
> A set of "good" students cannot exist because goodness is a subjective measure.

- Infinite sets can be denoted using ellipses ($\ldots$)
- $\emptyset$ is the empty (null) set, containing no elements
- **U** is the universal set, containing all possible elements
- *Subsets* are sets whose elements can all be found within another set
    - Other set is a *superset*
    - A set is always a sub- and superset of itself
- Denoting a set with duplicate entries is legal
    - Can be reduced to the same notation with unique elements

### Common Sets of Numbers
| Symbol    | Elements              | Examples                                                  |
|-----------|-----------------------|-----------------------------------------------------------|
| C         | complex numbers       | 2 + 7i                                                    |
| R         | real numbers          | $\pi$, 16                                                 |
| Z         | integers              | -3, 0, 24                                                 |
| Q         | rational numbers      | 0.25, 9                                                   |
| $^+, ^-$  | positives, negatives  | $R^+ = (0, \infty)$ is set of all positive real numbers   |

- $C \supseteq R \supseteq W \supseteq Z$
- Sets denoted in either
    - **Roster notation:** $\{ e_1,e_2,e_3, \ldots , e_n \}$
    - **Set builder notation:** $\{ var \space type? | condition \}$
        - **Ex:** $\{ x \in Z | x \lt 7 \} = \{ \ldots ,4,5,6 \}$

## 2. Statements and Logical Operators

### Logical Operators
| Notation              | Alternate Notation    | Name          | Pronunciations                | Condition for Truth                               | Equivalent Form                                   |
|-----------------------|-----------------------|---------------|-------------------------------|---------------------------------------------------|---------------------------------------------------|
| ~p                    | $\neg$                | negation      | *not p*                       | p is false                                        |                                                   |
| p $\land$ q           | &, AND                | conjunction   | *p and q*, *p but q*          | Both p and q are true                             |                                                   |
| p $\lor$ q            | OR                    | disjunction   | *p or q*, *p unless q*        | p or q are true                                   |                                                   |
| p $\oplus$ q          | XOR                   | exclusive-or  | *p or q, but not both*        | Exclusively either p or q are true                | (p $\lor$ q) $\land$ ~(p $\land$ q)               |
| p $\rightarrow$ q     | $\implies$            | conditional   | *if p, then q*, *p implies q* | Always true, unless p is true and q is false      | ~p $\lor$ q                                       |
| p $\leftrightarrow$ q | $\iff$                | biconditional | *p, if and only if, q*        | Both p and q are true, or both p and q are false  | (p $\rightarrow$ q) $\land$ (q $\rightarrow$ p)   |

### Logical Identities
| Name                  | Conjunction Form          | Disjunction Form          |
|-----------------------|---------------------------|---------------------------|
| Identity Law          | 1x = x                    | 0 + x = x                 |
| Null (Dominance) Law  | 0x = 0                    | 1 + x = 1                 |
| Idempotent Law        | xx = x                    | x + x = x                 |
| Inverse Law           | xx' = 0                   | x + x' = 1                |
| Commutative Law       | xy = yx                   | x + y = y + x             |
| Associative Law       | (xy)z = x(yz)             | (x + y) + z = xy + xz     |
| Distributive Law      | x + (yz) = (x + y)(x + z) | x(y + z) = xy + xz        |
| Absorption Law        | x(x + y) = x              | x + xy = x                |
| DeMorgan's Law        | (xy)' = x' + y'           | (x + y)' = x'y'           |
| Double Complement Law | x'' = x                   | <small>*same*</small>     |

- A "neither-nor" relationship implies *~p $\land$ ~q*
- Conditionals represent an "if-then" relationship
    - The hypothesis has no bearing on whether the conclusion is true or not
    - If the hypothesis is true, then the conclusion must be true. Otherwise, relationship is false

### Transformations of $p \rightarrow q$
| Name              | Form                  |
|-------------------|-----------------------|
| Negation          | p $\land$ ~q          |
| Contrapositive    | ~q $\rightarrow$ ~p   |
| Converse          | q $\rightarrow$ p     |
| Inverse           | ~p $\rightarrow$ ~q   |

- A *statement* (proposition) is something that can be given a truth value
    - Compound if contains connectives (*and*, *or*, etc.)

>**Example:** Self-referential sentences cannot be given a truth value, so they can never be statements.
>
>"This sentence is true" is not a statement by this logic.

### Types of statements
| Type          | Claim                                     | Example                                                   |
|---------------|-------------------------------------------|-----------------------------------------------------------|
| universal     | property is true for every element        | *Every person in this class is a USF student*             |
| existential   | property is true for at least one element | *Some person in this class is not a USF student*          |
| conditional   | consequent is true if antecedent is true  | *If a person is in this class, they are a USF student*    |

- Universal and existential statements are types of *quantified* statements

### Statement Vocabulary
| Term                      | Definition                                                                                    | Example                                       |
|---------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| tautology                 | A statement that is always true regardless of statement variables                             | p $\lor$ ~p                                   |
| contradiction             | A statement that is always false regardless of statement variables                            | p $\land$ ~p                                  |
| condition (antecedent)    | A statement variable that if true, the hypothesis must also be true                           | p $\rightarrow$ q, where p is the condition   |
| hypothesis (consequent)   | An event that may happen if its condition is false, but must happen if its condition is true  | p $\rightarrow$ q, where q is the hypothesis  |

- Universal bounds defined by their identities
    - **t** $\equiv$ p $\lor$ **t**
    - **c** $\equiv$ p $\land$ **c**
- Statement forms are expressions with statement variables, typically *p* and *q*
- A *rule of inference* is a valid, typically simple, argument form
- *Domain* is set of all possible statement variables
- Logical arguments are statement that follows the form:
    1. **Premises:** a sequence of statements
    2. **$\therefore$ Conclusion:** any statement
- An argument form is *valid* iff it is impossible for the premises to be true while the conclusion is false

>**Example:** Logical arguments can be converted to their equivalent conditional.
>
>&emsp;It is not the case that today is neither Saturday nor Sunday<br>
>$\therefore$ Today is Saturday
>
>If we say that $s$ is whether today is Saturday and $u$ is whether today is Sunday, the premise becomes *~(~s $\land$ ~u)* and the conclusion is $s$.
>Therefore, the equivalent conditional would be *~(~s $\land$ ~u) $\rightarrow$ s*.

- Two statements are *logically equivalent* ($\equiv$) if they always produce same truth value, given same inputs
    - If two statements have the same entries in a *truth table*, they are logically equivalent

>**Example:** Create a truth table for *x $\land$ ~y + z(~x $\lor$ y)*.
>
>| x | y | z | x $\land$ ~y + z(~x $\lor$ y)    |
>|---|---|---|----------------------------------|
>| 0 | 0 | 0 | 0                                |
>| 0 | 0 | 1 | 1                                |
>| 0 | 1 | 0 | 0                                |
>| 0 | 1 | 1 | 1                                |
>| 1 | 0 | 0 | 1                                |
>| 1 | 0 | 1 | 1                                |
>| 1 | 1 | 0 | 0                                |
>| 1 | 1 | 1 | 1                                |

- Statements equivalent to each other will always have **the same** row values in their column on a truth table
- Statements that negate each other will always have **opposite** row values in their columns on a truth table
- A statement is *vacuously true (true by default)* if its condition for truth requires either, or something similar:
    - Some element exist, and every possible element is present
    - Some element not exist, and no elements are present
    - The statement is a conditional and the hypothesis is false
- Method of exhaustion

### Common Rules of Inference
| Valid                 |                                                                                           | Invalid (Fallacy) |                                                           |
|-----------------------|-------------------------------------------------------------------------------------------|-------------------|-----------------------------------------------------------|
| **Name**              | **Form**                                                                                  | **Name**          | **Form**                                                  |
| Modus ponens          | &emsp;p $\rightarrow$ q<br>&emsp;p<br>$\therefore$ q                                      | Converse error    | &emsp;p $\rightarrow$ q<br>&emsp;q<br>$\therefore$ p      |
| Modus tollens         | &emsp;p $\rightarrow$ q<br>&emsp;~q<br>$\therefore$ ~p                                    | Inverse error     | &emsp;p $\rightarrow$ q<br>&emsp;~p<br>$\therefore$ ~q    |
| Elimination           | &emsp;p $\lor$ q<br>&emsp;~q<br>$\therefore$ p                                            | False exclusion   | &emsp;p $\lor$ q<br>&emsp;p<br>$\therefore$ ~q            |
| Generalization        | &emsp;p<br>$\therefore$ p $\lor$ q                                                        |                   | &emsp;p $\lor$ q<br>$\therefore$ p                        |
| Specialization        | &emsp;p $\land$ q<br>$\therefore$ p                                                       |                   | &emsp;p<br>$\therefore$ p $\land$ q                       |
| Conjunction           | &emsp;p<br>&emsp;q<br>$\therefore$ p $\land$ q                                            |                   |                                                           |
| Transitivity          | &emsp;p $\rightarrow$ q<br>&emsp;q $\rightarrow$ r<br>$\therefore$ p $\rightarrow$ r      |                   |                                                           |
| Division into Cases   | &emsp;p $\lor$ q<br>&emsp;p $\rightarrow$ r<br>&emsp;q $\rightarrow$ r<br>$\therefore$ r  |                   |                                                           |
| Contradiction         | &emsp;~p $\rightarrow$ **c**<br>$\therefore$ p                                            |                   |                                                           |

- To show that some predicate $P(k)$ implies $P(k + 1)$ is part of *mathematical induction*
    - Method of proof
    - 
P(1)


how to solve knights/knaves