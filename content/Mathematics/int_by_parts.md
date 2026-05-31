# Integration by Parts


```{admonition} Connection to MTP
 Used in all chapters, with the strongest connection to Chapters 3 and 4.   
 * Chapter 3: Solving problems with Maxwell’s velocity distribution  
 * Chapter 4: The derivation of Langevin theory
```

## Theory

### Formula for integration by parts:
$
\int_{a}^b u(x) v'(x) dx= [uv]_{a}^b - \int_{a}^b u'(x) v(x) dx
$

### Video on integration by parts:
<iframe width="560" height="315" 
src="https://www.youtube.com/embed/TLVVUC0DSFM" 
frameborder="0" allowfullscreen></iframe>

## Exercises

Given that $\int_{x=-\infty}^{\infty} e^{-x^2} dx =\sqrt{\pi}$ , solve the following integrals: 

1. $\int_{x=-\infty}^{\infty} x e^{-x^2} dx$

2. $\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
3. $\int_{x=-\infty}^{\infty} x^3 e^{-x^2} dx$
4. $\int_{x=0}^{\infty} x e^{-x^2} dx$
5. $\int_{x=0}^{\infty} x^3 e^{-x^2} dx$
6. $\int_{x=0}^{\infty} x^4 e^{-x^2} dx$



## Solutions

```{dropdown} Exercise 1
$0$ 
```

```{dropdown} Exercise 2
$\frac{\sqrt{\pi}}{2}$  
```

```{dropdown} Exercise 3
$0$ 
```

```{dropdown} Exercise 4
$\frac{1}{2}$  

Choose $v(x) = e^{-x^2}$ such that $v'(x) = -2x e^{-x^2}$.  
As $u(x)v'(x) = x e^{-x^2}$, we find  $u(x) = -1/2$ and  $u'(x) = 0$.  
So, we can now write $\int_{0}^{\infty} x e^{-x^2} dx= [-1/2 e^{-x^2}]_{0}^{\infty} - \int_{0}^{\infty}  0 dx = [0 + 1/2] = 1/2$.
```

```{dropdown} Exercise 5
$\frac{1}{2}$  

Choose $v(x) = e^{-x^2}$ such that $v'(x) = -2x e^{-x^2}$.  
As $u(x)v'(x) = x^3 e^{-x^2}$, we find  $u(x) = -x^2/2$ and  $u'(x) = -x$.  
So, we can now write 
$\int_{0}^{\infty} x^3 e^{-x^2} dx= [x^2e^{-x^2}/2]_{0}^{\infty} - \int_{0}^{\infty} -x e^{-x^2} dx$.  
The first term equals zero (verify yourself).  
Hence,  $\int_{0}^{\infty} x^3 e^{-x^2} dx =  \int_{0}^{\infty} x e^{-x^2} dx$ = 1/2 (which we know from d).
```

```{dropdown} Exercise 6
$\frac{3\sqrt{\pi}}{8}$
```



## Other GUI option

```{exercise}
:label: Exercise1
$\int_{x=-\infty}^{\infty} x e^{-x^2} dx$
```
```{solution} Exercise1
:label: Solution1
:class: dropdown
$0$
```

```{exercise}
$\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
```

```{exercise}
$\int_{x=-\infty}^{\infty} x^3 e^{-x^2} dx$
```

```{exercise}
$\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
```

```{exercise}
$\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
```

```{exercise}
$\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
```