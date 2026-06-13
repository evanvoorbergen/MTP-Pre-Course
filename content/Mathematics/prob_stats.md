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
A group of dancers is waltzing on a one-dimensional dance floor of
length $L$. Since the dancers avoid the walls, the probability of finding a dancer at a position $x$ between the walls at $x = 0$ and $x = L$ is  proportional to $\sin^2(\pi x/L)$.

```{exercise}
:label: Exercise1
Determine the normalized distribution function for the position of the waltzers.
```
```{solution} Exercise1
:label: Solution1
:class: dropdown
The probability density function equals $pdf(x) = A \sin^2 (\pi x/L)$ with $A$ the proportionality
  constant. For a normalized probability density function, this constant
  is such that $\int_{x=0}^{L}  pdf(x) dx = 1$. Working this out gives the expression for $A$.
```

```{exercise}
:label: Exercise2
Make a sketch of the normalized distribution function.
```
```{solution} Exercise2
:label: Solution2
:class: dropdown
Do yourself.
```

```{exercise}
:label: Exercise3
Calculate the most probable position of the waltzers from the distribution function.
```
```{solution} Exercise3
:label: Solution3
:class: dropdown
Most probable position $x_{mp}$ is found for $\frac{d pdf(x)}{dx}|_{x=x_{mp}} = 0$. Working it
  out gives $x_{mp} = L/2$.
```

```{exercise}
:label: Exercise4
Give the general equation to calculate the mean position $\overline{x}$ from a distribution function.
```
```{solution} Exercise4
:label: Solution4
:class: dropdown
General equation for the mean position $\overline{x}$ of a distributed parameter  
$$ \overline{x} = \frac{\int_{x=0}^L x pdf(x) dx }{ \int_{x=0}^L pdf(x) dx}$$
Since the probability density function we consider here is normalized, we immediately know that the denominator equals 1.
```

```{exercise}
:label: Exercise5
Calculate the mean position of the waltzers. 
```
```{solution} Exercise5
:label: Solution5
:class: dropdown
Working it out gives $\overline{x} = L/2$ (which is logical as the system is symmetric). 
```

```{exercise}
:label: Exercise6
Give the general equation to calculate the mean square position $\overline{x^2}$ from a distribution function.
```
```{solution} Exercise6
:label: Solution6
:class: dropdown
General equation for the mean square position $\overline{x^2}$ of a distributed parameter $$\overline{x^2} = \frac{\int_{x=0}^L x^2 pdf(x) dx}{\int_{x=0}^L pdf(x) dx}$$. 
```

```{exercise}
:label: Exercise7
Calculate the mean square position of the waltzers. Also calculate the standard deviation using the definition $\sigma = \sqrt{\overline{x^2}  - \overline{x}^2}$, which is a measure for the spread around the mean and hence characterizes the width of the distribution.
```
```{solution} Exercise7
:label: Solution7
:class: dropdown

```

```{exercise}
:label: Exercise8
Consider part of the dance floor between $L/2 - s$ and $L/2 + s$. Calculate the value of $s$ to find 70\% of the people in this part of the dance floor. Useful relations: $\sin^2(x) = 0.5\left(1-\cos(2x)\right)$; $\int x \cos(x) dx = \cos(x) + x\sin(x)$. 
```
```{solution} Exercise8
:label: Solution8
:class: dropdown
The value of $s$ can be calculated from $\int_{L/2 - s}^{L/2 +s} pdf(x) dx = 0.7$, with $s$ the only unknown in this expression; work out yourself.
```

### Exercise B
In the previous assignment, you considered a distribution function that is continuous and you determined its statistical properties. In this exercise, you will consider two examples of discrete distribution functions. Consider an experiment in which you throw a fair dice. The outcome, $n_i$ of each throw is a (discrete) number $n_i = \{1,2,3,4,5, 6\}$. The probability $p_i$ of each outcome is the same, i.e. $p_1 = p_2 = ... = p_6 = 1/6$.


```{exercise}
:label: Exercise1.1
Calculate the mean value $\overline{n}$ that is obtained after throwing the dice many times. Also calculate the mean square value $\overline{n^2}$ and the standard deviation $\sigma = \sqrt{\overline{n^2} - \overline{n}^2}$.
```
```{solution} Exercise1.1
:label: Solution1.1
:class: dropdown

```

```{exercise}
:label: Exercise2.1
Now consider the case in which 2 dices are thrown simultaneously. In this case, the outcome is a number between 2 and 12 and the probabilities $p_1$ to $p_{12}$ are no longer the same. Write down the values of $p_1$ to $p_{12}$. Then, calculate the mean value.
```
```{solution} Exercise2.1
:label: Solution2.1
:class: dropdown

```

