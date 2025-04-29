(classical-electromagnetism:circuits-electric:energy)=
# Energy balance in circuit approximation

Integral balance of electromagnetic energy {eq}`eq:energy:integral:2` reads

$$\dfrac{d}{dt} \int_V u + \int_{V} \vec{e} \cdot \vec{j} = - \oint_{\partial V} \, \phi \vec{j} \cdot \hat{n} + \oint_{\partial V} \hat{n} \cdot \left[ \frac{1}{\mu_0} \partial_t \vec{a} \times \vec{b} + \varepsilon_0 \, \phi\, \partial_t \vec{e} \right] \ .$$

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
