<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:waves:wave-equation)=
# Wave Equations in Electromagnetism

Wave equations for physical quantities in electromagnetism are derived from the governing equations for linear local isotropic homogeneous ($\varepsilon$, $\mu$ uniform, not function of space) media with constitutive equations

$$\vec{d} = \varepsilon \vec{e} \qquad , \qquad \vec{b} = \mu \vec{h} \ ,$$

using [vector identity](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/calculus-identities.html#equation-eq-identity-laplacian)

$$\Delta \vec{v} = \nabla ( \nabla \cdot \vec{v} ) - \nabla \times \nabla \times \vec{v} \ .$$

If some of the assumptions made above is not true, slight modifications and extra terms in the equations are likely to appear during the manipulation of the equations done below.


(classical-electromagnetism:waves:wave-equation:potentials)=
## Electromagnetic Potentials

<!--
Starting from the definitions of electromagnetic potentials and Maxwell's equations, with the help of some vector identities, it is possible (**TODO** *list the necessary assumptions for the derivation*) to write wave equations for the vector potential and the scalar potential.

$$\begin{aligned}
 \vec{e} & = - \nabla \varphi - \partial_t \vec{a} \\
 \vec{b} & = \nabla \times \vec{a} \\
\end{aligned}$$

Using the constitutive equations

$$\vec{d} = \varepsilon \ \vec{e} \qquad , \qquad
\vec{b} = \mu \vec{h} $$
-->

### Vector potential

Wave equation for the vector potential,

$$\vec{b} = \nabla \times \vec{a} \ ,$$

is derived taking the curl of its definition,

$$\begin{aligned}
\vec{0} & = \nabla \times \nabla \times \vec{a} - \nabla \times \vec{b} = && (1.a) \\
 & = - \Delta \vec{a} + \nabla(\nabla \cdot \vec{a})  - \mu \nabla \times \vec{h} = && (2) \\
 & = - \Delta \vec{a} + \nabla(\nabla \cdot \vec{a})  - \mu ( \partial_t \vec{d} + \vec{j}_f )  = && (1.b) \\
 & = - \Delta \vec{a} + \nabla(\nabla \cdot \vec{a})  - \mu ( \varepsilon \partial_t \vec{e} + \vec{j}_f )  = && (3) \\
 & = - \Delta \vec{a} + \nabla(\nabla \cdot \vec{a})  - \mu \varepsilon ( - \partial_t \nabla \varphi - \partial_{tt} \vec{a} ) + \mu \vec{j}_f = \\
 & = - \Delta \vec{a} + \nabla(\nabla \cdot \vec{a})  + \frac{1}{c^2} \partial_t \nabla \varphi + \dfrac{1}{c^2} \partial_{tt} \vec{a} - \mu \vec{j}_f  \\
\end{aligned}$$

and using (1) the constitutive law for homogeneous isotropic linear media, (2) Ampére-Maxwell's equation, (3), and (4) the definition of the electric field {eq}`eq:potentials`(a)  in terms of the potentials. Using the Lorentz gauge condition {eq}`eq:potential:gauge:lorentz`

$$\nabla \cdot \vec{a} + \frac{1}{c^2} \partial_t  \varphi = 0 \ ,$$

wave equation for the vector potential reads,

$$ \dfrac{1}{c^2} \partial_{tt} \vec{a} - \Delta \vec{a}  =  \mu \vec{j}  \ .$$ (eq:wave:a)

### Scalar potential

Wave equation for the the scalar potential, $\varphi(\vec{r},t)$, can be derived taking the time derivative of Lorentz's gauge condition,

$$\begin{aligned}
 0 & = \partial_t \left(\frac{1}{c^2} \partial_t \varphi + \nabla \cdot \vec{a} \right) = \\
   & = \frac{1}{c^2} \partial_{tt} \varphi + \nabla \cdot \partial_t \vec{a} = && (1) \\
   & = \frac{1}{c^2} \partial_{tt} \varphi - \nabla \cdot \nabla \varphi - \nabla \cdot \vec{e} = && (2) \\
   & = \frac{1}{c^2} \partial_{tt} \varphi - \Delta \varphi - \frac{\rho_f}{\varepsilon} \ ,
\end{aligned}$$

using (1) the definition {eq}`eq:potentials`(a)  of the electric field as a function of the potentials, and (2) Gauss' law for the electric field,

$$ \frac{1}{c^2} \partial_{tt} \varphi - \Delta \varphi = \frac{\rho_f}{\varepsilon} \ .$$ (eq:wave:phi)

## Electric Field and Magnetic Field
<!--
Using the definitions of the physical fields in terms of the electromagnetic potentials and the linearity (**TODO** *everything must be linear, including the constitutive laws*) of the operations, starting from the wave equations for the potentials, we can derive the wave equations for the physical fields. **TODO** *Assuming constant and uniform properties*
-->

Exploiting the linearity - obviously, if the problem is linear - wave equations for the electric and the magnetic field can be readily derived from applying the wave operator

$$\square := \frac{1}{c^2} \partial_{tt} - \Delta \ ,$$

to the (1) definitions {eq}`eq:potentials` of the electric and the magnetic fields as functions of the potentials, (2) swapping the order of the operator $\square$ with $\partial_t$ and $\nabla$[^swap], and (3) using the expressions of the wave equations for the vector potential {eq}`eq:wave:a` and the scalar potential {eq}`eq:wave:phi`.

[^swap]: $\square \partial_k f = \left( \frac{1}{c^2} \partial_{tt} - \partial_{ii} \right) \partial_k f = \partial_k \left( \frac{1}{c^2} \partial_{tt} - \partial_{ii} \right) f = \partial_k \, \square f $.

### Electric field

$$\begin{aligned}
\square \vec{e} & = && (1) \\
& =\square ( -\nabla \varphi - \partial_t \vec{a}) = && (2) \\
& = - \nabla \square \varphi - \partial_t \square \vec{a} = && (3) \\
& = - \nabla \dfrac{\rho}{\varepsilon} - \mu \partial_t \vec{j}  \ .
\end{aligned}$$

### Magnetic field

$$\begin{aligned}
 \square \vec{b} & = && (1) \\
 & = \square \nabla \times \vec{a} = && (2) \\
 & = \nabla \times \square \vec{a} = && (3) \\
 & = \mu \nabla \times \vec{j}
\end{aligned}$$

