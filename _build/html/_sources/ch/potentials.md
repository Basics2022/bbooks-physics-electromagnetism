<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:potentials)=
# Electromagnetic Potentials

It is possible to demonstrate that the system of Maxwell's equations and the charge continuity equation is overdetermined. Specifically, it can be shown that, given the distribution of charge and current density—considered as the generating causes of the electric field—and the constitutive laws of the material, four unknowns are sufficient to define the six unknowns (three components for two vector fields) of the problem. Therefore, the problem can be formulated in terms of a scalar potential $\varphi$ and a vector potential $\vec{a}$, along with a gauge condition that eliminates the remaining two arbitrary factors (irrelevant for the calculation of physical fields).

## Vector Potential and Scalar Potential

Starting from Maxwell's equations, the potentials of the electromagnetic field can be defined. Using Gauss's law for the magnetic field, the vector potential $\vec{a}(\vec{r},t)$ can be introduced,

$$0 = \nabla \cdot \vec{b} \qquad \rightarrow \qquad \vec{b} = \nabla \times \vec{a} \ ,$$

since the divergence of a curl is identically zero. Introducing this relationship into the Faraday-Neumann-Lenz equation, assuming sufficient regularity of the fields to allow the inversion of the order of derivatives,

$$0 = \nabla \times \vec{e} + \partial_t \vec{b} = \nabla \times \vec{e} + \partial_t \nabla \times \vec{a} = \nabla \times (\vec{e} + \partial_t \vec{a}) \qquad \rightarrow \qquad \vec{e} + \partial_t \vec{a} = - \nabla \varphi \ ,$$

since the curl of a gradient is identically zero. The "physical" quantities of the electric field $\vec{e}(\vec{r},t)$ and the magnetic field $\vec{b}(\vec{r},t)$ can therefore be written using the electromagnetic potentials as

$$\begin{aligned}
 \vec{e} & = - \nabla \varphi - \partial_t \vec{a} && (a) \\
 \vec{b} & = \nabla \times \vec{a} && (b) \\
\end{aligned}$$ (eq:potentials)

## Gauge Conditions

The potentials are defined up to a gauge condition, an additional condition that eliminates any arbitrariness in the definition. For example, the vector potential is defined up to the gradient of a scalar function, since $\nabla \times \nabla f \equiv \vec{0}$, and thus the potential $\tilde{\vec{a}} = \vec{a} + \nabla f$ produces the same magnetic field $\vec{b}$

$$\nabla \times \tilde{\vec{a}} = \nabla \times (\vec{a} + \nabla f) = \nabla \times \vec{a} \ .$$

**Lorentz Gauge Condition.** For reasons that will become clearer in the section on [electromagnetic waves](classical-electromagnetism\:waves), a convenient gauge condition is

$$\nabla \cdot \vec{a} + \frac{1}{c^2} \partial_t \varphi = 0$$ (eq:potential:gauge:lorentz)

**Coulomb Gauge Condition.**

$$\nabla \cdot \vec{a} = 0$$


