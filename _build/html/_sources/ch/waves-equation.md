<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism\:waves\:wave-equation)=
# Wave Equations in Electromagnetism

**Vector Identity.**

$$\Delta \mathbf{v} = \nabla ( \nabla \cdot \mathbf{v} ) - \nabla \times \nabla \times \mathbf{v}$$

**Proof.**

$$\begin{aligned}
 \nabla \times \nabla \times \mathbf{v} & = \varepsilon_{ijk} \partial_j ( \varepsilon_{klm} \partial_l v_m ) = \\
 & = \varepsilon_{kij} \varepsilon_{klm} \partial_{jl} v_m = \\
 & = ( \delta_{il} \delta_{jm} - \delta_{im} \delta_{jl} )  \partial_{jl} v_m = \\
 & = \partial_{ij} v_j - \partial_{jj} v_i = \\
 & = \nabla (\nabla \cdot \mathbf{v}) - \Delta \mathbf{v} \ ,
\end{aligned}$$

using the identity

$$\varepsilon_{ijk} \varepsilon_{ilm} = \delta_{jl} \delta_{km} - \delta_{jm} \delta_{kl}$$

## Electromagnetic Potentials

Starting from the definitions of electromagnetic potentials and Maxwell's equations, with the help of some vector identities, it is possible (**TODO** *list the necessary assumptions for the derivation*) to write wave equations for the vector potential and the scalar potential.

$$\begin{aligned}
 \mathbf{e} & = - \nabla \varphi - \partial_t \mathbf{a} \\
 \mathbf{b} & = \nabla \times \mathbf{a} \\
\end{aligned}$$

Using the constitutive equations

$$\mathbf{d} = \varepsilon \ \mathbf{e} \qquad , \qquad
\mathbf{b} = \mu \mathbf{h} $$

**Vector Potential.**

$$\mathbf{b} = \nabla \times \mathbf{a}$$

$$\begin{aligned}
\mathbf{0} & = \nabla \times \nabla \times \mathbf{a} - \nabla \times \mathbf{b} = \\
 & = - \Delta \mathbf{a} + \nabla(\nabla \cdot \mathbf{a})  - \mu \nabla \times \mathbf{h} = \\
 & = - \Delta \mathbf{a} + \nabla(\nabla \cdot \mathbf{a})  - \mu ( \partial_t \mathbf{d} + \mathbf{j} )  = \\
 & = - \Delta \mathbf{a} + \nabla(\nabla \cdot \mathbf{a})  - \mu ( \varepsilon \partial_t \mathbf{e} + \mathbf{j} )  = \\
 & = - \Delta \mathbf{a} + \nabla(\nabla \cdot \mathbf{a})  - \mu \varepsilon ( - \partial_t \nabla \varphi - \partial_{tt} \mathbf{a} ) + \mu \mathbf{j} = \\
 & = - \Delta \mathbf{a} + \nabla(\nabla \cdot \mathbf{a})  + \frac{1}{c^2} \partial_t \nabla \varphi + \dfrac{1}{c^2} \partial_{tt} \mathbf{a} - \mu \mathbf{j}  \\
\end{aligned}$$

Using the Lorentz gauge condition

$$\nabla \cdot \mathbf{a} + \frac{1}{c^2} \partial_t  \varphi = 0 \ ,$$

we obtain a wave equation for the vector potential

$$ \dfrac{1}{c^2} \partial_{tt} \mathbf{a} - \Delta \mathbf{a}  =  \mu \mathbf{j}  \ .$$

**Scalar Potential.**

$$\mathbf{e} = \nabla \varphi - \partial_t \mathbf{a}$$

Taking the time derivative of the Lorentz gauge condition

$$\begin{aligned}
 0 & = \partial_t (\frac{1}{c^2} \partial_t \varphi + \nabla \cdot \mathbf{a}) = \\
   & = \frac{1}{c^2} \partial_{tt} \varphi + \nabla \cdot \partial_t \mathbf{a} = \\
   & = \frac{1}{c^2} \partial_{tt} \varphi - \nabla \cdot \nabla \varphi - \nabla \cdot \mathbf{e} = \\
   & = \frac{1}{c^2} \partial_{tt} \varphi - \Delta \varphi - \frac{\rho}{\varepsilon} = \\
\end{aligned}$$

we arrive at the wave equation for the scalar potential,

$$ \frac{1}{c^2} \partial_{tt} \varphi - \Delta \varphi = \frac{\rho}{\varepsilon} \ .$$

## Electric Field and Magnetic Field

Using the definitions of the physical fields in terms of the electromagnetic potentials and the linearity (**TODO** *everything must be linear, including the constitutive laws*) of the operations, starting from the wave equations for the potentials, we can derive the wave equations for the physical fields. **TODO** *Assuming constant and uniform properties*

**Electric Field.**

$$\begin{aligned}
\square \mathbf{e} & = \square ( -\nabla \varphi - \partial_t \mathbf{a}) = \\
& = - \nabla \square \varphi - \partial_t \square \mathbf{a} = \\
& = - \nabla \dfrac{\rho}{\varepsilon} - \mu \partial_t \mathbf{j}  \ .
\end{aligned}$$

**Magnetic Field.**

$$\begin{aligned}
 \square \mathbf{b} & = \square \nabla \times \mathbf{a} = \\
 & = \nabla \times \square \mathbf{a} = \\
 & = \mu \nabla \times \mathbf{j}
\end{aligned}$$
```

