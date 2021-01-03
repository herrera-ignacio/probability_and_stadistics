# Axiomatic Probability Theory

* Introduction
* Kolmogorov's three axioms
* Axioms consequences

## Introduction

Probability theory treats the concept in a rigorous mathematical manner by expressing it through a set of _axioms_.

Typically these aximos formalise probability in terms of a _probability space_, which assigns a measure taking values between 0 and 1, termed the _probability measure_, to a set of outcomes called the _sample space_. Any specified subset of these outcomes is called an _event_.

Central subjects in probability theory include:

* Discrete and continuous random variables
* Probability distributions
* Stochastic processes (family of random variables)

They provide mathematical abstraction of non-deterministic or uncertain processes or measured quantities that may either be single occurrences or evolve over time in a random fashion.

> Determinism is the philosophical view that all events are determined completely by previously existing causes.

Altough it is not possible to perfectly predict random events, much can be said about their behavior. Two major results in probability theory describing such behaviour are the _law of large numbers_ and _central limit theorem_.

## Kolmogorov Axioms

Kolmogorov axioms are the foundations of probability theory introduced by Kolmogorov in 1933.

The assumptions as to setting up the axioms can be summarised as follows:

Let $(\Omega, F, P)$ be a _measure space_ with $P(E)$ being the probability of some event $E$ and $P(\Omega) = 1$. Then $(\Omega, F, P)$ is a _probability space_, with sample space $\Omega$, event space $F$ and probability measure $P$.

### 1st Axiom: non-negative probability

Probability of an event is a non-negative real number:

$P(E) \in \mathbb{R}, P(E) \ge 0$   $\forall E \in F$

### 2nd Axiom: unit measure

Unit measure, probability that at least one of the elementary events in the entire sample space will occur is 1.

$P(\Omega) = 1$

### 3rd $\sigma-additivity$

Any countable sequence of disjoint sets (mutually exclusive events) $E_1, E_2, ...$ satisfies:

$P( \bigcup_{i=1}^{\infty} E_i) = \sum_{i=1}^{\infty} P(E_i)$

#### Consequence

$P( \bigcup_{i=1}^{\infty} E_i) \le \sum_{i=1}^{\infty} P(E_i)$

## Axioms consequences

### Monotonicity

if $A \subseteq  B$ then $P(A) \le P(B)$

### Probability of the empty set

$P(\emptyset) = 0$

### Complement rule

$P(A^{c}) = P(\Omega \smallsetminus A) = 1 - P(A)$

#### Consequence

* $P(B \cap A^c) = P(B-A)$

### Numeric bound

It immediately follows from the monotonicity property that:

$0 \le P(E) \le 1$ , $\forall E \in F$

### Addition law of probability / sum rule

$P(A \cup B) = P(A) + P(B) - P(A \cap B)$

