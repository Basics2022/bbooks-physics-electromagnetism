(classical-electromagnetism:circuits-electromagnetic)=
# Electromagnetic Circuits

Under appropriate assumptions, it is possible to use a circuit model for electromagnetic systems, such as transformers or electric motors.

- **Gauss's Law for Magnetic Fields:**

  $$\nabla \cdot \vec{b} = 0$$

- **Ampère-Maxwell's Law:**

  $$\nabla \times \vec{h} - \partial_t \vec{d} = \vec{j}$$

Additional assumptions include:
- Linear, non-dissipative, and non-dispersive materials: $\vec{b} = \mu \vec{h}$ <span style="color:red">**todo** discuss this assumption, along with material hysteresis, magnetization cycles, etc.</span>.
- Negligible time variations of the field $\vec{d}$, i.e., $\partial_t \vec{d} = \vec{0}$.

The integral form of Gauss's law for the magnetic field allows writing the **node law** for the magnetic field flux in magnetic circuits:

$$0 = \oint_{\partial V} \vec{b} \cdot \hat{\vec{n}} = \sum_k \phi_k \ .$$

The integral form of Ampère-Maxwell's law, considering:
- A path linked only with the inductor:

  $$\int_{\ell_{ind}} \vec{h} \cdot \hat{\vec{t}} + \int_{\ell_{12}} \vec{h} \cdot \hat{\vec{t}} = \oint_{\ell_{1}} \vec{h} \cdot \hat{\vec{t}} = \int_{S^{ind}} \vec{j} \cdot \hat{\vec{n}} =  N i =: m$$

- A path linked with the air gap, bypassing the inductor:

  $$0 = \int_{\ell_{traf}} \vec{h} \cdot \hat{\vec{t}} + \int_{\ell_{21}} \hat{h} \cdot \hat{\vec{t}} = \sum_{k} h_k \ell_k + \int_{\ell_{21}} \hat{h} \cdot \hat{\vec{t}}$$

By summing these two equations and recognizing that the two line integrals over the same path in opposite directions cancel each other out, we obtain the **loop law** for magnetic circuits:

$$\begin{aligned}
  m & = \int_{\ell_{ind}} \vec{h} \cdot \hat{\vec{t}} + \int_{\ell_{traf}} \vec{h} \cdot \hat{\vec{t}} \\
    & \approx \sum_{k \in \ell} h_k \, \ell_k \\
    & = \sum_{k \in \ell} \frac{b_k}{\mu_k} \, \ell_k \\
    & = \sum_{k \in \ell} \frac{\ell_k}{\mu_k \, A_k} \, \phi_k \ .
\end{aligned}$$

Kirchhoff's laws for magnetic circuits are therefore:

$$\begin{cases}
  \sum_{k \in N_j} \phi_k = 0 \\
  m_{\ell_i} = \sum_{k \in \ell_i} \theta_k \phi_k \ ,
\end{cases}$$

where $\theta_k = \frac{\ell_k}{\mu_k \, A_k}$ is the reluctance, the inverse of the permeance $\Lambda_k = \theta_k^{-1}$.

