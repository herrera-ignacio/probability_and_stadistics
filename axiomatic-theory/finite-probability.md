# Probability on Finite Sample Spaces

* Uniform probability distribution
* Independent Events
* Conditional Probability
* Law of Total Probability
* Bayes' Theorem

## Uniform probability distribution

Suppose that the sample space $\Omega = \{\omega_1, ..., \omega_n \}$ is finite. For example, if we toss a die twice, then $\Omega$ has 36 elements: $\Omega = \{(i,j): i,j \in \{1, ..., 6\}\}$. If each outcome is equally likely, then $P(A) = |A|/36$ where $|A|$ denotes the number of elements in $A$. The probability that the sum of the dice is $11$ is $2/36$ since there are two outcomes that correspond to this event.

If $\Omega$ is finite and if each outcome is equally likely, then

$P(A) = \frac{|A|}{|\Omega|}$

which is called the __uniform probability distribution__. To compute probabilities, we need to count the number of points in an event $A$. Methods for counting points are called combinatorial methods (_Counting Theory_).

## Independent Events

Two events $A$ and $B$ are __independent__ if and only if

$P(AB) = P(A) * P(B)$

and we write $A \bot B$.

A set of events $\{ A_i : i \in I\}$ is idependent if

$P(\bigcap_{i \in J}^{} A_i) = \prod_{i \in J}^{} P(A_i)$

for every finite subset $J$ of $I$.

### Consequences

Independence can arise in two distinct ways. Sometimes, we explicitly __asume__ that thwo events are independent. For example, in tossing a coin twice, we usually assume that tosses are independent which reflects the fact that the coin has no memory of the first toss. In other instances, we __derive__ independence by verifying that $P(AB) = P(A)P(B)$ holds, for example, in tossing a fair die, let $A = \{2,4,6\}$ and let $B=\{1,2,3,4\}$. Then $A \cap B = {2,4}$, $P(AB) = 2/6 = P(A)P(B) = (1/2) * (2/3)$ and so $A$ and $B$ are independent.

Also, we know that disjoint events with positive probability are not independent. This follows since $P(A)P(B) \gt 0$ yet $P(AB) = P(\emptyset) = 0$.

## Conditional Probability

Assuming that $P(B) > 0$, we define the conditional probabiltiy of $A$ given that $B$ has occurred as follows:

$P(A|B) = \frac{P(AB)}{P(B)}$

Think of $P(A|B)$ as the fraction of times $A$ occurs among those in which $B$ occurs. Foy any fixed B such that $P(B) > 0$, $P(\cdot | B)$ is a probability (i.e., it satisfies the three axioms of probability). In particular, $P(A|B) \ge 0$, $P(\Omega | B) = 1$ and if $A_1, ..., A_n$ are disjoint then $P (\bigcup_{i = 1}^{\infty} A_i | B) = \sum_{i=1}^{\infty} P(A_i | B)$. But it is in general __not__ true that $P(A | B \bigcup C) = P(A|B) + P(A|C)$, neither that $P(A|B) = P(B|A)$, the rules of probability apply to events on the left of the bar.

Also, for any pair of events $A$ and $B$:

$P(AB) = P(A|B)P(B) = P(B|A)P(A)$

### Conditional Probability of Independent Events

$A$ and $B$ are independent events if and only if $P(A|B) = P(A)$. 

## Law of Total Probability

Let $A_1, ..., A_k$ be a _partition_ of $\Omega$. Then, foy any event $B$,

$P(B) = \sum_{i=1}^{k} P(B|A_i) P(A_i)$

## Bayes Theorem

Let $A_1, ..., A_k$ be a _partition_ of $\Omega$ such that $P(A_i) > 0$ for each _i_. If $P(B) \ge 0$ then, for each $i = 1, ..., k$,

$P(A_i | B) = \frac{P(B | A_i)P(A_i)}{\sum_{j}^{} P(B | A_j)P(A_j)}$
