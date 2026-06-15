# Differential Equations

```{admonition} Connection to MTP
 Used in all chapters, with the strongest connection to Chapters 3 and 4.
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

Solution:
$b(t) =  Ct + C_1$, with $C_1$ a constant of integration. 

Steps:
$\frac{d^2 }{d t^2} \left( x^2\right) = \frac{d}{\partial t} \left(\frac{d}{d t} x^2 \right) = \frac{d}{d t} \left(2x\frac{d x}{d t}\right)$. Continue applying the chain rule in a similar fashion as for example in $\frac{d}{d t} \left( a b \right) = a \frac{d b}{d t} + b \frac{d a}{d t}$ with $a$ and $b$ two functions that depend on time. In this case, $a=2x$ and $b= \frac{d x}{d t}$.
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
$db/dt = Cb$
```
```{solution} Exercise1ODE
:label: Solution1ODE
:class: dropdown
Integrating Factor  

$b(t) = C_1 e^{Ct} -2t-2/C$, with $C_1$ a constant of integration.
```

## Second-Order Linear ODEs

### Video on Second-Order Linear ODEs:
<iframe width="560" height="315" src="https://www.youtube.com/embed/_tBF-EsMI4U?si=l3MaCqTHTcqdG7_W" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Exercise

```{exercise}
:label: Exercise2ODE
$d^2b/dt^2 = Cb$
```
```{solution} Exercise2ODE
:label: Solution2ODE
:class: dropdown
Characteristic Equation  

$b(t) = C_1 e^{\sqrt{C}t} + C_2 e^{-\sqrt{C}t}$, with $C_1$ and $C_2$ two constants of integration.
```

## Inhomogeneous Second-Order Linear ODEs

### Video on Inhomogeneous Second-Order Linear ODEs:
<iframe width="560" height="315" src="https://www.youtube.com/embed/axlzqvb2Swg?si=03l0Lpdfm74WlW8X" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Exercise

```{exercise}
:label: ExerciseI2ODE
$d^2b/dt^2 = db/dt + Ct$
```
```{solution} ExerciseI2ODE
:label: SolutionI2ODE
:class: dropdown
Undetermined Coefficients  

$b(t)=C_1e^t -\frac{C}{2}t^2 -Ct + C_2$, with $C_1$ and $C_2$ two constants of integration.
```