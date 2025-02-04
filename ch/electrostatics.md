(classical-electromagnetism:electrostatics)=
# Electrostatics

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




