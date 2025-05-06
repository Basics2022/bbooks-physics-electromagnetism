<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:principles:free-space)=
# Principles of Classical Electromagnetism in Free Space

The progress in the study of electromagnetic phenomena during the 19th century allowed James Clerk Maxwell to formulate what are now known as *Maxwell's equations*, which can be considered the first consistent formulation of the principles of classical electromagnetism, together with the charge conservation law and the expression for the Lorentz force on an electric charge immersed in an electromagnetic field.

Principles are introduced here for total charges and the electric and the magnetic field, in the form that is known as **equations of electromagnetism in vacuum**. Equations of [electromagnetism in matter](classical-electromagnetism:media) (1) separate the contribution of free and bound charges and currents, and (2) introduce **polarization** and **magnetization** of matter in constitutive equations representing the macroscopic response of the media as a result of local microscopic charge distribution induced by "external" fields.

Here principles of electromagnetism are first shown in their [differential form](classical-electromagnetism:principles:differential): (1) continuity equation of electric charge describes the conservation of electric charge, (2) Maxwell's equations govern the generation of the electromagnteic field by electric charge and currents, while (3) the differential form of Lorentz's force gives the expression of the force per unit volume acting on a distribution of electric charge and currents immersed in an electromagnetic field. Then, the more general [integral form](classical-electromagnetism:principles:integral)[^integral-to-differential] is presented for [control volume](classical-electromagnetism:principles:integral:control-volume), at rest w.r.t. the observer - an inertial one? - and then derived form [arbitrary domains](classical-electromagnetism:principles:integral:arbitrary-volume), using the [rules for time derivatives of integrals over moving domains](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/time-derivative-of-integrals.html), and this description is used to have a first discussion about relativity in electromagnetism.

[^integral-to-differential]: As in continuum mechanics, integral equations are the most general form of the equations that governs the global behavior of a system and requires no assumption of regularity of the physical quantities involved. Under the assumptions of regularity, differential equations can be derived from integral equations using theorems of calculus involving differential operators of the fields: differential equations provide local balances. If the fields are piece-wise regular in different regions of the domain, it's possible to derive and use differenial equations in each sub-domain, and link them through jump conditions.




(classical-electromagnetism:principles:differential)=
## Principles in Differential Form

The principles in differential form can be derived from the more general [integral form](classical-electromagnetism:principles:integral), provided the fields satisfy the necessary minimal regularity conditions, which can be qualitatively stated as "all operations must make sense."

**Conservation of Electric Charge.** Differential form of conservation of electric charge is described by a continuity equation for the electric charge density $\rho(\vec{r},t)$, with electric current $\vec{j} = \rho \vec{v}$ as the flux - where $\vec{v}(\vec{r},t)$ is the average velocity of the charges in the point $\vec{r}$ of space at time $t$

$$\partial_t \rho + \nabla \cdot \vec{j} = 0 \ .$$

**Maxwell's Equations.** Maxwell's equations give the relations between the electric charge and current densities, with the electromagnetic field $\vec{e}(\vec{r}, t)$, $\vec{b}(\vec{r},t)$,

$$\begin{cases}
 \nabla \cdot \vec{e} = \frac{\rho}{\varepsilon_0} \\
 \nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\ 
 \nabla \cdot \vec{b} = 0 \\
 \nabla \times \vec{b} - \varepsilon_0 \mu_0 \, \partial_t \vec{e} = \mu_0 \vec{j}  \ ,\\
\end{cases}$$

with the **permittivity of free space** - or the **dielectric constant of free space** - $\varepsilon_0$ and the **permeability of the free space**, $\mu_0$ 

$$\begin{aligned}
  \varepsilon_0 & = 8.85 \cdot 10^{-12} \, \text{F}\, \text{m}^{-1} \\
          \mu_0 & = 4 \pi \cdot 10^{-7} \, \text{N}\, \text{A}^{-2} \\
\end{aligned}$$

<!--
with the need to define constitutive equations $\vec{d}(\vec{e}, \vec{b})$, $\vec{h}(\vec{e}, \vec{b})$.
-->

**Lorentz Force.** The force per unit volume acting on the electric charges at point $\vec{r}$ and time $t$ is governed by differential form of Lorent'z force

$$\begin{aligned}
  \vec{f}(\vec{r},t) & = \rho(\vec{r},t) \, \vec{e}(\vec{r},t) + \vec{j}(\vec{r},t) \times \vec{b}(\vec{r},t) = \\
                           & = \rho(\vec{r},t) \left[ \vec{e}(\vec{r}) + \vec{v}(\vec{r},t) \times \vec{b}(\vec{r},t) \right] =  \\
                           & = \rho^*(\vec{r},t) \, \vec{e}^*(\vec{r},t) 
\end{aligned}$$

having defined $\rho^*{(\vec{r}), t}$ $\vec{e}^*(\vec{r}, t)$ as the current desntiy and the electric field **as seen by the moving charge**

```{admonition} Maxwell's equations and continuity equation of electric charge are overdetermined - proof with differential equations
:class: tip

Introducing (1) the time derivative of Gauss law of the electric field $\vec{e}(\vec{r},t)$ and Ampére-Maxwell law in the continuity equation of the electric charge 

$$\begin{aligned}
  0 & = \partial_t \rho + \nabla \cdot \vec{j} = && (1) \\
    & = \varepsilon_0 \partial_t \nabla \cdot \vec{e} + \nabla \cdot \left(\dfrac{1}{\mu_0}\nabla \times \vec{b} - \varepsilon_0 \partial_t \vec{e} \right) = && (2) \\
    & = 0
\end{aligned}$$

an identity appears as (2) the divergence of a curl is identically equal to zero. Thus, these equations are not linearly independent and the system is over-determined.
```

(classical-electromagnetism:principles:integral)=
## Principles in Integral Form: Electromagnetic Equations and Galilean Relativity

(classical-electromagnetism:principles:integral:control-volume)=
### Integral Form on Control Volumes

The integral form of the principles of electromagnetism for fixed volumes $V$ and surfaces $S$ in space is obtained by integrating the differential equations over the domains and using the divergence theorem to obtain flux terms, and Stokes' theorem to obtain circulation terms.

**Continuity of Electric Charge.**

$$\begin{aligned}
    \dfrac{d}{dt} \int_{V} \rho + \oint_{\partial V} \vec{j} \cdot \hat{n} & = 0 \\ \\
    \dfrac{d}{dt} Q_V + \Phi_{\partial V}\left( \vec{j} \right) & = 0
\end{aligned}$$

**Gauss's Law for the Field $\vec{e}(\vec{r},t)$.**

$$\begin{aligned}
    \oint_{\partial V} \vec{e} \cdot \hat{n} & = \int_{V} \frac{\rho}{\varepsilon_0} \\ \\
    \Phi_{\partial V}(\vec{e}) & = \frac{Q_V}{\varepsilon_0}
\end{aligned}$$

**Gauss's Law for the Field $\vec{b}(\vec{r},t)$.**

$$\begin{aligned}
    \oint_{\partial V} \vec{b} \cdot \hat{n} & = 0 \\  \\
    \Phi_{\partial V}\left( \vec{b} \right) & = 0
\end{aligned}$$

**Faraday–Neumann–Lenz Law for Electromagnetic Induction.**

$$\begin{aligned}
    \oint_{\partial S} \vec{e} \cdot \hat{t} + \dfrac{d}{dt} \int_{S} \vec{b} \cdot \hat{n} & = 0 \\  \\
    \Gamma_{S} \left( \vec{e} \right) + \dfrac{d}{dt} \Phi_{S} \left( \vec{b} \right) & = 0
\end{aligned}$$

**Ampère–Maxwell Law.**

$$\begin{aligned}
    \oint_{\partial S} \vec{b} \cdot \hat{t} - \dfrac{d}{dt} \int_{S} \varepsilon_0 \mu_0 \, \vec{e} \cdot \hat{n} & = \int_{S} \mu_0 \, \vec{j} \cdot \hat{n} \\ \\
    \Gamma_{\partial S} \left( \vec{b} \right) - \frac{1}{c_0^2} \dfrac{d}{dt} \Phi_{S} \left( \vec{e} \right) & = \mu_0 \Phi_{S} \left( \vec{j} \right) \ ,
\end{aligned}$$

having introduced the speed of velocity in free space, $c_0 = \dfrac{1}{\sqrt{\varepsilon_0 \mu_0}}$.

```{admonition} Maxwell's equations and continuity equation of electric charge are overdetermined - proof with integral equations
:class: tip

Introducing (1) the time derivative of Gauss law of the electric field $\vec{e}(\vec{r},t)$ and (2) the Ampére-Maxwell law in the continuity equation of the electric charge 

$$\begin{aligned}
  0 & = \dot{Q}_V + \Phi_{\partial V}\big( \vec{j} \big) = && (1) \\
    & = \varepsilon_0 \dot{\Phi}_{\partial V}\big( \vec{e} \big) + \Phi_{\partial V}\big( \vec{j} \big) =\\
    & = \frac{1}{\mu_0} \left[ \mu_0 \varepsilon_0 \dot{\Phi}_{\partial V}\big( \vec{e} \big) + \mu_0 \Phi_{\partial V}\big( \vec{j} \big)\right] =  && (2) \\
    & = \frac{1}{\mu_0} \Gamma_{\partial \partial V} \big( \vec{b} \big) = 0 \ ,
\end{aligned}$$

an identity appears as the contour $\partial S$ of a closed surface $S = \partial V$ has zero dimension. Thus, these equations are not linearly independent and the system is over-determined.
```

(classical-electromagnetism:principles:integral:arbitrary-volume)=
### Integral Form on Arbitrary Volumes

Due to their importance in fundamental applications such as electric motors, and to avoid confusion or leaps in logic when dealing with electromagnetic induction, it is crucial to provide the correct expression of the electromagnetic principles when moving volumes are involved in space. Not only is the form of these principles shown, but also the correct procedure to derive them starting from the fixed-control-volume version. This is done using rules for [time derivative for fundamental integrals over moving domains](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/time-derivative-of-integrals.html), such as the integral of a density function over a volume, the flux of a vector field through a surface, or the circulation along a curve.

These three derivative rules are listed here and proved in the material about [Mathematics](https://basics2022.github.io/bbooks-math-miscellanea/intro.html):Vector and Tensor Algebra and Calculus:[Time derivatives of integrals over moving domains](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/time-derivative-of-integrals.html)

$$\begin{aligned}
  \dfrac{d}{dt} \int_{v_t} f & = \int_{v_t} \dfrac{\partial f}{\partial t} + \oint_{\partial v_t} f \, \vec{v}_b \cdot \hat{n} & \text{(density)} \\
  \dfrac{d}{dt} \int_{s_t} \vec{f} \cdot \hat{n} & = \int_{s_t} \dfrac{\partial \vec{f}}{\partial t} \cdot \hat{n} + \int_{s_t} \nabla \cdot \vec{f} \, \vec{v}_b \cdot \hat{n} - \oint_{\partial s_t} \vec{v}_b \times \vec{f} \cdot \hat{t} & \text{(flux)} \\
  \dfrac{d}{dt} \int_{\ell_t} \vec{f} \cdot \hat{t} & = \int_{\ell_t} \dfrac{\partial \vec{f}}{\partial t} \cdot \hat{t} + \int_{\ell_t} \nabla \times \vec{f} \, \cdot \, \vec{v}_b \times \hat{t} + \vec{f}_B \cdot \vec{v}_B - \vec{f}_A \cdot \vec{v}_A & \text{(circulation)}
\end{aligned}$$

**Continuity of Electric Charge.**

$$\begin{aligned}
   0 & = \dfrac{d}{dt} \int_{V} \rho + \oint_{\partial V} \vec{j} \cdot \hat{n} = \\
   & = \dfrac{d}{dt} \int_{v_t} \rho - \oint_{\partial v_t } \rho \vec{v}_b \cdot \hat{n} + \oint_{\partial v_t} \vec{j} \cdot \hat{n} 
\end{aligned}$$

$$
    \dfrac{d}{dt} \int_{v_t} \rho + \oint_{\partial v_t} \underbrace{\rho (\vec{v} - \vec{v}_b)}_{\vec{j}^*} \cdot \hat{n} 
$$

**Gauss's Law for the Field $\vec{e}(\vec{r},t)$.**

$$
    \oint_{\partial v_t} \vec{e} \cdot \hat{n} = \int_{v_t} \dfrac{\rho}{\varepsilon_0}
$$

**Gauss's Law for the Field $\vec{b}(\vec{r},t)$.**

$$
    \oint_{\partial v_t} \vec{b} \cdot \hat{n} = 0
$$

**Faraday–Neumann–Lenz Law for Electromagnetic Induction.**

$$\begin{aligned}
   \vec{0} & = \oint_{\partial S} \vec{e} \cdot \hat{t} + \dfrac{d}{dt} \int_{S} \vec{b} \cdot \hat{n} = \\
    & = \oint_{\partial s_t} \vec{e} \cdot \hat{t} + \dfrac{d}{dt} \int_{s_t} \vec{b} \cdot \hat{n} - \int_{s_t} \underbrace{\nabla \cdot \vec{b}}_{=0} \, \vec{v}_b \cdot \hat{n} + \oint_{s_t} \vec{v}_b \times \vec{b} \cdot \hat{t} =  \\
\end{aligned}$$

$$
    \oint_{\partial s_t} \vec{e}^* \cdot \hat{t} + \dfrac{d}{dt} \int_{s_t} \vec{b} \cdot \hat{n} \ ,
$$
with the definition $\vec{e}^* := \vec{e} + \vec{v}_b \times \vec{b}$, already used in the expression of the Lorentz force law.

**Ampère–Maxwell Law.**

$$\begin{aligned}
    \vec{0} & = \oint_{\partial S} \vec{b} \cdot \hat{t} - \varepsilon_0 \mu_0 \dfrac{d}{dt} \int_{S}  \vec{e} \cdot \hat{n} - \int_{S} \mu_0 \vec{j} \cdot \hat{n} = \\
    & = \oint_{\partial s_t} \vec{b} \cdot \hat{t} - \varepsilon_0 \mu_0 \dfrac{d}{dt} \int_{s_t} \vec{e} \cdot \hat{n} + \varepsilon_0 \mu_0 \int_{s_t} \underbrace{\nabla \cdot \vec{e}}_{=\frac{\rho}{\varepsilon_0}} \, \vec{v}_b \cdot \hat{n} - \varepsilon_0 \mu_0 \oint_{s_t} \vec{v}_b \times \vec{e} \cdot \hat{t} -  \mu_0 \int_{s_t} \vec{j} \cdot \hat{n} =  \\
\end{aligned}$$

$$
    \oint_{\partial s_t} \vec{b}^{* *} \cdot \hat{t} - \varepsilon_0 \mu_0 \dfrac{d}{dt} \int_{s_t} \vec{e} \cdot \hat{n} = \mu_0 \int_{s_t} \vec{j}^{*} \cdot \hat{n} \ ,
$$

having defined $\vec{b}^{* *} := \vec{b} - \dfrac{\vec{v}_b \times \vec{e}}{c^2}$, and $\vec{j}^{*} := \vec{j} - \rho \vec{v}_b$.

The definition of fields

$$\begin{aligned}
     \rho^*     & = \\
  \vec{j}^*     & = \\
  \vec{e}^*     & = \\
  \vec{b}^{* *} & = \\
\end{aligned}$$

provides nothing more than the transformation of the fields for two observers in relative motion, and correspond to the **low-speed limit** of [Lorentz transformations from special relativity](https://basics2022.github.io/bbooks-physics-modern/ch/relativity-special/lorentz.html#inertial-reference-frames-and-lorentz-s-transformations) for velocities $|\vec{v}_b| \ll c$, and Lorentz's factor $\gamma \sim 1$: in this procedure, the transformations for low relative speeds are obtained, as no transformation of spatial and temporal dimensions has been considered, unlike Einstein's theory of relativity.

While here $\vec{b}$ contains a higher order term, and $\vec{e}$ appears in Ampére-Maxwell's law, a cleaner formulation of low-speed relativity in electromagnetism arises from balance equations of [electromagnetism in matter](classical-electromagnetism:principles:matter).

**todo** Reference Galilean and Lorentz transformations for relativity in electromagnetism.

**todo** Sistematic power expansion

**todo** Take into account higher-order contributions

<!--
$$\begin{aligned}
  \rho^*    & = \rho    - \dfrac{\vec{j}}{c^2} + \text{terms coming from $\gamma c \rho$} \\
  \vec{d}^* & = \vec{d} - \dfrac{\vec{h} \times \vec{v}}{c^2} + \text{terms coming from $(1-\gamma) \hat{v} \hat{v} \cdot \vec{d}$}  \\
  \vec{b}^* & = \vec{b} + \dfrac{\vec{e} \times \vec{v}}{c^2} + \text{terms coming from $(1-\gamma) \hat{v} \hat{v} \cdot \vec{b}$}  \\
\end{aligned}$$

**todo** Relativity of polarization and magnetization

$$\begin{aligned}
  \vec{p} 
  := & \  \vec{d} - \varepsilon_0 \vec{e} = \\
   = & \  \vec{d}^* + \dfrac{\vec{h} \times \vec{v}}{c^2} - \varepsilon_0 \left( \vec{e}^* + \vec{b} \times \vec{v} \right) = \\
   = & \  \vec{d}^* - \varepsilon_0 \vec{e}^* + \left( \dfrac{\vec{h}}{c^2} - \varepsilon_0 \vec{b} \right) \times \vec{v} = \\ 
   = & \  \vec{p}^* - \dfrac{ \vec{m} \times \vec{v}}{c^2} \ .
\end{aligned}$$

$$\begin{aligned}
  \vec{m} 
  := & \ \dfrac{1}{\mu_0} \vec{b} - \vec{h} = \\
   = & \ \dfrac{1}{\mu_0} \vec{b}^* + \dfrac{1}{\mu_0} \dfrac{\vec{v} \times \vec{e}}{c^2} - \vec{h}^* - \vec{v} \times \vec{d} = \\ \\
   = & \ \vec{m}^* - \vec{v} \times \vec{p} \ .
\end{aligned}$$
-->
