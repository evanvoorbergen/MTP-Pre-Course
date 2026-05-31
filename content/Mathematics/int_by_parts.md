# Integration by Parts


```{admonition} Connection to MTP
 Used in all chapters, but strongest connection is to chapters 3 and 4. The derivation of langevin theory requires both of these concepts, and solving problems that make use of Maxwell’s velocity distribution usually requires integration by parts.
```

## Theory

Formula for integration by parts:
$$
\int_{a}^b u(x) v'(x) dx= [uv|_{a}^b - \int_{a}^b u'(x) v(x) dx
$$ (intbyparts)

Video on integration by parts:
```{iframe} https://www.youtube.com/watch?v=TLVVUC0DSFM
:width: 100%
```

## Exercises

Given that $\int_{x=-\infty}^{\infty} e^{-x^2} dx =\sqrt{\pi}$ solve the following integrals (hint: use integration by parts) : 
\def\labelenumi{\alph{enumi})}
1. $\int_{x=-\infty}^{\infty} x e^{-x^2} dx$
1. $\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
1. $\int_{x=-\infty}^{\infty} x^3 e^{-x^2} dx$
1. $\int_{x=0}^{\infty} x e^{-x^2} dx$
1. $\int_{x=0}^{\infty} x^3 e^{-x^2} dx$
1. $\int_{x=0}^{\infty} x^4 e^{-x^2} dx$

## Exercise Solutions
a) $0$  
b) $\sqrt{\pi}/2$  
c) $0$  
d) $1/2$  
Choose $v(x) = e^{-x^2}$ such that $v'(x) = -2x e^{-x^2}$. As $u(x)v'(x) = x e^{-x^2}$, we find  $u(x) = -1/2$ and  $u'(x) = 0$. So, we can now write 
$\int_{0}^{\infty} x e^{-x^2} dx= [ -1/2 e^{-x^2}|_{0}^{\infty} - \int_{0}^{\infty}  0 dx = [0 + 1/2] = 1/2$.
e) $1/2$  
f) $3\sqrt{\pi}/8$.  

Derivation d)  \\ \\
Derivation e) Choose $v(x) = e^{-x^2}$ such that $v'(x) = -2x e^{-x^2}$. As $u(x)v'(x) = x^3 e^{-x^2}$, we find  $u(x) = -x^2/2$ and  $u'(x) = -x$. So, we can now write 
$\int_{0}^{\infty} x^3 e^{-x^2} dx= [x^2e^{-x^2}/2|_{0}^{\infty} - \int_{0}^{\infty} -x e^{-x^2} dx$. The first term equals zero (verify yourself). Hence,  $\int_{0}^{\infty} x^3 e^{-x^2} dx =  \int_{0}^{\infty} x e^{-x^2} dx$ = 1/2 (which we know from d). \\

```{exercise} MarkDown files
:class: dropdown
Try making a MarkDown file yourself. Note how this exercise 'folds out'. This setting can be turned on or off centrally in the configuration file of your book, or locally per block (which is what I've done here).
```
