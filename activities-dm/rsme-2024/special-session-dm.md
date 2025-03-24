---
layout: page
title: ""
---
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">

<style type="text/css">

h1 {
  font-size: 1.5rem;
}
h2 {
  margin-top: 1.5rem;
  font-size: 1.2rem;
}
h3 {
  margin-top: 1.5rem;
  font-size: 1.1rem;
}
h4, h5, h6 {
  margin-top: 1rem;
  font-size: 1rem;
}

body, td {
   font-size: 0.9rem;
}

.container {
    max-width: 56rem;
    }
    @media (min-width: 38em) {
    .container {
        max-width: 38rem;
    }
    }
    @media (min-width: 56em) {
    .container {
        max-width: 56rem;
    }
}

</style>

# Sesión Especial 4: [Matemática Discreta y Algorítmica](https://2024.bienalrsme.com/sites/default/files/S4%20MatDiscretaAlgoritmica.pdf)
[Congreso Bienal de la Real Sociedad Matemática Española](https://2024.bienalrsme.com/)

Del 22 al 26 de enero de 2024

Aula A 6B, edificio El Sario, UPNA

##  Organizadores
- Delia Garijo (Universidad de Sevilla)
- Marc Noy (Universidad Politécnica de Cataluña)
- Francisco Santos (Universidad de Cantabria)

## Descripción
La matemática discreta estudia estructuras combinatorias o discretas, particularmente grafos, geometrías finitas, estructuras geométricas discretas y aspectos combinatorios de estructuras algebraicas y de teoría de números, y en ella los aspectos algorítmicos tienen una relevancia particular de forma natural. La sesión propuesta está auspiciada por la recientemente creada [Red de Matemática Discreta y Algorítmica](https://dam-network.github.io), financiada por el Ministerio de Ciencia e Innovación para el periodo 2023-2025 (RED2022-134947-T), y presentará una panorámica de la investigación actual del área en España.

## Programa

### Lunes, 22 de enero de 2024

#### Moderadora: Maria Bras-Amorós

- Pedro A. García Sánchez (Universidad de Granada), Factorizaciones en extensiones de ideales de monoides libres conmutativos [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-pedro.pdf %}) [[arXiv]](https://arxiv.org/abs/2311.06901)
    <details>
    <summary>Resumen</summary>
    <p>En esta charla estudiaremos submonoides de $(\mathbb{N}^{(I)},+)$, con $I$ un conjunto de enteros, que cumplen (1)  la suma de dos huecos es o bien un hueco o un átomo o la suma de dos átomos, y (2) la suma de un hueco y un átomo es un átomo o la suma de dos átomos.  Todos estos monoides son de la forma $\{0\}\cup (X+\mathbb{N}^{(I)})$, con $X\subseteq \mathbb{N}^{(I)}$.</p>

    <p>Nos centraremos en el estudio de algunos invariantes de factorización en estos monoides. 
    Probamos que el máximo de los conjuntos Delta es a lo sumo uno, con lo que o bien son monoides de factorización media o única, o las longitudes de las factorizaciones de cualquier elemento conforman un intervalo de enteros. También probaremos que la catenariedad es a lo sumo cuatro. Para ello será crucial demostrar que los grados de Betti de estos monoides son suma de a lo sumo de tres átomos. Daremos cotas inferiores y superiores para la $\omega$-primalidad en estos monoides.</p>

    <p>Este trabajo es una continuación de [1], y está dedicado a su autor.</p>
    <strong>Referencias</strong>
    <br>
    [1] N. Baeth, Complement-Finite Ideals. In: JL. Chabert, M. Fontana, S. Frisch, S. Glaz, K. Johnson, (eds) Algebraic, Number Theoretic, and Topological Aspects of Ring Theory. Springer, Cham, (2023).
    <br>
    [2] A. Geroldinger, F. Halter-Koch, Non-unique factorizations. Algebraic, combinatorial and analytic theory. Pure and Applied Mathematics (Boca Raton), 278. Chapman & Hall/CRC, Boca Raton, FL, (2006).
    <br>
    <strong>Agradecimientos</strong>
    <br>
    Esta investigación se ha llevado a cabo con la financiación del grupo FQM–343 y del Proyecto de Excelencia ProyExcel_00868 de la Junta de Andalucía, el proyecto PID2022-138906NB-C21 financiado por MCIN/AEI/10.13039/501100011033 y fondos FEDER, además de por el MICINN, a través del “Programa Severo Ochoa y María de Maeztu para Centros y Unidades de Excelencia” (CEX2020-001105-M) y la RED2022-134947-T, financiada por la Agencia Estatal de Investigación.
    <br>
    <br>
    </details>

- Kolja Knauer (Universitat de Barcelona), Colorear grafos de Cayley [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-kolja.pdf %})
    <details>
    <summary>Resumen</summary>
    <p>Un grafo de Cayley $\mathrm{Cay}(G,C)$ de un grupo finito $G$ is <em>minimal</em> si $C$ es un conjunto generador de $G$ minimal por inclusion. En los setentas Babai [1] discute por primera vez el problema de determinar el número cromático de un grafo de Cayley minimal y propone una conjetura fuerte que implicaría que todos estos grafos tienen numero cromático acotado por una constante global. En este trabajo mostramos que esta conjetura fuerte es falsa. Sin embargo también mostramos que todo grafo minimal de un grupo nilpotente o dihedral generalizado tiene numero cromático a lo mucho tres. También encontramos grafos minimales de Cayley con numero cromático cuatro y mostramos que eso es lo mas alto posible hasta orden $215$. Nótese que veinte años más tarde el mismo Babai [2] propuso otra conjetura fuerte que implica que existen familias de grafos minimales de Cayley con numero cromático no acotado. Esta sigue abierta.</p>
    <strong>Referencias</strong>
    <br>
    [1] L. Babai, Chromatic number and subgraphs of Cayley graphs, Theor. Appl. Graphs, Proc. Kalamazoo 1976, Lect. Notes Math. 642, 10-22 (1978), 1978.
    <br>
    [2] L. Babai, Automorphism groups, isomorphism, reconstruction, in Handbook of combinatorics. Vol. 1-2, Amsterdam: Elsevier (North-Holland); Cambridge, MA: MIT Press, 1995, pp. 1447-1540.
    <br><br>
    </details>

- Julio José Moyano Fernández (Universitat Jaume I), Algunos elementos combinatorios dentro de la teoría de singularidades de curvas planas [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-julio.pdf %})
    <details>
    <summary>Resumen</summary>
    <p>Algunos de los invariantes usados en la clasificación topológica de las singularidades de curvas planas poseen una naturaleza combinatoria; ejemplos de ello son el semigrupo de valores o la serie de Poincaré asociados a la singularidad (ver e.g. [4] y los trabajos allí referenciados).</p>

    <p>Esta conferencia tiene como objetivo presentar a la comunidad de <em>Matemática discreta y algorítmica</em> ambos objetos combinatorios, además de los resultados más interesantes o novedosos concernientes a los mismos dentro de la teoría de singularidades de curvas planas: destacaremos la relación de la serie de Poincaré con la función zeta de Stöhr en un contexto de singularidades de curvas definidas sobre cuerpos finitos, demostrada por Delgado y el autor [3], su coincidencia con el polinomio de Alexander en el caso de curvas complejas (resultado debido a Campillo, Delgado y Gusein-Zade [2]), así como los avances recientes del autor con P. Almirón [1] analizando la naturaleza de esta igualdad.</p>
    <strong>Referencias</strong>
    <br>
    [1] P. Almirón, J.J. Moyano Fernández (2023). The intrinsic topological nature of the Poincaré series of a plane curve singularity. Preprint, arXiv:2302.12079v2.
    <br>
    [2] A. Campillo, F. Delgado, S.M. Gusein-Zade (2003). The Alexander polynomial of a plane curve singularity via the ring of functions on it. Duke Math. J. 117(1), 125-156.
    <br>
    [3] F. Delgado, J.J. Moyano Fernández (2009). On the relation between the generalized Poincaré series and the Stöhr zeta function. Proc. Am. Math. Soc. 137(1), 51-59.
    <br>
    [4] J.J. Moyano Fernández (2022). Generalized Poincaré series for plane curva singularities. In: C. Galindo et al., $p$-adic Analysis, Arithmetic and Singularities. Contemp. Math., vol. 778, 25-69.
    <br><br>
    </details>

- Delia Garijo (Universidad de Sevilla), Diámetro continuo en grafos [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-delia.pdf %})
    <details>
    <summary>Resumen</summary>
    <p>Los <em>problemas de aumento</em> en grafos han sido ampliamente estudiados para medidas relacionadas con distancias, como el diámetro o la dilación. El objetivo en estos problemas es añadir un conjunto mínimo de aristas al grafo (o de mínimo peso) de forma que se satisfaga una condición establecida sobre el parámetro en estudio, por ejemplo, la disminución del diámetro del grafo resultante con respecto al original.
    Si se considera el lugar geométrico de la realización de un grafo en algún espacio euclídeo, surge la posibilidad de permitir que los extremos de las aristas insertadas sean, no ya vértices, sino puntos cualesquiera que estén sobre las aristas del grafo. Se pasa por tanto de considerar un número finito de distancias (entre pares de vértices) a tratar con un número infinito (entre pares de puntos de dicho lugar geométrico). Este salto de lo que llamamos la <em>versión discreta</em> del problema a la <em>versión continua</em> ha despertado mucho interés en los últimos años, no solo en problemas de aumento, sino en diversos tipos de problemas de grafos.</p>

    <p>En esta charla nos centraremos en la versión continua de problemas relacionados con el diámetro del grafo. Ilustraremos elementos que hacen muy difícil este salto "del discreto al continuo" y que provocan que los avances en esta línea de investigación estén siendo muy lentos. También plantearemos diversas cuestiones que serían interesantes de aproximar.</p>

    <p>Esta charla se enmarca en una serie de trabajos con distintos coautores: J. Cáceres (U. Almería), Fabian Klute (UPC), Alberto Márquez (U. Sevilla), Irene Parada (UPC), Rodrigo Silveira (UPC).</p>
    <strong>Agradecimientos</strong>
    <br>
    Financiado por MICINN a través del proyecto PID2019-104129GB-I00/MCIN/AEI/10.13039/501100011033.
    <br><br>
    </details>

### Martes, 23 de enero de 2024

#### Moderador: Pablo Candela

- María A.Hernádez Cifre(Universidad de Murcia), On discrete Brunn-Minkowski type inequalities [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-mangeles.pdf %})
<details>
    <summary>Resumen</summary>
    <p>The well-known Brunn-Minkowski inequality states that for a pair of convex bodies (i.e., non-empty compact and convex sets) $K,L\subset{\Bbb R}^n$, the functional $\mathrm{vol}\bigl((1-\lambda)K+\lambda L\bigr)^{1/n}$ is concave in $\lambda\in(0,1)$, where $\mathrm{vol}(\,\cdot)$ represents the volume (Lebesgue measure) and $+$ is the Minkowski (vectorial) addition.</p>

    <p>The $L_p$ version (for $p\geq 1$) of the Brunn-Minkowski inequality was originally proven by Firey in the 60's in the setting of convex bodies containing the origin, and was recently extended to arbitrary non-empty compact sets by Lutwak, Yang and Zhang in 2012. It asserts that for non-empty compact sets $K,L\subset{\Bbb R}^n$ and $\lambda\in(0,1)$,
    \[
    \mathrm{vol}\bigl((1-\lambda)\cdot K +_p \lambda\cdot L\bigr)^{p/n}\geq(1-\lambda)\mathrm{vol}(K)^{p/n}+\lambda\mathrm{vol}(L)^{p/n}.
    \]
    When $p=0$ (or even $0<p<1$), the conjectured log-Brunn-Minkowski inequality for centrally symmetric convex bodies, namely, $\mathrm{vol}\bigl((1-\lambda)\cdot K+_0\lambda\cdot L\bigr) \geq\mathrm{vol}(K)^{1-\lambda}\mathrm{vol}(L)^\lambda$, is known to be true only in the plane
    and for particular families of sets.</p>

    <p>Nowadays there is a growing interest in getting discrete counterparts of classical inequalities, i.e., discrete analogues in which, either convex bodies and volume are replaced by finite sets of points and cardinality $|\,\cdot|$, respectively, or just the volume is replaced by the so-called {\it lattice-point enumerator} $\mathrm{G}(\,\cdot)$, which is defined as $\mathrm{G}(M)=|M\cap\mathbb{Z}^n|$. Of course, the Brunn-Minkowski inequality is one of the first results to be considered in this discrete setting. In this talk we will discuss discrete analogues of the above-mentioned results in the setting of the lattice point enumerator.</p>

    <strong>Referencias</strong>
    <br>
    [1] D. Iglesias, J. Yepes Nicolás, A. Zvavitch (2020).  Brunn-Minkowski type inequalities for the lattice point enumerator. Adv. Math. 370, 107193.
    <br>
    [2] M. A. Hernández Cifre, E. Lucas, J. Yepes Nicolás (2022). On discrete $L_p$ Brunn-Minkowski type inequalities. RACSAM 116, Article 164.
    <br>
    [3] M. A. Hernández Cifre, E. Lucas (2022). On discrete log-Brunn-Minkowski type inequalities. SIAM J. Discrete Math. 36, 1748-1760.
    <br><br>
    </details>

- Maria Bras-Amorós (Universitat Rovira i Virgili), Numerical semigroups within the COPRICA research group [[transparencias]](http://crises-deim.urv.cat/~mbras/2024Pamplona.pdf)
    <details>
    <summary>Resumen</summary>
    <p>A numerical semigroup is a subset of the positive integers $\mathbb{N}$ together with $0$, closed under addition, and with a finite complement in $\mathbb{N}\cup\{0\}$. The number of gaps is its genus. Numerical semigroups arise in algebraic geometry, coding theory, privacy models, and in musical analysis. It is one of the main topics of the research group COPRICA at Universitat Rovira i Virgili. We will explain some classical problems on which we contributed or are currently working related to numerical semigroups and their counting by genus.</p>

    <strong>Agradecimientos</strong>
    <br>
    This work is supported by the grant PID2021-124928NB-I00 and 2021SGR00115.
    <br><br>
    </details>

- Simon Briend (Universitat Pompeu Fabra), Estimating Adam's genealogy [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-simon.pdf %})
    <details>
    <summary>Resumen</summary>
    <p>Growing random structures are ever more present in our lives, be it in information technologies, social networks, epidemiology, genomics etc. Propagation phenomena can be modelled by randomly growing graphs and in particular, recursive trees. These random models account for the growth over time of a network resulting from an attachment or spreading process. However, the history of this process is often hidden and only a snapshot of the network is observed in the present-day. Retrieving information from the past of the network can shed light on the origin of an infection or a fake news, and explain the current network structure. In this talk I will present methods estimating the order of arrival of the vertices in a recursive tree. Specifically, we study two fundamental random recursive tree models: the uniform attachment model and the linear preferential attachment model. I will start by presenting an order estimator based on the Jordan centrality measure and defining a parametric family of risk measures to quantify the quality of the ordering procedure. Then, I will establish a minimax lower bound for this problem based on the shape exchangeability of these recursive trees, and demonstrate that the proposed estimator is near-optimal. Finally, I will also consider alternative ordering procedures based on degree centrality, spectral method and a peeling strategy and conclude by displaying numerical evidences that the Jordan ordering is the best performer for our measure of error.</p>
    </details>

- Francisco Santos (Universidad de Cantabria), Towards a realization of the k-associahedron? [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-paco.pdf %})
    <details>
    <summary>Resumen</summary>
    <p>A subset of  $k+1$ diagonals of the $n$-gon is called a $(k+1)$-crossing if thyy all mutually cross, and a general subset is called $(k+1)$-crossing free if it does not contain a $k$-crossing.  $(k+1)$-crossing free subsets form a simplicial complex that we call the $k$-associahedron and denote $Ass_k(n)$ since for $k=1$ one recovers the (simplicial) associahedron. The $k$-associahedron is known to be a shellable sphere and conjectured to be polytopal [2] . It is also a subword complex in the root system of the $A$ and, moreover, every (spherical) subword complex is a link in some $k$-associahedron. In particular, polytopality of $k$-associahedra would imply the same for spherical subword complexes (in type $A$), a question asked by Knutson and Miller [3] .</p>

    <p>The dimension of the $k$-associahedron  coincides with that of any abstract rigidity matrix of dimension $2k$ on $n$ elements. This made Pilaud and Santos [4] conjecture that $k$-triangulations are generically isostatic graphs in dimension $2k$, in the usual bar-and-joint rigidity theory, as a step towards the construction of the $k$-associahedron via the corresponding rigidity matrix. We explore this possibility [1] .</p>

    <strong>Referencias</strong>
    <br>
    [1]Luis Crespo Ruiz, Francisco Santos. Multitriangulations and tropical Pfaffians. Preprint, 29 pages, March 2022. arXiv:2203.04633
    <br>
    [2] Jakob Jonsson, Generalized triangulations and diagonal-free subsets of stack polyominoes, J. Comb. Theory Ser. A 112(1), 117-142 (2005).

    [3] Allen Knutson and Ezra Miller. Subword complexes in Coxeter groups. Adv. Math., 184(1) (2004), 161-176.

    [4] Vincent Pilaud, Francisco Santos, Multitriangulations as Complexes of Star Polygons, Discrete Comput. Geom. 41 (2009), 284-317.
    <br><br>
    </details>

#### Moderador: Pedro A. García-Sánchez

- Pablo Candela (Universidad Autónoma de Madrid),  Nilespacios finitos y aplicaciones recientes
    <details>
    <summary>Resumen</summary>
    <p>El análisis de las normas de Gowers es uno de los temas más activos de la combinatoria aritmética desde finales de los años 1990, gracias especialmente a las nuevas extensiones que ofrece del análisis de Fourier discreto. Recientemente, este tema recibió un nuevo impulso basado en interesantes preguntas y conjeturas de Jamneshan, Shalom y Tao. Una de estas cuestiones concierne a las normas de Gowers en el ámbito discreto de grupos abelianos finitos con exponente acotado [1, Question 1.9]. Hablaremos de avances recientes en esta dirección (en colaboración con González-Sánchez y Szegedy), que la conectan con una nueva rama de la teoría de los nilespacios. Aprovecharemos para ofrecer una breve introducción a esta joven teoría, y en particular a los nilespacios finitos, que abren nuevas direcciones de investigación en matemática discreta.</p>

    <strong>Referencias</strong>
    <br>
    [1] A. Jamneshan, O. Shalom, T. Tao, The structure of totally disconnected Host--Kra--Ziegler factors, and the inverse theorem for the $U^k$ Gowers uniformity norms on finite abelian groups of bounded torsion, preprint (2023). [arXiv:2303.04860](https://arxiv.org/pdf/2303.04860.pdf)
    <br><br>
    </details>

-  Mariana Rosas-Ribeiro (Universitat Rovira i Virgili),  Infinite chains in the tree of numerical semigroups [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-mariana.pdf %})
    <details>
    <summary>Resumen</summary>
    <p>A numerical semigroup is a submonoid of the additive monoid $\mathbb{N}$ with finite complement in $\mathbb{N}$. The cardinality of the complement of a numerical semigroup is its genus and its smallest non-zero element is the multiplicity. For a given positive integer $g$, there is a limited amount of numerical semigroups that have genus $g$. There is no formula for the number $n_g$ of numerical semigroups of genus $g$, but in 2008 Bras-Amorós [1] conjectured that as $g$ grows $n_g$ grows Fibonacci-like. One of the tools to study the growth of this $n_g$ sequence is the tree of numerical semigroups, that organizes all the numerical semigroups in such a way that each level $g$ of the tree is formed by the numerical semigroups of genus $g$. In this tree there are nodes that have infinite descendants. In [2], the authors characterize these nodes (numerical semigroups) using the greatest common divisor of the first elements of the numerical semigroup. The collection formed by a numerical semigroup and its infinitely many descendants, if applicable, is an infinite chain. In this talk we show that at each level of the tree there are more nodes which are not in an infinite chain than the other way around. Furthermore, we find a self-replicating behavior in the subtrees formed by numerical semigroups with fixed multiplicity $m$. With this, we can determine the number of numerical semigroups that have infinitely many descendants, genus $g$ and multiplicity $m\leq7$.</p>

    <strong>Referencias</strong>
    <br>
    [1]  M. Bras-Amorós (2008). Fibonacci-like behavior of the number of numerical semigroups of a given genus. Semigroup Forum, 76, pp. 379-384.
	<br>
    [2] M. Bras-Amorós, S. Bulygin (2009). Towards a better understanding of the semigroup tree. Semigroup Forum, 79, 561-574.
    <br>

    <strong>Agradecimientos</strong>
    The first author was supported by the Catalan government under grant 2021 FISDUR 00189. Both authors were supported by the Spanish government under grant PID2021-124928NB-I00, and by the Catalan government under grant 2021 SGR 00115.
    <br><br>
    </details>

-  Marc Noy (Universidad Politécnica de Cataluña), Grupo GAPCOMB de la UPC. Sistemas de votaciones y combinatoria analítica [[transparencias]]({{ site.baseurl }}{% link /activities-dm/rsme-2024/Slides-marc.pdf %})
    <details>
    <summary>Resumen</summary>
    <p>En la charla se dará una breve descripción del grupo de investigación <em>Combinatoria Geométrica, Algebraica  y Probabilística</em> (GAPCOMB) de la  Universidad Politécnica de Cataluña.
    A continuación se presentará un trabajo en curso sobre sistemas  de votaciones que utiliza funciones generadoras y métodos analíticos, en colaboración con Emma Caizerges, Fran\c{c}ois Durand, élie de Panafieu (Nokia Bell Labs, France) y Vlady Ravelomanana (Université Paris-Cité).</p>

    <p>Consideramos un sistema de votación con $m$ electores y $n$ candidatos. Cada elector ordena de forma estricta sus preferencias de  los $n$ candidatos. Se dice que el candidato $C$ es un ganador de Condorcet [1] si la mayoría de electores (suponemos $n$ impar para evitar empates) prefiere $C$ a cualquier otro candidato. Suponiendo que cada elector elige el orden de los candidatos de forma aleatoria e  independiente, un problema ampliamente estudiado es la probabilidad $p_m$ de que haya un ganador de Condorcet cuando $n\to \infty$. Claramente $p_2=1$. Se sabe que $p_3 = \frac{3}{4}+ \frac{3}{2\pi } \arcsin(1/3) \approx 0.9123$ y que $p_m \to 0$ cuando $m \to \infty$.</p>

    <p>En este trabajo codificamos las preferencias de los electores mediante una función generadora racional $F(x_1,\dots,x_{m-1})$. La probabilidad  de que exista un ganador de Condorcet se pude expresar en términos del coeficiente de $x_1^{n/2}x_2^{n/2}\cdots x_{m-1}^{n/2}$ en $F(x_1,\dots,x_{m-1})$. Utilizando métodos analíticos se puede estimar dicha probabilidad con precisión. Esto proporciona un nuevo  método para estudiar este y otros problemas de sistemas de votaciones.</p>

    <strong>Referencias</strong>
    <br>
    [1] W. Gehrlein (2006). Condorcet's Paradox. Springer.
    <br><br>
    </details>
