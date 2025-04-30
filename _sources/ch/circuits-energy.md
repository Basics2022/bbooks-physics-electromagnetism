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
- the "VI" contribution, that can be re-written as the product of voltage and current intensity at wires of the electric ports, the only "active" interface in circuit approximation

   $$\oint_{\partial V} \phi \vec{j} \cdot \hat{n} = - \sum_{k \in \text{wires}} \phi_k \int_{S_k} \hat{j} \cdot \hat{n} = \sum_{k \in \text{wires}} v_k \, i_k \ ,$$

   having defined the current current entering the system through wire $k$ (assuming equipotential section of the wire, constant $\phi = v_k$ on section $S_k$ of the $k^{th}$ wire), 

    $$i_k = - \int_{S_k} \vec{j} \cdot \hat{n} \ ,$$

    as the unit vector $\hat{n}$ is pointing outwards the boundary of the system.

- a radiation term, due to radiation of electromagnetic energy in free-space through the boundary of the domain; this contribution is the dominant contribution making antenna wokr, and it's usually negligible for slow regimes of systems of moderate dimensions, as discussed below comparing the order of magnitude of these contributions.

(classical-electromagnetism:circuits:energy:boundary)=
## Boundary terms in circuit approximation

In the limit of [slow regime](classical-electromagnetism:regimes:slow), $\frac{f L}{c_0} \ll 1$, the comparison of the characteristic dimensions of the three boundary contributions gives

$$\begin{aligned}
  - \oint_{\partial V} \phi \, \vec{j} \cdot \hat{n} & = \sum_{k \in \text{wires}} v_k i_k = V I \sum_{k \in \text{wires}} v_k i_k && (1) \\
  \oint_{\partial V} \hat{n} \cdot \frac{1}{\mu_0} \partial_t \vec{a} \times \vec{b} & = S \dfrac{ f A B }{\mu_0} \oint_{\partial \widetilde{V}} \hat{n} \cdot \partial_t \vec{a} \times \vec{b} = S \dfrac{B^2 f L}{\mu_0}  \oint_{\partial \widetilde{V}} \hat{n} \cdot \partial_t \vec{a} \times \vec{b}  && (2) \\
  \oint_{\partial V} \hat{n} \cdot \varepsilon_0 \, \phi\, \partial_t \vec{e} & = S \, \varepsilon_0 f E \Phi \oint_{\partial \widetilde{V}} \hat{n} \cdot \phi\, \partial_t \vec{e} = S \dfrac{B^2 f L}{\mu_0} \left( \dfrac{f L}{c_0} \right)^2 \oint_{\partial \widetilde{V}} \hat{n} \cdot \phi\, \partial_t \vec{e} && (3) \\
\end{aligned}$$

being $E = B f L$, and $\Phi = E L = B f L^2$, $E \Phi = (B f L)^2 L$, and $\varepsilon_0 = \dfrac{1}{\mu_0 c_0^2}$. If the integrals with non-dimensional quantities have the same order of magnitude (and this should occur if the non-dimensional equations are build using reference quantities of the system), the contribution (3) is smaller than the contribution (2) in the slow regime limit, as its $\left( \frac{f L}{c_0} \right)^2 \ll 1$ times the order of magnitude.

Comparing (1) and (2), the second contribution is negligible if

$$1 \gg \dfrac{S \frac{B^2 f L}{\mu_0}}{VI} = \dots$$

**todo** <span style="color:red">*check this! Is it ok that the frequency disappears? Term (1) is non-zero but (2) is identically zero for steady regime, $f = 0$. And if it's required to separate steady and unsteady contributions in the discussion of non-dimensional equations*</span>

$$1 \gg \dfrac{S \frac{B^2 f L}{\mu_0}}{VI} = S \dfrac{B^2 f L}{\mu_0 \Phi I} = S \frac{B^2 f L}{\mu_0 B f L^2 I} = S \frac{B}{\mu_0 L I} = S \frac{\mu_0 J L}{\mu_0 L I} = \frac{S J}{I} \ .$$

<span style="color:red">The dimension of the boundary of the domain is proprotional to the square of the linear dimension of the system, $S \sim L_{V}^2$. This inequality holds if the product of the dimension of the boundary of the domain and the characteristic current density $J$ is much smaller than the characteristic current $I$ at the boundary.</span>

<!--
---

$$1 \gg \dfrac{S \frac{B^2 f L}{\mu_0}}{VI} = S \dfrac{\mu_0^2 J^2 L^2 f L}{\mu_0 \Phi I} = S \frac{B^2 f L}{\mu_0 B f L^2 I} = S \frac{B}{\mu_0 L I} = S \frac{\mu_0 J L}{\mu_0 L I} = \frac{S J}{I} \ .$$

-->
