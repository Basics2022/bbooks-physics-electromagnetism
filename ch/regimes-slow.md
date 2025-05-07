(classical-electromagnetism:regimes:slow)=
# Slow regime

Slow regime leads to circuit approximations of electromagnetic systems with **moderate dimensions** at **low frequency**. For these systems and regimes, the ratio appearing into [non-dimensional equations of electromagnetism](classical-electromagnetism:regimes:non-dimensional) reads,

$$\dfrac{f L }{c_0} \ll 1 \ .$$

Under this assumption, approximate governing equations of electromagnetism in slow opearint regime is obtained setting $\frac{fL}{c} = 0$ in the non-dimensional equations of the electromagnetism {eq}`eq:em:non-dimensional`,

$$
\begin{aligned}
  & \text{continuity equation for charge}        &&  \partial_t \rho_f +  \nabla \cdot \vec{j}_f = 0 \\ \\
  & \text{Maxwell's equations}                   &&  \nabla \cdot \vec{d} - \rho_f = 0 \\
  &                                              &&  \nabla \times \vec{e} +  \partial_t \vec{b} = \vec{0} \\ 
  &                                              &&  \nabla \cdot \vec{b} = 0 \\
  &                                              &&  \nabla \times \vec{h} = \, \vec{j}_f  \\ \\
  & \text{constitutive equations}                &&  \vec{d} = \vec{e} \\
  &                                              &&  \vec{b} = \vec{h} \\ \\
  & \text{EM potentials}                         &&  \vec{b} = \nabla \times \vec{a} \\
  &                                              &&  \vec{e} = - \nabla \phi - \partial_t \vec{a} \\ \\
  & \text{Lorentz's gauge}                       &&  \nabla \cdot \vec{a} + \partial_t \phi = 0
\end{aligned}
$$ (eq:em:non-dimensional:slow)

<span style="color:red">**todo** *check consistency of $\vec{e} = - \nabla \phi$ with Faraday's induction law $\nabla \cdot \vec{e} + \partial_t \vec{b} = \vec{0}$. [Non-dimensionalization process](classical-electromagnetism:regimes:non-dimensional) could be not 100\% ok yet*</span>

From the approximate governing equations some consequences follow:
- in slow operating regime wave equations can be approximated with Poisson equations: perturbations can't travel anymore in form of waves, while their transmission is governed by a diffusive equation.
    [Wave equations](classical-electromagnetism:waves:wave-equation) becomes Poisson equations, as the wave operator $\square \sim \nabla^2$ if $\left( \frac{L F}{c} \right)^2 \ll 1$, as the non-dimensional form of a wave equation follows from

    $$\begin{aligned}
      \frac{F^2}{c^2} \partial_{tt} f - \dfrac{1}{L^2} \nabla^2 f & = \dots \\
      \dfrac{1}{L^2} \left[ \left( \frac{F L}{c}\right)^2 \partial_{tt} f -  \nabla^2 f \right] & = \dots \\
     - \dfrac{1}{L^2} \nabla^2 f  & \sim \dots 
    \end{aligned}$$

- radiation is negligible in energy balance, as it's shown for [energy balance in circuit approximation](classical-electromagnetism:circuits:energy:boundary)
 


<!--
Under this assumption, the equations of electromagnetism can be approximated as

**Continuity equation of electric charge.**

  $$\partial_t \rho + \nabla \cdot \vec{j} = 0$$

**Maxwell's equations.**

  $$\begin{cases}
    \nabla \cdot \vec{e} = \dfrac{\rho}{\varepsilon_0} \\
    \nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\ 
    \nabla \cdot \vec{b} = 0 \\
    \nabla \times \vec{b} \simeq \mu_0 \vec{j} 
  \end{cases}$$

**Potentials.**

   $$\begin{aligned}
      \vec{b} & = \nabla \times \vec{a} \\
      \vec{e} & \simeq - \nabla \phi \\
   \end{aligned}$$
-->
