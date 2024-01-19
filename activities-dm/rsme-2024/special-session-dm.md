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
  font-size: 1rem;
}
h3 {
  margin-top: 1.5rem;
  font-size: 1rem;
}
h4, h5, h6 {
  margin-top: 1rem;
  font-size: 1rem;
}

body, td {
   font-size: 0.9rem;
}

.container {
  max-width: 54rem;
}
@media (min-width: 38em) {
  .container {
    max-width: 34rem;
  }
}
@media (min-width: 56em) {
  .container {
    max-width: 54rem;
  }
}

</style>

# Sesión Especial 4 Matemática Discreta y Algorítmica

##  Organizadores
- Delia Garijo (Universidad de Sevilla)
- Marc Noy (Universidad Politécnica de Cataluña)
- Francisco Santos (Universidad de Cantabria)

## Descripción
La matemática discreta estudia estructuras combinatorias o discretas, particularmente grafos, geometrías finitas, estructuras geométricas discretas y aspectos combinatorios de estructuras algebraicas y de teoría de números, y en ella los aspectos algorítmicos tienen una relevancia particular de forma natural. La sesión propuesta está auspiciada por la recientemente creada Red de Matemática Discreta y Algorítmica, financiada por el Ministerio de Ciencia e Innovación para el periodo 2023-2025 (RED2022-134947-T), y presentará una panorámica de la investigación actual del área en España.

## Programa

### Lunes, 22 de enero de 2024

- Pedro A. García Sánchez (Universidad de Granada), Factorizaciones en extensiones de ideales de monoides libres conmutativos [transparencias]({{ site.baseurl }}{% link /activities-dm/rsme-2024/slides-pedro.pdf %})
    <details>
    <summary>Resumen</summary>
    <p>En esta charla estudiaremos submonoides de $(\mathbb{N}^{(I)},+)$, con $I$ un conjunto de enteros, que cumplen (1)  la suma de dos huecos es o bien un hueco o un átomo o la suma de dos átomos, y (2) la suma de un hueco y un átomo es un átomo o la suma de dos átomos.  Todos estos monoides son de la forma $\{0\}\cup (X+\mathbb{N}^{(I)})$, con $X\subseteq \mathbb{N}^{(I)}$.</p>

    <p>Nos centraremos en el estudio de algunos invariantes de factorización en estos monoides. 
    Probamos que el máximo de los conjuntos Delta es a lo sumo uno, con lo que o bien son monoides de factorización media o única, o las longitudes de las factorizaciones de cualquier elemento conforman un intervalo de enteros. También probaremos que la catenariedad es a lo sumo cuatro. Para ello será crucial demostrar que los grados de Betti de estos monoides son suma de a lo sumo de tres átomos. Daremos cotas inferiores y superiores para la $\omega$-primalidad en estos monoides.</p>

    <p>Este trabajo es una continuación de [1], y está dedicado a su autor.</p>
    <strong>Referencias</strong>
    <br>
    [1] N. Baeth, Complement-Finite Ideals. In: JL. Chabert, M. Fontana, S. Frisch, S. Glaz, K.~Johnson, (eds) Algebraic, Number Theoretic, and Topological Aspects of Ring Theory. Springer, Cham, (2023).
    <br>
    [2] A. Geroldinger, F. Halter-Koch, Non--unique factorizations. Algebraic, combinatorial and analytic theory. Pure and Applied Mathematics (Boca Raton), 278. Chapman & Hall/CRC, Boca Raton, FL, (2006).
    </details>

- Kolja Knauer (Universitat de Barcelona), Colorear grafos de Cayley
    <details>
        <summary>Resumen</summary>
        <p>Un grafo de Cayley $\mathrm{Cay}(G,C)$ de un grupo finito $G$ is <em>minimal</em> si $C$ es un conjunto generador de $G$ minimal por inclusion. En los setentas Babai [1] discute por primera vez el problema de determinar el número cromático de un grafo de Cayley minimal y propone una conjetura fuerte que implicaría que todos estos grafos tienen numero cromático acotado por una constante global. En este trabajo mostramos que esta conjetura fuerte es falsa. Sin embargo también mostramos que todo grafo minimal de un grupo nilpotente o dihedral generalizado tiene numero cromático a lo mucho tres. También encontramos grafos minimales de Cayley con numero cromático cuatro y mostramos que eso es lo mas alto posible hasta orden $215$. Nótese que veinte años más tarde el mismo Babai [2] propuso otra conjetura fuerte que implica que existen familias de grafos minimales de Cayley con numero cromático no acotado. Esta sigue abierta.</p>
        <p><strong>Referencias</strong></p>
        <p>[1] L. Babai, Chromatic number and subgraphs of Cayley graphs, Theor. Appl. Graphs, Proc. Kalamazoo 1976, Lect. Notes Math. 642, 10-22 (1978), 1978.</p>
        <p>[2] L. Babai, Automorphism groups, isomorphism, reconstruction, in Handbook of combinatorics. Vol. 1-2, Amsterdam: Elsevier (North-Holland); Cambridge, MA: MIT Press, 1995, pp. 1447-1540.</p>
    </details>

- Julio José Moyano Ferna ́ndez (Universitat Jaume I), Algunos elementos combinatorios dentro de la teoría de singularidades de curvas planas
    <details>
        <summary>Resumen</summary>
        <p>Algunos de los invariantes usados en la clasificación topológica de las singularidades de curvas planas poseen una naturaleza combinatoria; ejemplos de ello son el semigrupo de valores o la serie de Poincaré asociados a la singularidad (ver e.g. [4] y los trabajos allí referenciados).</p>

        <p>Esta conferencia tiene como objetivo presentar a la comunidad de <em>Matemática discreta y algorítmica</em> ambos objetos combinatorios, además de los resultados más interesantes o novedosos concernientes a los mismos dentro de la teoría de singularidades de curvas planas: destacaremos la relación de la serie de Poincaré con la función zeta de Stöhr en un contexto de singularidades de curvas definidas sobre cuerpos finitos, demostrada por Delgado y el autor [3], su coincidencia con el polinomio de Alexander en el caso de curvas complejas (resultado debido a Campillo, Delgado y Gusein-Zade [2]), así como los avances recientes del autor con P. Almirón [1] analizando la naturaleza de esta igualdad.</p>
        <p><strong>Referencias</strong></p>
         <p>[1] P. Almirón, J.J. Moyano Fernández (2023). The intrinsic topological nature of the Poincaré series of a plane curve singularity. Preprint, arXiv:2302.12079v2.</p>
        <p>[2] A. Campillo, F. Delgado, S.M. Gusein-Zade (2003). The Alexander polynomial of a plane curve singularity via the ring of functions on it. Duke Math. J. 117(1), 125-156.</p>
        <p>[3] F. Delgado, J.J. Moyano Fernández (2009). On the relation between the generalized Poincaré series and the Stöhr zeta function. Proc. Am. Math. Soc. 137(1), 51-59.</p>
        <p>[4] J.J. Moyano Fernández (2022). Generalized Poincaré series for plane curva singularities. In: C. Galindo et al., $p$-adic Analysis, Arithmetic and Singularities. Contemp. Math., vol. 778, 25-69. </p>
    </details>

- Delia Garijo (Universidad de Sevilla), Diámetro continuo en grafos
    <details>
        <summary>Resumen</summary>
        <p>Los <em>problemas de aumento</em> en grafos han sido ampliamente estudiados para medidas relacionadas con distancias, como el diámetro o la dilación. El objetivo en estos problemas es añadir un conjunto mínimo de aristas al grafo (o de mínimo peso) de forma que se satisfaga una condición establecida sobre el parámetro en estudio, por ejemplo, la disminución del diámetro del grafo resultante con respecto al original.
        Si se considera el lugar geométrico de la realización de un grafo en algún espacio euclídeo, surge la posibilidad de permitir que los extremos de las aristas insertadas sean, no ya vértices, sino puntos cualesquiera que estén sobre las aristas del grafo. Se pasa por tanto de considerar un número finito de distancias (entre pares de vértices) a tratar con un número infinito (entre pares de puntos de dicho lugar geométrico). Este salto de lo que llamamos la <em>versión discreta</em> del problema a la <em>versión continua</em> ha despertado mucho interés en los últimos años, no solo en problemas de aumento, sino en diversos tipos de problemas de grafos.</p>

        <p>En esta charla nos centraremos en la versión continua de problemas relacionados con el diámetro del grafo. Ilustraremos elementos que hacen muy difícil este salto "del discreto al continuo" y que provocan que los avances en esta línea de investigación estén siendo muy lentos. También plantearemos diversas cuestiones que serían interesantes de aproximar.</p>

        <p>Esta charla se enmarca en una serie de trabajos con distintos coautores: J. Cáceres (U. Almería), Fabian Klute (UPC), Alberto Márquez (U. Sevilla), Irene Parada (UPC), Rodrigo Silveira (UPC).</p>
        <p><strong>Agradecimientos</strong></p>
         <p>Financiado por MICINN a través del proyecto PID2019-104129GB-I00/MCIN/AEI/10.13039/501100011033.</p>
    </details>
