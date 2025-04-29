(classical-electromagnetism:electrostatics)=
# Electrostatics

Elextrostatics studies the electric phenomena in systems with stationary charges. Thus, current is identically zero $\vec{j} = \vec{0}$.


So far, random topics

- governing equations of electrostatics
- zero electric field insiede a conductor

## Governing equation of electrostatics

Electrostatics studies systems with no motion of charges, and thus no currents, $\vec{j} = \vec{0}$, and time dependency, $\partial_t \equiv 0$.

**Maxwell's equations.**

  $$\begin{cases}
    \nabla \cdot \vec{e} = \dfrac{\rho}{\varepsilon_0} \\
    \nabla \times \vec{e} = \vec{0} \\ 
    \nabla \cdot \vec{b} = 0 \\
    \nabla \times \vec{b} = \vec{0}
  \end{cases}$$

**Potentials.**

   $$\begin{aligned}
      \vec{b} & = \nabla \times \vec{a} \\
      \vec{e} & = - \nabla \phi \\
   \end{aligned}$$

As both the divergence and the curl of the magnetic field are zero, only constant and uniform magnetic field are allowed.
In absence of magnetic field, the problem is fully determined by the Gauss' law for the electric field and the steady condition of the Faraday's law, implying that the irrotational electric field can be written as the gradient of a scalar potential,

$$\vec{e} = - \nabla \varphi \ .$$

Introducing this expression into Gauss' law for the electric field, electrostatics can be formulated as a problem governed by a Laplace equation for the scalar potential

$$-\Delta \varphi = \dfrac{\rho}{\varepsilon_0} \ ,$$

supplied with the proper boundary conditions. **todo** *discuss boundary conditions...*


## Zero electric field inside a conductor

Studying the transient of the electric charge distribution inside a conductor,

$$\vec{e} = \rho_R \vec{j} \ ,$$

whose constitutive equation is

$$\vec{d} = \varepsilon \vec{e} \ ,$$

with free electric charge continuity equation

$$\partial_t \rho_f + \nabla \cdot \vec{j}_f = 0 \ ,$$

and Gauss equation for the displacement field 

$$\nabla \cdot \vec{d} = \rho_f \ .$$

$$\begin{aligned}
  \partial_t \rho_f
  & = - \nabla \cdot \vec{j}_f = \\
  & = - \nabla \cdot \left( \frac{1}{\rho_R} \vec{e} \right) = \\
  & = - \frac{1}{\rho_R \varepsilon} \nabla \cdot \vec{d} = \\
  & = - \frac{1}{\rho_R \varepsilon} \rho_f \ ,
\end{aligned}$$

having assumed uniform properties. The differential equation in the volume of the conductor provides the evolution of the electric charge in the volume $\rho(\mathbf{r},t)$, given the initial condition $\rho(\mathbf{r},0) = \rho_{f,0}(\mathbf{r})$

$$\partial_t \rho_f = - \frac{1}{\rho_R \varepsilon} \rho_f$$

$$\rho_f(\mathbf{r},t) = \rho_{f,0}(\mathbf{r}) \exp\left[ - \dfrac{t}{\rho_R \varepsilon} \right] \ .$$

For a conductor:
- $\varepsilon \sim \varepsilon_0 = 8.85 \cdot 10^{-12} \text{F} \text{m}^-1$
- $\rho_R \sim 10^{-7}  \Omega \, \text{m}$

so that the time constant (that can be thought as a characteristic time) of the process is

$$\tau = \rho_R \varepsilon \sim 8.85 \cdot 10^{-19} \, \text{s} \ , $$

and thus, after a very short period of time the volume charge density is approximately zero everywhere in the volume: it accumulates in a very thin surface layer.


```{dropdown} Proof

$$\partial_t \left( \rho_f e^{\frac{t}{\rho_R \varepsilon}} \right) = 0$$

$$\rho_f(\mathbf{r},t) e^{\frac{r}{\rho_R \varepsilon}} = a(\mathbf{r})$$

and appylying initial conditions in all the points of the domain, $\rho_{f}(\mathbf{r},0) = \rho_{f,0}(\mathbf{r})$, function $a(\mathbf{r})$ must be equal to $\rho_{f,0}(\mathbf{r})$ and the solution reads

$$\rho_f(\mathbf{r},t) = \rho_{f,0}(\mathbf{r}) \exp \left[ -\dfrac{t}{\rho_R \varepsilon} \right]$$

```




