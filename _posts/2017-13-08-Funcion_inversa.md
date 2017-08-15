---
layout: post
title: Teorema de la función inversa
date: 13/08/2017
category: notas
---

## Cálculo
Tomemos un momento para recordar algunos de los contenidos de cálculo.

Sea $U$ un abierto de $\mathbb{R}^n$.
<div class='definicion'>
Una función $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^m$ es diferenciable en $p \in U$ si existe una
transformación lineal $T: \mathbb{R}^n \rightarrow \mathbb{R}^m$ tal que la transformación afín $A: \mathbb{R}^n \rightarrow 
\mathbb{R}^m$ dada por $A(q) = f(p) + T(q-p)$ es una buena aproximación a $f$ en $p$. Esto es
$$
    \lim_{h \to 0} \frac{\| f(p+h) - A(p+h) \| }{\| h \|} = 0
$$
Si existe tal transformación es única, por lo que podemos denotarla por $Df_p$.
Decimos que $f$ es diferenciable, si es diferenciable en $p$ para todo $p \in U$.
</div>

Esta transformación lineal provee la información de como la función transforma direcciones en el siguiente sentido: 

Sea $\alpha: I \rightarrow \mathbb{R}^n$ una trayectoria diferenciable con $\alpha(0) = p$. La trayectoria tiene un dirección infinitesimal
en $p$ dada por el vector $v = \alpha'(0)$. Al transformar el espacio con $f$, la trayectoria se convierte en una nueva curva $\beta = 
f \circ \alpha: I \rightarrow \mathbb{R}^m$. Esta nueva curva tiene una dirección infinitesimal en $f(p)$ dada por $\beta'(0)$.

<div class='proposicion'>
Si $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^m$ es diferenciable en $p \in U$ y $\alpha: I \rightarrow \mathbb{R}^n$
es una curva diferenciable con $\alpha(0) = p$ entonces la curva $\beta = f \circ \alpha$ tiene como vector tangente en $0$
a
$$
    \beta'(0) = Df_p(\alpha'(0))
$$
</div>

<div class='prueba'>
Es una consecuencia de la regla de la cadena.
</div>

De este modo es más claro el enunciado del teorema de la regla de la cadena, puesto que una curva $\alpha$ es deformada
por una composición $f \circ g$ en pasos, cargando la dirección infinitesimal de $\alpha$ primero a través de la deformación
de $g$ y después la de $f$.

<div class='teorema'> 
**Regla de la cadena**
Sea $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^m$ y $g: V \subset \mathbb{R}^m \rightarrow \mathbb{R}^q$. Si
$f$ es diferenciable en $p \in U$ y $g$ es diferenciable en $f(p) \in V$, entonces $(g \circ f)$ es diferenciable en $p$
y
$$
    D(g \circ f)_{p} = Dg_{f(p)} \circ Df_p
$$
</div>

La definición de derivada de una función multidimensional no deja en claro el método para calcularla. Sin embargo, en el caso en 
que la función $f$ tenga derivadas parciales y sus derivadas parciales sean continuas, es decir que la
función sea tipo $C^1$, entonces es fácil calcular la diferencial de $f$ en $p$. Simplemente está dada por

$$
Df_p = \begin{pmatrix}
    \frac{\partial f_1}{\partial x_1}(p) & \cdots & \frac{\partial f_1}{\partial x_n}(p) \\
    \vdots & \ddots & \vdots \\
    \frac{\partial f_m}{\partial x_1}(p) & \cdots & \frac{\partial f_m}{\partial x_n}(p)
\end{pmatrix} = \frac{\partial (f_1,\cdots,f_m)}{\partial (x_1,\cdots,x_n)}(p)
$$

La interepretación que hemos dado a la diferencial, como la representación del modo en que la función $f$ transforma las
direcciones infinitesimales, ayuda a visualizar geométricamente ciertas situaciones. Por ejemplo, si $\|Df_p(v)\| \geq \| v\|$
esto indica que la función estira el espacio en la dirección de $v$, o bien que si $\alpha$ es una curva con dirección
infinitesimal $v$ en $p$, entonces $f$ estira a $\alpha$ al menos cerca de $p$. También parece sugerir que si $ Df_p(v)  = 0$, entonces $f$
colapsa a un solo punto curvas que tienen a $v$ como dirección infinitesimal en $p$. Aunque en cierto modo el enunciado anterior
es correcto a escalas infinitesimales, no resulta cierto como lo demuestra cualquier curva no constante con tangente cero en algún punto.

Sin embargo, ofrece un poco de justificación e intuición para el siguiente importante teorema

<div class='teorema'>
**Teorema de la función inversa**
Sea $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^n$ una función de tipo $C^1$, con $U$ abierto. Si $p$ es tal que
$Df_p: \mathbb{R}^n \rightarrow \mathbb{R}^n$ es un isomorfismo lineal, entonces $f$ es localmente invertible en $p$. Esto es:
existe una vecindad $p \in V \subset U$ abierta tal que $f\Big|_V$ es biyectiva y $f\Big|_V^{-1}$ es de tipo $C^1$.
</div>

La demostración se puede ver en \cite{spivak_calculus, rudin}.

Otra manera de enunciar el teorema de la función inversa es que si
la diferencial es invertible en $p$ entonces $f$ es invertible cerca a $p$. Esto es, la diferencial, como aproximación lineal, es tan
buena cerca a $p$ que le ``hereda'' la propiedad de ser invertible.

En términos prácticos, la condición de ser un isomorfismo se puede traducir en cualquiera de las siguientes condiciones:

1. $Df_p$ es inyectiva.
2. El núcleo de $Df_p$ es trivial.
3. $Det(Df_p) \neq 0$.
4. Los gradientes $\nabla f_1(p), \cdots, \nabla f_n(p)$ son linealmente independientes.


## Coordenadas locales y representaciones locales de funciones

Desde el punto de vista de la topología diferencial, cualesquiera dos sistemas coordenados son equivalentes, y para analizar el
comportamiento de una función se permite elegir arbitrariamente un sistema coordenado. 


<div class='definicion'>
Sea $f: M \rightarrow N$ una función diferenciable. Si $(U,\varphi_U)$ y $(V, \varphi_V)$ son cartas de $M$ y $N$ respectivamente
tales que $p \in U$ y $f(p) \in V$ entonces la función $\tilde f: \varphi_U( U \cap f^{-1}V) \subset \mathbb{R}^n \rightarrow \varphi_V(V \cap f(U)) \subset \mathbb{R}^m$
$$
    \tilde f = \varphi_V \circ f \circ \varphi_U^{-1}
$$
es llamada una representación coordenada de $f$ cerca de $p$.
</div>

Esta idea la podemos aplicar a las funciones $f: \mathbb{R}^n \rightarrow \mathbb{R}^m$, puesto que $\mathbb{R}^n$ y $\mathbb{R}^m$ son
variedades. Y dado que toda variedad es localmente equivalente a $\mathbb{R}^n$ basta con estudiar este caso. Así la pregunta se
convierte en la siguiente: ¿Qué coordenadas son útiles para analizar una función diferenciable? ¿Cuantos comportamientos distintos puede
tener una función diferenciable si se permiten cambios de coordenadas?

El teorema de la función inversa ofrece la respuesta en el caso en el cual la diferencial es invertible.

<div class='proposicion'>
Si $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^n$ es $C^1$ y en $p \in U$ la diferencial $Df_p$ es invertible, entonces existe una representación coordenada
de $f$ cerca de $p$ tal que
$$
    \tilde f(x) = x
$$
</div>

<div class='prueba'>
Demostrar que existe semejante representación coordenada exige encontrar las cartas para las que se da dicha representación.

Por el teorema de la función inversa existe $V \subset U$ abierto tal que $f|_V$ es invertible con inversa $C^1$. Para simplificar
la notación llamemos $g=f|_V$. Notemos que $g: V \rightarrow f(V)$
es una parametrización o bien $g^{-1}: f(V) \rightarrow V$ es una carta. También $(V, Id)$ es un carta, donde $Id$ es la función
identidad ($Id(x) = x$). Con estas dos cartas, $(V,Id)$ y $(f(V), g^{-1})$, se obtiene una representación coordenada de $f$ dada
por
$$
    \tilde f = g^{-1} \circ f \circ Id^{-1} = (f|_V)^{-1} \circ f = Id
$$
y luego $\tilde f(x) = x$.
</div>

El teorema anterior nos dice que todo par de funciones con diferenciales invertibles son localmente equivalente (al menos
bajo cambio de coordenadas). La situación cuando la diferencial no es invertible es mucho más interesante y complicada. Los puntos donde
la función tiene diferencial no invertible, y de modo más general no tiene rango máximo, son llamados singularidades o puntos singulares. El estudio y la
clasificación de dichas singularidades forman una rama amplia y fértil a la cual no entraremos en detalle. Para el interesado le sugerimos
el libro \cite{stable_mappings}.

<div class='proposicion'>
Sea $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^m$ una función de tipo $C^1$. Decimos que $p$ es un punto regular
si $Df_p$ tiene rango máximo.
</div>

Lo que hemos probado hasta ahora es que si $p$ es un punto regular de una función $f: \mathbb{R}^n \rightarrow \mathbb{R}^m$ con $n = m$
entonces tiene una representación sencilla. Pero ¿qué ocurre en los otros casos, cuando las dimensiones son distintas?

Podemos inspirarnos un poco en el teorema de la función inversa y suponer que la diferencial $Df_p$ es un buen sustituto de la función
$f$ cerca a $p$. Dado que $Df_p: \mathbb{R}^n \rightarrow \mathbb{R}^m$ es una transformación lineal de rango máximo esto quiere decir
que


1. Si $n > m$ entonces $Df_p$ es suprayectiva y existen bases $\left\lbrace e_1,\cdots, e_n \right\rbrace$ y $\left\lbrace l_1, \cdots, l_m \right\rbrace$ de $\mathbb{R}^n$ y $\mathbb{R}^m$, respectivamente, tales que 

    $$
        Df_p(e_i) = \begin{cases} l_i & i \leq m \\
            0 & i > m
        \end{cases}
    $$

2. Si $n < m$ entonces $Df_p$ es inyectiva y existen bases $\left\lbrace e_1, \cdots, e_n \right\rbrace$ y $\left\lbrace l_1, \cdots, l_m \right\rbrace$ de $\mathbb{R}^n$ y $\mathbb{R}^m$, tales que

    $$
        Df_p(e_i) = l_i
    $$



Un cambio de bases es también un cambio de coordenadas de tipo lineal.
<div class='teorema'>
**Teorema de la inmersión**
Sea $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^m$, $U$ abierto, una función de tipo $C^1$ con $n < m$. Si $p \in U$
es un punto regular de $f$, es decir $Df_p$ es de rango máximo (inyectiva), entonces existe una representación coordenada
de $f$ cerca de $p$ tal que
$$
    \tilde f(x_1,\cdots,x_n) = (x_1,\cdots, x_n, 0, \cdots, 0)
$$
</div>

<div class='prueba'>
De nuevo debemos de encontrar cartas cerca de $p$ y $f(p)$ para las cuales $f$ tiene la representación mencionada.

En primer lugar $Df_p$ tiene rango máximo, o equivalentemente la matriz
$$
    Df_p = \begin{pmatrix}
        \frac{\partial f_1}{\partial x_1}(p) & \cdots & \frac{\partial f_1}{\partial x_n}(p) \\
        \vdots & \ddots & \vdots \\
        \frac{\partial f_m}{\partial x_1}(p) & \cdots & \frac{\partial f_m}{\partial x_n}(p)
    \end{pmatrix}
$$
tiene rango máximo. Esto implica que hay un subconjunto de índices $\left\lbrace i_1, \cdots, i_n \right\rbrace \subset \left\lbrace 1, \cdots, m \right\rbrace$ tales que la matriz
cuadrada
$$
    \frac{\partial (f_{i_1},\cdots,f_{i_n})}{\partial (x_1,\cdots,x_n)}
$$
tiene determinante no nulo.

Podemos suponer sin perdida de generalidad que $i_j = j$ (es decir $f_{i_1} = f_1, \cdots, f_{i_n} = f_n$). De no ser así,
podemos modificar a $f$ con una tranformación lineal invertible adecuada $L$ en la función $g = L \circ f$ que sí satisface
que $i_j = j$, y además se puede probar que si el teorema es cierto para $g$ entonces es cierto para $f$ [Ejercicio: Encontrar $L$
y justificar la última afirmación]. 

Ahora consideremos la siguiente función $h: U \times \mathbb{R}^{m-n} \rightarrow \mathbb{R}^m$ dada por
$$
    h(x,y) = f(x) + (0,y) 
$$

Notemos que esta función satisface que $h(x,0) = f(x)$ y además
$$
    Dh_{(p,0)} = \begin{pmatrix}
        \frac{\partial (f_1,\cdots,f_n)}{\partial (x_1,\cdots,x_n)}(p) & 0 \\
        \frac{\partial (f_{n+1}, \cdots, f_m)}{\partial (x_1,\cdots,x_n)}(p) & Id_{m-n}
    \end{pmatrix}
$$

Esta matriz tiene como determinante $Det(Dh_{(p,0)}) = Det\left(\frac{\partial (f_1,\cdot, f_n)}{\partial (x_1,\cdots, x_n)}(p)\right)$ 
[Ejercicio] el cual es no nulo por (\ref{eq:3}). Esto es, la función $h$ es regular en el punto $p$ por lo que existe una vecindad $W$ de $(p,0)$
tal que $h$ es un difeomorfismo en $W$.

La función transforma un pequeño abierto de $\mathbb{R}^m$, que contiene $(p,0)$ a una vecindad de $h(p,0) = f(p)$. Luego podemos
usar $(h(W), h^{-1})$ como una carta alrededor de $f(p)$. Esta carta alrededor de la imagen, junto con la carta trivial $(U,Id)$
alrededor de $p$ dan lugar a la representación coordenada $\tilde f = h^{-1} \circ f \circ Id$. Sea $x \in U$ suficientemente
cercano a $p$ [Exercicio: ¿Qué tanto es suficiente?] y notemos
que $h(x,0) = f(x)$ por lo que $\tilde f = h^{-1}(f(x)) = (x,0)$.
</div>

Y para el caso de $n > m$:
<div class='teorema'>
**Teorema de la sumersión**
Sea $f: U \subset \mathbb{R}^n \rightarrow \mathbb{R}^m$, $U$ abierto, una función de tipo $C^1$ con $m < n$. Si $p \in U$
es un punto regular de $f$, es decir $Df_p$ es de rango máximo (suprayectiva), entonces existe una representación coordenada
de $f$ cerca de $p$ tal que
$$
    \tilde f(x_1,\cdots,x_n) = (x_1,\cdots, x_m)
$$
</div>

<div class='prueba'>
En este caso el hecho de que la matriz
$$
    \frac{\partial (f_1,\cdots,f_m)}{\partial (x_1,\cdots,x_n)}
$$
tenga rango máximo implica que existe un subconjunto de índices $\left\lbrace i_1,\cdots, i_m \right\rbrace \subset \left\lbrace 1,\cdots, n \right\rbrace$
tales que
$$
    Det\left(  \frac{\partial (f_1,\cdots,f_m)}{\partial (x_{i_1},\cdots,x_{i_m})} \right) \neq 0
$$

De nuevo, podemos suponer sin perdida de generalidad que $i_1=1, \cdots, i_m = m$ [Ejercicio: En este caso hay que encontrar $L$
tal que $g = f \circ L$ tiene las propiedades deseadas, y verificar que si el teorema es válido para $g$ entonces lo es para $f$].
Podemos también asumir que $p = 0$ [Ejercicio: ¿Por qué?].

Sea $h: \mathbb{R}^m \times \mathbb{R}^{n-m} \cap U \rightarrow \mathbb{R}^m \times \mathbb{R}^{m-n}$ la función dada por
$$
    h(x,y) = (f(x,y),y) = (f(x,y),0) + (0, y)
$$

Notemos que $h(0) = (f(0), 0)$ y que la diferecial de $h$ en $0$ está dada por
$$
    Dh_0 = \begin{pmatrix}
        \frac{\partial (f_1,\cdots,f_m)}{\partial (x_1,\cdots,x_m)}(0) & \frac{\partial (f_1,\cdots,f_m)}{\partial (x_{m+1},\cdots,x_n)}(0) \\
        0 & Id_{m-n}
    \end{pmatrix}
$$
que tiene determinante $Det\left( Dh_0 \right) = Det\left( \frac{\partial (f_1,\cdots,f_m)}{\partial (x_1,\cdots,x_m)} \right) \neq 0$.

Por el teorema de la función inversa existe una vecindad $W \subset U$ tal que $0 \in W$ y $h$ es un difeomorfismo en $W$. Podemos
usar $(W, h)$ como una carta alrededor de $0$ y la carta trivial alrededor de $f(0)$ para obtener una representación coordenada de
$f$ dada por
$$
    \tilde f = Id \circ f \circ h^{-1}
$$
Si $(x,y) \in h(W)$ entonces quiere decir que $(x,y) = (f(z,y),y)$ para algún $(z,y) \in W$. Luego $x = f(z,y)$ y $(z,y) = h^{-1}(x,y)$, de donde se sigue que $\tilde(x,y) = f \circ h^{-1}(x,y) = x$.
</div>

<div class='ejercicio'>
Demuestra el teorema de la función implícita usando el teorema de la sumersión:
Sea $f: U \subset \mathbb{R}^n \times \mathbb{R}^m \rightarrow \mathbb{R}^n$ una función de tipo $C^1$. Si $p \in U$ es tal que
$Det\left(\frac{\partial (f_1,\cdots,f_n)}{\partial (x_1,\cdots,x_n)}\right) \neq 0$ y $f(p) = 0$ entonces existe una función $g:V \subset \mathbb{R}^n \rightarrow \mathbb{R}^m$ de tipo $C^1$, con $V$ abierto, tal que
$$
    f(x,g(x)) = 0
$$
</div>
