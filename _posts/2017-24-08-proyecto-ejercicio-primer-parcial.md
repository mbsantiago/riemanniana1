---
layout: post
date: 24-08-2017
title: proyecto-tarea parcial 1
category: proyectos
permalink: proyecto1
---

Este parcial no habrá proyecto. Sin embargo, con el fin de motivar el trabajo continuo del alumno, hemos decidido que este parcial los ejercicios que pueden ver en este [pdf]({{ site.baseurl }}/assets/proyectos/parcial1.pdf), o que vienen a continuación, fungirán como proyecto.

Esto es, si entregan los ejercicios antes del día del exámen tienen derecho a un examen corto (mitad de los ejercicios). Si lo entregan la calificación de su parcial será 50% lo que obtengan en los ejercicios (también serán evaluados) y 50% de lo que obtengan en el exámen. Es por esto que si desean entregarlos sería mejor estar seguros de que está bien. Por lo mismo estaremos dando retroalimentación a los ejercicios hasta el miércoles 30 de agosto. Es decir, si lo entregan hasta la clase del miércoles, nosotros les daremos los ejercicios calificados lo más pronto posible y ustedes podrán corregir sus escritos para hacer una nueva entrega.

Creemos que vale la pena asegurarse el 50% de la calificación parcial usando este método que reduce bastante la incertidumbre (siempre y cuando consigan retroalimentación).

# Ejercicios

Recuerden que definimos una subvariedad encajada de $\mathbb{R}^n$ de la siguiente manera

<div class='definicion'>
    Un subconjunto $A \subset \mathbb{R}^n$ es una subvariedad (de tipo $C^r$) de dimensión $m$ si para todo $p \in A$ existe
    un abierto $U \subset \mathbb{R}^n$ que contiene a $p$, junto con una carta (cambio de coordenadas) $\varphi: U \rightarrow \mathbb{R}^m \times \mathbb{R}^{n-m}$ (de tipo $C^r$) tal que 
    $$
        \varphi(A \cap U) \subset \mathbb{R}^m \times {0}
    $$
    esto es, salvo cambio de coordenadas, el pedazo de $A$ en $U$ es un pedazo de subplano de dimensión $m$ en $\mathbb{R}^n$.
</div>

<div class='ejercicio'>
    Demuestra que si $A$ es una subvariedad encajada, entonces $A$ es una variedad como lo definimos en las <a href="{{ site.baseurl }}/assets/notas/parcial1/introduccion_a_variedades.pdf"> notas de variedades </a>. Es preciso dar cartas y demostrar que los cambios de coordenada son diferenciables.
</div>

<div class='ejercicio'>
    Sea $A \subset \mathbb{R}^n$ una subvariedad encajada de dimensión $m$. Sea $\alpha: I \rightarrow A$ una trayectoria continua, con $I$ un intervalo abierto de $\mathbb{R}$. Demuestra que $\alpha$ es diferenciable en el sentido de variedades (con la estructura diferenciable definida en el ejercicio anterior) si y solo si es diferenciable como función
    $\alpha: I \rightarrow A \subset \mathbb{R}^n$.
</div>

<div class='ejercicio'>
Demuestra que el toro
    $$
        T = \left\{ (2 \cos(\theta) + \cos(\varphi)  \cos(\theta), 2 \sin(\theta) + \cos(\varphi) \sin(\theta), \sin(\varphi)) \mid \theta, \varphi \in [0, 2\pi] \right\}
    $$
    es una subvariedad encajada de $\mathbb{R}^3$.
</div>

[Notas de subvariedades]({{ site.baseurl }}/assets/notas/parcial1/subvariedades.pdf)
