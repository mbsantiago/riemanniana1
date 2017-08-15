---
layout: post
title: Ejercicios semana 1
date: 13/08/2017
category: notas
---

Aqui están los ejercicios de la primer semana, finalmente.


## El grupo ortogonal

<ol>
    <li>
        <div class='ejercicio'>
            Recordemos que el conjunto de matrices ortogonales, $O(n)$, está definido por:
            $$
                O(n) = \left\lbrace M \in M_{n \times n}(\mathbb{R}) \mid M M^* = Id \right\rbrace
            $$
            y que $SO(n) = \left\lbrace M \in O(n) \mid \det(M) = 1 \right\rbrace$.
            <ol>
                <li> Definamos las matrices $R_\alpha$ como
                    $$
                        R(\alpha) = \begin{pmatrix}
                            \cos(\alpha) & -\sin(\alpha) \\
                            \sin(\alpha) & \cos(\alpha)
                        \end{pmatrix}
                    $$
                    y $R_y$ como
                    $$
                        R_y = \begin{pmatrix}
                            1 & 0 \\
                            0 & -1
                        \end{pmatrix}
                    $$
                    Demuestra que $R(\alpha), R_y \in O(2)$ y que $R(\alpha) \in SO(2)$ pero $R_y \notin SO(2)$.</li>
                <li> Demuestra que $R(\alpha+\beta) = R(\alpha) R(\beta)$ y $R_{0} = Id$.</li>
                <li> Demuestra que $O(2) = \left\lbrace R(\alpha) \mid \alpha \in \mathbb{R}\right\rbrace \cup \left\lbrace R_yR(\alpha) \mid \alpha \in \mathbb{R} \right\rbrace $.</li>
                <li> Demuestra que $O(2)$ es difeomorfo a $\mathbb{S}^2 \times \left\lbrace 0,1 \right\rbrace$.</li>
            </ol>
        </div>
    </li>
    <li>
        <div class='ejercicio'>
            Demuestra que $O(n)$ es una variedad diferenciable y calcula su dimensión.
        </div>
    </li>
    <li>    
        <div class='ejercicio'>[*]
            Demuestra que $SO(n)$ es conexo.    
        </div>
    </li>
</ol>

## Construcción de variedades

Los siguientes ejercicios conciernen algunas construcciones comunes y útiles para generar nuevas variedades a partir de variedades dadas.
<ol>
    <li>
        <div class='ejercicio'>
            Sean $M$ y $N$ variedades diferenciables. 
            <ol>
                <li> Sean $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^m$ y $g: V \subset \mathbb{R}^k \rightarrow \mathbb{R}^l$ dos funciones
                diferenciables. Demuestra que la función $f \times g: U \times V \subset \mathbb{R}^{n+k} \rightarrow \mathbb{R}^{m+l}$ definida
                por
                $$
                    (f \times g)(x,y) = (f(x), g(y))
                $$
                es diferenciable y calcula su diferencial. </li>
                <li> Sean $(U, \varphi_U)$ y $(V, \varphi_V)$ cartas de $M$ y $N$, respectivamente. Demuestra que $(U \times V, \varphi_U \times \varphi_V)$ es una carta. </li>
                <li> Si $\mathscr{A}_M$ y $\mathscr{A}_N$ son los atlas de $M$ y $N$ (de tipo $C^r$), demuestra que 
                $$
                    \mathscr{A} = \left\lbrace (U \times V, \varphi_U \times \varphi_V) \mid (U, \varphi_U) \in \mathscr{A}_M \text{ y } (V, \varphi_V) \in \mathscr{A}_N  \right\rbrace
                $$
                forma un atlas de tipo $C^r$ de $M \times N$. </li>
                <li> Demuestra que con el atlas del inciso anterior $M \times N$ es una variedad diferenciable para el cual las funciones, llamadas
                las proyecciones canónicas, $\pi_M, \pi_N$ definidas por $\pi_M(x,y) = x$ y $\pi(x,y) = y$, son diferenciables. </li>  
            </ol>
        </div>
    </li>
    <li>
        <div class='ejercicio'>
            Sea $M$ una variedad diferenciable y $f: M \rightarrow M$ un difeomorfismo inyectivo tal que $f^{2} = Id$.
            <ol>
                <li> Demuestra que para todo $p \in M$ existen una vecindad $U$ de $p$ tal que $f(U) \cap U = \emptyset$.
                    cartas diferenciables $(U, \varphi_U), (V, \varphi_V)$.</li>    
                <li> Definimos una relación de equivalencia $x \sim y$ si $x = f(y)$. Las clases de equivalencia, o bien el conjunto
                    obtenido de identificar $p$ con $f(p)$ es llamado
                    $$
                        M/f = \left\lbrace [p]_{\sim} \mid p \in M \right\rbrace
                    $$
                    Demuestra, usando el inciso anterior, que $M/f$ tiene una estructura diferenciable tal que la proyección canónica
                    $\pi_f: M \rightarrow M_f$, dada por $\pi_f(p) = [p]$, es diferenciable.</li>
            </ol>
        </div>
    </li>
</ol>