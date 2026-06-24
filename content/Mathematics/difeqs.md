# Differential Equations

```{admonition} Connection to MTP
 Used in all chapters, with the strongest connection to Chapters 3 and 4.
```

## The Chain Rule for Differential Equations

### Exercise
```{exercise}
:label: ExerciseChainRule
Given that $x$ is a function of $t$, show that $\frac{d^2 }{d t^2} \left( x^2\right) = 2 \left( \frac{d x}{d t} \right)^2 + 2x \frac{d^2 x}{d t^2}$
```
```{solution} ExerciseChainRule
:label: SolutionChainRule
:class: dropdown
$\frac{d^2 }{d t^2} \left( x^2\right) = \frac{d}{\partial t} \left(\frac{d}{d t} x^2 \right) = \frac{d}{d t} \left(2x\frac{d x}{d t}\right)$. Continue applying the chain rule in a similar fashion as for example in $\frac{d}{d t} \left( a b \right) = a \frac{d b}{d t} + b \frac{d a}{d t}$ with $a$ and $b$ two functions that depend on time. In this case, $a=2x$ and $b= \frac{d x}{d t}$ 
```

## Direct Integration

### Video on Direct Integration:
<iframe width="560" height="315" src="https://www.youtube.com/embed/OFGvktKTD5g?si=oxhymImWMI0Prt9G" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Exercise

```{exercise}
:label: ExerciseDI
$db/dt = C$
```
```{solution} ExerciseDI
:label: SolutionDI
:class: dropdown
$b(t) =  Ct + C_1$, with $C_1$ a constant of integration. 
```


## Separable Differential Equations

### Video on Separable Differential Equations:
<iframe width="560" height="315" src="https://www.youtube.com/embed/-6nl3kJWlXw?si=gu5yMEA7wZqfgDMT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Exercise

```{exercise}
:label: ExerciseSDE
$db/dt = Cb$
```
```{solution} ExerciseSDE
:label: SolutionSDE
:class: dropdown
$b(t) = C_1 e^{Ct}$, with $C_1$ a constant of integration.
```

## First-Order Linear ODEs

### Video on First-Order Linear ODEs:
<iframe width="560" height="315" src="https://www.youtube.com/embed/-6nl3kJWlXw?si=gu5yMEA7wZqfgDMT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Exercise

```{exercise}
:label: Exercise1ODE
$db/dt = Cb + 2Ct$
```
```{solution} Exercise1ODE
:label: Solution1ODE
:class: dropdown
Integrating Factor  

$b(t) = C_1 e^{Ct} -2t-2/C$, with $C_1$ a constant of integration.

Rearranging gives $db/dt - Cb = 2Ct$, a first-order linear ODE.  
Multiplying by integrating factor $e^{-Ct}$:  
$
\frac{d}{dt}\!\left(e^{-Ct}b\right) = 2Cte^{-Ct}.
$  
Integrating the right-hand side by parts ($u=2Ct$, $dv = e^{-Ct}dt$):  
$ 
e^{-Ct}b = -2te^{-Ct} - \frac{2}{C}e^{-Ct} + C_1 \implies \boxed{b(t) = C_1e^{Ct} - 2t - \frac{2}{C}.}
$

```

## Second-Order Linear ODEs

### Video on Second-Order Linear ODEs:
<iframe width="560" height="315" src="https://www.youtube.com/embed/_tBF-EsMI4U?si=l3MaCqTHTcqdG7_W" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Exercise

```{exercise}
:label: Exercise2ODE
$d^2b/dt^2 = Cb$
```

```{hint}
:label: Hint2ODE
:class: dropdown
Try a solution of the form $b(t) = e^{\lambda t}$
```

```{solution} Exercise2ODE
:label: Solution2ODE
:class: dropdown
Characteristic Equation  

With a solution of the form $b(t) = e^{\lambda t}$, since we need a function whose second derivative returns itself (up to a constant). 

Substituting:
$
 \lambda^2 e^{\lambda t} - C e^{\lambda t} = 0 \implies e^{\lambda t}(\lambda^2 - C) = 0.$  
Since $e^{\lambda t} \neq 0$, we obtain the characteristic equation $\lambda^2 - C = 0$, giving two roots:  
$
 \lambda = \pm\sqrt{C}.
$

Each root gives an independent solution $e^{\sqrt{C}t}$ and $e^{-\sqrt{C}t}$.   
Since the ODE is linear, the general solution is a superposition of both:  
$\boxed{b(t) = C_1e^{\sqrt{C}t} + C_2e^{-\sqrt{C}t}}$
```

## Inhomogeneous Second-Order Linear ODEs

### Video on Inhomogeneous Second-Order Linear ODEs:
<iframe width="560" height="315" src="https://www.youtube.com/embed/axlzqvb2Swg?si=03l0Lpdfm74WlW8X" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Exercise

```{exercise}
:label: ExerciseI2ODE
$d^2b/dt^2 = db/dt + Ct$
```

```{hint}
:label: HintI2ODE
:class: dropdown
Split the solution into homogenous and particular parts.
```

```{solution} ExerciseI2ODE
:label: SolutionI2ODE
:class: dropdown
Undetermined Coefficients  

Rearranging gives $d^2b/dt^2 - db/dt = Ct$. We split the solution into a homogeneous part $b_h$ (with right-hand side set to zero) and a particular part $b_p$.  

For $b_h$, substituting $b = e^{\lambda t}$:  

$
 \lambda^2 e^{\lambda t} - \lambda e^{\lambda t} = 0 \implies e^{\lambda t}\lambda(\lambda - 1) = 0,
$
giving $\lambda = 0$ or $\lambda = 1$, so $b_h = C_1e^{t} + C_2$.  

For $b_p$, since the right-hand side is a first-order polynomial in $t$, we try $b_p = at^2 + bt$.   
Substituting:
$
 \underbrace{2a}_{d^2b_p/dt^2} - \underbrace{(2at + b)}_{db_p/dt} = Ct.
$

 Matching coefficients of $t^1$ and $t^0$ respectively:
$
-2a = C \implies a = -\tfrac{C}{2}, \qquad 2a - b = 0 \implies b = -C.
$  

The general solution $b = b_h + b_p$ is:
$
\boxed{b(t) = C_1e^{t} - \frac{C}{2}t^2 - Ct + C_2.}
$
```