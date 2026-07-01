---
layout: post
title: "Recent Trends XIII: Colourful questions and seating plans"
abstract: "What a wonderful thing it is to be able to learn from other people. It is especially enriching when we step outside our usual circles, because then we get to hear about things that are very different from our day-to-day lives. These interactions are often transformative, not only in how we understand the world beyond our bubble, but also in how they can change the way we do the things we are used to doing."
tag: 'Trend'
---


What a wonderful thing it is to be able to learn from other people. It is especially enriching when we step outside our usual circles, because then we get to hear about things that are very different from our day-to-day lives. These interactions are often transformative, not only in how we understand the world beyond our bubble, but also in how they can change the way we do the things we are used to doing.

In science and mathematics, this is no different. One of the most
exciting things a mathematician can do is to find a connection between
seemingly unrelated concepts, areas, or ideas. These bridges are
exciting because they change the way we reason about things on either
side.

Combinatorics, and especially graph theory, is a very good case in
point. We shall see how it allows us to connect guessing games, network
search, seating arrangements, colouring problems, and Sudoku-like
puzzles.

## Guessing, searching, colouring and decompositions

It goes without saying that searching is a fundamental operation in
today's world. We look up the meanings of words in a dictionary, search
for nearby restaurants, filter emails, and try to locate defective or
malicious nodes in communication networks.

[Google has
said](https://blog.google/products/ads-commerce/ai-personalization-and-the-future-of-shopping/)
that people make more than 5 trillion searches on Google each year, and
OpenAI told Axios, [as reported by
TechCrunch](https://techcrunch.com/2025/07/21/chatgpt-users-send-2-5-billion-prompts-a-day/),
that ChatGPT receives billions of prompts per day. Taken together, these
searches and prompts require a very large computing infrastructure, with
associated energy and cooling costs. This is one reason why developing
efficient query strategies is a core problem in computer science.

Searching for information is deeply connected to guessing games. In
fact, the two are, in many ways, two sides of the same coin. This is our
first bridge: we may think of queries as a way to narrow down a pool of
candidate places where the desired information or item might be stored.

Here is a concrete problem. Suppose one is given a graph with $n$
vertices and $m$ edges, one of whose edges is defective; think of a
failure in a network or circuit connection. In other words, our guessing
game is to find the defective edge quickly. Our goal is to identify it
using as few queries as possible.

Formulated in this way, the question is still a bit too vague. Let us
say that a query is a subset of edges, and that each query $Q$ can
result in one of two answers:

- **YES**: the defective edge lies in $Q$;
- **NO**: the defective edge does not lie in $Q$.

It is not difficult to devise a divide-and-conquer strategy in this
scenario:

1.  label the edges with distinct binary strings of length
    $\lceil\log_2 m\rceil$;
2.  for each bit position $i$, make query $Q_i$ be the set of edges
    whose label has a 1 in the $i$-th position;

This works because any pair of *distinct* edges $e$ and $f$ must
have labels that differ in some bit, say the \$j\$h bit. Then $Q_i$
contains either $e$ or $f$, but not both, so the answer to the query
$Q_j$ distinguishes these two possibilities. Equivalently, the full
vector of yes/no answers uniquely identifies the defective edge. Thus
$\lceil \log_2 m\rceil$ unrestricted yes/no queries suffice.

### Path queries

So far, so good. But what if some questions are more natural, practical,
or cheaper than others? A question proposed by Gyula O. H. Katona, and
which also appears in the network-design and electrical-engineering
literature, asks for the worst-case number of queries needed in an
$n$-vertex graph if each query must be a path.

In this case, the number of edges might be quadratic in $n$, and we
already know that, if no restriction were placed on the queries, then a
logarithmic number of unrestricted queries would suffice.

Here is a strategy:

1.  Find a small collection of edge-disjoint paths $P_1,P_2,\dots,P_s$
    whose union is the whole edge set. Think of the edges in $P_i$ as
    being coloured with colour $i$.
2.  Find another collection of paths $R_1,R_2,\dots,R_t$ such that
    every edge lies in some $R_i$, but no $R_i$ repeats a colour
    among its edges.

We call the paths in the second category *rainbow*. If we have these two
collections, then we can find any defective edge with $s+t$ path
queries.

<figure id="fig-paths" class="figure-img" width="600px">
<img src="/public/img/fig-path-cover.png" />
<figcaption>Two collections of paths</figcaption>
</figure>

Indeed, ask, for each of the paths $P_1,\dots,P_s,R_1,\dots,R_t$,
whether it contains the defective edge. These answers identify the
defective edge because the combined family of paths separates every pair
of edges.

To see this, take two distinct edges $e$ and $f$. If $e$ and $f$
have the same colour, choose a rainbow path $R_j$ that contains $e$.
Since $R_j$ is rainbow, it cannot also contain $f$. Thus $R_j$
distinguishes $e$ from $f$. If $e$ and $f$ have distinct
colours, then the unique path $P_a$ containing $e$ in the first
decomposition does not contain $f$. Thus $P_a$ distinguishes $e$
from $f$.

So every two edges give different answer patterns. The edge whose
pattern matches the answers to all $s+t$ queries is therefore the
defective edge. This means that, if we can build these two collections
of paths, then $s+t$ is an upper bound on the number of queries needed
in the worst case.

This extends our collection of bridges: searching for an edge in a
network is related to edge decompositions of (edge-coloured) graphs.

# Edge decompositions and seating arrangements

Our next connection dates back to a famous problem proposed by the
mathematician Gerhard Ringel during a conference at the Oberwolfach
research centre:

> A group of mathematicians meets for a few days at a workshop in
> Oberwolfach. Every day, they all dine together. Can we come up with
> seating arrangements such that each person has different neighbours
> every day, and such that, after a few days, every pair of participants
> has sat side by side exactly once?

Here is the graph-theoretic translation: a seating arrangement around
circular tables gives a collection of cycles, one cycle for each table.
The pairs of people who sit next to each other are the edges of those
cycles. Solving the problem means decomposing all edges of the complete
graph on the participants into copies of the same cycle pattern.

Here is a small example. Suppose our conference participants are Alex,
Bruna, Carla, Diana, and Eric, and suppose they will always sit at the
same table.

It turns out that we are in luck. On the first day, they sit in cyclic
order. This uses 5 pairs of people who sit side by side. The unused
pairs form precisely another cycle of length 5, which gives our
arrangement for the second day. After these two days, everyone has sat
next to everyone else exactly once.

<figure id="fig-5" class="figure-img" width="350px">
<img src="/public/img/fig-5-people-seating.png" />
<figcaption>Five at the table, twice!</figcaption>
</figure>

Coincidence? Not quite. It turns out that, for every sufficiently large
odd number of participants, and for any prescribed way of splitting them
into circular tables of size at least 3, such a seating plan exists.
This was shown by Stefan Glock, Felix Joos, Jaehoon Kim, Daniela Kühn,
and Deryk Osthus in their 2021 resolution of the Oberwolfach problem.

No solution is possible, in this exact form, for an even number of
participants. This is because at every meal each person sits next to
exactly two others. Therefore, the number of people we “check off” from
anyone's list of meal-neighbours is always even.

Here is a solution for 7 people, using two ordinary round tables, one of
size 3 and one of size 4. This requires 3 days.

<figure id="fig-7" class="figure-img" width="700px">
<img src="/public/img/fig-7-people-seating.png" />
<figcaption>Two tables for 7</figcaption>
</figure>

## Sudokus and coloured networks

Sudoku is a well-known puzzle game in which a $9\times 9$ grid is to
be filled so that each row, each column, and each of the nine
$3\times 3$ subgrids contains all the numbers $1,2,3,\dots,9$.

<figure id="fig-sudoku" class="figure-img" width="350px">
<img src="/public/img/fig-sudoku.png" />
<figcaption>A solved Sudoku grid. The puzzle would start with only the
dark-coloured numbers filled.</figcaption>
</figure>

A completed Sudoku grid is a type of *Latin square*, with the extra
condition imposed by the $3\times 3$ subgrids. Latin squares have been
studied for centuries by many mathematicians, including the illustrious
and prolific Leonhard Euler. A Latin square is simply an $n\times n$
table whose cells are filled with $n$ symbols, with no symbol repeated
in any row or column.

One particular theme in the study of Latin squares is the search for a
*transversal*. This is a set of $n$ cells containing one cell from
each row, one cell from each column, and one occurrence of each symbol.

And here is another bridge, or two: a Latin square turns out to be
equivalent to a specific type of coloured graph. We take two collections
of vertices, one representing the rows and the other representing the
columns. Then, for each cell, we join the corresponding row-vertex to
the corresponding column-vertex, and colour the edge with the symbol
appearing in that cell.

In particular, a transversal is a perfect matching whose edges have
pairwise distinct colours: a rainbow perfect matching in the graph.

<figure id="fig-latin-graph" class="figure-img" width="700px">
<img src="/public/img/fig-latin-square-graph.png" />
<figcaption>A Latin square is an edge-coloured complete bipartite graph.
In both the Latin square and the graph, a transversal is
highlighted.</figcaption>
</figure>

# More connections

This completes our foray into mathematical connections. Lurking behind
these there is another network of connections (pun intended): the one
between researchers with whom I have had the honour of discussing these
topics, and many other interesting things.

A big shout-out to the following collaborators! 👋

- [Marthe Bonamy](https://www.labri.fr/perso/mbonamy/) (Centre National
  de la Recherche Scientifique)
- [Fábio Botler](https://www.cos.ufrj.br/~fbotler/) (Universidade de São
  Paulo)
- [François Dross](https://sites.google.com/view/francoisdross/)
  (Université de Bordeaux)
- [Antônio Kaique](https://www.ime.usp.br/~antoniokaique/) (Universitat
  Politècnica de Catalunya)
- [Guilherme Oliveira Mota](http://www.ime.usp.br/~mota/) (Universidade
  de São Paulo)
- [Jozef Skokan](http://www.maths.lse.ac.uk/personal/jozef/) (London
  School of Economics)
- [Walner Mendonça](https://walnerm.github.io) (Universidade Federal do
  Ceará)
- [Lyuben Lichev](http://lyubenlichev.rf.gd/) (Technische Universität
  Wien)
- [Jaehoon Kim (김재훈)](https://sites.google.com/view/jaehoon-kim/home)
  (KAIST)
- [Marc Noy](https://web.mat.upc.edu/marc.noy/) (Universitat Politècnica
  de Catalunya)

# Pint of Science: my experience and thoughts

This was my first time speaking publicly about my research directly to
people who were not researchers. As one can imagine, this was both
exciting and nerve-wracking. Mathematics has a bad reputation, but this
has begun to change as more and more science communicators reach larger
audiences on social media.

All that being said, I enjoyed the whole process: interacting with the
event organisers, preparing the talk, attending the event as a
spectator, and then speaking.

The talks are short, and there is time for a few questions afterwards,
with interactive activities between some of the talks: quizzes, and even
bingo.

The questions I was asked were interesting. Unsurprisingly, I got asked
something along the lines of “So what?” While I had not especially
anticipated this question — in hindsight, it is not unexpected after a
maths talk — it was actually great. After years of chatting with friends
and family members about the purpose of mathematics, I was happy to have
an open mic to talk about some of the many faces of mathematics and its
value.

- Mathematics has a knack for helping us find flaws in our reasoning,
  much like touching an optical illusion to see that something is not
  really moving. Following algorithms, or even mathematics, blindly [can
  be a very bad
  idea](https://en.wikipedia.org/wiki/Weapons_of_Math_Destruction).
- Solving hard problems is a great way to come up with new ideas to
  attack even harder problems, which is toolbox-building. Solving many
  problems is also a great way of spotting general patterns, which is
  theory-building. These are [two cultures of
  mathematics](https://www.dpmms.cam.ac.uk/~wtg10/2cultures.pdf), each
  of which has its own allure for mathematicians and makes its own
  contribution.
- And, of course, some mathematics does solve real-life problems
  [surprisingly
  effectively](https://en.wikipedia.org/wiki/The_Unreasonable_Effectiveness_of_Mathematics_in_the_Natural_Sciences).

Not to mention the interest in pursuing knowledge for its own sake,
which, let us be frank, is no shabby reason!

With all this being said, I look forward to participating in other
editions of the Pint of Science and related events, and got me curious
to try to collaborate with other science divulgation initiatives.


---

Tássio Naia is an MSCA research fellow at the [Centre de Recerca Matemática](https://www.crm.cat/), working with Guillem Perarnau and the [GAPCOMB-UPC](https://gapcomb.upc.edu/en) group.