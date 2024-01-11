---
layout: post
title:  Geometry, randomness and Ramsey theory, by [Patrick Morris](asdf)
---


Since its inception in  the early 1900s, Ramsey theory has flourished and become a cornerstone of modern discrete mathematics (and beyond). The central question asks to determine $r(s,t)$; the minimum integer $n\in \mathbb{N}$ such that any red/blue-colouring of the edges of the complete graph $K_n$ results in either a red $K_s$ or a blue $K_t$. Very small values can be calculated but already $r(5,5)$ is beyond our computational power to determine exactly. Therefore Ramsey theorists have  focused mainly on asymptotics.  Erdős and his collaborators drove the subject forward in the 1940s, establishing bounds and posing  beautiful  open problems, many of which are known to be notoriously hard and have remained stubborn to this day.

Seemingly out of nowhere, we had a landmark year for Ramsey theory in 2023. Indeed,  Campos, Griffiths, Morris and Sahasrabudhe showed that $r(t,t)\leq (4-\varepsilon)^t$ for some $\varepsilon>0$ [[1]](#1). It was known already in the 40s that 
$$
\begin{align}\tag{1}
\sqrt{2}^{t+o(1)}\leq r(t,t)\leq 4^{t+o(1)}
\end{align}    
$$
and so this may seem like a tiny improvement but it is so significant because until now people had only managed to improve lower order terms and had done so with tremendous effort, often pioneering new techniques in the process. This result last year will thus go down in history as the first exponential improvement on the initial bounds $(1)$ of Erdős and collaborators. Moreover, there was  another Ramsey theory highlight  in 2023 that shocked the community. This was the breakthrough result of Mattheus and Verstraete showing that $r(4,t)=t^{3+o(1)}$ [[2]](#2). The upper bound here follows from classical work of Erdős and Szekeres in 1935 and so it was the lower bound that was the breakthrough, that is, providing a construction with many vertices and a colouring avoiding red $K_4$'s and blue $K_t$'s. 

Despite solving the correct exponent of growth of $r(4,t)$ (answering a longstanding question of Erdős), this result is also significant due to the methods used. Indeed, there has been a well-established trend of providing lower bounds for Ramsey problems using randomness. This was initiated already by Erdős, establishing the lower bound $(1)$ in 1947, one of the first instances of the hugely influential 
*probabilistic method*. Later advances in probabilistic techniques, such as the *Lovász Local Lemma* and the *differential equations method* for random processes, paralleled improvements in constructions for Ramsey graphs, and had success in  certain  central problems, for example establishing $r(3,t)$ up to a factor of 4. These same methods that did so well for $r(3,t)$ give a lower bound of $r(4,t)\geq t^{5/2+o(1)}$ and so fail to give the right exponent. In order to close the gap, Mattheus and Verstraete had to introduce a new idea. Their insight was to start with a point-line incidence geometry over a finite field known as a *Hermitian unital*. This object, known well to  finite geometers, has the special  property that there are no 4 points in general position that are pairwise collinear. In order to turn the collinearity graph into a good candidate for the red subgraph of $K_n$, they then need  to again use probabilistic ideas such as random sampling. The approach of using randomness in conjunction with constructions from finite geometry has had some other success in recent years  and this breakthrough did not come completely from nowhere but this perfect combination of several beautiful ideas hints at the power of finite geometry to provide new insight for Ramsey theory constructions. 

In September 2025, the workshop *Finite geometry and Ramsey theory* will joint the experts in this area at the [Banff International Research Station](https://www.birs.ca/). Simeon Ball and Patrick Morris, participants of the MDA network, are among the coorganizers of the event.

## References
<a id="1">[1]</a> 
M. Campos, S. Griffiths, R. Morris and J. Sahasrabudhe. An exponential improvement for diagonal Ramsey. arXiv preprint arXiv:2303.09521. 2023.

<a id="2">[2]</a>
S. Matheus, J. Verstraëte. The asymptotics of r(4,t). Accepted to Annals of Mathematics. arXiv:2306.04007, 2023.