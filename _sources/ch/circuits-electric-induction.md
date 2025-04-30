(classical-electromagnetism:circuits-electric:induction)=
# Electromagnetic Induction in Circuit Approximation

It is possible to apply the circuit approximation even in the presence of regions where the term $\partial_t \mathbf{b}$ cannot be neglected, such as in electromagnetic circuits involving transformers, motors, or electric generators.

In these situations, if it is possible to identify a connected region $V_0$ in space where $\partial_t \mathbf{b} = \mathbf{0}$, and therefore $\nabla \times \mathbf{e} = \mathbf{0}$, it is possible to define the electric field in terms of a potential $\varphi$ in $V_0$:

$$\mathbf{e} = - \nabla \varphi \qquad , \qquad \mathbf{r} \in V_0 \ .$$

It is possible to calculate the potential differences at the terminals of a system where $\partial_t \mathbf{b} \ne 0$, enclosed in the volume $V_k$, using Faraday's law:

$$\oint_{\ell_k} \mathbf{e} \cdot \hat{\mathbf{t}} = - \frac{d}{dt} \int_{S_k} \mathbf{b} \cdot \hat{\mathbf{n}} \ ,$$

where the closed path $\ell_k = \ell_k^{cond} \cup \ell_k^{mors}$ describes the conductor in $V_k$ closed by the geometric line between the terminals. If the resistivity of the conductor in $V_k$ can be neglected, $\int_{\ell_k^{cond}} \mathbf{e} \cdot \hat{\mathbf{t}} = 0$, the voltage difference at the terminals is:

$$\Delta v_k = \int_{\ell^{mors}_k} \mathbf{e} \cdot \hat{\mathbf{t}} = - \frac{d}{dt} \int_{S_k} \mathbf{b} \cdot \hat{\mathbf{n}}$$

