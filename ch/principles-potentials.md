<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism\:potentials)=
# Electromagnetic Potentials

It is possible to demonstrate that the system of Maxwell's equations and the charge continuity equation is overdetermined. Specifically, it can be shown that, given the distribution of charge and current density—considered as the generating causes of the electric field—and the constitutive laws of the material, four unknowns are sufficient to define the six unknowns (three components for two vector fields) of the problem. Therefore, the problem can be formulated in terms of a scalar potential $\varphi$ and a vector potential $\mathbf{a}$, along with a gauge condition that eliminates the remaining two arbitrary factors (irrelevant for the calculation of physical fields).

## Vector Potential and Scalar Potential

Starting from Maxwell's equations, the potentials of the electromagnetic field can be defined. Using Gauss's law for the magnetic field, the vector potential $\mathbf{a}(\mathbf{r},t)$ can be introduced,

$$0 = \nabla \cdot \mathbf{b} \qquad \rightarrow \qquad \mathbf{b} = \nabla \times \mathbf{a} \ ,$$

since the divergence of a curl is identically zero. Introducing this relationship into the Faraday-Neumann-Lenz equation, assuming sufficient regularity of the fields to allow the inversion of the order of derivatives,

$$0 = \nabla \times \mathbf{e} + \partial_t \mathbf{b} = \nabla \times \mathbf{e} + \partial_t \nabla \times \mathbf{a} = \nabla \times (\mathbf{e} + \partial_t \mathbf{a}) \qquad \rightarrow \qquad \mathbf{e} + \partial_t \mathbf{a} = - \nabla \varphi \ ,$$

since the curl of a gradient is identically zero. The "physical" quantities of the electric field $\mathbf{e}(\mathbf{r},t)$ and the magnetic field $\mathbf{b}(\mathbf{r},t)$ can therefore be written using the electromagnetic potentials as

$$\begin{cases}
 \mathbf{e} & = - \nabla \varphi - \partial_t \mathbf{a} \\
 \mathbf{b} & = \nabla \times \mathbf{a} \\
\end{cases}$$

## Gauge Conditions

The potentials are defined up to a gauge condition, an additional condition that eliminates any arbitrariness in the definition. For example, the vector potential is defined up to the gradient of a scalar function, since $\nabla \times \nabla f \equiv \mathbf{0}$, and thus the potential $\tilde{\mathbf{a}} = \mathbf{a} + \nabla f$ produces the same magnetic field $\mathbf{b}$

$$\nabla \times \tilde{\mathbf{a}} = \nabla \times (\mathbf{a} + \nabla f) = \nabla \times \mathbf{a} \ .$$

**Lorentz Gauge Condition.** For reasons that will become clearer in the section on [electromagnetic waves](classical-electromagnetism\:waves), a convenient gauge condition is

$$\nabla \cdot \mathbf{a} + \frac{1}{c^2} \partial_t \varphi = 0$$

**Coulomb Gauge Condition.**

$$\nabla \cdot \mathbf{a} = 0$$


