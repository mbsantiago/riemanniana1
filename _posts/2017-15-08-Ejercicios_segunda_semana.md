---
layout: post
title: Ejercicios semana 2
date: 15/08/2017
category: notas
---

Los ejercicios de la semana 2, hasta ahora


## Espacios tangentes en $\mathbb{R}^n$

<ol>
    <li>
            Recordemos la definición de espacio tangente en $\mathbb{R}^n$ que manejamos en la clase:
 Dado $p \in \mathbb{R}^n$ definimos el conjunto 
$$T_p\mathbb{R}^n:= \left\{\gamma \middle | \gamma :(-\epsilon, \epsilon)\rightarrow \mathbb{R}^n, \gamma(0)=p \right\}/\sim_p$$
donde $\gamma_1 \sim_p \gamma_2$ cuando  $\dot{\gamma}_1(0)=\dot{\gamma}_2(0)$. Definimos además las operaciones siguientes:
$[\gamma_1]+[\gamma_2]:=[\psi]$ donde $\psi(t):=\gamma_1(t) +\gamma_2(t) -p$ y definimos $\lambda [\gamma]:=[\psi]$ con $\psi(t):= \lambda(\gamma(t)-p)+p$.
<ol>
<li> Demuestra que las operaciones antes mencionadas están bien definidas.</li>
<li> Demuestra que $T_p\mathbb{R}^n$ con las operaciones arriba definidas es un espacio vectorial.</li>
<li> Sea $\gamma_i$ la curva dada por $\gamma_i(t):= p+ t  \hat{e_i}$. Demuestra que los vectores $[\gamma_i]\in T_p\mathbb{R}^n$
forman una base.
</li>
</ol></li>
<li> Define la noción de espacio tangente en $p$ a la esfera unitaria $\mathbb{S}^n\subseteq \mathbb{R}^{n+1}$ a partir del conjunto
$\left\{\gamma \middle | \gamma:(-\epsilon,\epsilon)\rightarrow \mathbb{S}^n, \gamma(0)=p \right\}$. En particular
define la suma de vectores y el producto por un escalar. Finalmente demuestra que $T_p\mathbb{S}^n$ se puede identificar canónicamente
con el subespacio vectorial $perp(p):=\{x\in \mathbb{R}^n| \langle x,p\rangle=0\}$</li>
<li>
Análogamente, define la noción de espacio tangente a una subvariedad.


</li>
</ol>
Una referencia útil para estos ejercicios puede ser el capítulo 2 de *Introduction to differential topology* de Bröcker y Jänich.
