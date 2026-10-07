(classical-electromagnetism:transformed-domain)=
# Electromagnetism in transformed domain

(classical-electromagnetism:transformed-domain:fourier)=
## Fourier domain

```{dropdown} Equations of electromagnetism in physical domain
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

**Gauge conditions.**

$$\begin{aligned}
  & \nabla \cdot \mathbf{a} + \dfrac{1}{c^2} \partial_t \varphi && \text{(Lorentz)} \\
  & \nabla \cdot \mathbf{a} = 0 && \text{(Coulomb)} \\
\end{aligned}$$

```

### Semi-transform in space, $\ \mathbf{r} \leftrightarrow \mathbf{k}$

```{dropdown} Summary of Fourier transform and series
:open:

**Fourier transform.**

$$\begin{aligned}
  \widetilde{f}(\mathbf{k},t) & = \frac{1}{\left( 2 \pi \right)^{n/2}} \int_{\mathbf{r} = -\infty}^{+\infty}            f (\mathbf{r}, t) \, e^{-i \mathbf{k} \cdot \mathbf{r}} \, d \mathbf{r} \\
  f(\mathbf{r},t)             & = \frac{1}{\left( 2 \pi \right)^{n/2}} \int_{\mathbf{k} = -\infty}^{+\infty} \widetilde{f}(\mathbf{k}, t) \, e^{i \mathbf{k} \cdot \mathbf{r}} \, d \mathbf{k} \\
\end{aligned}$$

The inverse relation can be easily proved using the orthogonality of function $e^{i\mathbf{k} \cdot \mathbf{r}}$, i.e.

$$\delta(\mathbf{k}-\mathbf{k}') = \dfrac{1}{( 2 \pi )^n} \int_{\mathbf{r}'} e^{-i \mathbf{k} \cdot \mathbf{r}} \, e^{i \mathbf{k'} \cdot \mathbf{r}} \, d \mathbf{r} \ .$$

**Fourier series.**

$$\begin{aligned}
  f(\mathbf{r}, t) & = \sum_{\mathbf{k}} f_{\mathbf{k}}(t) \, e^{i \mathbf{k} \cdot \mathbf{r}} \\
\end{aligned}$$

for periodic functions in the domain $\Omega$, with linear size $\mathbf{L}$ (one component per each dimension). 
with the wave-vectors $\mathbf{k}$ that are integer "multiples" (each component) of a fundamental wave-vector $\mathbf{k}^{(1)} = \frac{2 \pi}{ \mathbf{L}}$, $k^{(n_a)}_a = n_a k^{(1)}_a = n_a \frac{2 \pi}{L_a}$. The coefficients of the series immediately follow from the orthogonality condition 

$$\int_{\mathbf{r} \in \Omega} e^{-i \mathbf{k} \cdot \mathbf{r}} e^{i \mathbf{k}' \cdot \mathbf{r}} \, d \mathbf{r} = \delta_{\mathbf{k} \mathbf{k}'} |\Omega| \ , $$

as

$$f_{\mathbf{k}}(t) = \frac{1}{|\Omega|} \int_{\mathbf{r} \in \Omega} e^{- i \mathbf{k} \cdot \mathbf{r}} f(\mathbf{r}, t) \, d \mathbf{r}$$

as

$$\begin{aligned}
  f_{\mathbf{k}}(t) 
  & = \dfrac{1}{|\Omega|} \int_{\mathbf{r} \in \Omega} e^{- i \mathbf{k} \cdot \mathbf{r}} f(\mathbf{r}, t) \, d \mathbf{r} = \\
  & = \dfrac{1}{|\Omega|} \int_{\mathbf{r} \in\Omega} e^{- i \mathbf{k} \cdot \mathbf{r}} \sum_{\mathbf{k}'} f_{\mathbf{k}'}(t) e^{i \mathbf{k}' \cdot \mathbf{r}} \, d \mathbf{r} = \\
  & = \sum_{\mathbf{k}'} \delta_{\mathbf{k} \mathbf{k}'} f_{\mathbf{k}'}(t) = f_{\mathbf{k}}(t) \ .
\end{aligned}$$

**Spatial derivatives** become

$$\partial_a f(\mathbf{r}, t) = \dfrac{1}{(2\pi)^{n/2}} \int_{\mathbf{k} = -\infty}^{\infty} i k_a \widetilde{f}(\mathbf{k}, t) e^{i \mathbf{k} \cdot \mathbf{r}} \, d \mathbf{k} \ ,$$

or

$$\partial_a f(\mathbf{r}, t) = \sum_{\mathbf{k}} i k_a \, f_{\mathbf{k}}(t) e^{i \mathbf{k} \cdot \mathbf{r}}$$

**Equations from physical to transformed domain.** Exploiting orthogonality of the basis functions, linear equations becomes a set of linear equatinos for each mode $\widetilde{f}(\mathbf{k},t)$ or $f_{\mathbf{k}}(t)$. Just as an example, let's perform all the steps explicitly for the Gauss equation for the electric field,

$$\nabla \cdot \mathbf{d} = \rho \ .$$

having dropped the ${}_f$ index in the for brevity in the free charge density. Using the representation of the dielectric field and charge density in the wave vector domain,

$$
\begin{aligned}
  \mathbf{d}(\mathbf{r},t)             & = \frac{1}{\left( 2 \pi \right)^{n/2}} \int_{\mathbf{k} = -\infty}^{+\infty} \widetilde{\mathbf{d}}(\mathbf{k}, t) \, e^{i \mathbf{k} \cdot \mathbf{r}} \, d \mathbf{k} \\
  \rho(\mathbf{r},t)             & = \frac{1}{\left( 2 \pi \right)^{n/2}} \int_{\mathbf{k} = -\infty}^{+\infty} \widetilde{\rho}(\mathbf{k}, t) \, e^{i \mathbf{k} \cdot \mathbf{r}} \, d \mathbf{k} \\
\end{aligned}
\qquad \text{or} \qquad
\begin{aligned}
  \mathbf{d}(\mathbf{r}, t) & = \sum_{\mathbf{k}} \mathbf{d}_{\mathbf{k}}(t) \, e^{i \mathbf{k} \cdot \mathbf{r}} \\
  \rho      (\mathbf{r}, t) & = \sum_{\mathbf{k}}       \rho_{\mathbf{k}}(t) \, e^{i \mathbf{k} \cdot \mathbf{r}} \\
\end{aligned}
$$

the equation becomes

$$
0 = \dfrac{1}{\left( 2 \pi \right)^{n/2}} \int_{\mathbf{k}} \left\{ i \mathbf{k} \cdot \widetilde{\mathbf{d}}(\mathbf{k},t) - \widetilde{\rho}(\mathbf{k},t) \right\} e^{i \mathbf{k} \cdot \mathbf{r}} \, d \mathbf{k}
\qquad \text{or} \qquad
0 = \sum_{\mathbf{k}} \left\{ i \mathbf{k} \cdot \widetilde{\mathbf{d}}_{\mathbf{k}}(t) - \widetilde{\rho} \right\} e^{i \mathbf{k} \cdot \mathbf{r}}
$$

Exploiting the orthogonality of the basis functions means integrating over $\mathbf{r} \in (-\infty,\infty)^n$ the Fourier transform equation times $e^{-i \mathbf{k}' \cdot \mathbf{r}}$, or integrating over $\mathbf{r} \in \Omega$ the Fourier series equation times $e^{-i \mathbf{k}' \cdot \mathbf{r}}$, to get for any feasible value of $\mathbf{k}$ - and using the same symbol $\widetilde{f}_{\mathbf{k}}$ for the Fourier transform and the coefficients of the Fourier series

$$i \mathbf{k} \cdot \widetilde{\mathbf{d}}_{\mathbf{k}} = \widetilde{\rho}_f \ .$$

```

```{dropdown} Semi-transform in space, $\ \mathbf{r} \rightarrow \mathbf{k}$
:open:

**Maxwell's equation.**

$$\left\{
\begin{aligned}
  & i \mathbf{k} \cdot  \mathbf{d}_{\mathbf{k}} = \rho_{\mathbf{k}} \\
  & i \mathbf{k} \times \mathbf{e}_{\mathbf{k}} + \partial_t \mathbf{b}_{\mathbf{k}} = \mathbf{0} \\
  & i \mathbf{k} \cdot  \mathbf{b}_{\mathbf{k}} = 0 \\
  & i \mathbf{k} \times \mathbf{h}_{\mathbf{k}} - \partial_t \mathbf{d}_{\mathbf{k}} = \mathbf{j}_{\mathbf{k}}
\end{aligned}
\right.$$

**Continuity equation.**

$$\partial_t \rho_{\mathbf{k}} + i \mathbf{k} \cdot \mathbf{j}_{\mathbf{k}} = 0$$

**Electromagnetic potentials.**

$$\begin{aligned}
  \mathbf{b}_{\mathbf{k}} & = i \mathbf{k} \times \mathbf{a}_{\mathbf{k}} \\
  \mathbf{e}_{\mathbf{k}} & = - \mathbf{k} \varphi_{\mathbf{k}} - \partial_t \mathbf{a}_{\mathbf{k}}
\end{aligned}$$

**Gauge conditions.**

$$\begin{aligned}
  & i \mathbf{k} \cdot \mathbf{a}_{\mathbf{k}} + \dfrac{1}{c^2} \partial_t \varphi_{\mathbf{k}} && \text{(Lorentz)} \\
  & i \mathbf{k} \cdot \mathbf{a}_{\mathbf{k}} = 0 && \text{(Coulomb)} \\
\end{aligned}$$

```

### Transform in space and time, $\ (\mathbf{r},t) \rightarrow (\mathbf{k}, \omega)$

```{dropdown} Transform in space and time, $\ (\mathbf{r},t) \rightarrow (\mathbf{k}, \omega)$
:open:

**Maxwell's equation.**

$$\left\{
\begin{aligned}
  & i \mathbf{k} \cdot  \mathbf{d}_{\mathbf{k}} = \rho_{\mathbf{k}} \\
  & i \mathbf{k} \times \mathbf{e}_{\mathbf{k}} + i \omega \mathbf{b}_{\mathbf{k}} = \mathbf{0} \\
  & i \mathbf{k} \cdot  \mathbf{b}_{\mathbf{k}} = 0 \\
  & i \mathbf{k} \times \mathbf{h}_{\mathbf{k}} - i \omega \mathbf{d}_{\mathbf{k}} = \mathbf{j}_{\mathbf{k}}
\end{aligned}
\right.$$

**Continuity equation.**

$$i \omega \rho_{\mathbf{k}, \omega} + i \mathbf{k} \cdot \mathbf{j}_{\mathbf{k}} = 0$$

**Electromagnetic potentials.**

$$\begin{aligned}
  \mathbf{b}_{\mathbf{k}} & = i \mathbf{k} \times \mathbf{a}_{\mathbf{k}} \\
  \mathbf{e}_{\mathbf{k}} & = - \mathbf{k} \varphi_{\mathbf{k}} - i \omega \mathbf{a}_{\mathbf{k}}
\end{aligned}$$

**Gauge conditions.**

$$\begin{aligned}
  & i \mathbf{k} \cdot \mathbf{a}_{\mathbf{k}} + \dfrac{i \omega}{c^2} \varphi_{\mathbf{k}} && \text{(Lorentz)} \\
  & i \mathbf{k} \cdot \mathbf{a}_{\mathbf{k}} = 0 && \text{(Coulomb)} \\
\end{aligned}$$

```

