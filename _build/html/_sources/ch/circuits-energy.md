(classical-electromagnetism:circuits:energy)=
# Energy balance in circuit approximation

Integral balance of electromagnetic energy {eq}`eq:energy:integral:2` reads

$$\dfrac{d}{dt} \int_V u + \int_{V} \vec{e} \cdot \vec{j} = - \oint_{\partial V} \, \phi \vec{j} \cdot \hat{n} + \oint_{\partial V} \hat{n} \cdot \left[ \frac{1}{\mu_0} \partial_t \vec{a} \times \vec{b} + \varepsilon_0 \, \phi\, \partial_t \vec{e} \right] \ .$$

**Volume terms** represent
- time derivative of the electromagnetic energy stored in the system, as an example in capacitors, inductors, air gaps in magnetic components,

  $$U = \sum_{k \in \text{Capacitors}} \dfrac{1}{2} C_k v_k^2 + \sum_{k \in \text{Inductors}} \dfrac{1}{2} L_k i_k^2 + \sum_{k \in \text{Gaps}} \dfrac{1}{2} \theta_k \phi_k^2 \ ,$$

  ...

- other contributions to electric power, like power dissipated in resistors
 
   $$\int_{V_k} \vec{e} \cdot \vec{j} = \int_{V_k} \rho_R \, |\vec{j}|^2 = \rho_{R_k} A_k \ell_k \dfrac{i_k^2}{A_k^2} = \dfrac{\rho_{R_k} \ell_k}{A_k} i_k^2 = R_k i_k^2 \ , $$

   with the constitutive law of Ohm resistors $\vec{e} = \rho_R \vec{j}$, the definition of electric current $i = \int_S \vec{j} \cdot \hat{n} \sim j A$ and resistance $R = \frac{\rho_R \ell}{A}$

**Boundary terms** represent:
- the **"vi"** contribution, that can be re-written as the product of voltage and current intensity at wires of the electric ports, the only "active" interface in circuit approximation

   $$\oint_{\partial V} \phi \vec{j} \cdot \hat{n} = - \sum_{k \in \text{wires}} \phi_k \int_{S_k} \hat{j} \cdot \hat{n} = \sum_{k \in \text{wires}} v_k \, i_k \ ,$$

   having defined the current current entering the system through wire $k$ (assuming equipotential section of the wire, constant $\phi = v_k$ on section $S_k$ of the $k^{th}$ wire), 

    $$i_k = - \int_{S_k} \vec{j} \cdot \hat{n} \ ,$$

    as the unit vector $\hat{n}$ is pointing outwards the boundary of the system.

- a **radiation** term, due to radiation of electromagnetic energy in free-space through the boundary of the domain; this contribution is the dominant contribution making an antenna work, and it's usually negligible for slow regimes of systems of moderate dimensions, as discussed below comparing the order of magnitude of these contributions.

(classical-electromagnetism:circuits:energy:boundary)=
## Boundary terms in circuit approximation

In the limit of [slow regime](classical-electromagnetism:regimes:slow), $\frac{f L}{c_0} \ll 1$, the comparison of the characteristic dimensions of the three boundary contributions gives (with the same abuse of notation used for [non-dimensional equations in electromagnetism](classical-electromagnetism:regimes:non-dimensional), indicating non-dimensional quantities with the same symbols as the dimensional quantities),

$$\begin{aligned}
  - \oint_{\partial V} \phi \, \vec{j} \cdot \hat{n} & = \sum_{k \in \text{wires}} v_k i_k = \Phi I \sum_{k \in \text{wires}} v_k i_k && (1) \\ \\
  \oint_{\partial V} \hat{n} \cdot \frac{1}{\mu_0} \partial_t \vec{a} \times \vec{b} & = S \dfrac{ F A B }{\mu_0} \oint_{\partial \widetilde{V}} \hat{n} \cdot \partial_t \vec{a} \times \vec{b} = S \frac{\Phi B F^2 L}{\mu c^2}  \oint_{\partial \widetilde{V}} \hat{n} \cdot \partial_t \vec{a} \times \vec{b}  && (2) \\ \\
  \oint_{\partial V} \hat{n} \cdot \varepsilon_0 \, \phi\, \partial_t \vec{e} & = S \, \varepsilon F E \Phi \oint_{\partial \widetilde{V}} \hat{n} \cdot \phi\, \partial_t \vec{e} = S \varepsilon \Phi B F^2 L \oint_{\partial \widetilde{V}} \hat{n} \cdot \phi\, \partial_t \vec{e} && (3) \\
\end{aligned}$$

having used results from {eq}`eq:non-dim:c`, namely in (2) $A = \frac{\Phi F L}{c^2}$, and in (3) $ \Phi = E L$, $E = B F L$. As $\varepsilon \mu = \frac{1}{c^2}$, terms (2) and (3) have the same order of magnitude, $\sim S \frac{\Phi B F^2 L}{\mu c^2}$.

<!--
being $E = B f L$, and $\Phi = E L = B f L^2$, $E \Phi = (B f L)^2 L$, and $\varepsilon_0 = \dfrac{1}{\mu_0 c_0^2}$. If the integrals with non-dimensional quantities have the same order of magnitude (and this should occur if the non-dimensional equations are build using reference quantities of the system), the contribution (3) is smaller than the contribution (2) in the slow regime limit, as its $\left( \frac{f L}{c_0} \right)^2 \ll 1$ times the order of magnitude.
-->

Comparing the order of magnitude of terms (1) and (2) (equal to (3)), radiation contributions (2), (3) are negligible if

$$1 \gg \dfrac{S \frac{\Phi B F^2 L}{\mu c^2}}{\Phi I} = \left(\frac{FL}{c}\right)^2 \ ,$$

having used the definition of the characteristic intensity of the magnetic field $B = \mu J L = \mu \frac{I}{S} L$, from {eq}`eq:non-dim:c`. In the limit of slow operating regime for systems of modest dimensions, $\frac{FL}{c} \ll 1$, **radiation is negligible** if compared with the **"vi" power flux at the electric port**. This conclusion is a strong argument in favor of **circuit approximation** of electromagnetic systems of modest dimensions with low characteristic frequencies.



<!--
<span style="color:red">*check if the non-dimensionalization is ok, with $B_{steady} = \mu_0 J L$, $B_{unsteady} = \frac{E}{fL}$*</span>

$$1 \gg \frac{S \frac{B^2 f L}{\mu_0}}{V I} = $$

**todo** <span style="color:red">*check this! Is it ok that the frequency disappears? Term (1) is non-zero but (2) is identically zero for steady regime, $f = 0$. And if it's required to separate steady and unsteady contributions in the discussion of non-dimensional equations*</span>

$$1 \gg \dfrac{S \frac{B^2 f L}{\mu_0}}{VI} = S \dfrac{B^2 f L}{\mu_0 \Phi I} = S \frac{B^2 f L}{\mu_0 B f L^2 I} = S \frac{B}{\mu_0 L I} = S \frac{\mu_0 J L}{\mu_0 L I} = \frac{S J}{I} \ .$$

<span style="color:red">The dimension of the boundary of the domain is proprotional to the square of the linear dimension of the system, $S \sim L_{V}^2$. This inequality holds if the product of the dimension of the boundary of the domain and the characteristic current density $J$ is much smaller than the characteristic current $I$ at the boundary.</span>
-->

<!--
---

$$1 \gg \dfrac{S \frac{B^2 f L}{\mu_0}}{VI} = S \dfrac{\mu_0^2 J^2 L^2 f L}{\mu_0 \Phi I} = S \frac{B^2 f L}{\mu_0 B f L^2 I} = S \frac{B}{\mu_0 L I} = S \frac{\mu_0 J L}{\mu_0 L I} = \frac{S J}{I} \ .$$

-->
