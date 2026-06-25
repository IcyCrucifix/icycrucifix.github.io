---
layout:     post
title:      "COMP2121: The Complete Study Guide"
date:       2026-06-25 13:00:00
author:     "Jeffery"
header-img: "img/HKU Grand Hall.HIF"
catalog: true
tags: [HKU]
---


# COMP2121 Final Exam Guide

Created by Jeffery Jingfeng Xu for personal study use; redistribution is not permitted.


For COMP2121 students preparing for the final exam. It is built from the COMP2121 lecture PDFs, especially Lec 21 and Lec 22, the COMP2121 final papers, and supporting assignments/midterms. 


Lec 21/22 final syllabus says the final covers:

- Logic.
- Counting and probability applications.
- Functions: injective, surjective, composition.
- Relations and equivalence relations.
- Probability: events, sample spaces, conditional probability.
- Counting: permutations, combinations, product rule, sum rule.
- Graph theory: degree, connectivity, Euler tours, Hamilton cycles, graph coloring.
- Inclusion-exclusion and pigeonhole principles.

The COMP2121 final papers repeatedly test five blocks:

1. Logic and proofs.
2. Sets, relations, functions, and growth.
3. Counting.
4. Probability and random variables.
5. Graph theory.


---

## Exam Rule Names And Statements To Cite

Why this section comes first: the professor explicitly expects rule names from the lecture material to appear in written logic solutions. Lec 3 lists the propositional rules of inference below; Lec 4 lists the quantified-statement rules immediately after them. When your argument uses one of these rules, write the rule name beside the step unless the table marks it as a basic rule name that the professor said need not be written.

### Propositional Rules Of Inference From Lec 3

| Lecture rule name          | What you may write in the exam                         | Lecture alias / meaning                                                    |
| -------------------------- | ------------------------------------------------------ | -------------------------------------------------------------------------- |
| **Modus Ponens**           | From $p$ and $p\to q$, conclude $q$.                   | **Affirming the Antecedent**; also described as the **Law of Detachment**. |
| **Modus Tollens**          | From $\neg q$ and $p\to q$, conclude $\neg p$.         | **Denying the Consequent**.                                                |
| **Hypothetical Syllogism** | From $p\to q$ and $q\to r$, conclude $p\to r$.         | **Transitivity of Implication** or **Chain Rule**.                         |
| **Disjunctive Syllogism**  | From $p\lor q$ and $\neg p$, conclude $q$.             | **Disjunction Elimination**.                                               |
| **Addition**               | From $p$, conclude $p\lor q$.                          | Introduces a disjunction.                                                  |
| **Simplification**         | From $p\land q$, conclude $p$.                         | Extracts one conjunct.                                                     |
| **Resolution**             | From $p\lor q$ and $\neg p\lor r$, conclude $q\lor r$. | The conclusion $q\lor r$ is the **resolvent**.                             |

This is the full propositional lecture list. Do not accidentally treat fallacies as inference rules: **Affirming the Conclusion** and **Denying the Hypothesis** from Lec 4 are invalid argument forms.

### Quantifier Inference Rules

These four quantified-statement rules are rules of inference from Lec 4. Name them when the step depends on a quantifier.

| Rule name | What it does |
| --- | --- |
| **Universal Instantiation** | From $\forall x\,P(x)$, infer $P(a)$ for a specific allowed object $a$. |
| **Universal Generalization** | After proving $P(a)$ for an arbitrary object $a$, infer $\forall x\,P(x)$. |
| **Existential Instantiation** | From $\exists x\,P(x)$, introduce a fresh witness $c$ satisfying $P(c)$. |
| **Existential Generalization** | From $P(a)$ for one object $a$, infer $\exists x\,P(x)$. |

### Logic Equivalence Rules Worth Naming

| Rule name | Statement |
| --- | --- |
| **Implication Rule** | $p\to q\equiv \neg p\lor q$. |
| **Contrapositive Equivalence** | $p\to q\equiv \neg q\to\neg p$. |
| **De Morgan's Laws** | $\neg(p\land q)\equiv\neg p\lor\neg q$ and $\neg(p\lor q)\equiv\neg p\land\neg q$. |
| **Quantifier Negation Rules** | $\neg\forall x\,P(x)\equiv\exists x\,\neg P(x)$ and $\neg\exists x\,P(x)\equiv\forall x\,\neg P(x)$. |
| **Distributive Laws** | $p\land(q\lor r)\equiv(p\land q)\lor(p\land r)$ and $p\lor(q\land r)\equiv(p\lor q)\land(p\lor r)$. |

### Proof Methods To State When Relevant

| Method | What it means |
| --- | --- |
| **Direct Proof** | Assume the hypotheses and derive the conclusion. |
| **Proof By Contraposition** | To prove $P\to Q$, prove $\neg Q\to\neg P$. |
| **Proof By Contradiction** | Assume the target claim is false and derive an impossibility. |
| **Proof By Cases** | Split into exhaustive cases and prove the target in every case. |
| **Constructive Existence Proof** | Explicitly construct an object satisfying the requirement. |
| **Counterexample** | Disprove a universal claim by one valid example where it fails. |
| **Mathematical Induction** | Prove a base case and an induction step. |
| **Strong Mathematical Induction** | In the induction step, assume all earlier cases needed, not only the immediately previous case. |

Exam habit for logic questions: when a step uses a named rule, write the name and then show the concrete propositions playing the roles of $p,q,r$. This is why the rule-name section is placed here before the logic unit.

---

## LaTeX Notation Used In This Sheet

Use these symbols in exam answers. They match the notation style used in the lecture slides and past papers more closely than the earlier plain-text version.

| Plain meaning                 | Exam-style notation                     |
| ----------------------------- | --------------------------------------- |
| not $p$                       | $\neg p$                                |
| $p$ and $q$                   | $p \land q$                             |
| $p$ or $q$                    | $p \lor q$                              |
| if $p$, then $q$              | $p \to q$                               |
| $p$ iff $q$                   | $p \leftrightarrow q$                   |
| for all $x$                   | $\forall x$                             |
| there exists $x$              | $\exists x$                             |
| unique existence              | $\exists!x$                             |
| $x$ is in $A$                 | $x \in A$                               |
| $A$ is subset of $B$          | $A \subseteq B$                         |
| empty set                     | $\emptyset$                             |
| union                         | $A \cup B$                              |
| intersection                  | $A \cap B$                              |
| complement                    | $\overline{A}$ or $A^c$                 |
| difference                    | $A - B$ or $A \setminus B$              |
| Cartesian product             | $A \times B$                            |
| cardinality                   | $\lvert A\rvert$                        |
| binomial coefficient          | $\binom{n}{k}$                          |
| probability                   | $\Pr(A)$                                |
| conditional probability       | $\Pr(A\mid B)$                          |
| expected value                | $\mathbb{E}[X]$                         |
| variance                      | $\operatorname{Var}(X)$                 |
| floor and ceiling             | $\lfloor x\rfloor,\ \lceil x\rceil$     |
| Big-O / Big-Omega / Big-Theta | $O(g(n)),\ \Omega(g(n)),\ \Theta(g(n))$ |
| graph vertex/edge set         | $G=(V,E)$                               |
| minimum/maximum degree        | $\delta(G),\ \Delta(G)$                 |
| chromatic number              | $\chi(G)$                               |
| edge chromatic number         | $\chi'(G)$                              |
| vertex/edge connectivity      | $\kappa(G),\ \lambda(G)$                |

When the sheet says something like $f(n)=O(g(n))$, write it exactly in this style in the exam unless the question uses a slightly different convention.

---

## 0. Exam Strategy

Why this unit is included: students lose marks not only from wrong facts, but from unclear proof structure, missing definitions, or unnamed rules. This section explains how to present solutions so the marker can see the logic.

### What "prove" means in this course

A proof is not a story. It is a chain of justified statements. Every step should be supported by a definition, a known theorem, a previously proved statement, or a clear construction.

When asked to prove a statement:

1. Write down what is given.
2. Write down what must be shown.
3. Translate jargon into definitions.
4. Use the relevant template.
5. End with a sentence that explicitly says the target statement follows.

### Common proof templates

Direct proof:

```text
Assume the hypotheses are true.
Using definitions and algebra/logical rules, derive the conclusion.
Therefore the implication is true.
```

Contrapositive proof:

To prove $P \to Q$, prove $\neg Q \to \neg P$.

This is usually easier for divisibility, parity, injectivity, and graph nonexistence problems.

Contradiction proof:

```text
Assume the statement is false.
Derive an impossibility, such as 0 = 1, an odd number is even, or a forbidden graph exists.
Therefore the assumption was false.
```

Counterexample:

To disprove a universal statement, one explicit example is enough.

Induction:

```text
Base case: verify the claim for the smallest n.
Induction hypothesis: assume the claim for n = k.
Induction step: prove it for n = k + 1.
Conclusion: by induction, the claim holds for all required n.
```

Strong induction:

Use when the `k+1` case may depend on many earlier cases.

```text
Assume the claim holds for all n <= k.
Prove it for k + 1.
```

Constructive existence proof:

To prove "there exists", explicitly build the object.

Example: For every positive integer $n$, there are $n$ consecutive composite integers:

$$
(n+1)!+2,\ (n+1)!+3,\ \ldots,\ (n+1)!+(n+1).
$$

For each $j=2,\ldots,n+1$, the number $(n+1)!+j$ is divisible by $j$ and is larger than $j$, so it is composite. There are $n$ such numbers.

Nonconstructive existence proof:

Prove something exists without naming it, often by pigeonhole principle or contradiction.

### How to write a high-scoring answer

Define every symbol you introduce. If you use $A_i$, say what it means. If you use $G=(V,E)$, say vertices and edges. If you use $X$, say it is a random variable.

Do not skip the "why". For example, in inclusion-exclusion, do not only write a formula; say what is being overcounted and corrected.

For graph questions, draw mentally:

- Is it simple or a multigraph?
- Is it connected?
- Are degrees even or odd?
- Is it bipartite?
- Is it planar?
- Are we coloring vertices or edges?

For probability, always identify:

- sample space,
- event,
- probability model,
- independence assumptions.

---

# 1. Logic and Proofs

Why this unit is included: logic questions often ask for formal transformations and named rules of inference. Learn this unit as a writing system: translate the sentence, apply the rule, and name the rule when it is one of the lecture rules.

## 1.1 Propositions and Connectives

A proposition is a statement that is either true or false.

Examples:

- "2 is even" is a proposition.
- "x is even" is not a proposition until the value/domain of `x` is specified.

Logical connectives:

| Symbol | Name | Meaning |
|---|---|---|
| $\neg p$ | negation | $p$ is false |
| $p \land q$ | conjunction | both true |
| $p \lor q$ | disjunction | at least one true |
| $p \oplus q$ | exclusive or | exactly one true |
| $p \to q$ | implication | if $p$, then $q$ |
| $p \leftrightarrow q$ | biconditional | same truth value |

The implication $p \to q$ is false only when $p$ is true and $q$ is false.

Important equivalences:

$$
\begin{aligned}
p \to q &\equiv \neg p \lor q,\\
\neg(p \to q) &\equiv p \land \neg q,\\
p \leftrightarrow q &\equiv (p \to q)\land(q \to p),\\
&\equiv (p\land q)\lor(\neg p\land \neg q),\\
\neg(p\land q) &\equiv \neg p\lor \neg q,\\
\neg(p\lor q) &\equiv \neg p\land \neg q.
\end{aligned}
$$

Converse, inverse, contrapositive:

For $p \to q$:

- Converse: $q \to p$.
- Inverse: $\neg p \to \neg q$.
- Contrapositive: $\neg q \to \neg p$.

Only the contrapositive is always equivalent to the original implication.

### Wason card test template

Rule: "If a card has property `P`, then it has property `Q`."

To test it, check:

- cards showing `P`;
- cards showing `not Q`.

You do not need to check `Q` or `not P`.

Example from COMP2121 2025: "If even number, then opposite face is B." Visible cards: `5, 8, B, D`.

Check:

- `8`, because it is even and must have `B` on the other side;
- `D`, because it is not `B`, so the other side must not be even.

Do not check `5` or `B`.

## 1.2 Logical Equivalence and Tautologies

A tautology is always true.

A contradiction is always false.

A contingency is sometimes true and sometimes false.

To prove two formulas are equivalent, use either:

1. truth table;
2. known equivalence laws;
3. show both implications.

Useful laws:

$$
\begin{aligned}
p\land T &\equiv p,& p\lor F &\equiv p,\\
p\land F &\equiv F,& p\lor T &\equiv T,\\
p\land p &\equiv p,& p\lor p &\equiv p,\\
p\land\neg p &\equiv F,& p\lor\neg p &\equiv T,\\
p\land q &\equiv q\land p,& p\lor q &\equiv q\lor p,\\
(p\land q)\land r &\equiv p\land(q\land r),&
(p\lor q)\lor r &\equiv p\lor(q\lor r),\\
p\land(q\lor r) &\equiv (p\land q)\lor(p\land r),&
p\lor(q\land r) &\equiv (p\lor q)\land(p\lor r).
\end{aligned}
$$

Implication-only rewriting:

Sometimes a final asks you to rewrite using only $\to$ and parentheses.

Use:

$$
\begin{aligned}
\neg p &\equiv p\to(q\to q) \quad \text{where } q\to q \text{ is a tautology},\\
p\lor q &\equiv (\neg p)\to q,\\
p\land q &\equiv \neg(p\to\neg q),\\
p\leftrightarrow q &\equiv (p\to q)\land(q\to p).
\end{aligned}
$$

If the exam literally allows no symbols except $\to$ and parentheses, pick a fixed tautology such as $(p\to p)$ and build negation from it. Be explicit about your convention.

## 1.3 Predicate Logic and Quantifiers

A predicate is a proposition with variables.

$P(x)$ means a statement about $x$.

Quantifiers:

| Symbol | Name | Meaning |
|---|---|---|
| $\forall x\,P(x)$ | universal | every $x$ satisfies $P$ |
| $\exists x\,P(x)$ | existential | at least one $x$ satisfies $P$ |
| $\exists!x\,P(x)$ | uniqueness | exactly one $x$ satisfies $P$ |

Order matters:

$$
\forall x\,\exists y\,P(x,y)
$$

means every `x` has possibly its own `y`.

$$
\exists y\,\forall x\,P(x,y)
$$

means one single `y` works for all `x`.

### Negating quantified statements

Push negation inward:

$$
\begin{aligned}
\neg\forall x\,P(x) &\equiv \exists x\,\neg P(x),\\
\neg\exists x\,P(x) &\equiv \forall x\,\neg P(x),\\
\neg(P\land Q) &\equiv \neg P\lor\neg Q,\\
\neg(P\lor Q) &\equiv \neg P\land\neg Q,\\
\neg(P\to Q) &\equiv P\land\neg Q.
\end{aligned}
$$

Negation normal form means all negations appear directly before atomic predicates, and only `and`, `or`, and quantifiers remain.

Example:

$$
\neg\forall x\,\forall y\left[(x<y)\to \exists z\,((x<z)\land(z<y))\right]
$$

Step-by-step:

$$
\begin{aligned}
&\exists x\,\exists y\,\neg\left[(x<y)\to\exists z\,((x<z)\land(z<y))\right]\\
\equiv{}&\exists x\,\exists y\,\left[(x<y)\land\neg\exists z\,((x<z)\land(z<y))\right]\\
\equiv{}&\exists x\,\exists y\,\left[(x<y)\land\forall z\,\neg((x<z)\land(z<y))\right]\\
\equiv{}&\exists x\,\exists y\,\left[(x<y)\land\forall z\,((x\ge z)\lor(z\ge y))\right].
\end{aligned}
$$

### Pulling quantifiers to the front

A formula with all quantifiers at the front is in prenex form.

Typical method:

1. Eliminate implications.
2. Push negations inward.
3. Rename bound variables if needed.
4. Move quantifiers outward when the variable is not free in the other part.

Example pattern:

$$
\begin{aligned}
\neg\forall d\,(A(d)\to\forall t\,W(t,d))
&\equiv \exists d\,\neg(A(d)\to\forall t\,W(t,d))\\
&\equiv \exists d\,(A(d)\land\neg\forall t\,W(t,d))\\
&\equiv \exists d\,\exists t\,(A(d)\land\neg W(t,d)).
\end{aligned}
$$

## 1.4 Rules of Inference

Rules of inference are legal argument moves.

Propositional rules from Lec 3:

| Rule | Form |
|---|---|
| Modus Ponens | $p,\ p\to q$, therefore $q$ |
| Modus Tollens | $\neg q,\ p\to q$, therefore $\neg p$ |
| Hypothetical Syllogism | $p\to q,\ q\to r$, therefore $p\to r$ |
| Disjunctive Syllogism | $p\lor q,\ \neg p$, therefore $q$ |
| Addition | $p$, therefore $p\lor q$; valid but basic, so the rule name is not required by the professor's note |
| Simplification | $p\land q$, therefore $p$; valid but basic, so the rule name is not required by the professor's note |
| Resolution | $p\lor q,\ \neg p\lor r$, therefore $q\lor r$ |

Quantifier rules from Lec 4:

| Rule | Meaning |
|---|---|
| Universal instantiation | from $\forall x\,P(x)$, infer $P(a)$ |
| Universal generalization | after proving arbitrary $a$, infer $\forall x\,P(x)$ |
| Existential instantiation | from $\exists x\,P(x)$, introduce a fresh witness $c$ with $P(c)$ |
| Existential generalization | from $P(a)$, infer $\exists x\,P(x)$ |

Fresh witness warning: when using existential instantiation, the chosen object must be new and not secretly assumed to have extra properties.

### Classic Agatha proof

Premises:

$$
\neg p\land q,\qquad r\to p,\qquad \neg r\to s,\qquad \neg t\to\neg s.
$$

Goal: $t$.

Proof:

$$
\begin{array}{rll}
1.&\neg p&\text{from }\neg p\land q\text{ by simplification},\\
2.&\neg r&\text{from }r\to p\text{ and }\neg p\text{ by modus tollens},\\
3.&s&\text{from }\neg r\to s\text{ and }\neg r\text{ by modus ponens},\\
4.&t&\text{from }\neg t\to\neg s\text{ and }s\text{ by modus tollens}.
\end{array}
$$

This exact structure appears in review/finals.

## 1.5 Proof by Cases

Use when the object naturally splits into exhaustive cases.

Example: prove square of an odd integer is $8m+1$.

Any odd integer is either $4k+1$ or $4k+3$.

$$
(4k+1)^2=16k^2+8k+1=8(2k^2+k)+1,
$$
$$
(4k+3)^2=16k^2+24k+9=8(2k^2+3k+1)+1.
$$

So in both cases the square has form $8m+1$.

## 1.6 Invariants

An invariant is a quantity or property that is preserved by every move.

COMP2121 2025 knight problem:

A knight move changes $(x,y)$ by $(\pm2,\pm1)$ or $(\pm1,\pm2)$.

Parity invariant:

Each move changes $x+y$ by one of:

$$
\pm3,\ \pm1.
$$

All are odd. Therefore each move flips the parity of $x+y$. Starting at $(0,0)$, $x+y$ is even after even moves and odd after odd moves.

Manhattan bound:

For each move, $|x|+|y|$ increases by at most $3$ by triangle inequality:

$$
|x+a|+|y+b|\le |x|+|y|+|a|+|b|=|x|+|y|+3.
$$

After $n$ moves, $|x|+|y|\le3n$.

---

# 2. Sets

Why this unit is included: set questions are usually proof-writing questions disguised as algebra. The main skill is to turn symbols into membership statements and justify each identity.

## 2.1 Basic Jargon

A set is a collection of distinct objects.

An element is an object in a set: $x\in A$.

A subset: $A\subseteq B$ means every element of $A$ is also in $B$.

A proper subset: $A\subset B$ means $A\subseteq B$ and $A\ne B$.

The empty set $\emptyset$ has no elements.

The universal set `U` is the ambient set when complements are used.

The power set $\mathcal{P}(A)$ is the set of all subsets of $A$.

If $|A|=n$, then:

$$
|\mathcal{P}(A)|=2^n.
$$

Cartesian product:

$$
A\times B=\{(a,b):a\in A \text{ and } b\in B\}.
$$

## 2.2 Set Operations

Union:

$$
A\cup B=\{x:x\in A\text{ or }x\in B\}.
$$

Intersection:

$$
A\cap B=\{x:x\in A\text{ and }x\in B\}.
$$

Difference:

$$
A-B=A\setminus B=\{x:x\in A\text{ and }x\notin B\}.
$$

Complement:

$$
A^c=U-A.
$$

Symmetric difference:

$$
A\triangle B=(A-B)\cup(B-A).
$$

## 2.3 Core Set Identities

$$
\begin{aligned}
A\cup\emptyset&=A,& A\cap U&=A,\\
A\cup U&=U,& A\cap\emptyset&=\emptyset,\\
A\cup A&=A,& A\cap A&=A,\\
A\cup B&=B\cup A,& A\cap B&=B\cap A,\\
(A\cup B)\cup C&=A\cup(B\cup C),&
(A\cap B)\cap C&=A\cap(B\cap C),\\
A\cap(B\cup C)&=(A\cap B)\cup(A\cap C),&
A\cup(B\cap C)&=(A\cup B)\cap(A\cup C),\\
(A\cup B)^c&=A^c\cap B^c,&
(A\cap B)^c&=A^c\cup B^c,\\
A-B&=A\cap B^c.
\end{aligned}
$$

## 2.4 How to Prove Set Equality

Method 1: element chasing.

To prove $X=Y$:

First prove $X\subseteq Y$: take arbitrary $x\in X$, then show $x\in Y$.

Then prove $Y\subseteq X$: take arbitrary $x\in Y$, then show $x\in X$.

Method 2: set identities.

Use algebraic set laws step by step.

Method 3: membership table.

Allowed sometimes, but some finals explicitly forbid it.

### Example: Cartesian product distributes over union

Prove:

$$
A\times(B\cup C)=(A\times B)\cup(A\times C).
$$

Proof:

$$
\begin{aligned}
(x,y)\in A\times(B\cup C)
&\iff x\in A \text{ and } y\in B\cup C\\
&\iff x\in A \text{ and } (y\in B \text{ or } y\in C)\\
&\iff (x\in A\text{ and }y\in B)\text{ or }(x\in A\text{ and }y\in C)\\
&\iff (x,y)\in A\times B \text{ or } (x,y)\in A\times C\\
&\iff (x,y)\in (A\times B)\cup(A\times C).
\end{aligned}
$$

## 2.5 Common Trap: Set Difference

$A-(A-B)$ is not always $B$.

Compute:

$$
\begin{aligned}
A-(A-B)
&=A\cap(A\cap B^c)^c\\
&=A\cap(A^c\cup B)\\
&=(A\cap A^c)\cup(A\cap B)\\
&=A\cap B.
\end{aligned}
$$

So it equals $A\cap B$, not $B$ in general.

Counterexample:

$$
A=\{1\},\qquad B=\{1,2\},\qquad
A-(A-B)=\{1\}\ne B.
$$

## 2.6 Inclusion-Exclusion for Sets

For two sets:

$$
|A\cup B|=|A|+|B|-|A\cap B|.
$$

For three sets:

$$
|A\cup B\cup C|
=|A|+|B|+|C|
-|A\cap B|-|A\cap C|-|B\cap C|
+|A\cap B\cap C|.
$$

---

# 3. Relations

Why this unit is included: relation questions repeatedly ask students to check definitions. Do not memorize examples only; learn the exact tests for reflexive, symmetric, antisymmetric, transitive, and equivalence relations.

## 3.1 What a Relation Is

A binary relation from $A$ to $B$ is a subset of $A\times B$.

A relation on $A$ is a subset of $A\times A$.

If $(a,b)\in R$, write $aRb$.

## 3.2 Properties of Relations

Reflexive:

$$
\forall a\in A,\ aRa.
$$

Irreflexive:

$$
\forall a\in A,\ \neg(aRa).
$$

Symmetric:

$$
\forall a,b\in A,\ aRb\to bRa.
$$

Antisymmetric:

$$
\forall a,b\in A,\ (aRb\land bRa)\to a=b.
$$

Transitive:

$$
\forall a,b,c\in A,\ (aRb\land bRc)\to aRc.
$$

Asymmetric:

$$
\forall a,b\in A,\ aRb\to\neg(bRa).
$$

Asymmetric implies irreflexive and antisymmetric.

## 3.3 Equivalence Relations

An equivalence relation is reflexive, symmetric, and transitive.

It means "same type under some criterion."

Equivalence class of `a`:

$$
[a]=\{x\in A:xRa\}.
$$

Equivalence classes partition the set:

- every element belongs to exactly one class;
- classes are either identical or disjoint.

Partition means splitting a set into nonempty, disjoint blocks whose union is the whole set.

Counting equivalence relations on a set of size $n$ equals the Bell number $B_n$.

For `n = 5`:

$$
B_5=S(5,1)+S(5,2)+S(5,3)+S(5,4)+S(5,5)
=1+15+25+10+1=52.
$$

Here $S(n,k)$ is a Stirling number of the second kind: number of ways to partition $n$ distinct elements into $k$ nonempty unlabeled blocks.

## 3.4 Standard Equivalence Relation Proof

To prove $R$ is an equivalence relation:

- Reflexive: take arbitrary $a$. Show $aRa$.
- Symmetric: assume $aRb$. Show $bRa$.
- Transitive: assume $aRb$ and $bRc$. Show $aRc$.

Example: On pairs $(x,y)$ with positive coordinates, define:

$$
(x_1,y_1)R(x_2,y_2)\iff x_1y_2=x_2y_1.
$$

This says the fractions $x/y$ are equal.

Reflexive:

$$
x_1y_1=x_1y_1.
$$

Symmetric:

If $x_1y_2=x_2y_1$, then $x_2y_1=x_1y_2$.

Transitive:

If $\frac{x_1}{y_1}=\frac{x_2}{y_2}$ and $\frac{x_2}{y_2}=\frac{x_3}{y_3}$, then $\frac{x_1}{y_1}=\frac{x_3}{y_3}$, so $x_1y_3=x_3y_1$.

Equivalence class of $(2,3)$ inside $\{1,\ldots,6\}\times\{1,\ldots,6\}$:

All pairs with ratio $2/3$:

$$
[(2,3)]=\{(2,3),(4,6)\}.
$$

Equivalence class of $(4,4)$:

Ratio $1$:

$$
[(4,4)]=\{(1,1),(2,2),(3,3),(4,4),(5,5),(6,6)\}.
$$

## 3.5 Complement of an Equivalence Relation

If $R$ is an equivalence relation on $A$, its complement $A\times A-R$ is generally:

- not reflexive, because all $(a,a)$ are in $R$;
- symmetric, because if $a$ is not equivalent to $b$, then $b$ is not equivalent to $a$;
- not necessarily transitive.

Counterexample for transitivity:

Let $A=\{1,2,3\}$ and $R$ be equality. Then complement is "not equal."

$$
1\ne2\text{ and }2\ne1,\quad\text{but }1=1.
$$

So transitivity fails.

## 3.6 Union and Intersection of Transitive Relations

Intersection of transitive relations is always transitive.

Proof:

If $(a,b)$ and $(b,c)$ are in $R\cap S$, then both are in $R$ and both are in $S$. Since both $R$ and $S$ are transitive, $(a,c)$ is in both. So $(a,c)\in R\cap S$.

Union of transitive relations is not always transitive.

Counterexample:

$$
A=\{1,2,3\},\qquad R=\{(1,2)\},\qquad S=\{(2,3)\}.
$$

Both are transitive vacuously, but $R\cup S$ has $(1,2)$ and $(2,3)$ without $(1,3)$.

## 3.7 Relation Composition and Inverse

Inverse:

$$
R^{-1}=\{(b,a):(a,b)\in R\}.
$$

Composition:

If $R\subseteq A\times B$ and $S\subseteq B\times C$,

$$
S\circ R=\{(a,c):\exists b\in B\text{ such that }aRb\text{ and }bSc\}.
$$

Read right to left: first `R`, then `S`.

## 3.8 Partial Orders

A partial order is reflexive, antisymmetric, and transitive.

Example: subset relation $\subseteq$ on $\mathcal{P}(S)$.

If a final asks about functions ordered pointwise:

Let $Y$ have partial order $\le_Y$. Define functions $F\preceq G$ iff for every $x\in X$,

$$
F(x)\le_Y G(x).
$$

Then this is a partial order:

- reflexive because $F(x)\le_Y F(x)$;
- antisymmetric because if $F(x)\le_Y G(x)$ and $G(x)\le_Y F(x)$ for all $x$, then $F(x)=G(x)$ for all $x$;
- transitive pointwise.

---

# 4. Functions and Growth

Why this unit is included: function questions test definitions such as injective and surjective, while growth questions test whether you can compare functions using formal asymptotic notation.

## 4.1 Function Jargon

A function $f:A\to B$ assigns each input in domain $A$ exactly one output in codomain $B$.

Domain: allowed inputs.

Codomain: declared target set.

Range/image:

$$
f(A)=\{f(a):a\in A\}.
$$

Preimage of $S\subseteq B$:

$$
f^{-1}(S)=\{a\in A:f(a)\in S\}.
$$

This notation does not require `f` to have an inverse function.

## 4.2 Injective, Surjective, Bijective

Injective / one-to-one:

$$
f(a_1)=f(a_2)\implies a_1=a_2.
$$

No two different inputs hit the same output.

Surjective / onto:

$$
\forall b\in B,\ \exists a\in A\text{ such that }f(a)=b.
$$

Every codomain element is hit.

Bijective:

Both injective and surjective.

For finite sets with same size, injective iff surjective iff bijective.

## 4.3 Composition and Identity

Composition:

$$
(g\circ f)(a)=g(f(a)).
$$

Identity function on $A$:

$$
I_A(a)=a.
$$

Important theorem from finals:

If $f:A\to B$, $g:B\to A$, and

$$
g\circ f=I_A,
$$

then:

- `f` is injective;
- `g` is surjective.

Proof `f` injective:

Assume `f(a1)=f(a2)`.

Apply `g`:

$$
g(f(a_1))=g(f(a_2)).
$$

Since $g\circ f=I_A$,

$$
a_1=a_2.
$$

Proof `g` surjective:

For any $a\in A$, choose $b=f(a)\in B$. Then:

$$
g(b)=g(f(a))=a.
$$

So every `a` is hit by `g`.

## 4.4 Floors and Ceilings

Floor:

$$
\lfloor x\rfloor=\text{greatest integer }\le x.
$$

Ceiling:

$$
\lceil x\rceil=\text{least integer }\ge x.
$$

Useful inequalities:

$$
\lfloor x\rfloor\le x<\lfloor x\rfloor+1,\qquad
\lceil x\rceil-1<x\le\lceil x\rceil,
$$
$$
x-1<\lfloor x\rfloor\le x\le\lceil x\rceil<x+1.
$$

Useful identity:

$$
\lceil x\rceil=-\lfloor -x\rfloor.
$$

Common proof style:

Let $n=\lfloor x\rfloor$. Then $n\le x<n+1$. Manipulate this inequality and identify the desired floor or ceiling.

## 4.5 Big-O, Big-Omega, Big-Theta

These compare eventual growth rates.

`f(n) = O(g(n))` means `f` is eventually at most a constant multiple of `g`.

Formal definition:

$$
f(n)=O(g(n))
\iff
\exists C>0,\exists n_0,\forall n\ge n_0,\ |f(n)|\le C|g(n)|.
$$

$f(n)=\Omega(g(n))$ means $f$ is eventually at least a constant multiple of $g$.

$$
f(n)=\Omega(g(n))
\iff
\exists c>0,\exists n_0,\forall n\ge n_0,\ |f(n)|\ge c|g(n)|.
$$

$f(n)=\Theta(g(n))$ means both $O$ and $\Omega$.

$$
f(n)=\Theta(g(n))
\iff
f(n)=O(g(n))\text{ and }g(n)=O(f(n)).
$$

Growth hierarchy:

$$
\log n \ll n^a \ll n^b \ll c^n \ll n! \ll n^n
$$

for constants `0 < a < b` and `c > 1`.

Examples:

$$
3n! = O((3n)!).
$$

because `(3n)!` contains all factors of `n!` and many more.

But:

$$
(3n)! \ne O(3n!).
$$

since `(3n)!/(3n!)` grows without bound.

### Big-O algebra

If $f_1=O(g_1)$ and $f_2=O(g_2)$, then:

$$
f_1+f_2=O(\max(g_1,g_2)),\qquad f_1f_2=O(g_1g_2).
$$

For positive functions:

$$
\sum_{k=1}^n k^2=\Theta(n^3),\qquad
\sum_{k=1}^n k^2\,2^k=\Theta(n^2 2^n).
$$

For the second, the final terms dominate because of the exponential factor.

---

# 5. Counting

Why this unit is included: counting questions are easy to overcount. This unit teaches which rule applies, why the cases are disjoint or sequential, and when to correct overcounting.

Counting is the most formula-heavy part of the course, but most problems reduce to asking:

1. Are objects distinct or indistinguishable?
2. Does order matter?
3. Are repetitions allowed?
4. Are boxes/groups labeled or unlabeled?
5. Is there an "at least one", "at most", or forbidden condition?

## 5.1 Product Rule and Sum Rule

Product rule:

If task A can be done in $m$ ways and then task B in $n$ ways, total $mn$.

Sum rule:

If a task can be done in either one of disjoint cases with counts $m$ and $n$, total $m+n$.

Subtraction rule:

$$
\text{valid}=\text{total}-\text{invalid}.
$$

Division rule:

If each object is counted exactly $k$ times, divide by $k$.

## 5.2 Permutations and Combinations

Permutation:

Choose and order `r` objects from `n` distinct objects:

$$
P(n,r)=\frac{n!}{(n-r)!}.
$$

Combination:

Choose `r` objects from `n` distinct objects without order:

$$
\binom{n}{r}=\frac{n!}{r!(n-r)!}.
$$

Permutations of multiset with repeated objects:

If there are $n$ total objects with multiplicities $n_1,\ldots,n_k$,

$$
\frac{n!}{n_1!n_2!\cdots n_k!}.
$$

## 5.3 Circular Arrangements

For `n` distinct people around a round table, rotations are the same:

$$
(n-1)!.
$$

If there is a distinguished person, fix that person and arrange the rest.

If reflection is also considered the same, divide by `2`; but COMP2121 circular seating usually only identifies rotations, not reflections, unless stated.

Example: 5 parents, 5 students, 1 teacher, no two students adjacent and no two parents adjacent.

Fix teacher. The seats must alternate around the teacher. Choose whether a parent or student is to the right of teacher: `2` choices. Arrange parents and students:

$$
2(5!)^2.
$$

## 5.4 Stars and Bars

Nonnegative integer solutions:

$$
x_1+x_2+\cdots+x_k=n,\qquad x_i\ge0.
$$

Count:

$$
\binom{n+k-1}{k-1}.
$$

Positive integer solutions:

$$
x_1+\cdots+x_k=n,\qquad x_i\ge1.
$$

Let `yi = xi - 1`, so count:

$$
\binom{n-1}{k-1}.
$$

Upper bounds:

For:

$$
x_1+\cdots+x_k=n,\qquad 0\le x_i\le u.
$$

use inclusion-exclusion:

$$
\sum_{j=0}^k(-1)^j\binom{k}{j}
\binom{n-j(u+1)+k-1}{k-1},
$$

where terms with negative top are zero.

Lower and upper bounds:

First shift by lower bounds, then apply upper-bound inclusion-exclusion.

Example:

$$
x_1+x_2+x_3+x_4=12,\qquad 1\le x_i\le4.
$$

Let `yi = xi - 1`, so:

$$
y_1+y_2+y_3+y_4=8,\qquad 0\le y_i\le3.
$$

Count:

$$
\binom{11}{3}-\binom{4}{1}\binom{7}{3}
+\binom{4}{2}\binom{3}{3}.
$$

## 5.5 Weak Compositions

A weak composition of `n` into `k` parts is a solution:

$$
x_1+\cdots+x_k=n,\qquad x_i\ge0.
$$

Number:

$$
\binom{n+k-1}{k-1}.
$$

Exactly `r` zero parts:

Choose which `r` parts are zero, then make remaining `k-r` parts positive:

$$
\binom{k}{r}\binom{n-1}{k-r-1}.
$$

Example: weak compositions of 10 into 5 parts with exactly 2 zeros:

$$
\binom{5}{2}\binom{9}{2}.
$$

## 5.6 Inclusion-Exclusion

For properties $P_1,\ldots,P_k$, number with none of the bad properties:

$$
\text{valid}
=\text{total}
-\text{one bad}
+\text{two bad}
-\text{three bad}
+\cdots.
$$

Formula:

$$
\left|\overline{A_1\cup\cdots\cup A_k}\right|
=\sum_{J\subseteq\{1,\ldots,k\}}(-1)^{|J|}
\left|\bigcap_{j\in J}A_j\right|.
$$

### Derangements

A derangement is a permutation with no fixed points.

Number of derangements:

$$
D_n=n!\sum_{i=0}^n\frac{(-1)^i}{i!}.
$$

Recurrences:

$$
D_n=nD_{n-1}+(-1)^n,\qquad
D_n=(n-1)(D_{n-1}+D_{n-2}).
$$

### Forbidden adjacent patterns in permutations

Example from Lec 21:

Permutations of $\{1,\ldots,8\}$ avoiding all consecutive patterns:

$$
(1,2),(2,3),\ldots,(7,8).
$$

Treat selected forbidden adjacent patterns as glued blocks. If `k` such patterns are forced, the permutation has `8-k` blocks, so `(8-k)!` arrangements. Therefore:

$$
8!-\binom{7}{1}7!+\binom{7}{2}6!-\cdots-\binom{7}{7}1!.
$$

## 5.7 Pigeonhole Principle

Basic form:

If `n+1` objects are placed into `n` boxes, some box has at least 2 objects.

Generalized form:

If `N` objects are placed into `k` boxes, some box has at least:

$$
\left\lceil\frac{N}{k}\right\rceil
$$

objects.

### Divisibility pigeonhole template

If $S\subseteq\{1,\ldots,2n\}$ has $n+1$ elements, prove two elements $a,b\in S$ satisfy $a\mid b$.

Write each number uniquely as:

$$
2^k m
$$

where $m$ is odd. The odd part $m$ is one of:

$$
1,3,5,\ldots,2n-1.
$$

There are $n$ possible odd parts. Since $S$ has $n+1$ elements, two have the same odd part:

$$
a=2^r m,\qquad b=2^s m.
$$

Assume $r\le s$, then $a\mid b$.

### Erdos-Szekeres monotone subsequence

Every sequence of $(r-1)(s-1)+1$ distinct numbers contains:

- an increasing subsequence of length $r$, or
- a decreasing subsequence of length $s$.

For increasing or decreasing length $7$, set $r=s=7$:

$$
(7-1)(7-1)+1=37.
$$

So any sequence of at least 37 distinct numbers contains an increasing or decreasing subsequence of length 7. Therefore a sequence of 40 distinct numbers certainly does.

Proof idea:

For each position, assign pair $(I,D)$ where:

- `I` = length of longest increasing subsequence starting there;
- `D` = length of longest decreasing subsequence starting there.

If no increasing/decreasing subsequence has length 7, then each coordinate is in $\{1,\ldots,6\}$, only 36 pairs. Two positions must share a pair, contradiction.

## 5.8 Surjections and Stirling Numbers

Number of functions from an $n$-element set to a $k$-element set:

$$
k^n.
$$

Number of injections from $n$ to $k$ if $n\le k$:

$$
P(k,n)=\frac{k!}{(k-n)!}.
$$

Number of bijections between two `n`-element sets:

$$
n!.
$$

Number of surjections from $n$ labeled elements onto $k$ labeled boxes:

$$
k!S(n,k)
=\sum_{i=0}^k(-1)^i\binom{k}{i}(k-i)^n.
$$

Stirling number of the second kind:

$$
S(n,k)=\#\{\text{partitions of }n\text{ distinct objects into }k\text{ nonempty unlabeled groups}\}.
$$

Formula:

$$
S(n,k)=\frac{1}{k!}\sum_{i=0}^k(-1)^i\binom{k}{i}(k-i)^n.
$$

Examples:

$$
S(5,1)=1,\quad S(5,2)=15,\quad S(5,3)=25,\quad
S(5,4)=10,\quad S(5,5)=1,\quad B_5=52.
$$

Distributing $11$ different people into $3$ nonempty unlabeled groups:

$$
S(11,3)=\frac{3^{11}-3\cdot2^{11}+3}{6}=28501.
$$

## 5.9 Counting Equivalence Relations

Equivalence relations correspond exactly to partitions.

If set $A$ has 5 elements, number of equivalence relations:

$$
B_5=52.
$$

If exactly $k$ equivalence classes:

$$
S(n,k).
$$

If class sizes are specified, divide by factorials for indistinguishable blocks of equal size.

Example: 6 elements, exactly two classes of size 3:

$$
\frac{\binom{6}{3}}{2}=10.
$$

## 5.10 Combinatorial Proofs

A combinatorial proof proves an identity by counting the same set in two ways.

Example:

$$
\binom{n}{k}=\binom{n-1}{k}+\binom{n-1}{k-1}.
$$

Count $k$-subsets of $\{1,\ldots,n\}$:

- subsets not containing $n$: $\binom{n-1}{k}$;
- subsets containing $n$: choose remaining $k-1$ from first $n-1$, giving $\binom{n-1}{k-1}$.

## 5.11 Generating Functions for Counting Dice Sums

For dice, generating functions are often fastest.

One fair die:

$$
x+x^2+x^3+x^4+x^5+x^6.
$$

Five dice sum to 14:

Number of outcomes is coefficient of `x^14` in:

$$
(x+x^2+x^3+x^4+x^5+x^6)^5.
$$

Probability:

$$
\frac{[x^{14}](x+x^2+\cdots+x^6)^5}{6^5}.
$$

Stars-and-bars version:

Let die values be `yi in {1,...,6}`. Set `xi=yi-1`, so:

$$
x_1+\cdots+x_5=9,\qquad 0\le x_i\le5.
$$

Count:

$$
\binom{13}{4}-\binom{5}{1}\binom{7}{4}.
$$

because at most one variable can exceed 5 when sum is 9.

## 5.12 Graph Coloring as Counting

Proper vertex coloring: adjacent vertices get different colors.

Example graph from COMP2121 2025:

Vertices $v_1,v_2,v_3,v_4$, edges:

$$
v_1v_2,\ v_2v_3,\ v_1v_3,\ v_1v_4,\ v_3v_4.
$$

This is two triangles sharing edge $v_1v_3$.

With 6 colors:

$$
6\cdot5\cdot4\cdot4=480.
$$

## 5.13 Descent Sets

For a permutation $p=p_1p_2\cdots p_n$, an index $k$ is a descent if:

$$
p_k>p_{k+1}.
$$

The descent set is the set of all descent positions.

If asked how many permutations have descent set contained in a set $T$, split the permutation into increasing blocks separated only at positions in $T$.

For $n=8$ and descents allowed only at $\{1,4,6\}$, the blocks are:

$$
1\mid 2,3,4\mid 5,6\mid 7,8.
$$

Within each block, entries must be increasing. Choose which values go into each block:

$$
\frac{8!}{1!\,3!\,2!\,2!}.
$$

This counts descent set subset of $\{1,4,6\}$, not exactly equal to it.

## 5.14 Counting Rules To Cite After Learning This Unit

Why this section is here: the rules below are used throughout counting questions, but they are placed after the counting unit so students first see what the rules mean and how they are used.

| Rule or theorem | Statement to remember | Why cite it in solutions |
| --- | --- | --- |
| **Product Rule** | If consecutive choices have $m$ and $n$ possibilities, total $mn$. | Shows that choices are sequential and independent in the counting sense. |
| **Sum Rule** | If disjoint cases have counts $m$ and $n$, total $m+n$. | Shows that you split into non-overlapping cases. |
| **Division Rule** | If each object was counted exactly $k$ times, divide by $k$. | Justifies dividing away overcounting, especially circular arrangements or unlabeled groups. |
| **Inclusion-Exclusion Principle** | Add single counts, subtract pair overlaps, add triple overlaps, and continue. | Explains corrections for overlapping forbidden or required properties. |
| **Pigeonhole Principle** | More objects than boxes forces some box to contain at least two objects. | Justifies existence conclusions without constructing the object directly. |
| **Generalized Pigeonhole Principle** | Putting $N$ objects into $k$ boxes gives a box with at least $\left\lceil N/k\right\rceil$ objects. | Gives the exact forced lower bound in stronger pigeonhole problems. |

---

# 6. Probability and Random Variables

Why this unit is included: probability questions require a model before a formula. Always identify the sample space, the event, and whether you are conditioning or using independence.

## 6.1 Sample Space and Events

Sample space $\Omega$: all possible outcomes.

Event: subset of $\Omega$.

For equally likely finite outcomes:

$$
\Pr(A)=\frac{|A|}{|\Omega|}.
$$

Complement:

$$
\Pr(A^c)=1-\Pr(A).
$$

Union:

$$
\Pr(A\cup B)=\Pr(A)+\Pr(B)-\Pr(A\cap B).
$$

Union bound:

$$
\Pr(A_1\cup\cdots\cup A_n)\le \Pr(A_1)+\cdots+\Pr(A_n).
$$

## 6.2 Conditional Probability

Definition:

$$
\Pr(A\mid B)=\frac{\Pr(A\cap B)}{\Pr(B)},\qquad \Pr(B)>0.
$$

Multiplication rule:

$$
\Pr(A\cap B)=\Pr(A\mid B)\Pr(B).
$$

Chain rule:

$$
\Pr(A\cap B\cap C)=\Pr(A)\Pr(B\mid A)\Pr(C\mid A\cap B).
$$

## 6.3 Independence

Events `A` and `B` are independent if:

$$
\Pr(A\cap B)=\Pr(A)\Pr(B).
$$

Equivalently, if $\Pr(B)>0$:

$$
\Pr(A\mid B)=\Pr(A).
$$

Conditional independence is different from independence.

An event of probability 0 is independent of every event, because:

$$
\Pr(A\cap B)=0=\Pr(A)\Pr(B).
$$

when $\Pr(A)=0$.

## 6.4 Law of Total Probability and Bayes

If $B_1,\ldots,B_k$ partition the sample space:

$$
\Pr(A)=\sum_i \Pr(A\mid B_i)\Pr(B_i).
$$

Bayes:

$$
\Pr(B_j\mid A)=
\frac{\Pr(A\mid B_j)\Pr(B_j)}
{\sum_i\Pr(A\mid B_i)\Pr(B_i)}.
$$

### Fire detector template

If:

$$
\Pr(T\mid F)=0.9,\qquad
\Pr(T\mid S)=0.1,\qquad
S:F=2:1.
$$

then:

$$
\Pr(F)=\frac13,\qquad \Pr(S)=\frac23.
$$

So:

$$
\Pr(F\mid T)
=\frac{(0.9)(1/3)}{(0.9)(1/3)+(0.1)(2/3)}
=\frac{0.3}{0.3+1/15}
=\frac{9}{11}.
$$

## 6.5 Random Variables

A random variable is a function from outcomes to numbers.

Expected value:

$$
\mathbb{E}[X]=\sum_x x\,\Pr(X=x).
$$

Linearity:

$$
\mathbb{E}[X+Y]=\mathbb{E}[X]+\mathbb{E}[Y].
$$

always, even if not independent.

Variance:

$$
\operatorname{Var}(X)
=\mathbb{E}\left[(X-\mathbb{E}[X])^2\right]
=\mathbb{E}[X^2]-\mathbb{E}[X]^2.
$$

If independent:

$$
\operatorname{Var}(X+Y)=\operatorname{Var}(X)+\operatorname{Var}(Y).
$$

Indicator variable:

For event `A`,

$$
I_A=\begin{cases}
1,&A\text{ occurs},\\
0,&A\text{ does not occur},
\end{cases}
\qquad
\mathbb{E}[I_A]=\Pr(A).
$$

Use indicators to count expected numbers.

## 6.6 Conditional Expectation and Total Variance

Conditional expectation:

$$
\mathbb{E}[X\mid Y=y]
$$

is the expected value of `X` after knowing `Y=y`.

Law of total expectation:

$$
\mathbb{E}[X]=\mathbb{E}[\mathbb{E}[X\mid Y]].
$$

Law of total variance:

$$
\operatorname{Var}(X)
=\operatorname{Var}(\mathbb{E}[X\mid Y])
+\mathbb{E}[\operatorname{Var}(X\mid Y)].
$$

Proof idea:

Start with:

$$
\operatorname{Var}(X)=\mathbb{E}[X^2]-\mathbb{E}[X]^2.
$$

Also:

$$
\mathbb{E}[\operatorname{Var}(X\mid Y)]
=\mathbb{E}\!\left[\mathbb{E}[X^2\mid Y]-\mathbb{E}[X\mid Y]^2\right]
=\mathbb{E}[X^2]-\mathbb{E}\!\left[\mathbb{E}[X\mid Y]^2\right].
$$

And:

$$
\operatorname{Var}(\mathbb{E}[X\mid Y])
=\mathbb{E}\!\left[\mathbb{E}[X\mid Y]^2\right]
-\mathbb{E}[\mathbb{E}[X\mid Y]]^2
=\mathbb{E}\!\left[\mathbb{E}[X\mid Y]^2\right]-\mathbb{E}[X]^2.
$$

Add them to get `E[X^2]-E[X]^2`.

## 6.7 Bernoulli, Binomial, Geometric

Bernoulli random variable:

$$
X=\begin{cases}1,&\text{with probability }p,\\0,&\text{with probability }1-p,\end{cases}
\qquad
\mathbb{E}[X]=p,\qquad
\operatorname{Var}(X)=p(1-p).
$$

Binomial:

`X ~ Bin(n,p)` counts successes in `n` independent Bernoulli trials.

$$
\Pr(X=k)=\binom{n}{k}p^k(1-p)^{n-k},\qquad
\mathbb{E}[X]=np,\qquad
\operatorname{Var}(X)=np(1-p).
$$

Geometric:

Number of independent trials until first success.

$$
\Pr(X=k)=(1-p)^{k-1}p,\qquad
\mathbb{E}[X]=\frac1p.
$$

## 6.8 Random Walks on Lattices

From `(0,0)`, each step goes right or up with probability `1/2`.

Probability of passing through `(a,b)`:

The walk reaches `(a,b)` after `a+b` steps, with exactly `a` right steps and `b` up steps.

$$
\Pr(\text{pass through }(a,b))
=\binom{a+b}{a}\frac{1}{2^{a+b}}.
$$

For multiple ordered points:

If:

$$
0\le a_1\le a_2\le\cdots\le a_n,\qquad
0\le b_1\le b_2\le\cdots\le b_n.
$$

then multiply segment probabilities:

$$
\frac{1}{2^{a_n+b_n}}
\prod_{i=1}^n
\binom{(a_i-a_{i-1})+(b_i-b_{i-1})}{a_i-a_{i-1}}.
$$

where `(a0,b0)=(0,0)`.

## 6.9 Random Walks on Subsets

Vertices are subsets of $[n]$. Start at $\emptyset$. At each step, add one uniformly chosen missing element.

Sample space:

All permutations of `[n]`. A permutation records the order in which elements are added.

Each permutation has probability:

$$
\frac{1}{n!}.
$$

Probability the walk passes through a fixed subset $S$ of size $k$:

The first `k` elements in the permutation must be exactly `S`.

$$
\Pr(\text{pass through }S)
=\frac{k!(n-k)!}{n!}
=\frac{1}{\binom{n}{k}}.
$$

Probability the walk passes through two subsets $A$ and $B$:

- If neither is subset of the other, probability $0$.
- If $A\subseteq B$, then:

$$
\Pr(\text{pass through both})
=\frac{|A|!(|B|-|A|)!(n-|B|)!}{n!}.
$$

## 6.10 Dice Pair / One Pair Probability

Five fair dice, exactly one pair and no triple/quad/quint.

Count outcomes:

1. Choose paired value: `6`.
2. Choose positions of the pair: $\binom{5}{2}$.
3. Choose distinct values for remaining 3 dice from the other 5 values and assign to positions:

$$
P(5,3)=5\cdot4\cdot3.
$$

Total favorable:

$$
6\binom{5}{2}P(5,3).
$$

Probability:

$$
\frac{6\binom{5}{2}P(5,3)}{6^5}.
$$

## 6.11 Midpoint Parity Probability

For lattice points, midpoint belongs to the integer lattice iff corresponding coordinates have the same parity.

If points are in:

$$
S=\{(x,y,z)\in\mathbb{N}^3:x\le2,\ y\le3,\ z\le4\}.
$$

then there are:

$$
3\cdot4\cdot5=60.
$$

points if $\mathbb{N}$ includes $0$, as in COMP2121.

Two distinct points have integer midpoint iff they lie in the same parity class modulo 2 in all coordinates.

Count sizes of the 8 parity classes, then:

$$
\Pr(\text{integer midpoint})
=\frac{\sum_{\text{parity classes }C}\binom{|C|}{2}}{\binom{60}{2}}.
$$

## 6.12 Half-Disk Probability

For $n$ random points independently uniformly on a disk, probability they all lie in some half-disk is a classic geometry probability:

$$
\frac{n}{2^{n-1}}.
$$

for points in general position and half-disk through the center.

For $n=4$:

$$
\frac48=\frac12.
$$

Idea:

Place the $n$ radial angles on a circle. All points lie in some semicircle iff one of the points can be chosen as the clockwise starting boundary and all other $n-1$ points lie within the next half-circle. For each starting point, probability is $(1/2)^{n-1}$. These events are disjoint almost surely, so total $n/2^{n-1}$.

## 6.13 Probability Rules To Cite After Learning This Unit

Why this section is here: these rules are cited in exam solutions because they justify how a probability expression was built. They are placed after the probability unit so the symbols and conditions have already been introduced.

| Rule or theorem | Statement to remember | Why cite it in solutions |
| --- | --- | --- |
| **Bayes' Theorem** | $\Pr(B_j\mid A)=\dfrac{\Pr(A\mid B_j)\Pr(B_j)}{\sum_i\Pr(A\mid B_i)\Pr(B_i)}$. | Use when reversing conditional probability, such as from $\Pr(\text{alarm}\mid\text{fire})$ to $\Pr(\text{fire}\mid\text{alarm})$. |
| **Law Of Total Probability** | If $B_1,\ldots,B_k$ partition the sample space, then $\Pr(A)=\sum_i\Pr(A\mid B_i)\Pr(B_i)$. | Use when an event can happen through several exhaustive cases. |
| **Linearity Of Expectation** | $\mathbb{E}[X+Y]=\mathbb{E}[X]+\mathbb{E}[Y]$, even without independence. | Use when an expected value is easier to split into parts or indicators. |
| **Law Of Total Variance** | $\operatorname{Var}(X)=\operatorname{Var}(\mathbb{E}[X\mid Y])+\mathbb{E}[\operatorname{Var}(X\mid Y)]$. | Use when a problem conditions on another random variable and asks for variance. |

---

# 7. Graph Theory

Why this unit is included: graph questions are theorem-trigger questions. First translate the story into a graph property, then cite the correct theorem only after checking its conditions.

## 7.1 Basic Graph Jargon

A graph $G=(V,E)$ has:

- vertex set `V`;
- edge set `E`.

Simple graph:

- no loops;
- no multiple edges;
- undirected unless stated.

Multigraph:

- multiple edges allowed.

Pseudograph:

- loops may be allowed.

Adjacent vertices share an edge.

Incident means a vertex touches an edge.

Degree `deg(v)` is the number of edges incident to `v`; loops count twice in undirected graphs.

Minimum degree:

$$
\delta(G)
$$

Maximum degree:

$$
\Delta(G)
$$

Complete graph $K_n$:

Every pair of vertices adjacent.

$$
|E(K_n)|=\binom{n}{2}.
$$

Complete bipartite graph $K_{m,n}$:

Vertices split into two parts of sizes `m,n`; all cross edges exist; no edges inside parts.

$$
|E(K_{m,n})|=mn.
$$

Cycle graph $C_n$: one cycle on $n$ vertices.

Wheel graph $W_n$: cycle plus a universal center vertex.

## 7.2 Handshaking Lemma

For undirected graph:

$$
\sum_{v\in V}\deg(v)=2|E|.
$$

Consequences:

- number of odd-degree vertices is even;
- average degree is $2|E|/|V|$.

### Football schedule impossibility

If each of 13 teams in a division plays exactly 9 games within its own division, then total internal degree sum in that division is:

$$
13\cdot9=117,
$$

which is odd. But degree sum must equal twice the number of internal games, hence even. Contradiction.

## 7.3 Connectivity

A path is a sequence of vertices connected by edges.

A graph is connected if every pair of vertices has a path between them.

Connected component: maximal connected subgraph.

Cut vertex: removing it increases number of connected components.

Cut edge / bridge: removing it increases number of connected components.

Vertex connectivity $\kappa(G)$: minimum number of vertices whose removal disconnects the graph or makes it trivial.

Edge connectivity $\lambda(G)$: minimum number of edges whose removal disconnects graph.

Important bound:

$$
\kappa(G)\le\lambda(G)\le\delta(G).
$$

## 7.4 Bipartite Graphs

A graph is bipartite if vertices can be split into $X\cup Y$ so every edge goes between $X$ and $Y$.

Equivalent facts:

$$
G\text{ is bipartite}
\iff G\text{ has no odd cycle}
\iff G\text{ is 2-colorable}.
$$

Planar edge bounds for bipartite graphs require Euler's formula, so they are proved later in the planar graph section after Euler's formula is introduced.

## 7.5 Euler Paths and Tours

Euler path: uses every edge exactly once.

Euler circuit/tour: Euler path that starts and ends at same vertex.

For connected undirected graphs:

Euler circuit exists iff every vertex has even degree.

Euler path but not circuit exists iff exactly two vertices have odd degree.

For disconnected graphs, ignore isolated vertices but all nonzero-degree vertices must lie in one connected component.

For multigraphs, the same degree criterion works.

### How operations affect Euler tours

Adding a cycle to an Eulerian graph preserves even degrees, but may fail connectivity if the cycle is added on vertices disconnected from the original nonzero component. In finals, check both:

1. all degrees even;
2. connectedness of non-isolated part.

Deleting edges of a cycle from an Eulerian graph preserves parity, but can disconnect the graph. So not always Eulerian.

## 7.6 Hamilton Paths and Cycles

Hamilton path: visits every vertex exactly once.

Hamilton cycle: cycle visiting every vertex exactly once and returning to start.

Complete graph $K_n$ has:

$$
\frac{(n-1)!}{2}
$$

Hamilton cycles, since rotations and reverse orientations are the same.

Hamilton cycles in $K_n$ containing edge $\{1,2\}$:

$$
(n-2)!.
$$

Containing two disjoint edges $\{1,2\}$ and $\{3,4\}$:

$$
2(n-3)!.
$$

Dirac's theorem:

If $G$ is simple with $n\ge3$ and every vertex has degree at least $n/2$, then $G$ has a Hamilton cycle.

Ore's theorem:

If $G$ is simple with $n\ge3$ and for every nonadjacent pair $u,v$:

$$
\deg(u)+\deg(v)\ge n,
$$

then `G` has a Hamilton cycle.

Useful negative fact:

If a connected graph has a bridge, it cannot have a Hamilton cycle.

If a graph has a cut vertex, it cannot have a Hamilton cycle.

## 7.7 Matchings and Hall's Theorem

A matching is a set of edges with no shared endpoints.

A perfect matching covers every vertex.

In a bipartite graph with parts $X,Y$, Hall's condition says there is a matching covering $X$ iff:

$$
\forall S\subseteq X,\quad |N(S)|\ge |S|.
$$

Here `N(S)` is the set of neighbors of vertices in `S`.

### Regular bipartite graph perfect matching

If $G$ is $k$-regular bipartite with equal parts $X,Y$, then it has a perfect matching.

Proof:

For any $S\subseteq X$, count edges from $S$ to $N(S)$.

There are exactly:

$$
k|S|
$$

edges leaving `S`.

Every vertex in `N(S)` has degree `k`, so it can receive at most `k` of those edges:

$$
k|S|\le k|N(S)|.
$$

Since `k>0`,

$$
|S|\le |N(S)|.
$$

Hall applies.

### Decomposing regular bipartite graphs

If a bipartite graph is $r$-regular, repeatedly find a perfect matching and remove it. Removing a perfect matching reduces every degree by 1. Repeat $r$ times.

This proves you can schedule $r$ rounds so each child gets a wanted toy each round and never repeats a toy.

## 7.8 Graph Coloring

A proper vertex coloring assigns colors to vertices so adjacent vertices have different colors.

Chromatic number $\chi(G)$ is the minimum number of colors needed.

Facts:

$$
\chi(K_n)=n,\qquad
\chi(C_n)=
\begin{cases}
2,&n\text{ even},\\
3,&n\text{ odd},
\end{cases}
$$
$$
G\text{ is bipartite}\iff \chi(G)\le2
\quad\text{(assuming at least one edge).}
$$

Clique lower bound:

If $G$ contains $K_r$, then:

$$
\chi(G)\ge r.
$$

Greedy upper bound:

$$
\chi(G)\le\Delta(G)+1.
$$

Planar graph theorem:

Every planar graph is 4-colorable, but not every 4-colorable graph is planar.

### Critical graphs

A graph is `k`-critical if:

$$
\chi(G)=k
$$

but deleting any edge lowers chromatic number.

If `G` is `k`-critical, then every vertex has degree at least `k-1`.

Proof idea:

If some vertex `v` has degree at most `k-2`, color `G-v` using `k-1` colors. Vertex `v` has at most `k-2` colored neighbors, so one of the `k-1` colors remains available. Then `G` would be `(k-1)`-colorable, contradiction.

## 7.9 Edge Coloring

An edge coloring assigns colors to edges so edges sharing an endpoint get different colors.

Edge chromatic number:

$$
\chi'(G)
$$

Minimum number of colors needed for edges.

Lower bound:

$$
\chi'(G)\ge\Delta(G).
$$

Because all edges incident to a maximum-degree vertex need different colors.

For bipartite graphs:

$$
\chi'(G)=\Delta(G).
$$

This is Konig's line coloring theorem. It appears in MATH3600 and is adjacent to COMP2121 matching material.

## 7.10 Planar Graphs

A planar graph can be drawn in the plane with no crossing edges.

Face/region: area bounded by edges in a planar drawing, including the outside face.

Euler's formula:

For a connected planar graph:

$$
v-e+f=2.
$$

For planar graph with `c` connected components:

$$
v-e+f=1+c.
$$

For simple connected planar graph with $v\ge3$:

$$
e\le3v-6.
$$

If triangle-free planar:

$$
e\le2v-4.
$$

For bipartite simple planar graphs with at least 3 vertices, every face has length at least 4. Therefore:

$$
2e\ge4f.
$$

Combining this with Euler's formula gives:

$$
e\le2v-4.
$$

If every vertex has degree at least $d$, then:

$$
dv\le2e\le4v-8.
$$

So $d<4$. Therefore the tight maximum possible minimum degree is:

$$
d=3.
$$

Tight example: cube graph is simple, bipartite, planar, and 3-regular.

$K_5$ and $K_{3,3}$ are nonplanar.

Kuratowski theorem:

A graph is nonplanar iff it contains a subdivision of $K_5$ or $K_{3,3}$.

### Planar graph with minimum degree at most 5

Every simple planar graph has a vertex of degree at most 5.

Proof:

If every vertex had degree at least 6:

$$
2e=\sum_{v\in V}\deg(v)\ge6v.
$$

so $e\ge3v$. But planar simple graphs satisfy:

$$
e\le3v-6,
$$

contradiction.

### No planar graph with 7 edges and min degree at least 3

If every vertex degree at least 3:

$$
2e\ge3v.
$$

With `e=7`:

$$
14\ge3v.
$$

so $v\le4$.

But a simple graph on at most 4 vertices has at most:

$$
\binom{4}{2}=6.
$$

edges. Contradiction.

## 7.11 Faces All Have Same Length

If a connected simple planar graph has every face bounded by `k` edges, then:

$$
kf=2e.
$$

Euler:

$$
v-e+f=2.
$$

Substitute `f=2e/k`:

$$
v-e+\frac{2e}{k}=2,\qquad
v-\frac{e(k-2)}{k}=2,\qquad
e=\frac{k(v-2)}{k-2}.
$$

## 7.12 Polyhedra and Euler Formula

A convex polyhedron can be represented as a planar graph.

Regular polyhedron:

- all faces congruent regular polygons;
- same number of faces meet at each vertex.

If every face is a triangle:

Let `f` be number of faces and `e` edges.

Each triangular face contributes 3 edge-sides, each edge belongs to 2 faces:

$$
e=\frac{3f}{2}.
$$

Euler:

$$
v-e+f=2,\qquad
v-\frac{3f}{2}+f=2,\qquad
v=\frac{f}{2}+2.
$$

If every vertex has degree `k`, then:

$$
e=\frac{kv}{2}.
$$

So:

$$
\frac{3f}{2}=\frac{k(f/2+2)}{2},
\qquad
k=\frac{6f}{f+4}.
$$

Possible integer degrees for triangular polyhedra are `k=3,4,5`, giving:

$$
f=4,8,20.
$$

These are:

- tetrahedron;
- octahedron;
- icosahedron.

## 7.13 Dual Graphs and Dodecahedron Coloring

The dual graph of a planar graph has:

- one vertex for each face;
- edges between vertices whose faces share an edge.

A dodecahedron has 12 pentagonal faces. Coloring faces so adjacent faces differ is equivalent to vertex-coloring the dual graph.

The dual of the dodecahedron is the icosahedron. Around any pentagonal face, the 5 neighboring faces form an odd cycle. Together with the central face, this creates a wheel with odd rim, requiring at least 4 colors.

Therefore 3 colors are not enough; two adjacent pentagons must share a color.

## 7.14 Graph Isomorphism

An isomorphism between graphs `G` and `H` is a bijection:

$$
f:V(G)\to V(H)
$$

such that:

$$
uv\in E(G)\iff f(u)f(v)\in E(H).
$$

Isomorphic graphs have the same:

- number of vertices;
- number of edges;
- degree sequence;
- number of connected components;
- chromatic number;
- planarity;
- number of cycles of each length.

But having same number of vertices, edges, and chromatic number does not guarantee isomorphism.

## 7.15 Line Graphs

The line graph `L(G)` has:

- one vertex for each edge of `G`;
- two vertices adjacent if the corresponding edges in `G` share an endpoint.

To show $L(K_5)$ is nonplanar:

$K_5$ has 10 edges, so $L(K_5)$ has 10 vertices.

Each edge of $K_5$ touches:

- 3 other edges at one endpoint;
- 3 other edges at the other endpoint.

So $L(K_5)$ is 6-regular with:

$$
e=\frac{10\cdot6}{2}=30.
$$

A simple planar graph with 10 vertices has at most:

$$
3\cdot10-6=24.
$$

edges. Since 30 > 24, nonplanar.

Example of planar graph whose line graph is nonplanar:

$K_{1,5}$ is a planar star. Its line graph is $K_5$, which is nonplanar.

## 7.16 Ramsey R(3,3)

Statement:

Among any 6 people, there are either 3 mutual acquaintances or 3 mutual strangers.

Graph translation:

Color edge red if two people know each other, blue otherwise. Need show every red/blue coloring of $K_6$ contains a monochromatic triangle.

Proof:

Pick a vertex $v$. It has 5 incident edges. By pigeonhole, at least 3 of them have the same color, say red, to vertices $a,b,c$.

If any edge among $a,b,c$ is red, it forms a red triangle with $v$.

If none are red, then all three edges among $a,b,c$ are blue, forming a blue triangle.

So either way, there is a monochromatic triangle.

## 7.17 Graph Theory Results To Cite After Learning This Unit

Why this section is here: graph-theory proofs are usually short only because they rely on named results. This summary is placed after the graph unit so formulas such as Euler's formula and Hall's theorem are not cited before they have been introduced.

| Theorem or result | Statement to remember | Why cite it in solutions |
| --- | --- | --- |
| **Handshaking Lemma** | $\sum_{v\in V}\deg(v)=2\lvert E\rvert$. In particular, the number of odd-degree vertices is even. | Use for degree-sum parity, average degree, or impossibility arguments. |
| **Euler Circuit Criterion** | A connected undirected graph has an Euler circuit iff every vertex has even degree. | Use when a question asks whether all edges can be used exactly once in a closed route. |
| **Euler Path Criterion** | A connected undirected graph has an Euler path but not an Euler circuit iff exactly two vertices have odd degree. | Use when a route may start and end at different vertices. |
| **Hall's Marriage Theorem** | A bipartite graph has a matching covering $X$ iff every $S\subseteq X$ satisfies $\lvert N(S)\rvert\ge \lvert S\rvert$. | Use for perfect matching, assignment, toy/children, or pairing problems. |
| **Dirac's Theorem** | If $G$ is simple, $\lvert V\rvert=n\ge3$, and every vertex has degree at least $n/2$, then $G$ has a Hamilton cycle. | Use when a high minimum degree forces a Hamilton cycle. |
| **Ore's Theorem** | If $G$ is simple, $\lvert V\rvert=n\ge3$, and $\deg(u)+\deg(v)\ge n$ for every nonadjacent $u,v$, then $G$ has a Hamilton cycle. | Use when nonadjacent degree sums, not individual degrees, are given. |
| **Euler's Formula For Planar Graphs** | For connected planar $G$, $v-e+f=2$. | Use for planar graph edge/face counting. |
| **Simple Planar Edge Bound** | For simple connected planar $G$ with $v\ge3$, $e\le3v-6$. | Use for nonplanarity or minimum-degree contradictions in simple planar graphs. |
| **Bipartite Planar Edge Bound** | For simple connected bipartite planar $G$ with $v\ge3$, $e\le2v-4$. | Use when the graph is both bipartite and planar. |

---

# 8. Past COMP2121 Final Paper Coverage Map

Why this unit is included: after learning the topics, use the past-paper map to verify coverage and identify repeated exam patterns. This section is not a substitute for the definitions above.

This section tells you what the actual COMP2121 finals emphasized.

## May 2023

Logic/proof:

- induction sums;
- Cartesian product over union;
- tautology involving predicates;
- quantified negation;
- rules of inference.

Sets/functions/relations:

- set difference counterexample;
- relation properties for Big-O-like relation;
- complement of equivalence relation;
- asymptotic functions;
- recurrence/growth comparison.

Counting:

- number of equivalence relations on 5 elements;
- tiling with dominoes;
- power extender net capacity;
- Erdos-Szekeres increasing/decreasing subsequence;
- permutations constrained by longest increasing/decreasing subsequence.

Probability:

- stopping-time expectation by cases;
- Bayes with false alarms;
- upper bound on many false alarms;
- points in a half-disk.

Graph theory:

- Dirac theorem seating around a table;
- connected components via edge count;
- Hamilton cycle counting in a given graph;
- planar graph contradiction using degree/edge bounds;
- Ramsey `R(3,3)`.

## May 2024

Logic/proof:

- Agatha inference proof;
- negation normal form;
- quantified rules of inference;
- constructive proof of consecutive composites.

Sets/relations:

- set identities;
- divisibility pigeonhole in `{1,...,2n}`;
- equivalence relation on $x-y\sqrt{5}$;
- equivalence class computation.

Functions:

- $g\circ f=I_A$ implies $f$ injective and $g$ surjective;
- asymptotic sum with `k^2 2^k`.

Counting:

- coprime factor splitting;
- divisor-pair counting;
- circular seating over multiple days;
- integer solutions with bounds by stars-and-bars and inclusion-exclusion.

Probability:

- shuffled deck top/bottom kings;
- birthday problem over 7 weekdays;
- total variance formula.

Graph theory:

- triangular regular polyhedra;
- vertex connectivity upper bound;
- dodecahedron face coloring;
- graph isomorphism true/false;
- Hall theorem for regular bipartite graph.

## May 2025

Logic/proof:

- card-rule logic;
- negation normal form with nested quantifiers;
- rules of inference;
- recurrence solved by induction.

Sets/relations:

- set identity by algebra;
- union/intersection of transitive relations;
- equivalence relation on pairs by ratio.

Functions:

- ceiling/floor identity;
- compare `3n!` and `(3n)!`.

Counting:

- existence of base-3 multiple with only 0s and 1s by pigeonhole;
- combinatorial identity;
- descent sets;
- circular arrangements with indistinguishable chairs;
- graph coloring count.

Probability:

- dice sum;
- midpoint parity in lattice box;
- conditional expectation after knowing at least 3 wins in first 4 games.

Graph theory:

- dense graph contains induced $K_4$;
- line graph nonplanarity;
- regular bipartite graph perfect matchings and repeated matchings;
- tight bound for minimum degree in simple bipartite planar graphs.

## Dec 2025

Logic/proof:

- propositional implication/equivalence;
- implication-only rewriting;
- translating natural language with quantifiers;
- prenex negation;
- relationship between quantified formulas;
- knight-move invariants.

Relations/Boolean functions:

- equivalence/disagreement relations on Boolean functions;
- reflexive/symmetric/transitive analysis;
- deterministic and randomized encoding lower bounds.

Counting/probability/random variables:

- product rule for weapon showcases;
- inclusion-exclusion for sequences using all categories;
- pigeonhole for repeated weapon type;
- multisets with bounded repetitions;
- Bayes spam filter;
- stopping process expectation.

Graph theory:

- bipartite multigraph closure under operations;
- Euler tours under graph operations;
- planarity under contractions/path independence;
- Euler formula statement;
- counting pentagonal faces of a 3D object.

---

# 9. Last-Day Checklist

Why this unit is included: this is a readiness test. If an item feels vague, return to the corresponding guide section before attempting more past-paper questions.

You should be able to do all of the following without notes:

- Push negations through nested quantifiers.
- Convert implications to `not p or q`.
- Use modus ponens, modus tollens, and quantifier instantiation correctly.
- Write induction proofs cleanly.
- Prove set equality by element chasing and by identities.
- Determine whether a relation is reflexive, symmetric, antisymmetric, transitive.
- Prove equivalence relation and compute equivalence classes.
- Prove injective/surjective statements from definitions.
- Compare functions using Big-O, Big-Omega, Big-Theta.
- Use product/sum/subtraction/division rules.
- Count permutations, combinations, circular arrangements, and multisets.
- Use stars-and-bars with upper bounds.
- Use inclusion-exclusion for forbidden conditions.
- Use pigeonhole for divisibility and monotone subsequences.
- Count surjections using inclusion-exclusion and Stirling numbers.
- Build sample spaces for probability problems.
- Apply Bayes and total probability.
- Use expectation, variance, indicators, and conditional expectation.
- Count dice sums with generating functions or bounded stars-and-bars.
- Apply handshaking lemma.
- Test bipartiteness via odd cycles.
- Use Euler path/circuit degree criteria.
- Apply Dirac/Ore for Hamilton cycles.
- Use Hall's theorem for bipartite matchings.
- Apply Euler's planar formula and edge bounds.
- Count colorings by choosing colors in a good vertex order.
- Recognize graph isomorphism invariants.

If you can solve the COMP2121 final papers while explaining each step using the definitions above, you are studying the right material.
