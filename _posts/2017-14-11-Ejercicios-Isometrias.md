---
layout: post
date: 14-11-2017
title: Ejercicios - Isometrías
category: ejercicios
---

Los ejercicios de esta semana conformarán un breve estudio de las isometrías. No solo se les recomienda
hacer lo ejercicios como práctica para asentar conceptos y técnicas, sino que su contenido es de gran
relevancia a la teoría.

versión [pdf]({{ site.baseurl }}/assets/ejercicios/parcial3/isometrias.pdf )

## Isometrías

<div class='definicion'>
    Una difeomorfismo $f: M \rightarrow N$ entre variedades riemannianas $(M, g^M)$ y $(N, g^N)$ es una isometría si para todo $p \in M$ y todo par de vectores tangentes $v,w \in T_pM$ se satisface
    $$
        g^N(Df_p(v), Df_p(w)) = g^M(v,w)
    $$
</div> 

<div class='definicion'>
    Si $f: M \rightarrow N$ es un difeomorfismo y $X \in \mathfrak{X}(M)$ es un campo vectorial, entonces $f$ induce un campo en $N$
    llamado el push-foward de $X$, denotado por $f_*(X)$ y definido por
    $$
        f_*(X)_{f(p)} = Df_p(X_p)
    $$
</div> 

<div class='ejercicio'>
    Demuestra que si $X \in \mathfrak{X}(M)$ entonces $f_*(X) \in \mathfrak{X}(N)$
</div>


<div class='ejercicio'>
    Demuestra que si $X,Y \in \mathfrak{X}(M)$ entonces
    $$
        f_*([X,Y]) = [f_*(X), f_*(Y)]
    $$
</div>

En los ejercicios que siguen vamos ver que efecto tienen las isometrías en la derivada de los campos. En todo lo que sigue $f: M \rightarrow N$ es un difeomorfismo y $\nabla^N$ es una conexión en $N$.

<div class='ejercicio'>
    Define $\nabla^M: \mathfrak{X}(M) \times \mathfrak{X}(M) \rightarrow \mathfrak{X}(M)$ como
    $$
        \nabla^M_{X} Y = \nabla^N_{f_*(X)}f_*(Y)
    $$
    Demuestra que $\nabla^M$ es una conexión en $M$. Esta llamada el pull-back de $\nabla^N$ a lo largo de $f$.
</div>

<div class='ejercicio'>
    Demuestra que si $\nabla^N$ es una conexión libre de torsión entonces $\nabla^M$ es libre de torsión.
</div>

<div class='ejercicio'>
    Demuestra que si $f$ es una isometría y $\nabla^N$ es compatible con la métrica, entonces $\nabla^M$ es compatible con la métrica.
</div>

<div class='ejercicio'>
    Demuestra que si $f$ es una isometría y $\nabla^N$ es la conexión de Levi-Civita de $N$ entonces $\nabla^M$ es la conexión de Levi-Civita de $M$.
</div>

<div class='ejercicio'>
    Concluye que si $f: M \rightarrow M$ es una isometría y $X,Y \in \mathfrak{X}(M)$ entonces
    $$
        f_*(\nabla_{X}Y) = \nabla_{f_*(X)}f_*(Y)
    $$
</div>

<div class='ejercicio'>
    Sea $\alpha: I \rightarrow M$ una curva diferenciable y $\beta = f \circ \alpha$ la curva imagen. Sea $X \in \mathfrak{X}(M)$ un campo
    a lo largo de $\alpha$ y $f_*(X)$ el campo a lo largo de $\beta$ definido por $f_*(X)(t) = Df_{\alpha(t)}(X(t))$. Si $D^\alpha$ y $D^{\beta}$ denotan las derivadas covariantes a lo largo de $\alpha$ y $\beta$, respectivamente, y $f$ es una isometría, demuestra que
    $$
        f_*(D^{\alpha}X) = D^{\beta} f_*(X)
    $$
</div>

<div class='ejercicio'>
    Demuestra que si $f$ es una isometría y $\gamma: I \rightarrow M$ es una geodésica entonces $f \circ \gamma$ es una geodésica.
</div>

<div class='ejercicio'>
    Demuestra que si $p \in M$, $v \in T_pM$ y $f$ es una isometría entonces $f(exp_p(v)) = exp_{f(p)}(Df_p(v))$.
</div>

<div class='ejercicio'>[2Pts]
    Demuestra que si $M$ es conexo y $f,g: M \rightarrow N$ son un par de isometrías tales que $f(p)=g(p)$ y $Df_p = Dg_p$ entonces
    $f=g$. Es decir que las isometrías están determinadas por su valor y su diferencial en un punto.
</div>