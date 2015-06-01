---
layout: post
title: "Basic Algebra I (1)"
description: Note for Basic Algebra I
headline: Concepts from Set Theory. The Integers
modified: 2015-05-31 09:18:07 +0800
category: Algebra
tags: [set, map, relation, naturual number, integer, cardinality]
mathjax: true
comments: true
featured: false
---

# Glossary

* elimination: 消除
* ramification: 后果，结果
* ingredient: 要素，组成部分
* perspectivity: 透视
* resultant: 因而产生的
* criterrion: 标准
* stipulate: 规定
* equidistant: 等距的
* compatible: 相容的
* correspondence: 对应
* encompass: 包含
* non-vacuous: 非空的
* a priori: 先验的
* analogous: 类似的
* algorithm: 算法，运算法则
* equipotent: 等势的


# Abstract

This chapter has two important parts: set theory, natural numbers and intergers, which are the basic ingredients of structures.


# Main Content

## Set Theory, Maps and Equivalent relations

In the first part, we introduced the power set of a set, the Cartesian product set, maps and equivalence relations on a set.

**The "dressing-undressing" principle**:

>\\[(\beta\alpha)^{-1} = \alpha^{-1}\beta^{-1}\\]

We view the *relation* on $S$ as a subset of the product set $S \times S$. The *equivalence relation* is a relation with reflexive, symmetic and transitive properties. The concept of an equivalence relation is equivalent to that of a *partition*, $\pi(S)$, of a set, which is the just the *quotient set*, $S/E$. The we have a *natural map* of the set to the quotient set:
\begin{align}
\nu : \, & S \to S/E \\\
& a \mapsto \bar{a}
\end{align}

The another important connection between maps and equivalent relations is that we can *induce* a map $\bar{\alpha}$ of $S/E\_{\alpha}$ for a map $\alpha$ of $S$, where
\begin{gather}
a E\_{\alpha} b \iff \alpha(a) = \alpha(b) \\\
\bar{\alpha}(a) = \alpha(a)
\end{gather}
The map $\bar{\alpha}$ is injective and $\nu$ is surjective. Then we have the commutativity of the diagram
<p>
\[
\begin{xy}
\xymatrix {
S \ar[r]^{\alpha} \ar[d]_{\nu} & T \\
S/E_{\alpha} \ar[ur]_{\bar{\alpha}} &
}
\end{xy}
\]
</p>

We say that $\alpha\$ is *compatible* with $E$ if $a E b$ for $a$, $b$ is $S$ implies $\alpha(a) = \alpha(b)$. Then we can define
\begin{align}
\bar{\alpha} : \, & \bar{S} = S/E \to T \\\
& \bar{a} \equiv \bar{a}\_E \mapsto \alpha(a)
\end{align}
In this case, the induced map $\alpha$ need not to be injective. In fact $\alpha$ is injective iff $E = E\_{\alpha}$.

### Cardinality

**The "Pigeonhole" Principle**

>If there are more letters than pigonholes, then some pigeonhole must contains more than one letter.

**The Schröder-Bernstein Theorem**

>If we have injective maps of $S$ into $T$ and of $T$ to $S$, then $\lvert S \rvert = \lvert T \rvert$.

## The Natural Number

We begin with a non-vacuous set $\mathbb{n}$, a particular element of $\mathbb{N}$, designated as $0$, a *successor map* $a \to a^{+}$ of $\mathbb{N}$, and **Peano's Axioms**:

>1. $0 \ne a^{+}$ for any $a$ (i.e. $0$ is not the image of any successor map).
>2. The successor map is injective.
>3. (*Axiom of induction*) Any subset of $\mathbb{N}$ which contains $0$ and contains the successor of every element in the given subset coincides with $\mathbb{N}$.

Axiom 3 is the basis of the *first principle of induction*. Then we have *proofs by induction*.

The another we shall encounter frequently is *definitions by induction*, which is not as tivial as it may appear at first glance. It is based on the following

**Recursion Theorem**:

>Let $S$ be a set, $\phi$ a map of $S$ into itself, $a$ a element of $S$. Then there exist one and only one map $f$ from $\mathbb{N}$ to $S$ s.t.
>
>1. $f(0) = a$
>2. $f(n^{+}) = \phi(f(n))$, $n \in \mathbb{N}$

Note that the existence of $f$ must use *all* of the Peano's axioms.

A fundamental concept of the system $\mathbb{N}$ is the relation of *order*. We have the *well-ordering property* of $\mathbb{N}$:

>In any non-vacuous subset $S$ of $\mathbb{N}$ there is a least number,
>i.e. an $l \in S$ s.t. $l \le s$ for $s \in S$

The well-ordering property is the basis of the *second principle of induction*.

## Integers

We can construct the number system $\mathbb{Z}$ from $\mathbb{N}$ using the method analogous to the standard one for constructing $\mathbb{Q}$ from $\mathbb{N}$.

**The Fundamental Theorem of Arithmetic[^1]**

>Any integer $\ne 0, \pm 1$ can be written as a product of primes. Apart from order and signs of the factors this factorization is unique.

**The Division Algorithm in $\mathbb{Z}$**

>If $a$ and $b$ are integers and $b \ne 0$ then there exist integers $q$ and $r$ s.t. $a = bq + r$.



[^1]: This is a special case of the *arithemetic of principal ideal domains*.
