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

$$\rho_p = - \nabla \cdot \vec{p} \quad , \quad \vec{j}_p = \partial_t \vec{p} \quad , \quad \vec{j}_M = \nabla \times \vec{m} \ .$$

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

$$\begin{aligned}
& \quad \partial_t \rho_f + \nabla \cdot \vec{j}_f = 0 \\ \\
& \begin{cases}
 \nabla \cdot \vec{d} = \rho_f \\
 \nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\
 \nabla \cdot \vec{b} = 0 \\
 \nabla \times \vec{h} - \partial_t \vec{d} = \vec{j}_f
\end{cases} \\
\end{aligned}
\qquad , \qquad
\begin{aligned}
& \quad \partial_t \rho + \nabla \cdot \vec{j} = 0 \\ \\
& \begin{cases}
 \nabla \cdot \vec{e} = \frac{\rho}{\varepsilon_0} \\
 \nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\
 \nabla \cdot \vec{b} = 0 \\
 \nabla \times \vec{b} - \varepsilon_0 \mu_0 \partial_t \vec{e} = \mu_0 \vec{j}
\end{cases} \\
\end{aligned}$$

with the splitting of charge and currents in free and bound (from both polarization and magnetization) contributions

$$\begin{aligned}
  \rho    & =   \rho_f +   \rho_p +   \rho_m \\
  \vec{j} & =\vec{j}_f +\vec{j}_p +\vec{j}_m  \\
\end{aligned}$$

with the definition of polarization $\vec{p}$ and magnetization $\vec{m}$ fields

$$\begin{aligned}
  \vec{d} & = \varepsilon_0 \vec{e} + \vec{p} \\
  \vec{b} & = \mu_0 \vec{h} + \mu_0 \vec{m} \\
\end{aligned}$$

with $\rho_p = - \nabla \cdot \vec{p}$, and $\vec{j}_m = \nabla \times \vec{m}$, and thus

$$\begin{aligned}
  \partial_t \rho_p + \nabla \cdot \vec{j}_p & = 0 \qquad \rightarrow \qquad \vec{j}_p = \partial_t \vec{p} \\
  \partial_t \rho_m + \nabla \cdot \vec{j}_m & = 0 \qquad \rightarrow \qquad    \rho_m = 0                  \\
\end{aligned}$$

(classical-electromagnetism:media:integral)=
## Governing equation in integral form

(classical-electromagnetism:media:integral:control-volume)=
### Integral Form on Control Volumes

Integral form of Maxwell's equations

$$\begin{cases}
 \displaystyle \oint_{\partial V} \vec{d} \cdot \hat{n} = \int_{V} \rho_f \\
 \displaystyle \oint_{\partial S} \vec{e} \cdot \hat{t} + \dfrac{d}{dt} \int_S \vec{b} \cdot \hat{n} = 0 \\
 \displaystyle \oint_{\partial V} \vec{b} \cdot \hat{n} = 0 \\
 \displaystyle \oint_{\partial S} \vec{h} \cdot \hat{t} - \dfrac{d}{dt} \int_S \vec{d} \cdot \hat{n} = \int_{S} \vec{j}_f \cdot \hat{n} \\
\end{cases}$$

(classical-electromagnetism:media:integral:arbitrary-volume)=
### Integral Form on Arbitrary Volumes

Due to their importance in fundamental applications such as electric motors, and to avoid confusion or leaps in logic when dealing with electromagnetic induction, it is crucial to provide the correct expression of the electromagnetic principles when moving volumes are involved in space. Not only is the form of these principles shown, but also the correct procedure to derive them starting from the fixed-control-volume version. This is done using rules for [time derivative for fundamental integrals over moving domains](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/time-derivative-of-integrals.html), such as the integral of a density function over a volume, the flux of a vector field through a surface, or the circulation along a curve.

These three derivative rules are listed here and proved in the material about [Mathematics](https://basics2022.github.io/bbooks-math-miscellanea/intro.html):Vector and Tensor Algebra and Calculus:[Time derivatives of integrals over moving domains](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/time-derivative-of-integrals.html)

$$\begin{aligned}
  \dfrac{d}{dt} \int_{v_t} f & = \int_{v_t} \dfrac{\partial f}{\partial t} + \oint_{\partial v_t} f \, \vec{v}_b \cdot \hat{n} & \text{(density)} \\
  \dfrac{d}{dt} \int_{s_t} \vec{f} \cdot \hat{n} & = \int_{s_t} \dfrac{\partial \vec{f}}{\partial t} \cdot \hat{n} + \int_{s_t} \nabla \cdot \vec{f} \, \vec{v}_b \cdot \hat{n} - \oint_{\partial s_t} \vec{v}_b \times \vec{f} \cdot \hat{t} & \text{(flux)} \\
  \dfrac{d}{dt} \int_{\ell_t} \vec{f} \cdot \hat{t} & = \int_{\ell_t} \dfrac{\partial \vec{f}}{\partial t} \cdot \hat{t} + \int_{\ell_t} \nabla \times \vec{f} \, \cdot \, \vec{v}_b \times \hat{t} + \vec{f}_B \cdot \vec{v}_B - \vec{f}_A \cdot \vec{v}_A & \text{(circulation)}
\end{aligned}$$

**Continuity of Electric Charge.**

$$\begin{aligned}
   0 & = \dfrac{d}{dt} \int_{V} \rho + \oint_{\partial V} \vec{j} \cdot \hat{n} = \\
   & = \dfrac{d}{dt} \int_{v_t} \rho - \oint_{\partial v_t } \rho \vec{v}_b \cdot \hat{n} + \oint_{\partial v_t} \vec{j} \cdot \hat{n} 
\end{aligned}$$

$$
    \dfrac{d}{dt} \int_{v_t} \rho + \oint_{\partial v_t} \underbrace{\rho (\vec{v} - \vec{v}_b)}_{\vec{j}^*} \cdot \hat{n} 
$$

**Gauss's Law for the Field $\vec{d}(\vec{r},t)$.**

$$
    \oint_{\partial v_t} \vec{d} \cdot \hat{n} = \int_{v_t} \rho^f
$$

**Gauss's Law for the Field $\vec{b}(\vec{r},t)$.**

$$
    \oint_{\partial v_t} \vec{b} \cdot \hat{n} = 0
$$

**Faraday–Neumann–Lenz Law for Electromagnetic Induction.**

$$\begin{aligned}
   \vec{0} & = \oint_{\partial S} \vec{e} \cdot \hat{t} + \dfrac{d}{dt} \int_{S} \vec{b} \cdot \hat{n} = \\
    & = \oint_{\partial s_t} \vec{e} \cdot \hat{t} + \dfrac{d}{dt} \int_{s_t} \vec{b} \cdot \hat{n} - \int_{s_t} \underbrace{\nabla \cdot \vec{b}}_{=0} \, \vec{v}_b \cdot \hat{n} + \oint_{s_t} \vec{v}_b \times \vec{b} \cdot \hat{t} =  \\
\end{aligned}$$

$$
    \oint_{\partial s_t} \vec{e}^* \cdot \hat{t} + \dfrac{d}{dt} \int_{s_t} \vec{b} \cdot \hat{n} \ ,
$$
with the definition $\vec{e}^* := \vec{e} + \vec{v}_b \times \vec{b}$, already used in the expression of the Lorentz force law.

**Ampère–Maxwell Law.**

$$\begin{aligned}
    \vec{0} & = \oint_{\partial S} \vec{h} \cdot \hat{t} - \dfrac{d}{dt} \int_{S} \vec{d} \cdot \hat{n} - \int_{S} \vec{j}_f \cdot \hat{n} = \\
    & = \oint_{\partial s_t} \vec{h} \cdot \hat{t} - \dfrac{d}{dt} \int_{s_t} \vec{d} \cdot \hat{n} + \int_{s_t} \underbrace{\nabla \cdot \vec{d}}_{=\rho_f} \, \vec{v}_b \cdot \hat{n} - \oint_{s_t} \vec{v}_b \times \vec{d} \cdot \hat{t} - \int_{s_t} \vec{j}_f \cdot \hat{n} =  \\
\end{aligned}$$

$$
    \oint_{\partial s_t} \vec{h}^* \cdot \hat{t} - \dfrac{d}{dt} \int_{s_t} \vec{d} \cdot \hat{n} = \int_{s_t} \vec{j}_f^{*} \cdot \hat{n} \ ,
$$

having defined $\vec{h}^* := \vec{h} - \vec{v}_b \times \vec{d}$, and using the previously introduced definition $\vec{j}^{f*} := \vec{j}^f - \rho^f \vec{v}_b$.

Adding the definitions:

$$\begin{aligned}
  \rho^*_f  &  = \rho_f  \\
  \vec{d}^* &  = \vec{d}  \\
  \vec{b}^* &  = \vec{b}
\end{aligned}$$

one obtains equations having the same form as those written for stationary domains in space, but which can be applied to moving domains. The definitions:

$$\begin{aligned}
\rho^*_f = \rho_f   \qquad & , \qquad \vec{j}^*_f = \vec{j}_f - \rho \vec{v}_b \\
\vec{d}^* = \vec{d} \qquad & , \qquad \vec{e}^* = \vec{e} + \vec{v}_b \times \vec{b} \\
\vec{b}^* = \vec{b} \qquad & , \qquad \vec{h}^* = \vec{h} - \vec{v}_b \times \vec{d} \\
\end{aligned}$$

are nothing more than the transformation of the fields for two observers in relative motion, and correspond to the **low-speed limit** of [Lorentz transformations from special relativity](https://basics2022.github.io/bbooks-physics-modern/ch/relativity-special/lorentz.html#inertial-reference-frames-and-lorentz-s-transformations) for velocities $|\vec{v}_b| \ll c$, and Lorentz's factor $\gamma \sim 1$: in this procedure, the transformations for low relative speeds are obtained, as no transformation of spatial and temporal dimensions has been considered, unlike Einstein's theory of relativity.

**todo** Reference Galilean and Lorentz transformations for relativity in electromagnetism.

**todo** Sistematic power expansion

**todo** Take into account higher-order contributions

$$\begin{aligned}
  \rho^*    & = \rho    - \dfrac{\vec{j}}{c^2} + \text{terms coming from $\gamma c \rho$} \\
  \vec{d}^* & = \vec{d} - \dfrac{\vec{h} \times \vec{v}}{c^2} + \text{terms coming from $(1-\gamma) \hat{v} \hat{v} \cdot \vec{d}$}  \\
  \vec{b}^* & = \vec{b} + \dfrac{\vec{e} \times \vec{v}}{c^2} + \text{terms coming from $(1-\gamma) \hat{v} \hat{v} \cdot \vec{b}$}  \\
\end{aligned}$$

**todo** Relativity of polarization and magnetization

$$\begin{aligned}
  \vec{p} 
  := & \  \vec{d} - \varepsilon_0 \vec{e} = \\
   = & \  \vec{d}^* + \dfrac{\vec{h} \times \vec{v}}{c^2} - \varepsilon_0 \left( \vec{e}^* + \vec{b} \times \vec{v} \right) = \\
   = & \  \vec{d}^* - \varepsilon_0 \vec{e}^* + \left( \dfrac{\vec{h}}{c^2} - \varepsilon_0 \vec{b} \right) \times \vec{v} = \\ 
   = & \  \vec{p}^* - \dfrac{ \vec{m} \times \vec{v}}{c^2} \ .
\end{aligned}$$

$$\begin{aligned}
  \vec{m} 
  := & \ \dfrac{1}{\mu_0} \vec{b} - \vec{h} = \\
   = & \ \dfrac{1}{\mu_0} \vec{b}^* + \dfrac{1}{\mu_0} \dfrac{\vec{v} \times \vec{e}}{c^2} - \vec{h}^* - \vec{v} \times \vec{d} = \\ \\
   = & \ \vec{m}^* - \vec{v} \times \vec{p} \ .
\end{aligned}$$

(classical-electromagnetism:media:jump)=
## Jump Conditions

Letting $V$ and $S$ "collapse on a discontinuity"...

$$\begin{aligned}
  \left[ j^*_n \right] & = 0         & \text{charge continuity} \\
  [ d^*_n ] & = \sigma_f             & \text{Gauss' law for $\vec{d}^*$} \\
  [ e^*_t ] & = 0                    & \text{Faraday's law} \\
  [ b^*_n ] & = 0                    & \text{Gauss' law for $\vec{b}^*$} \\
  [ h*_t ]  & = \iota^*_f            & \text{Ampére-Maxwell's law} 
\end{aligned}$$ (eq:em-jump)

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

