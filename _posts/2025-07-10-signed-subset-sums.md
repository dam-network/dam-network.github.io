---
layout: post
title: "Recent Trends IX: Finding signed subset sums of unit vectors of large norm"
abstract: "Amongst every signed sum of a subset of k elements of a given set of n unit vectors in the d-dimensional space, select the one of maximum Euclidean norm, and find how small can this value be. This problem belongs to a very important family of problems in discrete and convex geometry, in particular, to that of 'unit vector balancing problems'. This problem is connected to geometric optimization, geometric discrepancy theory, lp-polarization problem, or p-frame energies, amongst others."
tag: 'Trend'
---

**Open question 1**. *Given $2 \leq d\leq n$, $1\leq k\leq n$, what is
the largest value $c(d,n,k)$ such that from any set of $n$ unit vectors
$\omega_n:=\{u_1,\dots,u_n\}\in\mathbb S^{d-1}$, there exist indices
$1\leq i_1<\cdots<i_k\leq n$ and signs
$\varepsilon_1,\dots,\varepsilon_k\in\{\pm 1\}$ such that*

$$
\|\varepsilon_1u_{i_1}+\cdots+\varepsilon_ku_{i_k}\|_2\geq c(d,n,k)?
$$



Equivalently,

$$c(d,n,k)=\min_{\{u_1,\dots,u_n\}\in\mathbb S^{d-1}} \max_{1\leq i_1<\cdots<i_k\leq n} \max_{\varepsilon_1,\dots,\varepsilon_k\in\{\pm 1\}}  \|\varepsilon_1u_{i_1}+\cdots+\varepsilon_ku_{i_k}\|_2.$$

One can rewrite the above quantity as the *quadratic problem*

$$\begin{split}    
\min  & \,\, \lambda \,\, \\
& \text{s.t.} \\
 & \|\varepsilon_1 u_{i_1}+\cdots+\varepsilon_k u_{i_k}\|_2^2 \leq \lambda^2 \\
 & \|u_1\|_2^2=\cdots=\|u_n\|_2^2=1 \\
 & u_j\in\mathbb R^d,\,\, 1\leq j\leq n,\,\, \\
  & \varepsilon_1,\dots,\varepsilon_k\in\{\pm 1\} \\
 & \forall \,\, 1\leq i_1<\cdots<i_k\leq n \\
 & \lambda\geq 0.
\end{split}$$

These numbers have been studied in detail in [[1]](#AmGon) and [[2]](#AmNi). They belong to the so-called subset sum type question, and they lie at the core of discrete geometry and related topics. For instance, they would solve the optimal ratio between some radii functional evaluated on the Minkowski sum of convex bodies and the sum of the radii evaluated over every such convex body (see [[8]](#GonHC)). Some things are already known about these numbers.

Let us notice first some basic monotonic properties of $c(d,n,k)$:

$$c(d_2,n_1,k_1) \leq c(d_2,n_1,k_2) \leq c(d_2,n_2,k_2) \leq c(d_1,n_2,k_2)$$

for every $2\leq d_1<d_2$ and $1\leq k_1<k_2\leq n_1<n_2$. The first non
trivial lower bound is provided by simply taking the average over all
sign sequences, arriving in

$$c(d,n,k)\geq\sqrt{k} \quad \text{ for every }d\geq 1\text{, }1\leq k\leq n.$$

Moreover, this estimate turns out to be sharp if and only if $n\leq d$,
and the set of vectors $\omega_n$ has to form an orthonormal set of
vectors from $\mathbb S^{d-1}$.

Ambrus and Nietert [[2]](#AmNi) proved by using the connection with the $p=1$ case of the $\ell_p$-polarization problem on the sphere $\mathbb S^{d-1}$ that

$$c(d,n,n)=\Theta\left(\frac{n}{\sqrt{d}}\right)\quad \text{ when }n\rightarrow\infty.$$

Notice here that this asymptotic behavior contrasts with that of
$\Omega(\sqrt{n})$ for when $n\leq d$. Next result [[1](#AmGon),Thm. 2] explains pretty much
the asymptotic behavior of $c(d,n,k)$: 

<div id="eq:thm2" class="equation">
$$
c(d,n,k) \geq \max\left\{k-8\cdot k^\frac{d+1}{d-1}\cdot n^{-\frac{2}{d-1}},\sqrt{\frac{2}{\pi}}\cdot \frac{1}{\sqrt{d}}\cdot k\right\}, \tag{1}
$$
</div>

whenever $n\geq d\geq 2$ and $k\geq 3$. The inequality on the left
follows from counting the points of $\omega_n$ within spherical caps of
a suitably chosen radius on $\mathbb S^{d-1}$. Notice that the second
estimate on the right is better than the first when $k$ is relatively
close to $n$. In fact, the tightness of
[(1)](#eq:thm2) is provided by suitable estimates
of particular examples, when using the notion of largest set of
$\delta$-separated vectors on $\mathbb S^{d-1}$: 

$$\begin{split}
    c(d,n,k) \leq \left\{ 
    \begin{array}{lccr}
        k-\alpha_1\cdot \frac{1}{d^2}\cdot k^\frac{d+1}{d-1}\cdot n^{-\frac{2}{d-1}}  &&&  \text{for }3\leq k\leq 6\cdot 100^{d-1}, \\
        k-\alpha_2 \cdot k^\frac{d+1}{d-1}\cdot n^{-\frac{2}{d-1}}  &&&  \text{for }6\cdot 100^{d-1} \leq k\leq n, \\
        \frac{4\varphi}{\sqrt{\pi}}\cdot \frac{1}{\sqrt{d}}\cdot k  & && \text{for }k>\frac{1}{\sqrt{d}}e^{-\frac d2}n,\,\frac{\varphi k}{n} = e^{-\frac{\varphi^2}{2}},\,\varphi>0.
    \end{array}\right.
\end{split}$$ 

Therefore, it is not yet clear what is the asymptotic
behavior of $c(d,n,k)$ for small values of $k$.

The exception to the case of small $k$ is certainly $c(d,n,2)$, which
has been studied in detail. Since $\|u+v\|_2^2=2+2\langle u,v\rangle$
for $u,v\in\mathbb S^{d-1}$, bounding $c(d,n,2)$ is equivalent to
estimating $\max_{1\leq i<j\leq n}|\langle u_i,u_j\rangle|$. This is a
well-known problem: this quantity is called the *coherence of the vector
set* $\omega_n$, which is a special case of the $p$-*frame energies* [[4](#BGMPV), [7](#CGGKO)].
Its minimizers are called *Grassmannian frames* and play an important
role in equiangular spherical codes [[3]](#BDKS). The classical Welch bound [[10]](#Wel) states that one can always select $1\leq i<j\leq n$ such that 

<div id="eq:k2" class="equation">
$$\label{eq:k2}
|\langle u_i,u_j\rangle| \geq \sqrt{\frac{n-d}{d(n-1)}}.\tag{2}
$$ 
</div>

Very recently, Bukh and Cox [[6]](#BuCo) improved the estimates in
[(2)](#eq:k2) when $d+2\leq n\leq d+O(d^2)$. In
particular, they were able to show that

$$
c (d, d + 1,2) =\sqrt{2+\frac2d}.
$$ 

Here equality holds if and only if
the vectors $u_1,\dots,u_{d+1}$ form, up to change of signs, the
vertices of a $d$-dimensional regular simplex. In [[1](#AmGon), Thm. 4], the authors calculated a better estimate for the asymptotic behavior of $c(d,n,2)$. To do so, they used maximal $\delta$ separated sets estimates to obtain

$$
2-0.51\cdot n^{-\frac{2}{d-1}} <c(d,n,2) < 2-0.14\cdot n^{-\frac{2}{d-1}},
$$

for each sufficiently large $d$ and $n$ larger than some $n(d)$.

A much more concrete bound has been provided in the planar case [[1](#AmGon), Thm. 5], where it has been proven 

$$
c(2,n,k) \geq \left\{
\begin{array}{lccr}
   k\cos\frac{(k-1)\pi}{2n}  &&& \text{for }k\text{ even,} \\
   & \\
   \sqrt{1+(k-1)(k+1)\cos^2\frac{(k-1)\pi}{2n}}  &&& \text{otherwise.}
\end{array}\right.
$$ 

Moreover, those estimates are best possible when
and only when $n$ is divisible by $k-1$, and in those cases, equality
occurs when $\{\pm u_1,\dots,\pm u_n\}$ forms the vertex of a regular
$\frac{2n}{k-1}$-gon inscribed in $\mathbb S^1$, and each vertex of
multiplicity $k-1$. The particular case where $n=k$ has been completely
solved by Ambrus and Nietert [[2]](#AmNi) and Grundbacher [[9]](#Gru), by very different
methods. They have proven that

$$
c(2,n,k) \geq \frac{1}{\sin\left(\frac{\pi}{2k}\right)},
$$ 

with
equality only if $k\in\{1,n\}$, and if $k=n$, when and only when
$u_1,\dots,u_n$ are such that $\{\pm u_1,\dots,\pm u_n\}$ form the
vertices of a regular $2n$-gon inscribed in the unit circle (see also [[5]]#BFGK) when $n=3$).

Of all the still unsolved remaining cases, we find that the next one is
possibly the most appealing one:


**Open question 2**. *What is the exact value of $c(d,d+1,d+1)$, for
$d\geq 3$.*


It was conjectured (see [[1](#AmGon), Conj. 1]) that $$c(d,d+1,d+1)=\sqrt{d+2},$$ and equality would hold if and only if the set $\omega_{d+1}$ is either the vertices of a $d$-dimensional regular simplex if $d$ is even, or the union of the vertex set of a $(d-1)$-dimensional regular simplex in a hyperplane $H$ centered at the origin and a unit vector of $H^\bot$ otherwise.

### References

<ol style="padding-left: 0;">

<li id="AmGon"> G. Ambrus, B. González Merino, Large signed subset sums, Mathematika 67 (2021), no. 3, 579–595.</li>

<li id="AmNi"> G. Ambrus, S. Nietert, Polarization, sign sequences and isotropic vector systems, Pacific J. Math. 303 (2019), no. 2, 385–399.</li>

<li id="BDKS"> I. Balla, F. Dräxler, P. Keevash, B. Sudakov, Equiangular lines and spherical codes in Euclidean space, Invent. math. 211 (2018), no. 1,
179–212.</li>

<li id="BGMPV"> D. Bilyk, A. Glazyrin, R. Matzke, J. Park, O. Vlasiuk, Energy on spheres and discreteness of minimizing measures, J. Funct. Anal. 280 (2021), no. 11, 108995.</li>

<li id="BFGK"> M. Brugger, M. Fiedler, B. González Merino, A. Kirschbaum, Additive colourful Carathéodory type results with an application to radii, Lin. Alg. Appl. 554 (2018), no. 1, 342–357.</li>

<li id="BuCo"> B. Bukh, C. Cox, Nearly orthogonal vectors and small antipodal spherical codes, Israel J. Math. 238 (2020), no. 1, 359–388.</li>

<li id="CGGKO"> X. Chen, V. González, E. Goodman, S. Kang, A. Okoudjou, Universal optimal configurations for the p-frame potentials, Adv. Comput. Math. 46 (2020), no. 4, 1–22.</li>

<li id="GonHC"> B. González Merino, M. Hernández Cifre, Successive radii and Minkowski addition, Monat. Math. 166 (2012), no. 3-4, 395–409.</li>

<li id="Gru">F. Grundbacher, A sharp bound on large planar signed vector sums,
arXiv:2502.13752.</li>

<li id="Wel">L. Welch, Lower bounds on the maximum cross correlation of signals, IEEE Trans. Inform. Theory 20 (1974), 397–399.</li>

</ol>

---

[Bernardo González Merino](https://portalinvestigacion.um.es/investigadores/333022/detalle) is a Profesor Titular de Universidad (Senior Lecturer) at the University of Murcia.
