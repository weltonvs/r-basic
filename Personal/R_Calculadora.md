---
title: "R_Calculadora"
author: "Welton Vieira dos Santos"
date: "4/2/2020"
output: 
  html_document: 
    keep_md: yes
---
# Suma y Resta

```r
2 + 2
```

```
## [1] 4
```

```r
2 - 2
```

```
## [1] 0
```

```r
#Con números reales
2.5 + 2
```

```
## [1] 4.5
```

# Multiplicación

```r
2 * 4
```

```
## [1] 8
```


# División

## División Entera

```r
7 %/% 3
```

```
## [1] 2
```

## División Normal

```r
7 / 3
```

```
## [1] 2.333333
```

## Resta de una división Entera

```r
7 %% 3
```

```
## [1] 1
```


# Operadores con constantes

```r
pi
```

```
## [1] 3.141593
```

```r
2^pi
```

```
## [1] 8.824978
```

```r
pi^2
```

```
## [1] 9.869604
```

# Operador infinito y desconocido

```r
#Infinito positivo
Inf
```

```
## [1] Inf
```

```r
#Infinito negativo
-Inf
```

```
## [1] -Inf
```

```r
#Desconocido
NA
```

```
## [1] NA
```

```r
#División por cero
5/0
```

```
## [1] Inf
```

# Funciones
### Raiz cuadrada - $\sqrt{x}$

```r
x <- 3
sqrt(x)
```

```
## [1] 1.732051
```


### Exponencial - $e^x$

```r
x <- 1
exp(x)
```

```
## [1] 2.718282
```



### Logaritmo natural - $\ln{(x)}$

```r
x <- 10
log(x)
```

```
## [1] 2.302585
```


### Logarítmo base 10 - $\log_{10}{(x)}$

```r
x <- 10
log10(x)
```

```
## [1] 1
```

### Logarítmo base a - $\log_{a}(x)$

```r
x <- 1000
a <- 10
log(x,a)
```

```
## [1] 3
```

### Valor absoluto - $\begin{vmatrix}x\end{vmatrix}$

```r
x <- -10
abs(x)
```

```
## [1] 10
```

# Combinatoria

### Factorial x - $x!$

```r
x <- 4
factorial(x)
```

```
## [1] 24
```

### Coeficiente binomial - ${n}\choose{m}$
\vspace{0.2cm}

- <l class="definition">[Número factorial](https://es.wikipedia.org/wiki/Factorial).</l> Se define como número factorial de un número entero positivo $n$ como $n!=n\cdot(n-1)\cdots 2\cdot 1$
- <l class="definition">[Coeficiente binomial](https://es.wikipedia.org/wiki/Coeficiente_binomial).</l> Se define el coeficiente binomial de $n$ sobre $m$ como $$\begin{pmatrix}n\\ m\end{pmatrix}=\frac{n!}{m!(n-m)!}$$

```r
n <- 10
m <- 2
choose(n,m)
```

```
## [1] 45
```
<l class="definition">[Triángulo de Pascal](https://es.wikipedia.org/wiki/Triángulo_de_Pascal).</l>
\usepackage{mathdots}
\usepackage{yhmath}
\usepackage{mathdots}
\usepackage{MnSymbol}
$$\begin{matrix}
&&&&&1&&&&&\\
&&&&1&&1&&&&\\
&&&1&&2&&1&&&\\
&&1&&3&&3&&1&&\\
&1&&4&&6&&4&&1&\\
1&&5&&10&&10&&5&&1\end{matrix}$$
<l class="definition">[Triángulo de Pascal - Combinatoria](https://es.wikipedia.org/wiki/Triángulo_de_Pascal).</l>
$$\begin{matrix}
&&&&\begin{pmatrix}0\\0\end{pmatrix}&&&&\\
&&&\begin{pmatrix}1\\0\end{pmatrix}&&\begin{pmatrix}1\\1\end{pmatrix}&&&\\
&&\begin{pmatrix}2\\0\end{pmatrix}&&\begin{pmatrix}2\\1\end{pmatrix}&&\begin{pmatrix}2\\2\end{pmatrix}&&\\
&\begin{pmatrix}3\\0\end{pmatrix}&&\begin{pmatrix}3\\1\end{pmatrix}&&\begin{pmatrix}3\\2\end{pmatrix}&&\begin{pmatrix}3\\3\end{pmatrix}&\\
\begin{pmatrix}4\\0\end{pmatrix}&&\begin{pmatrix}4\\1\end{pmatrix}&&\begin{pmatrix}4\\2\end{pmatrix}&&\begin{pmatrix}4\\3\end{pmatrix}&&\begin{pmatrix}4\\4\end{pmatrix}\end{matrix}$$

### Trigonometría en radianes

Código |  Función                                 
--------------------|--------------------
```sin(x)``` | $\sin(x)$
```cos(x)``` | $\cos(x)$
```tan(x)``` | $\tan(x)$
```asin(x)``` | $\arcsin(x)$
```acos(x)``` | $\arccos(x)$
```atan(x)``` | $\arctan(x)$




```r
sin(pi/2)
```

```
## [1] 1
```

```r
cos(pi)
```

```
## [1] -1
```

```r
tan(0)
```

```
## [1] 0
```

## Trigonometría en radianes

<div class = "aligncenter">
![Circunferencia Goniométrica](Imgs/trigon.png)

### Cálculos con grados en R


```r
# seno de 60º
sin(60*pi/180)
```

```
## [1] 0.8660254
```

```r
# coseno de 60º
cos(60*pi/180)
```

```
## [1] 0.5
```

```r
# Función especial para no multiplicar con pi
sinpi(1/2) # = sin (pi/2)
```

```
## [1] 1
```

```r
# Representación de un número próximo a cero.
tan(pi) # -1.224647e-16 ~ 0
```

```
## [1] -1.224647e-16
```

```r
# Representación de un número muy grande - infinito
tan(pi/2) # 1.633124e+16 ~ Inf
```

```
## [1] 1.633124e+16
```

```r
# Arco sin en radianes
asin(0.8660254) #arc sin en radianes
```

```
## [1] 1.047198
```

```r
# Arco sin en grados
asin(0.8660254) * 180 /pi #arc sin en grados
```

```
## [1] 60
```

```r
# Esta fuera de rango, ya que esta acotado entre -1 y 1
asin(5) #arc sin x in [-1,1]
```

```
## Warning in asin(5): Se han producido NaNs
```

```
## [1] NaN
```

```r
# No permite números negativos
acos(-8)
```

```
## Warning in acos(-8): Se han producido NaNs
```

```
## [1] NaN
```

## Números en coma flotante

Código |  Función                                 
-------|--------------------
```print(x,n)``` | Muestra las $n$ cifras significativa del número $x$
```round(x,n)``` | Redondea a $n$ cifras significativas un resultado o vector numérico $x$
```floor(x)``` | $\lfloor x\rfloor$, parte entera por defecto de $x$
```ceiling(x)``` | $\lceil x\rceil$, parte entera por exceso de $x$
```trunc(x)``` | Parte entera de $x$, eliminando la parte decimal

#### Ejemplos:
1. Quiero calcular $\sqrt{2}$

```r
sqrt(2)
```

```
## [1] 1.414214
```
2. Quero calcular $\sqrt{2}$, pero con 10 cifras significativas

```r
print(sqrt(2),10)
```

```
## [1] 1.414213562
```

3. Quero calcular $\sqrt{2}$, pero redondear a 3 cifras significativas

```r
round(sqrt(2),3)
```

```
## [1] 1.414
```

4. Quero calcular $\sqrt{2}$, pero redondear hacia abajo (suelo)

```r
floor(sqrt(2))
```

```
## [1] 1
```


5. Quero calcular $\sqrt{2}$, pero redondear hacia arriba (techo)

```r
ceiling(sqrt(2))
```

```
## [1] 2
```

6. Quero calcular $\sqrt{2}$, pero redondear con la función trunc

```r
trunc(sqrt(2))
```

```
## [1] 1
```

