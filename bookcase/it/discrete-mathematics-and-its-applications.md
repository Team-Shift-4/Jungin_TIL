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

* $$2+2=3$$ (Proposition이나 False)
* $$x+1=2$$ (Not proposition)
{% endhint %}

#### Logical Operators

| Name          | Sign   | Example  | Mean               |
| ------------- | ------ | -------- | ------------------ |
| Negation      | $$￢$$  | $$￢p$$   | not p              |
| Conjunction   | $$∧$$  | $$p∧q$$  | p and q            |
| Disjunction   | $$∨$$  | $$p∨q$$  | p or q             |
| Exclusivr-or  | $$⊕$$  | $$p⊕q$$  | p excusive or q    |
| Implication   | $$→$$  | $$p→q$$  | if p, then q       |
| Biconditional | $$↔︎$$ | $$p↔︎q$$ | p if and only if q |

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
| 1        | $$￢$$            |
| 2        | $$∧$$            |
| 3        | $$∨$$            |
| 4        | $$→$$            |
| 5        | $$↔︎$$           |

#### Compound Proposition

Compound proposition(복합 명제)은 괄호와 Operator의 순서에 따라 Truth value를 도출한다.

{% hint style="info" %}
Example

$$(p∨￢q)→(p∧q)$$

단계 별로 나눠  해결한다.

$$p = T$$, $$q = T$$

1. $$p∨￢q = T$$
2. $$p∧q = T$$
3. $$(p∨￢q)→(p∧q)$$
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
| AND           | `&`  | Retruns 1 when all corresponding bits are 1.                             | `A&B=1001`                  |
| OR            | `\|` | If any of the corresponding bits are 1, then 1 is returned.              | `A\|B=1111`                 |
| NOT           | `~`  | Inverse bits.                                                            | `~B=0100`                   |
| XOR           | `^`  | If the corresponding bits are different, then 1 is returned.             | `A^B=0110`                  |
| Left Shift    | `<<` | Move a specified number of bits to the left.                             | `A<<2=11 0100`              |
| Right Shift   | `>>` | Move bits to the right by a specified number while maintaining the sign. | `B>>2=10`                   |

### 1.2. Propositional Equivalences

#### Tautology and Contingency

Tautology(항진 명제) = 항상 Value가 True인 Compound proposition\
Contigency(모순 명제) = 항상 Value가 False인 Compound proposition

#### Logical Equivalences

Logical equivalences(논리적 동치)는 항상 같은 Truth value를 갖는 Compound proposition의 관계를 말한다.\
Compound proposition p, q가 Logical equivalence라면 Notation으로 p≡q이다.

#### Propositional Laws

De Morgan's laws(드 모르간 법칙)

* $$￢(p∨q)≡(￢p∧￢q)$$
* $$￢(p∧q)≡(￢p∨￢q)$$

Identity laws(항등 법칙)

* $$p∧T≡p$$
* $$p∨F≡p$$

Domination laws(지배 법칙)

* $$p∨T≡T$$
* $$p∧F≡F$$

Idenpotent laws(등멱 법칙)

* $$p∨p≡p$$
* $$p∧p≡p$$

Double negation laws(이중 부정 법칙)

* $$p∨￢p≡T$$
* $$p∧￢p≡F$$

Commutative laws(교환 법칙)

* $$p∨q≡q∨p$$
* $$p∧q≡q∧p$$

Associative laws(결합 법칙)

* $$(p∨q)∨r≡p∨(q∨r)$$
* $$(p∧q)∧r≡p∧(q∧r)$$

Distributive laws(분배 법칙)

* $$p∨(q∧r)≡(p∨q)∧(p∨r)$$
* $$p∧(q∨r)≡(p∧q)∨(p∧r)$$

Absorption laws(흡수 법칙)

* $$p∨(p∧q)≡p$$
* $$p∧(p∨q)≡p$$

#### Logical Equivalences Involving Conditional Statements

* $$p→q≡￢p∨q$$
* $$p→q≡￢q→￢p$$
* $$p∨q≡￢p→q$$
* $$p∧q≡￢(p→￢q)$$
* $$￢(p→q)≡p∧￢q$$
* $$(p→q)∧(p→r)≡p→(q∧r)$$
* $$(p→r)∧(q→r)≡(p∨q)→r$$
* $$(p→q)∨(p→r)≡p→(q∨r)$$
* $$(p→r)∨(q→r)≡(p∧q)→r$$

#### Logical Equivalences Involving Biconditionals

* $$p↔︎q≡(p→q)∧(q→p)$$
* $$p↔︎q≡￢p↔︎￢q$$
* $$p↔︎q≡(p∧q)∨(￢p∧￢q)$$
* $$￢(p↔︎q)≡p↔︎￢q$$

#### Constructing New Logical Equivalences

식 풀이 편이를 위해 Logical equivalence를 이용할 수 있다.

{% hint style="info" %}
Example

$$￢(p∨(￢p∧q))≡￢p∧￢q$$

$$￢(p∨(￢p∧q))$$

$$≡ ￢p∧￢(￢p∧q)$$ ∵ De Morgan's laws

$$≡ ￢p∧(￢(￢p)∨￢q)$$ ∵ De Morgan's laws

$$≡ ￢p∧(p∨￢q)$$ ∵ Double negation laws

$$≡ (￢p∧p)∨(￢p∧￢q)$$ ∵ Distributive laws

$$≡ F∨(￢p∧￢q)$$ ∵ ￢p∧p=Contingency

$$≡ ￢p∧￢q$$ ∵ Commutative laws and Identity laws
{% endhint %}

### 1.3. Predicates and Quantifiers

#### Predicates

Proposion 'A is B'에서 A를 Subject(주어), B를 Predicate(술어)라고 한다.

Propositional function(=Condition)은 Variable value에 따라 Truth value가 달라지는 Proposition이다.

Propositional function $$P(x_1, x_2, x_3, ..., x_n)$$을 n-place predicate(n항 술어)라 한다.

Propositional function는 Variable이 지정되지 않은 경우 Truth value를 가질 수 없다.

* Precondition(사전 조건): 유효한 Input을 기술하는 Statement를 의미
* Postcondition(사후 조건): 유효한 Output을 기술하는 Statement를 의미

{% hint style="info" %}
Example

`temp := x`\
`x := y`\
`y := temp`

Precondition: x=a, y=b\
Postcondition: x=b, y=a
{% endhint %}

#### Quantifiers

Quantifier(한정자, 양화사)는Propositional function의 Truth value를 판별하기 위해 Domain(=Universe of discourse)의 범위를 지정하기 위해 사용하는 것이다.

* Universal quantifier
  * 한국어로 전체한정자, 전체양화사, 전칭기호라고도 하며 Domain의 모든 Value를 의미한다.
  * Domain의 모든 Element에 대해 만족할 경우에만 True이다.
  * Domain U에 속하는 모든 x에 대해 Propositional function $$P(x)$$를 Notation으로 $$∀xP(x)$$로 표기한다.
* Existential Quantifier
  * 한국어로 존재한정자, 존재양화사, 존재기호라고도 하며 Domain에 속하는 어떠한 Value를 의미한다.
  * Domain의 Element 중 하나라도 만족할 경우 True이다.
  * Domain U에 속하는 어떤 x에 대해 Propositional funtion $$P(x)$$를 Notation으로 $$∃xP(x)$$로 표기한다.
  * $$∃_1$$로 표기한 것은 Uniqueness quantifier로 Domain의 Element 중 단 하나만 만족할 경우에만 True이다.

#### Quantifiers with Restricted Domains

Abbreviated notation은 종종 Domain을 제한하는 데 사용한다.\
Abbreviated에서 Variable이 충족해야 하는 Condition이 Quantifier 이후 포함된다.

{% hint style="info" %}
Example

Domain이 Real number인 Poposition P가 "Negative number의 제곱은 Positive number이다." 일 때

$$∀x<0(x^2>0)$$의 경우 $$∀x(x<0→x^2>0)$$
{% endhint %}

#### Precedence of Quantifiers

Quantifier는 모든 Logical Operation보다 우선순위가 높다.

#### Binding Variables

Variable x에 Quantifier를 사용할 경우 Variable x는 Bound(범위에 든다)라고 표현한다.\
Variable x가 Bound하지 않거나 특정 Value로 지정되지 않은 경우 Free(범위에서 벗어났다)라고 표현한다.

Bound variable을 한국어로 기속 변수라 하고 Free variable을 한국어로 자유 변수라고 한다.

Variable이 Quantifier가 적용된 Scope를 벗어나면 Free variable이 된다.

#### Logical Equivalences Involving Quantifiers

Predicate와 Quantifier를 포함하는 Statement는 어떤 Predicate거나 Quantifier이던 상관 없이 동일한 Truth value를 갖는 경우에만 Logical equivalence(논리적 동치)하다고 한다.

Predicateㅇ와 Quantifier를 포함하는 두 Statement S, T에 대해 S와 T가 Logical equivalence할 경우 Notation으로 $$S≡T$$라 한다.

#### Negating Quantified Expressions

$$￢∀xP(x)≡∃x￢P(x)$$이고 $$￢∃xP(x)≡∀x￢P(x)$$임을 De Morgan's laws for quantifiers라고 부른다.

| Negation | Equivalent statement | When is negation true?                         | When False                                    |
| -------- | -------------------- | ---------------------------------------------- | --------------------------------------------- |
| ￢∃xP(x)  | ∀x￢P(x)              | For every $$x$$, $$P(x)$$ is false.            | There is an $$x$$ for which $$P(x)$$ is true. |
| ￢∀xP(x)  | ∃x￢P(x)              | There is an $$x$$ for which $$P(x)$$ is false. | $$P(x)$$ is true for every x.                 |

#### Translating from Natural Language into Logical Expressions

Statement of natural language를 Logical expression으로 변환하는 것은 수학, Logical programming, AI, Software Engineering 등에 중요한 작업이다.

Quantifier를 사용할 때 Natural language를 Logical expression으로 변환하는 것이 더 복잡하므로 주의하여 변환하여야 한다.

#### Examples from Lewis Carroll

{% hint style="info" %}
Example

"All lions are fierce." = $$∀x(P(x)→Q(x))$$\
"Some lions do not drink coffee." = $$∃x(P(x)∧￢R(x))$$\
"Some fierce creatures do not drink coffee." = $$∃x(Q(x)∧￢R(x))$$

$$P(x)$$ is "x is lion.".\
$$Q(x)$$ is "x is fierce.".\
$$R(x)$$ is "x drinks coffee."
{% endhint %}

#### Logical Programming

Programming language의 중요한 유형은 Rule of preicate logic을 사용하여 추론하도록 설계된 것이다.\
아래는 1970년대 AI 분야 Computer Science들이 개발한 Prolog(PROgramming in LOGic)라는 Language를 예시로 들어 설명한다.

{% hint style="info" %}
Example

각 수업 교수와 학생이 등록한 수업을 알려주는 Prolog program을\
Predicate `instructor(p, c)`와 `enrolled(s, c)`를 사용해 교수 `p`가 수업 `c`의 강사이고 학생 `s`가 수업 `c`를 신청했다는 것을 표현 가능하다.

`instructor(chan, math273)`

`...`

`enrolled(kevin, math273)`

`...`&#x20;

새로운 Predicate 교수 `p`가 학생 `s`를 가르치는 것을 만들 때 Prolog rules를 사용하여 정의할 수 있다.

`teaches(p, s) :- instructor(p, c), enrolled(s, c)`

즉 `teaches(p, s)`는 교수 `p`가 `c` 수업의 강사이며 학생 `s`가 `c` 수업을 신청한 경우에만 참이다.

Prolog는 주어진 facts와 rules를 사용하여 Query에 답변한다.

`?enrolled(kevin, math273) //yes`

`?enrolled(X, math273) // kevin`
{% endhint %}

### 1.4. Nested Quantifiers

