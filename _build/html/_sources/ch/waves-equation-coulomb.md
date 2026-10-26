<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:waves:wave-equation-coulomb)=
# Poisson and Wave Equations in Electromagnetism - using Coulomb gauge

(classical-electromagnetism:waves:wave-equation-coulomb:potentials)=
## Electromagnetic Potentials

(classical-electromagnetism:waves:wave-equation-coulomb:potentials:scalar)=
### Scalar potential

Starting from the definition $\vec{e} = - \nabla \varphi - \partial_t \vec{a}$, taking the divergence, swapping time and space derivatives in $\nabla \cdot \partial_t \vec{a}$ and using Coulomb gauge condition {eq}`eq:potential:gauge:coulomb`, and Gauss law for the electric field $\nabla \cdot \vec{e} = \tfrac{\rho}{\varepsilon}$,

$$\begin{aligned}
  0 
  & = \nabla \cdot \left( \vec{e} + \nabla \varphi + \partial_t \vec{a} \right) 
    = \frac{\rho}{\varepsilon} + \nabla^2 \varphi \ ,
\end{aligned}$$

a Poisson equation - to be supplemented with **boundary conditions** only, as there's no explicit time derivative[^todo-poisson] - for the scalar potential $\varphi(\vec{r},t)$ holds

$$- \nabla^2 \varphi = \frac{\rho}{\varepsilon} \ .$$

[^todo-poisson]: Add a discussion of these aspects of Poisson equation in Math book. This also helps the discussion of incompressible and compressible fluid dynamics.

(classical-electromagnetism:waves:wave-equation-coulomb:potentials:vector)=
### Vector potential

Starting from the definition $\vec{b} = \nabla \times \vec{a}$, using Maxwell equations and constitutive laws,

$$\begin{aligned}
\vec{0} & = \nabla \times \left( \nabla \times \vec{a} - \vec{b} \right) = \\
 & = - \Delta \vec{a} + \nabla(\nabla \cdot \vec{a})  + \frac{1}{c^2} \partial_t \nabla \varphi + \dfrac{1}{c^2} \partial_{tt} \vec{a} - \mu \vec{j} \ .
\end{aligned}$$

Using Coulomb gauge $\nabla \cdot \vec{a} = 0$, a wave eqaution for $\vec{a}$ follows

$$\frac{1}{c^2} \partial_{tt} \vec{a} - \nabla^2 \vec{a} = \mu \vec{j} - \frac{1}{c^2} \partial_t \nabla \varphi \ .$$

The last term can be written as a function of the irrotational part of the current density, using expresion {eq}`eq:wave-coulomb:j-irrot`, so that the wave equation becomes

$$\frac{1}{c^2} \partial_{tt} \vec{a} - \nabla^2 \vec{a} = \mu \vec{j}_{\perp} \ ,$$

as $\mu\vec{j} - \tfrac{1}{c^2}\partial_t \nabla \varphi = \mu\vec{j} - \tfrac{1}{\varepsilon c^2} \vec{j}_{\parallel} = \mu \left( \vec{j} - \vec{j}_{\parallel} \right) = \mu \vec{j}_{\perp}$.



````{dropdown} Helmholtz decomposition of the charge current density
:open:

Let $\vec{j} = \vec{j}_{\parallel} + \vec{j}_{\perp}$, with $\vec{j}_{\parallel}$ irrotational ($\nabla \times \vec{j}_{\parallel} = \vec{0}$) and $\vec{j}_{\perp}$ solenoidal ($\nabla \cdot \vec{j}_{\perp} = 0$). The irrotational part reads

$$\vec{j}_{\parallel} = \varepsilon \partial_t \nabla \varphi \ .$$ (eq:wave-coulomb:j-irrot)

```{dropdown} Proof

Continuity reads

$$0 = \partial_t \rho + \nabla \cdot \vec{j} = \partial_t \rho + \nabla \cdot \vec{j}_{\parallel} \ ,$$

and using Poisson equation for the scalar potential $\varphi$,

$$0 = \nabla \cdot \left( - \varepsilon \partial_t \nabla \varphi + \vec{j}_{\parallel} \right) \ .$$

It follows $\vec{j}_{\parallel} = \varepsilon \partial_t \nabla \varphi + \nabla \times \vec{f} = \varepsilon \partial_t \nabla \varphi$, with the curl contribution being identically zero by the definition of $\vec{j}_{\parallel}$, and the vector identity $\nabla \times \nabla \varphi = \vec{0}$. 

```
````

(classical-electromagnetism:waves:wave-equation-coulomb:em-field)=
## Electric Field and Magnetic Field

(classical-electromagnetism:waves:wave-equation-coulomb:em-field:e)=
### Electric field

(classical-electromagnetism:waves:wave-equation-coulomb:em-field:b)=
### Magnetic field

