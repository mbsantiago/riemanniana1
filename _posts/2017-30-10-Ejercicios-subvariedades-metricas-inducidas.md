---
layout: post
date: 31-10-2017
title: Ejercicios - Métricas inducidas en subvariedades
category: ejercicios
---

Hola!

Aquí les dejamos los ejercicios de métricas inducidas en subvariedades. Recuerden que estos ejercicios tienen como
objetivo que repasen los temas que hemos visto de modo muy inconexo a lo largo de estas extrañas semanas. Les instamos
a que pregunten en clase, o por correo, en caso de que surgan dudas.

[version pdf]({{ site.baseurl }}/assets/ejercicios/parcial3/subvariedades.pdf)

## Ejercicios:

Recuerden que si $M$ es una variedad riemanniana entonces un subconjunto $S \subset M$ es
una subvariedad encajada si para todo $p \in S$ existe una carta $(U, \varphi_U)$ de $M$ tal
que
$$
    \varphi_U( U \cap S) \subset V \times \left\{ 0 \right\} \subset \mathbb{R}^k \times \mathbb{R}^{n-k}
$$

Recuerden también que esto le daba una estructura de variedad a $S$ usando las restricciones de
$\varphi_U$ a $S$ (y proyectando a las primeras $k$-coordenadas) para conformar un atlas.

Ahora estudiaremos el caso cuando $(M,g^M)$ es una variedad riemanniana. En todo lo que sigue,
$S$ es una subvariedad encajada de $M$ y $g^M$ es una métrica riemanniana en $M$. 

<div class='ejercicio'>
    Demuestra que la función $i: S \rightarrow M$ dada por $i(p) = p$ es diferenciable. Aquí
    nos referimos a diferenciable cuando a $S$ se le da la estructura de variedad previamente descrita.
</div>

<div class='ejercicio'>
    Para cada $p \in S$ define la función $i_p: T_pS \rightarrow T_pM$ por
    $$
        i_p(\left[ \alpha \right]) = \left[ i \circ \alpha \right]
    $$
    Demuestra que $i_p$ está bien definida y es una transformación lineal inyectiva. Traduce
    $i_p$ a la versión de derivaciones.
</div>

El ejercicio anterior muestra que podemos pensar a los vectores de $T_pS$ como vectores en $T_pM$. Luego
si tenemos un par de vectores en $T_pS$ podemos calcular su producto punto usando la métrica $g^M$.

<div class='definicion'>
    La métrica inducida en $S$ está dada por
    $$
        g^S_p(v,w) = g^M_p(i(v),i(w))
    $$
    para todo $p \in S$, $v,w \in T_pS$.
</div> 

<div class='ejercicio'>
    Demuestra que $g^S_p$ es una métrica riemanniana en $S$.
</div>

<div class='ejercicio'>
    Demuestra que para todo $p \in S$ existe una descomposición
    $$
        T_pM = iT_pS \oplus N_p
    $$
    de tal forma que $g^M_p(v,w) = 0$ para todo $v \in iT_pS$ y $w \in N_p$. Luego
    todo vector $v \in T_pM$ se pude descomponer de manera única como $v = v^T + v^N$
    donde $v^T \in iT_pS$, $v^N \in N_p$ y 
    $$
        g^M(v^T,v^N) = 0
    $$
    (La notación $v^T$ y $v^N$ hacen referencia a que son las componentes tangentes y normales a $S$ de $v$).
</div>

<div class='ejercicio'>
    Define una transformación lineal $P_p: T_pM \rightarrow T_pS$ tal que
    $i_p(P_p(v)) = v^T$. Demuestra que $Nuc(P_p) = N_p$ y que si $v,w \in iT_pS$ entonces
    $$
        g^M(v,w) = g^N(P_p(v),P_p(w))
    $$
</div>

De ahora en adelante evitaremos los subíndices $P_p$ e $i_p$ puesto que suele estar claro en el contexto
el punto de referencia. Notemos que la $P$ definida anteriormente se puede interpretar como la proyección
ortogonal de los vectores en $T_pM$ en los vectores de $T_pS$.

<div class='ejercicio'>
    Sean $X,Y \in \mathfrak{X}(S)$ y $\tilde X, \tilde Y \in \mathfrak{X}(S)$ tales que
    $\tilde X \big|_S = iX$ y $\tilde Y \big|_S = iY$. Demuestra que es posible calcular los corchetes
    de Lie en $S$ como
    $$
        [X,Y] = P([\tilde X, \tilde Y])
    $$
</div>

Sea $\nabla$ cualquier conexión en $M$. Podemos definir la conexión inducida en $S$ de la siguiente
manera

<div class='definicion'>
    La conexión inducida en $S$ está dada por
    $$
        \nabla^S_X Y = P( \nabla_{\tilde X}\tilde Y)
    $$
    donde $\tilde X$ y $\tilde Y$ son cualesquiera campos en $M$ tales que $\tilde X \big|_S = iX$
    y $\tilde Y \big|_S = iY$.
</div> 

<div class='ejercicio'>
    Demuestra que $\nabla^S$ es una conexión en $S$.
</div>

<div class='ejercicio'>
    Demuestra que si $\nabla$ es una conexión libre de torsión en $M$ entonces $\nabla^S$
    es libre de torsión.
</div>

<div class='ejercicio'>
    Demuestra que si $\nabla$ es una conexión en $M$ compatible con la métrica entonces $\nabla^S$
    es compatible con la métrica inducida $g^s$.
</div>

<div class='ejercicio'>
    Usando los últimos resultados calcula la conexión en $\mathbb{S}^n \subset \mathbb{R}^{n+1}$.
</div>