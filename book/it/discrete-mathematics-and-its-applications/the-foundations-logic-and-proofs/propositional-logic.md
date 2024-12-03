---
description: 1장 1절에 대한 원문이다.
icon: '1'
---

# Propositional Logic

## Introduction

The rules of logic give precise meaning to mathematical statements.\
These rules are used to distinguish between valid and invalid mathematical arguments.\
Because a major goal of this book is to teach the reader how to understand and how to construct correct mathematical arguments, we begin our study of discrete mathematics with an introduction to logic.

In addition to its importance in understanding mathematical resoning, logic has numerous applications iin computer science.\
These rules are used in the design of computer circuits, the construction of computer programs, the verfication of the correctness of prgrams, and in many oother ways.\
Furthermore, software systems have been developed for constucting proofs automatically.\
We will discuss these applications of logic in the upcoming chapters.

## Propsitions

Our discussion begins with an introduction to the basic building blocks of logic-propositions.\
A **propositiion** is a declarative sentence (that is, a sentence that declares a fact) that is ether true of false, but not both.

### Example 1

All the following declarative sentences are propositions.

1. Washington, D. C., is the captal of the Unted States of America.
2. Toronto is the capital of Cananda.
3. 1 + 1 = 2.
4. 2 + 2 = 3.

Propositions 1 and 3 are true, whereas 2 and 4 are false.

> Some sentences that are not propositions are given iin Example 2.

### Example 2

Consider the following sentences.

1. What time is iit?
2. Read this carefully.
3. x + 1 = 2.
4. x + y = z.

Sentences 1 and 2 are not propositions because they are not declarative sentences.\
Sentences 3 and 4 are not propositions because they are neither true nor false.\
Note that each of sentences 3 and 4 can be turned into a proposition if we assign values to the varables.\
We will also discuss other ways to turn sentences such as these into propositions in Sectiion 1.3.

We use letters to denote **propositional variables** (or **statement variables**), that is, variables that represent propositions, just as letters are used to denote numerical variables.\
The conventional letters used for propositional variables are _p_, _q_, _r_, _s_, _..._ .\
The **truth value** of a propositon is truem denoted by T, f t s a true proposition and false, denoted by F, if it s a false proposiition.

The area of logic that deals with proposiitions is called the **propositional calculus** of **proposiitional logIc**.\
It was first developed systematically by the Greek philosopher Aristotle more than 2300 years ago.

### Definication 1

Let _p_ be a proposition.\
The _negation of p_, denoted by _¬p_, is the statement "It is not case that _p_."

The proposition _¬p_ is read "not _p_".\
The truth value of the negation of _p_, _¬p_, is the opposite of the truth value of _p_.

### Example 3

Find the negation of the proposition "Today is Friday." and express thish in simple English.

_Solution_: The negation is "It is not the case that today is Friday."\
This negation can be more simply expressed by "Today is not Friday." of "It is not Friday today."

### Example 4

Find the negation of the proposition "At least 10 inches of rain fell today in Miami." and express this in simple English.

_Solution_: The negation is "It is not the case that at least 10 inches of rain fell today in Miami."\
This negation can be more simply expressed by "Less than 10 inches of rain fell today in Miami."

#### Table 1 The Truth Table for the Negation of a Proposition.

| p | ¬p |
| - | -- |
| T | F  |
| F | T  |

_Remark_: Strictly speaking, sentences involving variable times such as those in Examples 3 and 4 are not proposions unless a fixed time is assumed.\
The same holds for variable places unless a fixed place is assumed and for pronouns unless a particular person is assumed.\
We will always assume fixed times, fixed places, and particular people in such sentences unless otherwise noted.

Table 1 displays the **truth table** for the negation of a proposition _p_.\
This table has a row for each of the two possible truth values fo a proposition _p_.\
Each raw shows the truth value of ¬_p_ corresponding to the truth value of _p_ for this row.

The negation of a proposition can also be considered the result of the operation of the **negation operator** on a proposition.\
The negation operator constructs a new proposition from a single exsting proposition.\
We will now introduce the logical operators that are used to from new propositions from two or more existing propositions.\
These logical operators are also called **connectives**.

### Definition 2

Lep _p_ and _q_ be propositions.\
The _conjunction_ of _p_ and _q_, denoted by _p ∧_ q, is the propsition "_p_ and _q_."\
The conjunction _p ∧ q_ is true when both _p_ and _q_ are true and is false otherwise.

Table 2 displays the truth table of _p ∧ q_.\
This table has a row for each of the four possible combinations of truth values of _p_ and _q_.\
The four rows correspond to the pairs of truth values TT, TF, FT, and FF, where the first truth value in the pair is the truth value of _p_ and the second truth value is the truth value of _q_.

Note that in logic the word "but" sometimes is used instead of "and" in a conjunction.\
For example, the statement "The sun is shining, but it is raining" is another way of saying " The sun is shining and it is raining." (in natural language, there is subtle difference in meaning between "and" and "but"; we will not be concerned with this nuance here.)

#### Table 2 The Truth Table for the Conjunction of Two Propositions.

| p | q | p ∧ q |
| - | - | ----- |
| T | T | T     |
| T | F | F     |
| F | T | F     |
| F | F | F     |

### Example 5

Find the conjunction of the propositions _p_ and _q_ where _p_ is the proposition "Today is Friday" and _q_ is the proposition"It is raining today."\
This proposition is true on rainy Fridays and is false on any day that is not a Friday and on Fridays when it does not rain.

### Definition 3

Let _p_ and _q_ be propositions.\
The _disjunction_ of _p_ and _q_, denoted by _p ∨ q_, is the proposition "_p_ or _q_."\
The disjunction _p ∨ q_ is false when both _p_ and _q_ are false and is true otherwise.

Table 3 display the truth table for _p ∨ q._

The use of the connective _or_ in a disjunction corresponds to one of the two ways the word _or_ is used in English, namely, in an inclusive way.\
A disjunction is true when at least one of the two propositions is true.\
For instance, the inclusive or is being used in the statement "Students who have taken calculus or computer science can take this class."\
Here, we mean that students who have taken both calculus and computer science can take the class, as well as the students who have taken only one of the two subjects.\
On the other hand, we are using the exclusive or when we say "Students who have taken calculus or computer science, but not both, can enroll in this class."\
Here, we mean that students who have taken both calculus and a computer science course cannot take the class.\
Only those who have taken exactly one of the two courses can take the class.

Similarly, when a menu at a restaurant states, "Soup or salad comes with an entree," the restaurant almost always means that customers can have either soup or salad, but not both.\
Hence, this is an exclusive, rather than an inclusive, or.

#### Table 3 The Truth Table for the Disjunction of Two Propositions.

| p | q | p ∨ q |
| - | - | ----- |
| T | T | T     |
| T | F | T     |
| F | T | T     |
| F | F | F     |

### Example 6

What is the disjunction of the propositions _p_ and _q_ where _p_ and _q_ are the same propositions as in Example 5?

_Solution_: The disjunction of _p_ and _q_, _p ∨ q_, is the proposition "Today is Friday or it is raining today."\
This proposition is true on any day that is either a Friday or rainy day (including rainy Fridays).\
It is only false on days that are not Fridays when





