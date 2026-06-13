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
:label: Exercise2
$\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
```
```{solution} Exercise2
:label: Solution2
:class: dropdown
$\frac{\sqrt{\pi}}{2}$
```

```{exercise}
:label: Exercise3
$\int_{x=-\infty}^{\infty} x^3 e^{-x^2} dx$
```
```{solution} Exercise3
:label: Solution3
:class: dropdown
$0$
```

```{exercise}
:label: Exercise4
$\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
```
```{solution} Exercise4
:label: Solution4
:class: dropdown
$\frac{1}{2}$  

Choose $v(x) = e^{-x^2}$ such that $v'(x) = -2x e^{-x^2}$.  
As $u(x)v'(x) = x e^{-x^2}$, we find  $u(x) = -1/2$ and  $u'(x) = 0$.  
So, we can now write $\int_{0}^{\infty} x e^{-x^2} dx= [-1/2 e^{-x^2}]_{0}^{\infty} - \int_{0}^{\infty}  0 dx = [0 + 1/2] = 1/2$.
```

```{exercise}
:label: Exercise5
$\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
```
```{solution} Exercise5
:label: Solution5
:class: dropdown
$\frac{1}{2}$  

Choose $v(x) = e^{-x^2}$ such that $v'(x) = -2x e^{-x^2}$.  
As $u(x)v'(x) = x^3 e^{-x^2}$, we find  $u(x) = -x^2/2$ and  $u'(x) = -x$.  
So, we can now write 
$\int_{0}^{\infty} x^3 e^{-x^2} dx= [x^2e^{-x^2}/2]_{0}^{\infty} - \int_{0}^{\infty} -x e^{-x^2} dx$.  
The first term equals zero (verify yourself).  
Hence,  $\int_{0}^{\infty} x^3 e^{-x^2} dx =  \int_{0}^{\infty} x e^{-x^2} dx$ = 1/2 (which we know from d).
```

```{exercise}
:label: Exercise6
$\int_{x=-\infty}^{\infty} x^2 e^{-x^2} dx$
```
```{solution} Exercise6
:label: Solution6
:class: dropdown
$\frac{3\sqrt{\pi}}{8}$
```
