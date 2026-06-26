# Microscopic Momentum Balances


```{admonition} Connection to MTP
* Chapter 6: Electro-osmotic Flow  
This concept is used in charged fluids between two plates driven by an electric field (electro-osmotic flow).
```
## Theory

### Video on Momentum Microbalances for Laminar Flow and Newtonian Fluids
The relevant part of this video is from 1:10 to 7:45.

<iframe width="560" height="315" src="https://www.youtube.com/embed/ZUdUri-_l2A?si=_NKeDcccMOvmh_vP&amp;start=70" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Exercises

**Setting up and solving a microbalance for momentum transport**

`````{exercise}
:label: Exercise1micromom
```{figure} ../../images/micro_mom/MTP_prereq_Sol02.png
:width: 30%
:align: center
```
Consider laminar flow between two, large, vertical plates. The distance between the two plates is $2D$. In the space between the two plates, a Newtonian fluid (constant density $\rho$, dynamic viscosity $\eta$) flows vertically downwards under the influence of gravity (no external pressure difference is applied to the system). The situation is in steady state. 

Set up a microbalance and show that the velocity profile is equal to: $v_y(x) = - \frac{\rho g}{2 \eta} \left( D^2 - x^2 \right)$. Remember that $\tau_{xy} = -\eta \frac{d}{dx}(v_y)$ for Newtonian fluids.
`````
```{solution} Exercise1micromom
:label: Solution1micromom
:class: dropdown
Consider the control volume in the sketch. 

Setting up the microbalance yields:  
$0 = \left[\tau_{xy} \right]_x dy H - \left[\tau_{xy} \right]_{x+dx} dy H - \rho g H dx dy$. 

Here, $H$, a dimension perpendicular to the paper, was introduced for convenience, just to work out the two-dimensional problem as if it were a three-dimensional problem. This (dummy) length scale cancels and we obtain:  
$\frac{d\tau}{dx} = -\rho g$. 

Note that the pressure has not been considered when setting up the microbalance, as it is given that there is no externally applied pressure difference.  
For Newtonian fluids: $\tau_{xy} = -\eta \frac{d}{dx}(v_y)$. 

Substitution and integrating twice with respect to $x$ yields:  
$v_y(x) = \frac{\rho g}{2 \eta} x^2 + C_1 x + C_2$. 

The integration constants ($C_1$ and $C_2$) follow from the no-slip boundary conditions at the walls:  
 $v_y (x=-D) = 0$ and $v_y (x=+D) = 0$. 

Alternatively, we can use the fact that the profile is symmetric around $x = 0$ in combination with one of the two no-slip conditions. This immediately tells us that $C_1 = 0$. For the second integration constant, we find $C_2 = - \frac{\rho g}{2 \eta} D^2$. 

Hence, $v_y(x) = - \frac{\rho g}{2 \eta} \left( D^2 - x^2 \right)$.
```

