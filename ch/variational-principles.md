(classical-electromagnetism:variational-principles)=
# Variational principles in electromagnetism

```{dropdown} Contents

* Particle in a prescribed electromagnetic field

* Field equations: Maxwell equations

* Particle-field equations: charged particles creating electromagnetic field and moving subject to electromagnetic force (i.e. Lorentz force)

```

(classical-electromagnetism:variational-principles:particle-motion-in-prescribed-field)=
## Particle in a prescribed electromagnetic field

For the equations in special relativity, see [Math: Examples of calculus of variations: Lagrange equations in special relativity](https://basics2022.github.io/bbooks-math-miscellanea/ch/calculus-variations/examples.html#lagrange-equations-in-special-relativity).

Starting from the equation of motion of a charged particle in an electromagnetic field

$$m \ddot{\mathbf{r}} = q \left( \mathbf{e}(\mathbf{r}, t) - \mathbf{b}(\mathbf{r},t) \times \dot{\mathbf{r}} \right) \ ,$$

with $\mathbf{r}(t)$ representing the position of the point particle. Using the definition of the electromangetic potentials, $\mathbf{b} = \nabla \times \mathbf{a}$, $\mathbf{e} = - \nabla \varphi - \partial_t \mathbf{a}$, multiplying by a test function $\delta \mathbf{r}$, and using integration by parts,

$$\begin{aligned}
  0 
  & = \delta \mathbf{r} \cdot \left\{ m \ddot{\mathbf{r}} - q \mathbf{e} + q \mathbf{b} \times \dot{\mathbf{r}} \right) = && \text{(1)} \\
  & = d_t \left( \delta \mathbf{r} \cdot m \dot{\mathbf{r}} \right) - \delta \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} + q \left[ \delta \mathbf{r} \cdot \nabla \varphi + \delta \mathbf{r} \cdot \partial_t \mathbf{a} + \delta \mathbf{r} \cdot \left( \nabla \times \mathbf{a} \right) \times \dot{\mathbf{r}} \right] = && \text{(2)} \\
  & = d_t \left( \delta \mathbf{r} \cdot m \dot{\mathbf{r}} \right) - \delta \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} + q \left[ \delta \mathbf{r} \cdot \nabla \varphi + \delta \mathbf{r} \cdot d_t \mathbf{a} - \delta \mathbf{r} \cdot \nabla \mathbf{a} \cdot \dot{\mathbf{r}} \right] = \\
  & = d_t \left( \delta \mathbf{r} \cdot m \dot{\mathbf{r}} \right) - \delta \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} + q \delta \mathbf{r} \cdot \nabla \varphi + q d_t \left( \delta \mathbf{r} \cdot \mathbf{a} \right) - q \delta \dot{\mathbf{r}} \cdot \mathbf{a} - q \delta \mathbf{r} \cdot \nabla \mathbf{a} \cdot \dot{\mathbf{r}} = \\
  & = d_t \left\{ \delta \mathbf{r} \cdot \left( m \dot{\mathbf{r}} + q \mathbf{a} \right) \right\} + \delta \left\{ - \dfrac{1}{2} m |\dot{\mathbf{r}}|^2 + q \left( \varphi - \mathbf{a} \cdot \dot{\mathbf{r}} \right) \right\} \ .
\end{aligned}$$

With prescribed extreme points of the trajectory $\delta \mathbf{r}(t_0) = \delta \mathbf{r}(t_1) = \mathbf{0}$, the equations of motion follows from the principle of stationariety of the action integral,

$$0 = \delta S = \delta \int_{t_0}^{t_1} \mathcal{L} \, d t = \delta \int_{t_0}^{t_1} \left\{ \dfrac{1}{2} m |\dot{\mathbf{r}}|^2 - q \left( \varphi - \mathbf{a} \cdot \dot{\mathbf{r}} \right) \right\} \, d t \ ,$$

being $\mathcal{L}$ the Lagrangian function.

```{dropdown} Details

$\text{(1)}$ electromagnetic field as a function of the electromagnetic potentials

$\text{(2)}$, as $\mathbf{r}(t)$, thus

$$d_t \mathbf{a}(\mathbf{r}(t), t) = \partial_t \mathbf{a} + \dot{\mathbf{r}} \cdot \nabla \mathbf{a} \ .$$

The vector product of $\dot{\mathbf{r}}$ with the curl of $\mathbf{a}$ can be recast using vector identity

$$\begin{aligned}
  \dot{\mathbf{r}} \times \left( \nabla \times \mathbf{a} \right) 
  & = \hat{\mathbf{e}}_i \varepsilon_{ijk} \dot{r}_j \varepsilon_{klm} \partial_l a_m = \\
  & = \hat{\mathbf{e}}_i \dot{r}_j \left( \delta_{il} \delta_{jm} - \delta_{im} \delta_{jl} \right) \partial_l a_m = \\
  & = \hat{\mathbf{e}}_i \left( \dot{r}_m \partial_i a_m - \dot{r}_{m} \partial_m a_i \right) = \\
  & = \nabla \mathbf{a} \cdot \dot{\mathbf{r}} - \dot{\mathbf{r}} \cdot \nabla \mathbf{a} \ .
\end{aligned}$$

```

**Lagrange equations without using the principle of stationariety of the action.** Using generalized coordinates $q^k(t)$ to write the position of the point particle $\mathbf{r}(q^k(t), t)$, the velocity becomes

$$\dot{\mathbf{r}} = \dot{q}^k \partial_{q^k} \mathbf{r} + \partial_t \mathbf{r} \ ,$$

so that $\partial_{\dot{q}^k} \dot{\mathbf{r}} = \partial_{q^k} \mathbf{r}$. Using the test function $\delta \mathbf{r} = \partial_{q^k} \mathbf{r}$,

$$\begin{aligned}
  0
  & = \partial_{q^k} \mathbf{r} \cdot \left\{ m \ddot{\mathbf{r}} - q \mathbf{e} + q \mathbf{b} \times \dot{\mathbf{r}} \right) = \\
  & = \partial_{\dot{q}^k} \dot{\mathbf{r}} \cdot m \ddot{\mathbf{r}} + \partial_{q^k} \mathbf{r} \cdot \left\{  - q \mathbf{e} + q \mathbf{b} \times \dot{\mathbf{r}} \right) = \\
  & = \dfrac{d}{dt} \left( \partial_{\dot{q}^k} \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} \right) - \partial_{q^k} \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} + \partial_{q^k} \mathbf{r} \cdot \left\{ q \nabla \varphi + q \partial_t \mathbf{a} + q ( \nabla \times \mathbf{a} ) \times \dot{\mathbf{r}} \right\} = \\
  & = \dfrac{d}{dt} \left( \partial_{\dot{q}^k} \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} \right) - \partial_{q^k} \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} + \partial_{q^k} \mathbf{r} \cdot \left\{ q \nabla \varphi + q \dot{ \mathbf{a} } - q \nabla \mathbf{a} \times \dot{\mathbf{r}} \right\} = \\
  & = \dfrac{d}{dt} \left( \partial_{\dot{q}^k} \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} \right) - \partial_{q^k} \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} + \dfrac{d}{dt} \left( q \partial_{q^k} \mathbf{r} \cdot \mathbf{a} \right) + \partial_{q^k} \mathbf{r} \cdot \left\{ q \nabla \varphi - q \nabla \mathbf{a} \times \dot{\mathbf{r}} \right\} - q \partial_{q^k} \dot{\mathbf{r}} \cdot \mathbf{a} = \\
  & = \dfrac{d}{dt} \left\{ \partial_{\dot{q}^k} \dot{\mathbf{r}} \cdot \left( m \dot{\mathbf{r}} +  q \mathbf{a} \right) \right\} - \partial_{q^k} \dot{\mathbf{r}} \cdot m \dot{\mathbf{r}} + \partial_{q^k} \mathbf{r} \cdot \left\{ q \nabla \varphi - q \nabla \mathbf{a} \times \dot{\mathbf{r}} \right\} - q \partial_{q^k} \dot{\mathbf{r}} \cdot \mathbf{a} = \\
  & = \dfrac{d}{dt} \dfrac{\partial}{\partial \dot{q}^k} \left\{ \frac{1}{2} m | \dot{\mathbf{r}} |^2 +  q \mathbf{a} \cdot \dot{\mathbf{r}} \right\} - \dfrac{\partial}{\partial q^k} \left\{ \dfrac{1}{2} m |\dot{\mathbf{r}}|^2 - q \varphi + q \mathbf{a} \cdot \dot{\mathbf{r}} \right\} \ .
\end{aligned}$$

as 

$$\partial_{q^k} \left( \mathbf{a} \cdot \dot{\mathbf{r}} \right) = \partial_{q^k} \mathbf{r} \cdot \nabla \mathbf{a} \cdot \dot{\mathbf{r}} + \mathbf{a} \cdot \partial_{q^k} \dot{\mathbf{r}} \ .$$

As $q \varphi(\mathbf{r},t)$ doesn't depend on $\dot{q}^k$, it's possible to defined the Lagrangian function 

$$\mathcal{L}(\dot{q}^k, q^k, t) := \dfrac{1}{2} m |\dot{\mathbf{r}}|^2 + q \mathbf{a}(\mathbf{r},t) \cdot \dot{\mathbf{r}} - q \varphi(\mathbf{r},t) \ ,$$

so that the equation of motion can be written as the common Lagrange equations

$$\dfrac{d}{dt}\dfrac{\partial \mathcal{L}}{\partial \dot{q}^k} - \dfrac{\partial \mathcal{L}}{\partial q^k} = 0 \ . $$

**Generalized momentum.**

$$p_k := \dfrac{\partial \mathcal{L}}{\partial \dot{q}^k} = m \partial_{\dot{q}^k} \dot{\mathbf{r}} \cdot \dot{\mathbf{r}} + q \mathbf{a} \cdot \partial_{\dot{q}^k} \mathbf{r} \ .$$

If the generalized coordinates are the position vector $\mathbf{r}$ itself, then

$$\mathbf{p} = m \dot{\mathbf{r}} + q \mathbf{a} \ .$$

**Hamiltonian function.**

$$\mathcal{H} := \mathbf{p} \cdot \dot{\mathbf{q}} - \mathcal{L} = \dfrac{1}{2} m |\dot{\mathbf{r}}|^2 + q \varphi \ .$$

(classical-electromagnetism:variational-principles:field-equations)=
## Field equations

```{dropdown} Equations of the electromagnetism
:open:

**Maxwell's equation.**

$$\left\{
\begin{aligned}
  & \nabla \cdot \mathbf{d} = \rho_f \\
  & \nabla \times \mathbf{e} + \partial_t \mathbf{b} = \mathbf{0} \\
  & \nabla \cdot \mathbf{b} = 0 \\
  & \nabla \times \mathbf{h} - \partial_t \mathbf{d} = \mathbf{j}_f
\end{aligned}
\right.$$

**Continuity equation.**

$$\partial_t \rho + \nabla \cdot \mathbf{j} = 0$$

**Electromagnetic potentials.**

$$\begin{aligned}
  \mathbf{b} & = \nabla \times \mathbf{a} \\
  \mathbf{e} & = - \nabla \varphi - \partial_t \mathbf{a}
\end{aligned}$$

```

Using the electromagnetic potentials, $\mathbf{a}$, $\varphi$,

$$\begin{aligned}
 0
 & = \delta u \, \left\{ \nabla \cdot \left( - \nabla \varphi - \partial_t \mathbf{a} \right) - \frac{\rho}{\varepsilon_0} \right\} + \delta \mathbf{v} \cdot \left( \nabla \times \nabla \times \mathbf{a} - \varepsilon_{0} \mu_0 \partial_t \left( -\nabla \varphi - \partial_t \mathbf{a} \right) - \mu_0 \mathbf{j} \right) = \\
 & = - \nabla \cdot \left\{ \delta u \left( \nabla \varphi + \partial_t \mathbf{a} \right) \right\} + \nabla \delta u \cdot \nabla \varphi + \nabla \delta u \cdot \partial_t \mathbf{a} - \delta u \dfrac{\rho}{\varepsilon_0} + \\
 & \quad + \nabla \cdot \left\{ \left( \nabla \times \mathbf{a} \right) \times \delta \mathbf{v} \right\} + \nabla \times \delta \mathbf{v} \cdot \nabla \times \mathbf{a} + \dfrac{1}{c_0^2} \partial_t \left\{ \delta \mathbf{v} \cdot \left( \nabla \varphi + \partial_t \mathbf{a} \right) \right\} - \dfrac{1}{c_0^2} \partial_t \delta \mathbf{v} \cdot \nabla \varphi - \dfrac{1}{c_0^2} \partial_t \delta \mathbf{v} \cdot \partial_t \mathbf{a} - \mu_0 \delta \mathbf{v} \cdot \mathbf{j} \ .
\end{aligned}$$

```{dropdown} Details

$$\begin{aligned}
  \delta \mathbf{v} \cdot \nabla \times \nabla \times \mathbf{a}
  & = \delta v_i \varepsilon_{ijk} \partial_j \varepsilon_{klm} \partial_l a_m = \\
  & = \varepsilon_{ijk} \partial_j \left( \delta v_i \varepsilon_{klm} \partial_{l} a_m \right) - \varepsilon_{ijk} \partial_j \delta v_i \, \varepsilon_{klm} \partial_{l} a_m  \\
  & = \nabla \cdot \left( \left( \nabla \times \mathbf{a} \right) \times \delta \mathbf{v} \right) + \nabla \times \delta \mathbf{v} \cdot \nabla \times \mathbf{a} 
\end{aligned}$$

```

If $\delta u = \varepsilon_0 \delta \varphi$, and $\delta \mathbf{v} = -\frac{1}{\mu_0} \delta \mathbf{a}$,

$$\begin{aligned}
 0
 & = - \nabla \cdot \left\{ \varepsilon_0 \delta \varphi \left( \nabla \varphi + \partial_t \mathbf{a} \right) \right\} + \varepsilon_0 \nabla \delta \varphi \cdot \nabla \varphi + \varepsilon_0 \nabla \delta \varphi \cdot \partial_t \mathbf{a} - \delta \varphi \, \rho + \\
 & \quad - \dfrac{1}{\mu_0} \nabla \cdot \left\{ \left( \nabla \times \mathbf{a} \right) \times \delta \mathbf{a} \right\} - \dfrac{1}{\mu_0} \nabla \times \delta \mathbf{a} \cdot \nabla \times \mathbf{a}  - \varepsilon_0 \partial_t \left\{ \delta \mathbf{a} \cdot \left( \nabla \varphi + \partial_t \mathbf{a} \right) \right\} + \varepsilon_0 \partial_t \delta \mathbf{a} \cdot \nabla \varphi + \varepsilon_0 \partial_t \delta \mathbf{a} \cdot \partial_t \mathbf{a} + \delta \mathbf{a} \cdot \mathbf{j} = \\
 & = \nabla \cdot \left\{ \dots \right\} + \partial_t \left\{ \dots \right\} + \delta \left\{  \varepsilon_0 \left[ \dfrac{|\nabla \varphi|^2}{2} + \nabla \varphi \cdot \partial_t \mathbf{a} + \dfrac{|\partial_t \mathbf{a}|}{2} \right] - \dfrac{1}{\mu_0} | \nabla \times \mathbf{a} |^2 \right\} - \delta \varphi \rho + \delta \mathbf{a} \cdot  \mathbf{j} \ .
\end{aligned}$$

The content of the curly bracket can be defined as the field Lagrangian function,

$$\begin{aligned}
  \mathcal{L}_{field}(\varphi, \mathbf{a}, \partial_t \varphi, \partial_t \mathbf{a}, \partial_k \varphi, \partial_k \mathbf{a} )
  & := \varepsilon_0 \left[ \dfrac{|\nabla \varphi|^2}{2} + \nabla \varphi \cdot \partial_t \mathbf{a} + \dfrac{|\partial_t \mathbf{a}|^2}{2} \right] - \dfrac{1}{\mu_0} \dfrac{| \nabla \times \mathbf{a} |^2}{2} = \\ 
  & = \dfrac{1}{2} \left[ \varepsilon_0 | \mathbf{e} |^2 - \dfrac{1}{\mu_0} | \mathbf{b} |^2 \right] \ .
\end{aligned}$$

The last two contributions can defined as the Lagrangian function of the interaction between prescribed charge and current densities with the electromagnetic field

$$\mathcal{L}_{inter} = - \varphi \rho + \mathbf{a} \cdot \mathbf{j} \ .$$

If charge and current densities are not prescribed, then the full variation of this contribution produces the continuous counterpart of the equations of motion for charges subject to Lorentz force,

$$m D_t \mathbf{u} = \rho \left( \mathbf{e} - \mathbf{b} \times \mathbf{u} \right) \ ,$$

with $m$ the charge mass density, and $\mathbf{u}(\mathbf{r},t)$ the velocity field of the continuous charge distribution, and $D_t = \partial_t + \mathbf{u} \cdot \nabla$ the total derivative.

**Generalized momentum.** 

$$\begin{aligned}
  \Pi_{\varphi} := \dfrac{\partial \mathcal{L}_{field}}{\partial (\partial_t \varphi)} & = 0 \\
  \dfrac{\partial \mathcal{L}_{field}}{\partial (\partial_k \varphi)} & = \varepsilon_0 \left( \partial_k \varphi + \partial_t a_k \right) = - \varepsilon_0 \left\{ \mathbf{e} \right\}_k \\
  \Pi_{a_i} := \dfrac{\partial \mathcal{L}_{field}}{\partial (\partial_t a_i)} & = \varepsilon_0 \left( \partial_i \varphi + \partial_t a_i \right) = - \varepsilon_0 \left\{ \mathbf{e} \right\}_i \\
  \dfrac{\partial \mathcal{L}_{field}}{\partial (\partial_k a_i)} & = - \dfrac{1}{\mu_0} \left( \partial_k a_i - \partial_i a_k \right) = - \dfrac{1}{\mu_0} \left\{ \mathbf{b}_{\times} \right\}_{ik} \ .
\end{aligned}$$

```{dropdown} Details

$$\begin{aligned}
  2 \dfrac{\partial \mathcal{L}}{\partial (\partial_k a_i)}
  & = - \dfrac{1}{\mu_0} \dfrac{\partial}{\partial (\partial_k a_i)} \left( \varepsilon_{abc} \partial_b a_c \right) \left( \varepsilon_{ade} \partial_d a_e \right) = \\
  & = - \dfrac{1}{\mu_0} \left( \varepsilon_{abc} \delta_{kb} \delta_{ic} \varepsilon_{ade} \partial_d a_e + \varepsilon_{abc} \partial_b a_c \varepsilon_{ade} \delta_{dk} \delta_{ei}  \right) = \\
  & = - \dfrac{1}{\mu_0} \left( \varepsilon_{aki} \varepsilon_{ade} \partial_d a_e + \varepsilon_{abc} \partial_b a_c \varepsilon_{aki} \right) = \\
  & = - \dfrac{1}{\mu_0} \left[ \left( \delta_{kd} \delta_{ie} - \delta_{ke} \delta_{id} \right) \partial_d a_e + \left( \delta_{bk} \delta_{ci} - \delta_{bi} \delta_{ck} \right) \partial_b a_c  \right] = \\
  & = - \dfrac{1}{\mu_0} \left[ \partial_k a_i - \partial_i a_k + \partial_k a_i - \partial_i a_k \right] = \\
  & = - \dfrac{2}{\mu_0} \left[ \partial_k a_i - \partial_i a_k \right] = \\
  & = - \dfrac{2}{\mu_0} \varepsilon_{ijk} b_j = \\
  & = - \dfrac{2}{\mu_0} \left\{ \mathbf{b}_{\times} \right\}_{ik} \ .
\end{aligned}$$

as

$$\varepsilon_{ijk} b_j = \varepsilon_{ijk} \varepsilon_{jlm} \partial_l a_m = \left( \delta_{kl} \delta_{im} - \delta_{km} \delta_{il} \right) \partial_l a_m = \partial_k a_i - \partial_i a_k \ .$$

```

**Hamiltonian.**
*uncomment*

<!--
$$\begin{aligned}
  \mathcal{H}
  & = \Pi_{\varphi} \partial_t \varphi + \Pi_{a_i} \partial_{t} a_i - \mathcal{L} = \\
  & = - \varepsilon_0 \mathbf{e} \cdot \partial_t \mathbf{a} - \varepsilon_0 \left[ \dfrac{|\nabla \varphi|^2}{2} + \dfrac{1}{2} \nabla \varphi \cdot \partial_t \mathbf{a} + \dfrac{1}{2} \partial_t \mathbf{a} \cdot \left( \nabla \varphi + \partial_t \mathbf{a} \right) \right] + \dfrac{1}{2\mu_0} | \nabla \times \mathbf{a} |^2 - \mathcal{L}_{inter} = \\
\end{aligned}$$
-->


