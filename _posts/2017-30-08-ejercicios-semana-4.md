---
layout: post
date: 30-08-2017
title: Ejercicios Semana IV
category: ejercicios
---

Les dejamos aquí los ejercicios de la cuarta semana. Les recordamos que pueden ver los ejercicios del parcial en el [pdf]({{ site.baseurl }}/assets/ejercicios/parcial1/ejercicios_parcial1.pdf).

## Haces vectoriales, campos vectoriales y formas diferenciales

<div class='ejercicio'>
Sea $M$ una variedad diferenciable de dimensión $n$. Sea $(U,\phi)$ una carta de $M$.
Denotemos por $ x_i$ a las coordenadas de la función $\phi$, es decir, $\phi(p)= (x_1(p), \ldots, x_n(p))$.

Sea $ \gamma_i(t) $ la curva que pasa por $ p$ dada por $ \gamma_i(t)= \phi^{-1}(\phi(p) +t\hat{e}_i)$
y sea $ \frac \partial {\partial x_i}(p):=[\gamma_i]\in T_pM$ el vector tangente a $ p$ determinado por $ \gamma_i$


<ol>
    <li> Demuestra que $ \{\frac \partial {\partial x_i}(p) \}_{i=1}^n$ es una base de $ T_pM$.</li>  
    <li> Denotemos por $ \{dx_i(p)\}_{i=1}^n$ a la base dual de $ T_p^*M$, dual a la base $ \{\frac \partial {\partial x_i}(p) \}_{i=1}^n$. Demuestra que $ d(x_i)(p)= dx_i(p)$ es decir, la derivada exterior de la función $ x_i$ es igual a el dual de $ \frac \partial {\partial x_i}(p)$.</li>
    <li> Sea $ f:M\rightarrow \mathbb{R}$ una función diferenciable sobre $ M$. Demuestra que $ d(f)(p)=\sum_{i=1}^n\frac \partial {\partial x_i}(p)(f)  dx_i$ donde $ \frac \partial {\partial x_i}(p)(f)$ es la derivación asociada al vector $ \frac \partial {\partial x_i }(p)$ aplicada a la función $ f$.</li>
<li> Sean $ f,g\in C^\infty(M)$. Demuestra que $ d(fg)=d(f)g+fd(g)$.</li>
    </ol>
</div>

<div class='ejercicio'>
    Sean $\partial_i$ los campos vectoriales (en el sentido de derivaciones) dados por
    $$
        (\partial_i)_p(g)= \frac{\partial g}{\partial x_i}(p) 
    $$
    <ol>
        <li> Demuestra que $\partial_i$ es un campo vectorial diferenciable en $\mathbb{R}^n$.</li>
         <li> Recuerda que $\Psi_p: T_p \mathbb{R}^n \rightarrow \mathscr{D}_p$ dado por $\Psi_p([\alpha])(g) = (g \circ \alpha)'(0)$ es un
            isomorfismo de espacios vectoriales. Demuestra que $\Psi_p(\frac{\partial}{\partial x_i}(p)) = (\partial_i)_p$, donde $\frac{\partial}{\partial x_i} = [\alpha_i]$ con $\alpha_i(t) = p + te_i$.</li>
        <li> Sea $X$ un campo vectorial en $\mathbb{R}^n$ (esto es, una derivación $X_p$ en $p$, para cada $p \in \mathbb{R}^n$). Recuerda que demostramos que $\left\{ (\partial_i)_p \right\}_{i=1}^n$ es una base de las derivaciones en $p$ (i.e. $\mathscr{D}_p$) por lo que para cada $p \in \mathbb{R}^n$ podemos expresar a $X_p$ en esta base. Así, existen números $a^i(p) \in \mathbb{R}$ tales que
            $$
                X_p = \sum_{i=1}^n a^i(p) (\partial_i)_p
            $$
            Estos números, al variar de punto a punto, forman funciones $a_i: \mathbb{R}^n \rightarrow \mathbb{R}$. Demuestra que
            $X$ es un campo vectorial diferenciable si y sólo si las funciones $\left\{ a_i \right\}_{i=1}^n$ son diferenciables.</li>
        <li> Sea $X$ un campo vectorial en la variedad $M$. Demuestra que $X$ es diferenciable si y sólo si para todo $p \in M$
            existe carta $(U,\varphi_U)$ alrededor de $p$ tal que $D\varphi_U(X)$ es un campo diferenciable en $\varphi_U(U) \subset \mathbb{R}^n$ en el sentido del inciso anterior.</li>
    </ol>

</div>