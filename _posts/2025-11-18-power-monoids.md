---
layout: post
title: "Recent Trends XI: The isomorphism problem for power semigroups"
abstract: "The systematic study of power semigroups began in the 1960s and was initiated by Tamura and Shafer. A central question that arose from their work was the so called isomorphism problem for power semigroups"
tag: 'Trend'
---

Let $(S,\cdot)$ be a semigroup. We denote by ${\mathcal P}(S)$ the *large power semigroup* of $S$, that is, the family of all non-empty subsets of $S$, endowed with the binary operation of setwise multiplication 

$$
  (X,Y)\mapsto \lbrace xy:x\in X,y\in Y\}.
$$

To consider an often studied example, let $S=(\mathbb{N}_0,+)$ be the additive monoid of non-negative integers. Although we easily see that ${\mathcal P}(S)$ retains the property of being a commutative monoid, with identity element being the singleton $\lbrace  0\rbrace$, it fails to be cancellative. This means that for $X,Y,Z\in{\mathcal P}(S)$, the equation 

$$
X+Y=X+Z
$$

does not necessarily imply that $Y=Z$. At first blush, this loss of cancellativity seems to make it quite difficult to study various properties of power semigroups. However, as it turns out, more often than not, these objects behave surprisingly well. 

The systematic study of power semigroups began in the 1960s and was initiated by Tamura and Shafer. A central question that arose from their work, called the *isomorphism problem for power semigroups*, is whether, for semigroups $S$ and $T$ in a certain class ${\mathcal O}$, an isomorphism between ${\mathcal P}(S)$ and ${\mathcal P}(T)$ implies that $S$ and $T$ are isomorphic. Although this was answered in the negative by Mogiljanskaja [[5]](#Mo73) for the class of all semigroups, several other classes have been found for which the answer is positive, such as the class of groups [[7]](#Sh67) and Clifford semigroups [[4]](#Ga-Zh14).


In recent years, the topic gained new attention, initially motivated by problems in factorization theory and additive combinatorics. In order to answer questions about how subsets of $\mathbb{N}\_0$, 
or other monoids, can be written as a sum of smaller, irreducible sets, one can study arithmetic properties of power semigroups. 
This new line of research was mainly pushed forward by Tringali [[1](#An-Tr21), [2](#Co-Tr25) [3](#Fa-Tr18)], who introduced several new types of power semigroups and power monoids. To name one, let $H$ be a monoid with identity $1$. The *reduced finitary* power monoid ${\mathcal P}\_{\operatorname{fin},1}(H)$ of $H$ consists of all finite subsets of $H$, containing $1$.


Returning back to the isomorphism problem, a recent result of Tringali gives a positive answer to this problem for the class of commutative and cancellative semigroups [[8]](#Tr25). In other words, if $S$ and $T$ are commutative, cancellative semigroups, then ${\mathcal P}(S)\simeq {\mathcal P}(T)$ if and only if $S\simeq T$. The proof of this result highlights that power semigroups can certainly be approached with simple, but clever methods. The core idea is to show that the cancellative elements of ${\mathcal P}(S)$ are precisely the singletons, which form a subsemigroup of ${\mathcal P}(S)$, isomorphic to $S$.
Since every isomorphism between semigroups bijectively maps cancellative elements to cancellative elements, we can conclude that every isomorphism between ${\mathcal P}(S)$ and ${\mathcal P}(T)$ induces an isomorphism between $S$ and $T$. Interestingly, the proof cannot be replicated in the non-commutative setting which leaves us with the following question.

**Open Question:** Does the isomorphism problem have a positive answer for the class of cancellative semigroups? 

Naturally, we can also consider the isomorphism problem for reduced finitary power monoids. A first step in this direction was made by Tringali and Yan [[9]](#Tr-Ya25), who gave a positive answer for the class of rational Puiseux monoids, that is, submonoids of the additive group of rational numbers, using the following crucial observation. Let $H$ and $K$ be arbitrary monoids and let $f$ be an isomorphism between ${\mathcal P}\_{\operatorname{fin},1}(H)$ and ${\mathcal P}\_{\operatorname{fin},1}(K)$. Then $f$ bijectively maps 2-element sets to 2-element sets. This allows us to define an auxiliary bijection $g:H\to K$, defined in the following way. We set $g(1)=1$ and if $x\in H\setminus\lbrace 1\rbrace $, then 

$$
f(\lbrace 1,x\rbrace )=\lbrace 1,g(x)\}.
$$ 

The existence of this map, called the *pullback* of $f$, is quite similar to the correspondence that we have seen in the previous proof. 
However, although it behaves quite well in many cases, $g$ is not always an isomorphism. To provide a trivial counterexample, let $H$ be the group of order two and let $K$ be the monoid with two elements, with both elements being idempotent. It is straightforward to verify that ${\mathcal P}\_{\operatorname{fin},1}(H)\simeq {\mathcal P}\_{\operatorname{fin},1}(K)$, whereas $H$ and $K$ are not isomorphic. Another surprising counterexample was given in [[6]](#Ra25), showing the existence of two non-isomorphic submonoids of $(\mathbb{Z}^2,+)$ with isomorphic reduced finitary power monoids, disproving the isomorphism problem in a very well-behaved class of monoids.


### References

<ol style="padding-left: 0;">
    <li id="An-Tr21">A. Antoniou and S. Tringali, On the arithmetic of power monoids and sumsets in cyclic groups, Pacific J. Math. 312 (2021), 279-308.</li>
    <li id="Co-Tr25">L. Cossu and S. Tringali, On factorization in power monoids, https://arxiv.org/abs/2503.08615.</li>
    <li id="Fa-Tr18">Y. Fan and S. Tringali, Power monoids: A bridge between Factorization Theory and Arithmetic Combinatorics, J. Algebra 512 (2018), 252-294.</li>
    <li id="Ga-Zh14">A. Gan and X. Zhao, Global determinism of Clifford semigroups, J. Aust. Math. Soc. 97 (2014), 63-77.</li>
    <li id="Mo73">E.M. Mogiljanskaja, Non-isomorphic semigroups with isomorphic semigroups of subsets, Semigroup Forum 6 (1973), 330-333.</li>
    <li id="Ra25">B. Rago, A counterexample to an isomorphism problem for power monoids, Proc. Amer. Math. Soc., to appear.</li>
    <li id="Sh67">J. Shafer,  Note on semigroups, Math. Japon. 12 (1967), 32.</li>
    <li id="Tr25">S. Tringali, "On the isomorphism problem for power semigroups", in: M. Brešar, A. Geroldinger, B. Olberding, and D. Smertnig (eds.), Recent Progress in Ring and Factorization Theory, Springer Proc. Math. Stat. 477, Springer, 2025.</li>
    <li id="Tr-Ya25">S. Tringali and W. Yan, A conjecture by Bienvenu and Geroldinger on power monoids, Proc. Amer. Math. Soc. 153 (2025), 913-919.</li>
</ol>     
    
---
Balint Rago is a PhD student at the University of Graz, Austria, and belongs to the Algebra and Number Theory research group ([AlgNTh](https://imsc.uni-graz.at/AlgNTh/)).