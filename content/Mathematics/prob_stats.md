# Probability and Statistics

```{admonition} Connection to MTP
  
 * Chapter 3: Solving problems with Maxwell’s velocity distribution  
 * Chapter 4: Langevin theory, random walk model
```

## Theory

### Video on Discrete Random Variables:
<iframe width="560" height="315" src="https://www.youtube.com/embed/dAge1vGRYf4?si=L7X0VWHVyOUgprd7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Video on Continuous Random Variables:
<iframe width="560" height="315" src="https://www.youtube.com/embed/nSA9fGcXnLg?si=NoUqb8d8DNEQzwm_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Exercises

### Exercise A
Consider fluid flowing between two parallel plates separated by a distance $L$ (with $0 \le x \le L$). The fraction of total kinetic energy is proportional to the function below.  
$
f(x) = \sin^2\left(\frac{\pi x}{L}\right),
$

```{exercise}
:label: Exercise1pb
Determine the normalized distribution function for the fraction of kinetic energy between 0 and L.
```
```{hint}
:class: dropdown
$\int_{0}^{\pi} \sin^2(x) dx = \int_{0}^{\pi} \cos^2(x) dx$
```

```{solution} Exercise1pb
:label: Solution1pb
:class: dropdown
We write the normalized distribution function as $f(x) = A\sin^2\!\left(\dfrac{\pi x}{L}\right)$, where $A$ is determined by the normalization condition:  
$
    \int_0^L f(x)\, dx = 1
    \implies
    A\int_0^L \sin^2\!\left(\frac{\pi x}{L}\right) dx = 1.
$  

Using the substitution $u = \pi x/L$, so $dx = L\,du/\pi$:  
$
    A \cdot \frac{L}{\pi}\int_0^{\pi} \sin^2(u)\, du = 1.
$  

To evaluate $\int_0^{\pi}\sin^2(u)\,du$, we use the hint $\int_{0}^{\pi} \sin^2(u)\, du = \int_{0}^{\pi} \cos^2(u)\, du$:  
$
    2\int_0^{\pi}\sin^2(u)\,du = \int_0^{\pi}\sin^2(u)\,du + \int_0^{\pi}\cos^2(u)\,du = \int_0^{\pi}\underbrace{\left(\sin^2(u)+\cos^2(u)\right)}_{=\,1}du = \pi,
$  
so $\int_0^{\pi}\sin^2(u)\,du = \dfrac{\pi}{2}$. 

Substituting back:  
$
    A \cdot \frac{L}{\pi} \cdot \frac{\pi}{2} = A\cdot\frac{L}{2} = 1
    \implies A = \frac{2}{L}.
$  

Therefore the normalized distribution function is:  
$
    \boxed{f(x) = \frac{2}{L}\sin^2\!\left(\frac{\pi x}{L}\right)}.
$

```

```{exercise}
:label: Exercise2pb
Make a sketch of the normalized distribution function.
```
`````{solution} Exercise2pb
:label: Solution2pb
:class: dropdown
```{figure} ../images/prob_stats/desmos.png
:width: 50%
:align: center
```
`````

```{exercise}
:label: Exercise3pb
What position is the kinetic energy density the highest?
```
```{solution} Exercise3pb
:label: Solution3pb
:class: dropdown
$x_{mp} = L/2$
```

```{exercise}
:label: Exercise4pb
Give the general equation to calculate the mean position $\overline{x}$ from a distribution function.
```
```{solution} Exercise4pb
:label: Solution4pb
:class: dropdown
General equation for the mean position $\overline{x}$ of a distributed parameter  
$$ \overline{x} = \frac{\int_{x=0}^L x pdf(x) dx }{ \int_{x=0}^L pdf(x) dx}$$
Since the probability density function we consider here is normalized, we immediately know that the denominator equals 1.
```

```{exercise}
:label: Exercise5pb
Calculate the mean position of kinetic energy. 
```
```{solution} Exercise5pb
:label: Solution5pb
:class: dropdown
Working it out gives $\overline{x} = L/2$ (which is logical as the system is symmetric). 
```

```{exercise}
:label: Exercise6pb
Give the general equation to calculate the mean square position $\overline{x^2}$ from a distribution function.
```
```{solution} Exercise6pb
:label: Solution6pb
:class: dropdown
General equation for the mean square position $\overline{x^2}$ of a distributed parameter $$\overline{x^2} = \frac{\int_{x=0}^L x^2 pdf(x) dx}{\int_{x=0}^L pdf(x) dx}$$. 
```

```{exercise}
:label: Exercise7pb
Calculate the mean square position, using the identity $\sin^2(\theta) = \dfrac{1 - \cos(2\theta)}{2}$. Also calculate the standard deviation using the definition $\sigma = \sqrt{\overline{x^2}  - \overline{x}^2}$, which is a measure for the spread around the mean and hence characterizes the width of the distribution. 
```
```{solution} Exercise7pb
:label: Solution7pb
:class: dropdown
Since $f(x)$ is already normalized, the denominator equals 1 and the mean square position is:  
$
    \overline{x^2} = \int_0^L x^2 f(x)\, dx = \frac{2}{L}\int_0^L x^2 \sin^2\!\left(\frac{\pi x}{L}\right) dx.
$

Using the identity $\sin^2(\theta) = \dfrac{1 - \cos(2\theta)}{2}$:  
$
    \overline{x^2} = \frac{2}{L}\int_0^L x^2 \cdot \frac{1 - \cos\!\left(\dfrac{2\pi x}{L}\right)}{2}\, dx
    = \frac{1}{L}\int_0^L x^2\, dx - \frac{1}{L}\int_0^L x^2\cos\!\left(\frac{2\pi x}{L}\right) dx.
$  

The first integral is straightforward:  
$
    \frac{1}{L}\int_0^L x^2\, dx = \frac{1}{L}\cdot\frac{L^3}{3} = \frac{L^2}{3}.
$  

For the second integral, we integrate by parts twice. Let $k = 2\pi/L$ for brevity. Starting with $u = x^2$, $dv = \cos(kx)\,dx$:  
$
    \int_0^L x^2\cos(kx)\,dx = \left[\frac{x^2\sin(kx)}{k}\right]_0^L - \frac{2}{k}\int_0^L x\sin(kx)\,dx.
$  

The boundary term vanishes since $\sin(kL) = \sin(2\pi) = 0$. Integrating by parts again with $u = x$, $dv = \sin(kx)\,dx$:  
$
    \int_0^L x\sin(kx)\,dx = \left[-\frac{x\cos(kx)}{k}\right]_0^L + \frac{1}{k}\int_0^L \cos(kx)\,dx
    = -\frac{L\cos(2\pi)}{k} + \frac{1}{k}\left[\frac{\sin(kx)}{k}\right]_0^L.
$  

Since $\cos(2\pi)=1$ and $\sin(2\pi)=0$:  
$
    \int_0^L x\sin(kx)\,dx = -\frac{L}{k}.
$  

Substituting back:  
$
    \int_0^L x^2\cos(kx)\,dx = -\frac{2}{k}\cdot\left(-\frac{L}{k}\right) = \frac{2L}{k^2} = \frac{2L}{(2\pi/L)^2} = \frac{L^3}{2\pi^2}.
$  

Therefore:  
$
    \overline{x^2} = \frac{L^2}{3} - \frac{L^2}{2\pi^2}.
$  

$
    \boxed{\overline{x^2} = L^2\left(\frac{1}{3} - \frac{1}{2\pi^2}\right) }
$  

The mean position is $\overline{x} = L/2$ (by symmetry of $f(x)$), so $\overline{x}^2 = L^2/4$. Using the result above:  
$
    \sigma = \sqrt{\overline{x^2} - \overline{x}^2} = \sqrt{L^2\left(\frac{1}{3} - \frac{1}{2\pi^2}\right) - \frac{L^2}{4}}
    = L\sqrt{\frac{1}{3} - \frac{1}{2\pi^2} - \frac{1}{4}}.
$

$
    \boxed{\sigma = L\sqrt{\frac{1}{3} - \frac{1}{2\pi^2} - \frac{1}{4}} }
$
```


### Exercise B
In the previous assignment, you considered a distribution function that is continuous and you determined its statistical properties. In this exercise, you will consider two examples of discrete distribution functions. Consider an experiment in which you throw a fair dice. The outcome, $n_i$ of each throw is a (discrete) number $n_i = \{1,2,3,4,5, 6\}$. The probability $p_i$ of each outcome is the same, i.e. $p_1 = p_2 = ... = p_6 = 1/6$.


```{exercise}
:label: Exercise1.1
Calculate the mean value $\overline{n}$ that is obtained after throwing the dice a million times. Also calculate the mean square value $\overline{n^2}$ and the standard deviation $\sigma = \sqrt{\overline{n^2} - \overline{n}^2}$. 
```
```{solution} Exercise1.1
:label: Solution1.1
:class: dropdown
$
    \bar{n} = \frac{\sum_{i=1}^{6} p_i\, n_i}{\sum_{i=1}^{6} p_i} = \frac{\frac{1}{6}(1+2+3+4+5+6)}{\frac{1}{6}\cdot 6}  = 3.5.
$  

The mean square value is:  
$
    \overline{n^2} = \frac{\sum_{i=1}^{6} p_i\, n_i^2}{\sum_{i=1}^{6} p_i} = \frac{\frac{1}{6}(1+4+9+16+25+36)}{\frac{1}{6}\cdot 6} = 15.17.
$  

The standard deviation is then:  
$
    \sigma = \sqrt{\overline{n^2} - \bar{n}^2} = \sqrt{\frac{91}{6} - (3.5)^2} = \sqrt{2.92} \approx 1.71.
$
```

```{exercise}
:label: Exercise2.1
Now consider the case in which 2 dices are thrown simultaneously. In this case, the outcome is a number between 2 and 12 and the probabilities $p_1$ to $p_{12}$ are no longer the same. Write down the values of $p_1$ to $p_{12}$. Then, calculate the mean value.
```
```{solution} Exercise2.1
:label: Solution2.1
:class: dropdown
Here the possible outcomes are $n_i = \{2,3,4, \cdots , 11, 12\}$. The probability of each of these is now no longer the same: a value of 2 means that each dice should be a one. The probability of this is $\frac{1}{36}$. However, the value of 7 can be made by many combinations: \{1,6\}, \{2,5\}, etc. This value has a six times higher probability: $p_7 = \frac{1}{6}$. All values and their probability are given in the table below.  

| value | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| probability | $\frac{1}{36}$ | $\frac{2}{36}$ | $\frac{3}{36}$ | $\frac{4}{36}$ | $\frac{5}{36}$ | $\frac{6}{36}$ | $\frac{5}{36}$ | $\frac{4}{36}$ | $\frac{3}{36}$ | $\frac{2}{36}$ | $\frac{1}{36}$ |

From this, we compute the average value:  
$$
\overline{n} = \frac{\sum_{i=1}^N {p_i n_i}}{\sum_{i=1}^N {p_i}}
$$

Substitution of the values for $n_i$ and $p_i$, we hence find $\overline{n} = 7$.

```

