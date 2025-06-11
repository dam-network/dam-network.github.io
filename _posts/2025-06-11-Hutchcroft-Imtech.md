---
layout: post
title: "Recent trends VIII. Tom Hutchcroft: an EMS prize for important progress on percolation theory"
abstract: 'As it is stated in Hutchcroft’s laudatio, this EMS Prize has been awarded *"for his revolutionary contributions to probability theory and geometric group theory, in particular to percolation theory on general graphs, using tools from geometry, operator theory, group theory and functional analysis."*.'
tag: 'Trend'
---

As it is stated in Hutchcroft’s laudatio, this EMS Prize has been
awarded *"for his revolutionary contributions to probability theory and
geometric group theory, in particular to percolation theory on general
graphs, using tools from geometry, operator theory, group theory and
functional analysis."*. In this short text we will describe possibly one
of his most important achievements: his resolution (joint with his PhD
student Philip Easo) of the so-called *Schramm locality conjecture* (see [[2]](#2)). This will show the taste and the kind of results in which Hutchcroft
had made decisive contributions.

Percolation theory is a fascinating and deep topic in the interplay of
probability theory and mathematical physics, with very important results
in the last recent years due to different authors (just to cite three of
them, the Field medallist Wendelin Werner, Stanislav Smirnov and Hugo
Dominil-Copin had made decisive contributions to this area). There are
different models (most of them inspired by physics) to study this
notion. Just to get an idea we will consider the following model:
consider an infinite connected graph $G$ where all vertices have
finite degree (namely, *locally finite*). We also assume that our graph
is transitive, which means that for any pair of vertices $v_1$ and
$v_2$ there is an automorphism of the graph that maps $v_1$ to
$v_2$ (for instance, the rectangular grid defines a transitive graph
where all vertices have degree 4). A good example of such graphs are
Cayley graphs, which are defined from groups and have nice symmetry
properties. Now delete or retain each edge independently with a certain
probability $p$ or $1-p$. Which is now the geometry of the subgraph
that we obtain, or more precisely, which is the structure of its
connected components? Are they all finite, or some of them is infinite?

Much of the interest in these type of models arises from the fact that
there exists a *phase transition*. In our case study, there is a
critical probability $p_c(G)$ from which the general picture of the
graph obtained dramatically depends on whether $p$ is smaller or bigger
than $p_c$. In particular, the value of $p_c$ rules the existence or
not of an infinite connected component (almost surely). For instance,
again in the rectangular grid we can see a dramatic change of behaviour
when passing the value $p_c=1/2$. In fact, a celebrated result by
Kesten [[3]](#3) states that $p_c=1/2$ is indeed the probability in which there is a sudden change, and that at $p_c=1/2$ there is not an infinite
cluster.

<figure>
<div align="center">
<img src="/public/img/46.png" style="height:4cm" alt="image" />       <img
src="/public/img/51.png" style="height:4cm" alt="image" />
</div>
<figcaption>Figure 1. Two samples of the percolation model on the rectangular grid
for <span class="math inline"><em>p</em> = 0.46</span> and <span
class="math inline"><em>p</em> = 0.51</span>. On the sample on the
right, there is an infinite cluster.</figcaption>
</figure>

The interesting features of percolation on an infinite transitive graph,
especially around the critical point, are expected to be *universal*.
This means they depend only on the graph’s overall shape, not its local
details, for instance finite considerations. In the opposite direction,
Oded Schramm (who introduced novel ideas coming from conformal field
theory into probability theory in a way that was advanced for his time)
conjectured in 2008 (see [[1]](#1)) that the value of the critical probability
$p_c(G)$ should be entirely determined by the local (microscopic)
geometry of the graph, subject to the global constraint that
$p_c(G) < 1$. Some cases have been known to be true but only last
year, in a 87-page paper Huchcroft and Easo fully solved this
conjecture.

The solution gives a better insight into what happens above the
percolation threshold. Huchcroft techniques open the door to study what
happens exactly at the threshold for most graphs: is there an infinite
cluster at $p_c(G)$. Even in the three-dimensional rectangular grid
this is still an open question.

## References

<ol style="padding-left: 0;">

<li id="1">I. Benjamini, A. Nachmias and Y. Peres. Is critical percolation
local?, Probability Theory and Related Fields, vol. 149, p. 261-269,
2011.</li>

<li id="2">T. Huchcroft, P. Easo. The critical percolation probability is local. Preprint, available on-line at arXiv:2310.10983v1.</li>

<li id="3">H. Kesten. The critical probability of bond percolation on the square lattice equals 1/2. Communications in Mathematical Physics,
74(1):41–59, 1980.</li>
</ol>

---

The author of this post, [Juan José Rué Perna](https://web.mat.upc.edu/juan.jose.rue/), is the Director of [CFIS](https://cfis.upc.edu/ca) and an Associate Professor at the Department of Mathematics of the Polytechnic University of Catalonia (UPC).