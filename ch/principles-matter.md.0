<!--
```{article-info}
\:author: basics
\:date: "{sub-ref}`today`"
\:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:principles:matter)=
# Electromagnetism in Matter

Electromagnetism in matter requires the description of the behavior of the matter involved in the process. In general, a medium immersed in an electromagnetic field may respond with local charge distributions, resulting in [**polarization**](classical-electromagnetism:media:polarization) and [**magnetization**](classical-electromagnetism:media:magnetization). Total electric $\vec{e}(\vec{r},t)$ and magnetic field $\vec{b}(\vec{r},t)$ can be written as the sum of contributions of free charges $\rho_f$ and currents $\vec{j}_f$ and bound charges $\rho_b$ and currents $\vec{j}_b$.

Bound charge density represents local separation of charges of molecules of dielectric media immersed in electric field, that can be represented as a volume distribution of charge dipole,

$$\rho = \rho_f + \rho_b = \rho_f + \rho_P \ .$$

Bound current density represents two effects: the variation of polarization charge and the orientation of Amperian currents - "non random" currents in the molecules of the medium, producing net contribution to the magnetic field, and can be represented as a volume distribution of elementary loop currents.

$$\begin{aligned}
  \vec{j} & = \vec{j}_f + \vec{j}_b 
            = \vec{j}_f + \vec{j}_P + \vec{j}_M  \ .
\end{aligned}$$

As it will shown below, the bound current can be written as the divergence of the polarization field $\vec{p}$, representing the volume density fo the dipole distribution, and the magnetization current as the curl of the magnetization field $\vec{m}$,

$$\rho_p = - \nabla \cdot \vec{p} \quad , \quad \vec{j}_M = \nabla \times \vec{m} \ .$$

(classical-electromagnetism:media:vacuum-to-matter)=
## Equations of electromagnetism in matter

Introducing the splitting of free and bound charge and current into the equations of the electromagnetism, namely electric charge continuity and Maxwell's equations,

$$
\partial_t \rho + \nabla \cdot \vec{j} = 0
\qquad , \qquad
\begin{cases}
\nabla \cdot \vec{e} = d\frac{\rho}{\varepsilon_0} \\
\nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\
\nabla \cdot \vec{b} = 0 \\
\nabla \times \vec{b} - \mu_0 \varepsilon_0 \partial_t \vec{e} = \mu_0 \vec{j}
\end{cases}$$


**Gauss' law for the electric field, and the dielectric field.**

  $$\begin{aligned}
    & 0  = \nabla \cdot \vec{e} - \frac{\rho}{\varepsilon_0} = \nabla \cdot \vec{e} - \frac{\rho_f - \nabla \cdot \vec{p}}{\varepsilon_0}  \\ \\
    & \rightarrow \qquad \nabla \cdot \vec{d} = \rho_f \ ,
  \end{aligned}$$

  with $\vec{d} = \varepsilon_0 \vec{e} + \vec{p}$ defined as the **displacement field**. 

**Continuity equation of electric charge.**

  $$
    0 
    & = \partial_t \rho + \nabla \cdot \vec{j} = \\
    & = \partial_t \rho_f + \nabla \cdot \vec{j}_f + \partial_t \rho_b + \nabla \cdot \vec{j}_b = \\
    & = \partial_t \rho_f + \nabla \cdot \vec{j}_f + \partial_t \rho_P + \nabla \cdot ( \vec{j}_P + \vec{j}_M ) = \\
    & = \partial_t \rho_f + \nabla \cdot \vec{j}_f + \partial_t \rho_P + \nabla \cdot ( \vec{j}_P + \nabla \times \vec{m} ) = \\
  $$

  Since $\nabla \cdot \nabla \times \vec{m} \equiv 0$, and keeping separated the contributions of free and bound charges, two continuity equations follow for free and bound charges,

  $$\begin{aligned}
     & \partial_t \rho_f + \nabla \cdot \vec{j}_f = 0 \\
     & \partial_t \rho_P + \nabla \cdot \vec{j}_P = 0 \\ \\
  \end{aligned}$$

As $\rho_P = - \nabla \cdot \vec{p}$, it follows the expression of the polarization current as a function of polarization field $\vec{j}_P = \partial_t \vec{p}$.

**Maxwell-Ampére equation.** Introducing the expression of the electric field as a function of the dielectric field and polarization, and the expression of the polarization and magnetization currents
  
  $$\begin{aligned}
    \vec{0}
    & = \nabla \times \vec{b} - \mu_0 \varepsilon_0 \partial_t \vec{e} - \mu_0 \vec{j} = \\
    & = \nabla \times \vec{b} - \mu_0 \, \partial_t \left( \vec{d} - \vec{p} \right) - \mu_0 \vec{j}_f - \mu_0 \partial_t \vec{p} - \mu_0 \nabla \times \vec{m} \\
    & = \nabla \times \left( \vec{b} - \mu_0 \vec{m} \right) - \mu_0 \, \partial_t \vec{d} - \mu_0 \vec{j}_f \\ \\ 
    & \rightarrow \qquad \nabla \times \vec{h}  - \, \partial_t \vec{d} = \vec{j}_f \\
  \end{aligned}$$

  habing introduced the **magnetic field strength**, $\vec{h} := \dfrac{1}{\mu_0} \vec{b} - \vec{m}$.

<!--
## Continuous Media

In general, some materials respond to an imposed "external" electromagnetic field with polarization and magnetization. In particular, the electric polarization of a material corresponds to a local separation of electric charges, macroscopically equivalent to a volume density of dipoles, $\vec{p}(\vec{r}_0)$; magnetization corresponds to an orientation of the axes of Amperian current loops, macroscopically equivalent to a density of magnetic moment $\vec{m}(\vec{r}_0)$.
-->


## Examples
- conductors
- ferromagnetic and weak magnetism (para-, dia-, anti-)

(classical-electromagnetism:media:differential)=
## Governing equations in differential form

Differential form of Maxwell's equations

$$\begin{cases}
 \nabla \cdot \vec{d} = \rho_f \\
 \nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\
 \nabla \cdot \vec{b} = 0 \\
 \nabla \times \vec{h} - \partial_t \vec{d} = \vec{j}_f
\end{cases}$$

**todo** *continuity equation for charge*

(classical-electromagnetism:media:integral)=
## Governing equation in integral form

Integral form of Maxwell's equations

$$\begin{cases}
 \displaystyle \oint_{\partial V} \vec{d} \cdot \hat{n} = \int_{V} \rho_f \\
 \displaystyle \oint_{\partial S} \vec{e} \cdot \hat{t} + \dfrac{d}{dt} \int_S \vec{b} \cdot \hat{n} = 0 \\
 \displaystyle \oint_{\partial V} \vec{b} \cdot \hat{n} = 0 \\
 \displaystyle \oint_{\partial S} \vec{h} \cdot \hat{t} - \dfrac{d}{dt} \int_S \vec{d} \cdot \hat{n} = \int_{S} \vec{j}_f \cdot \hat{n} \\
\end{cases}$$

- control volume
- arbitrary domain
- low-speed relativity

(classical-electromagnetism:media:jump)=
## Jump Conditions

Letting $V$ and $S$ "collapse on a discontinuity"...

$$\begin{cases}
  [ d_n ] = \sigma_f \\
  [ e_t ] = 0 \\
  [ b_n ] = 0 \\
  [ h_t ] = \iota_f \ ,
\end{cases}$$ (eq:em-jump)

being $\sigma_f$ and $\iota_f$ surface charge and current density, with physical dimension $\frac{\text{charge}}{\text{surface}}$, and $\frac{\text{current}}{\text{surface}}$ respectively. These contributions can be thought of as Dirac delta contributions in volume density, namely

$$\rho(\vec{r},t) = \rho_0(\vec{r},t) + \sigma(\vec{r}_s,t) \delta_{1}(\vec{r}-\vec{r}_s) \ ,$$

being $\rho(\vec{r},t)$ the regular part of the volume density in all the points of the domain $\vec{r} \in V$, $\sigma(\vec{r}_s,t)$ the surface density on 2-dimensional surfaces $\vec{r}_s \in S$, $\delta_1()$ the Dirac's delta with physical dimension $\frac{1}{\text{length}}$.

If there's no free surface charge and currents, jump conditions for linear media become

$$\begin{cases}
  [ d_n ] = 0 \\
  [ e_t ] = 0 \\
  [ b_n ] = 0 \\
  [ h_t ] = 0 \ ,
\end{cases}
\qquad \rightarrow \qquad
\begin{cases}
  d_{n,1} = d_{n,2}  \quad \rightarrow \quad \varepsilon_1 e_{n,1} = \varepsilon_2 e_{n,2} \\
  e_{t,1} = e_{t,2}  \\
  b_{n,1} = b_{n,2}  \\
  h_{t,1} = h_{t,2}  \quad \rightarrow \quad \frac{1}{\mu_1} b_{t,1} = \frac{1}{\mu_2} b_{t,2} \\
\end{cases}
$$ (eq:em-jump:no-surf-density)

