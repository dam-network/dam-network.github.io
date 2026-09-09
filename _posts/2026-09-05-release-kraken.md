---
layout: post
title: "Recent Trends XV: Release the Kraken and Other Graph-Embedding Adventures"
abstract: "A classic example used to introduce graph theory starts as follows. Imagine a room full of guests. Some of them know each other (we can draw a line, or an *edge*, between them), and some do not."
tag: 'Trend'
---

## Introduction: Friendship Networks, Seating Plans, and the Art of Finding Order in Chaos

A classic example used to introduce graph theory starts as follows. Imagine a room full of guests. Some of them know each other (we can draw a line, or an *edge*, between them), and some do not. In mathematics, this entire network of guests and connections is called a *graph*, where the people are *vertices* (or nodes). If we count the average number of friends each guest has in the room, we get the *average degree* of the network.

Now, a natural question arises: if we know that, on average, every person in the room knows at least, say, ten other people, what kinds of social structures are guaranteed to exist? Can we find a group of five people who are all mutual friends (a *clique*, that is, a complete graph)? Can we arrange a subset of guests around a circular table so that everyone sits next to two people they know (a *cycle*)?

In the branch of mathematics known as extremal graph theory, we look for these guaranteed structures. A classical result from 1967 by Mader shows that if the average number of connections per person is large enough, we can always find a network structure that looks like a “subdivided” complete network—where we have a set of key people, and every pair is connected either directly or through simple chains of mutual acquaintances.

However, if we want to place additional structural, parity, or geometric constraints on these paths and cycles, the problem becomes considerably harder. How do we find these structures when the network is sparse—meaning the overall density of edges is low?

The key tool in our work is a class of graphs called *sublinear expanders*. While classical expanders are graphs where any set of vertices connects to a much larger set of neighbours in a strict linear proportion, a sublinear expander allows this expansion rate to slow down slightly as the set grows.

Remarkably, a fundamental theorem shows that every graph contains a sublinear-expander subgraph with almost the same average degree (see <span class="cite">\[[4](#Xkomlos1994)\]</span>). This means that even in a highly chaotic and sparse global graph, we can always zoom in on a local dense neighbourhood that is extremely well-connected. In our work, we utilise *robust sublinear expanders*, which are expanders that maintain their excellent connectivity even if an adversary deletes a small portion of edges or vertices. We now try to illustrate how these expanders become useful in
two distinct problems.

## A First Problem: Erdős’s Conjecture on Nested Cycles with No Geometric Crossings

In 1975, Paul Erdős <span class="cite">\[[1](#Xerdos1975)\]</span> asked an elegant question about cycles: what is the minimum density that forces two *edge-disjoint nested cycles* $C_1$ and $C_2$ such that the vertex set of $C_2$ is a subset of the vertex set of $C_1$, and their cyclic orderings respect each other without crossing geometrically?

To visualise this, imagine placing the guests of $C_1$ around a large round table. We want to find a second, smaller dinner table $C_2$ using a subset of these same guests, such that when they converse (forming the edges of $C_2$), their lines of sight do not cross each other across the room.

<center>
<figure id="x1-20011" class="figure">
<span id="two-nested-cycles-without-geometric-crossings"></span>
<p><img src="/public/img/article_Recent_Trends_DAM_Thesis0x.svg"
alt="[Picture]" /></p>
<figcaption><span class="id">Figure 1: </span><span class="content">Two
nested cycles without geometric crossings.</span></figcaption>
</figure>
</center>

In our work <span class="cite">\[[2](#Xgil2022nested)\]</span>, we resolved this conjecture by establishing the optimal linear bound: an average degree of at least some constant $C$ is sufficient to force such nested cycles without crossings.

The core structure we build to achieve this is the *Kraken*. A kraken is a graph consisting of a central cycle $C$ where each vertex $v_i$  is attached to two disjoint, highly connected sets $A_{i,i}$ and $A_{i,2}$ 
(the “legs” of the kraken) via disjoint paths $R_{i,1}$ and $R_{i,2}$.

<center>
<figure id="x1-20022" class="figure">
<span
id="a-6mskraken-with-an-inner-cycle-c-of-length-6-each-vertex-vi-inc-has-two-legs-attached-to-it"></span>
<p><img src="/public/img/article_Recent_Trends_DAM_Thesis1x.svg"
alt="[Picture]" /></p>
<figcaption><span class="id">Figure 2: </span><span class="content">A
((6<span class="cmmi-10x-x-109">,m,s</span>))-kraken with an inner cycle
<span class="cmmi-10x-x-109">C </span>of length 6. Each vertex <span
class="cmmi-10x-x-109">v</span><sub><span class="cmmi-8">i</span></sub>
in <span class="cmmi-10x-x-109">C </span>has two legs attached to
it.</span></figcaption>
</figure>
</center>

Our embedding strategy works in the following order:

1.   First, we find a kraken in our expander. The central cycle of the kraken will serve as the inner cycle.

2. Then, we expand the legs of the kraken and link them together sequentially using the short diameter property of expanders (which says that we can always find a short path between two sets while avoiding a small set). By linking $A_{i,2}$ to $A_{i+1,1}$ for each $i$, we get a larger cycle that encloses the inner cycle without any geometric crossings.

## A Second Problem: How to Build a Pillar (and Solve a 30-Year-Old Conjecture)

In 1989, Carsten Thomassen proposed a conjecture: every graph with sufficiently large minimum degree contains a *pillar* as a subgraph. A pillar
consists of two vertex-disjoint cycles $C_1$, $C_2$ of the same length $s$, and $s$ disjoint paths of *exactly the same length* connecting matching vertices in order.

<center>
<figure id="x1-30013" class="figure">
<span id="a-pillar"></span>
<p><img src="/public/img/article_Recent_Trends_DAM_Thesis2x.svg"
alt="[Picture]" /></p>
<figcaption><span class="id">Figure 3: </span><span class="content">A
pillar.</span></figcaption>
</figure>
</center>

Pillars have resisted all embedding attempts for over three decades because they place degree-3 vertices (vertices connected to exactly three other vertices) adjacent to one another on the cycles. In extremal graph theory, degree-3 vertices are notorious game changers—in fact, a famous result of Pyber, Rödl, and Szemerédi shows that constant average degree is not even enough to force a 3-regular subgraph.

To solve Thomassen’s conjecture, we used a powerful tuning device: the
**adjuster** (introduced by Liu and Montgomery in <span class="cite">\[[8](#Xliu2020odd)\]</span>). An adjuster is a chain of even cycles where paths connect almost-antipodal vertices of the cycles.

<center>
<figure id="x1-30024" class="figure">
<span
id="an-adjuster-a-chain-of-cycles-allowing-finetuning-of-path-lengths-between-v1-and-v2-by-choosing-to-traverse-the-top-or-bottom-half-of-each-cycle-the-length-of-the-path-can-be-adjusted-by-even-increments"></span>
<p><img src="/public/img/article_Recent_Trends_DAM_Thesis3x.svg"
alt="[Picture]" /></p>
<figcaption><span class="id">Figure 4: </span><span class="content">An
Adjuster: a chain of cycles allowing fine-tuning of path lengths between
<span class="cmmi-10x-x-109">v</span><sub><span
class="cmr-8">1</span></sub> and <span
class="cmmi-10x-x-109">v</span><sub><span class="cmr-8">2</span></sub>.
By choosing to traverse the top or bottom half of each cycle, the length
of the path can be adjusted by even increments.</span></figcaption>
</figure>
</center>

The adjuster works as follows:

- Each even cycle has length $2\ell$ and two almost-antipodal vertices.

- Going through the cycle in one direction yields a path of length $\ell+1$.

- Going through it in the other direction yields a path of length $\ell-1$.

- By chaining $k$ such cycles, we can choose any path length of the same parity in a wide range of size $2k$, simply by deciding which direction to go around each cycle.

By finding two distinct krakens in a robust expander and linking them through sequential adjusters, we managed to find the paths of *exactly the same length*, proving Thomassen’s conjecture
<span class="cite">\[[3](#Xgil2023pillar)\]</span>.

### <span id="x1-4000"></span>References

1. <span id="Xerdos1975"></span>P. Erdős, *Problems and results in Graph Theory and Combinatorial Analysis*, Proceedings of the Fifth British Combinatorial Conference (1975), 169–192.

2. <span id="Xgil2022nested"></span>I. Gil Fernández, J. Kim, Y. Kim, and H. Liu, *Nested cycles with no geometric crossings*, Proceedings of the American Mathematical Society, Series B <span class="cmbx-10x-x-109">9 </span>(2022), 22–32.

3. <span id="Xgil2023pillar"></span>I. Gil Fernández and H. Liu, *How to build a pillar: A proof of Thomassen’s conjecture*, Journal of Combinatorial Theory, Series B <span class="cmbx-10x-x-109">162 </span>(2023), 13–33.

4. <span id="Xkomlos1994"></span>J. Komlós and E. Szemerédi, *Topological cliques in graphs*, Combinatorics, Probability and Computing <span class="cmbx-10x-x-109">3</span>(2) (1994), 247–256.

5. <span id="Xkomlos1996"></span>J. Komlós and E. Szemerédi,
*Topological cliques in graphs II*,
Combinatorics, Probability and Computing
<span class="cmbx-10x-x-109">5</span>(1) (1996), 79–90.

6. <span id="Xkrivelevich2019"></span>M. Krivelevich, *Expanders - how to find them, and what to find in them*, in A. Lo, R. Mycroft, G. Perarnau, & A. Treglown (Eds.), Surveys in Combinatorics 2019 (London Mathematical Society Lecture Note Series, pp. 115–142). Cambridge University Press.

7. <span id="Xletzter2024"></span>S. Letzter, *Sublinear expanders and their applications*, in F. Fischer & R. Johnson (Eds.), Surveys in Combinatorics 2024 (London Mathematical Society Lecture Note Series, pp. 89–130). Cambridge University Press.

8. <span id="Xliu2020odd"></span>H. Liu and R. H. Montgomery, *A solution to Erdős and Hajnal’s odd cycle problem*, Journal of the American Mathematical Society, <span class="cmbx-10x-x-109">36 </span>(2023), 1191–1234.

9. <span id="Xthomassen1989"></span>C. Thomassen, *Configurations in graphs of large minimum degree, connectivity, or chromatic number*, Annals of the New York Academy of Sciences <span class="cmbx-10x-x-109">555</span>(1) (1989), 402–412.


---

Irene Gil Fernandez is an assitant lecturer at the [University CEU San Pablo](https://www.uspceu.com) and was awarded the [Ramon Llull Prize](https://dam-network.github.io/ramon-llull/) in 2026.