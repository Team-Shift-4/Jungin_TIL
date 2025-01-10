---
icon: square
description: Discrete Mathematics and ITs Application(Sixth Edition)을 읽고 정리한 내용이다.
---

# Discrete Mathematics and ITs Applications

## 1. The Foundation: Logic and Proofs

### 1.1. Propositional Logic

Propositional logic(명제 논리) = 문장 구조를 모델링 할 때 사용한다.\
Proposition = True, Flase의 값 중 하나만 갖는 Statement이다.\
Proposition이기 위해 Declarative sentence여야 한다.

{% hint style="info" %}
Example

* 2+2=3 (Propositional이나 False)
* x+1=2(Not propositional)
{% endhint %}

#### Logical Operators

| Name          | Sign | Example | Mean               |
| ------------- | ---- | ------- | ------------------ |
| Negation      | ￢    | ￢p      | not p              |
| Conjunction   | ∧    | p∧q     | p and q            |
| Disjunction   | ∨    | p∨q     | p or q             |
| Exclusivr-or  | ⊕    | p⊕q     | p excusive or q    |
| Implication   | →    | p→q     | if p, then q       |
| Biconditional | ↔︎   | p↔︎q    | p if and only if q |

#### Negation Truth Table

| p | ￢p | ￢(￢p) |
| - | -- | ----- |
| T | F  | T     |
| F | T  | F     |

#### Conjunction Truth Table

| p | q | p∧q |
| - | - | --- |
| T | T | T   |
| T | F | F   |
| F | T | F   |
| F | F | F   |

#### Disjunction Truth Table

| p | q | p∨q |
| - | - | --- |
| T | T | T   |
| T | F | T   |
| F | T | T   |
| F | F | F   |

#### Exclusivr-or Truth Table

| p | q | p⊕q |
| - | - | --- |
| T | T | F   |
| T | F | T   |
| F | T | T   |
| F | F | F   |

#### Conditional Truth Table

| p | q | p→q |
| - | - | --- |
| T | T | T   |
| T | F | F   |
| F | T | T   |
| F | F | T   |

Antecedent(전건)가 False인 경우 그 Conditional은 Consequent(후건)에 관계 없이 True이다.\
이를 Vacuous Truth(공허한 참)이라고 한다.

#### Biconditional Truth Table

| p | q | p↔︎q |
| - | - | ---- |
| T | T | T    |
| T | F | F    |
| F | T | F    |
| F | F | T    |

Antecedent와 Consequent가 모두 False일 때 Vacuous Truth에 의거해 True이다.

#### Precedence of Logical Operators

| Priority | Logical operator |
| -------- | ---------------- |
| 1        | ￢                |
| 2        | ∧                |
| 3        | ∨                |
| 4        | →                |
| 5        | ↔︎               |

#### Compound Proposition

Compound proposition(복합 명제)은 괄호와 Operator의 순서에 따라 Truth value를 도출한다.

{% hint style="info" %}
Example

(p∨￢q)→(p∧q)

단계 별로 나눠  해결한다.

p = T, q = T

1. p∨￢q = T
2. p∧q = T
3. (p∨￢q)→(p∧q)
{% endhint %}

#### Translating Natural Language Sentences

Natural language를 Compound proposition으로 나타내어 문장의 모호성을 제거할 수 있다.

#### Boolean Search

Boolean search는 Propositional logical technique를 이용해 방대한 정보를 검색할 때 사용한다.

| Boolean operator | Decription   |
| ---------------- | ------------ |
| AND              | Intersection |
| OR               | Union        |
| NOT              | Subtraction  |

Boolean search로 정확도 향상, 유연한 검색, 검색 시간 절약 등 이점을 가질 수 있다.

#### Logic and Bit Operations

| Bit operation | Sign | Description                                                              | Example(A = 1101, B = 1011) |
| ------------- | ---- | ------------------------------------------------------------------------ | --------------------------- |
| AND           | &    | Retruns 1 when all corresponding bits are 1.                             | A\&B=1001                   |
| OR            | \|   | If any of the corresponding bits are 1, then 1 is returned.              | A\|B=1111                   |
| NOT           | \~   | Inverse bits.                                                            | \~B=0100                    |
| XOR           | ^    | If the corresponding bits are different, then 1 is returned.             | A^B=0110                    |
| Left Shift    | <<   | Move a specified number of bits to the left.                             | A<<2=11 0100                |
| Right Shift   | >>   | Move bits to the right by a specified number while maintaining the sign. | B>>2=10                     |

### 1.2. Propositional Equivalences

#### Tautology and Contingency

Tautology(항진 명제) = 항상 Value가 True인 Compound proposition\
Contigency(모순 명제) = 항상 Value가 False인 Compound proposition

#### Logical Equivalences

Logical equivalences(논리적 동치)는 항상 같은 Truth value를 갖는 Compound proposition의 관계를 말한다.\
Compound proposition p, q가 Logical equivalence라면 Notation으로 p≡q이다.

#### Propositional Laws

De Morgan's laws(드 모르간 법칙)

* ￢(p∨q)≡(￢p∧￢q)
* ￢(p∧q)≡(￢p∨￢q)

Identity laws(항등 법칙)

* p∧T≡p
* p∨F≡p

Domination laws(지배 법칙)

* p∨T≡T
* p∧F≡F

Idenpotent laws(등멱 법칙)

* p∨p≡p
* p∧p≡p

Double negation laws(이중 부정 법칙)

* p∨￢p≡T
* p∧￢p≡F

Commutative laws(교환 법칙)

* p∨q≡q∨p
* p∧q≡q∧p

Associative laws(결합 법칙)

* (p∨q)∨r≡p∨(q∨r)
* (p∧q)∧r≡p∧(q∧r)

Distributive laws(분배 법칙)

* p∨(q∧r)≡(p∨q)∧(p∨r)
* p∧(q∨r)≡(p∧q)∨(p∧r)

Absorption laws(흡수 법칙)

* p∨(p∧q)≡p
* p∧(p∨q)≡p

#### Logical Equivalences Involving Conditional Statements

* p→q≡￢p∨q
* p→q≡￢q→￢p
* p∨q≡￢p→q
* p∧q≡￢(p→￢q)
* ￢(p→q)≡p∧￢q
* (p→q)∧(p→r)≡p→(q∧r)
* (p→r)∧(q→r)≡(p∨q)→r
* (p→q)∨(p→r)≡p→(q∨r)
* (p→r)∨(q→r)≡(p∧q)→r

#### Logical Equivalences Involving Biconditionals

* p↔︎q≡(p→q)∧(q→p)
* p↔︎q≡￢p↔︎￢q
* p↔︎q≡(p∧q)∨(￢p∧￢q)
* ￢(p↔︎q)≡p↔︎￢q

#### Constructing New Logical Equivalences

식 풀이 편이를 위해 Logical equivalence를 이용할 수 있다.

{% hint style="info" %}
Example

￢(p∨(￢p∧q))≡￢p∧￢q

￢(p∨(￢p∧q))

≡ ￢p∧￢(￢p∧q)  ∵ De Morgan's laws

≡ ￢p∧(￢(￢p)∨￢q)	∵ De Morgan's laws

≡ ￢p∧(p∨￢q) ∵ Double negation laws

≡ (￢p∧p)∨(￢p∧￢q) ∵ Distributive laws

≡ F∨(￢p∧￢q) ∵ ￢p∧p=Contingency

≡ ￢p∧￢q ∵ Commutative laws and Identity laws
{% endhint %}

### 1.3. Predicates and Quantifiers

#### Predicates

Proposion 'A is B'에서 A를 Subject(주어), B를 Predicate(술어)라고 한다.

Propositional function(=Condition)은 Variable value에 따라 Truth value가 달라지는 Proposition이다.

Propositional function P($$x_1$$, $$x_2$$, $$x_3$$, ..., $$x_n$$)을 n-place predicate(n항 술어)라 한다.

Predicate는 Variable이 지정되지 않은 경우 Truth value를 가질 수 없다.

* Precondition(사전 조건): 유효한 Input을 기술하는 Statement를 의미
* Postcondition(사후 조건): 유효한 Output을 기술하는 Statement를 의미









\


