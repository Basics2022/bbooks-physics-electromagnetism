<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:principles)=
# Principles of Classical Electromagnetism

The progress in the study of electromagnetic phenomena during the 19th century allowed James Clerk Maxwell to formulate what are now known as *Maxwell's equations*, which can be considered the first consistent formulation of the principles of classical electromagnetism, together with the charge conservation law and the expression for the Lorentz force on an electric charge immersed in an electromagnetic field.

The principles in differential form can be derived from the more general integral form, provided the fields satisfy the necessary minimal regularity conditions, which can be qualitatively stated as "all operations must make sense."

(classical-electromagnetism:principles:differential)=
## Principles in Differential Form

**Conservation of Electric Charge.**

$$\partial_t \rho + \nabla \cdot \mathbf{j} = 0 \ .$$

**Maxwell's Equations.**

$$\begin{cases}
 \nabla \cdot \mathbf{d} = \rho \\
 \nabla \times \mathbf{e} + \partial_t \mathbf{b} = \mathbf{0} \\ 
 \nabla \cdot \mathbf{b} = 0 \\
 \nabla \times \mathbf{h} - \partial_t \mathbf{d} = \mathbf{j} \\
\end{cases}$$

with the need to define constitutive equations $\mathbf{d}(\mathbf{e}, \mathbf{b})$, $\mathbf{h}(\mathbf{e}, \mathbf{b})$.

**Lorentz Force.** The force per unit volume acting on the electric charge present at a point $\mathbf{r}$ in space is

$$\begin{aligned}
  \mathbf{f}(\mathbf{r},t) & = \rho(\mathbf{r},t) \, \mathbf{e}(\mathbf{r},t) + \mathbf{j}(\mathbf{r},t) \times \mathbf{b}(\mathbf{r},t) = \\
                           & = \rho(\mathbf{r},t) \left[ \mathbf{e}(\mathbf{r}) + \mathbf{v}(\mathbf{r},t) \times \mathbf{b}(\mathbf{r},t) \right] =  \\
                           & = \rho(\mathbf{r},t) \, \mathbf{e}^*(\mathbf{r},t) 
\end{aligned}$$

having defined $\mathbf{e}^*$ as the electric field **seen by the moving charge**.

(classical-electromagnetism:principles:integral)=
## Principles in Integral Form: Electromagnetic Equations and Galilean Relativity

(classical-electromagnetism:principles:integral:control-volume)=
### Integral Form on Control Volumes

The integral form of the principles of electromagnetism for fixed volumes $V$ and surfaces $S$ in space is obtained by integrating the differential equations over the domains and using the divergence theorem to obtain flux terms, and Stokes' theorem to obtain circulation terms.

**Continuity of Electric Charge.**

$$
    \dfrac{d}{dt} \int_{V} \rho + \oint_{\partial V} \mathbf{j} \cdot \hat{\mathbf{n}} = 0
$$

**Gauss's Law for the Field $\mathbf{d}(\mathbf{r},t)$.**

$$
    \oint_{\partial V} \mathbf{d} \cdot \mathbf{\hat{n}} = \int_{V} \rho
$$

**Gauss's Law for the Field $\mathbf{b}(\mathbf{r},t)$.**

$$
    \oint_{\partial V} \mathbf{b} \cdot \mathbf{\hat{n}} = 0
$$

**Faraday–Neumann–Lenz Law for Electromagnetic Induction.**

$$
    \oint_{\partial S} \mathbf{e} \cdot \hat{\mathbf{t}} + \dfrac{d}{dt} \int_{S} \mathbf{b} \cdot \hat{\mathbf{n}} = \mathbf{0}
$$

**Ampère–Maxwell Law.**

$$
    \oint_{\partial S} \mathbf{h} \cdot \hat{\mathbf{t}} - \dfrac{d}{dt} \int_{S} \mathbf{d} \cdot \hat{\mathbf{n}} = \int_{S} \mathbf{j} \cdot \hat{\mathbf{n}} \ .
$$

(classical-electromagnetism:principles:integral:arbitrary-volume)=
### Integral Form on Arbitrary Volumes

Due to their importance in fundamental applications such as electric motors, and to avoid confusion or leaps in logic when dealing with electromagnetic induction, it is crucial to provide the correct expression of the electromagnetic principles when moving volumes are involved in space. Not only is the form of these principles shown, but also the correct procedure to derive them starting from the fixed-control-volume version. This is done using time derivative rules for fundamental integrals over moving domains, such as the integral of a density function over a volume, the flux of a vector field through a surface, or the circulation along a curve.

These three derivative rules are **todo** Start the vector calculus bbook, and add reference

$$\dfrac{d}{dt} \int_{v_t} f = \int_{v_t} \dfrac{\partial f}{\partial t} + \oint_{\partial v_t} f \, \mathbf{u}_b \cdot \hat{\mathbf{n}}$$

$$\dfrac{d}{dt} \int_{s_t} \mathbf{f} \cdot \hat{\mathbf{n}} = \int_{s_t} \dfrac{\partial \mathbf{f}}{\partial t} \cdot \hat{\mathbf{n}} + \int_{s_t} \nabla \cdot \mathbf{f} \, \mathbf{u}_b \cdot \hat{\mathbf{n}} - \oint_{\partial s_t} \mathbf{u}_b \times \mathbf{f} \cdot \hat{\mathbf{t}}$$

$$\dfrac{d}{dt} \int_{\ell_t} \mathbf{f} \cdot \hat{\mathbf{t}} = \int_{\ell_t} \dfrac{\partial \mathbf{f}}{\partial t} \cdot \hat{\mathbf{t}} + \int_{\ell_t} \nabla \times \mathbf{f} \, \cdot \, \mathbf{u}_b \times \hat{\mathbf{t}} + \mathbf{f}_B \cdot \mathbf{u}_B - \mathbf{f}_A \cdot \mathbf{u}_A$$

**Continuity of Electric Charge.**

$$\begin{aligned}
   0 & = \dfrac{d}{dt} \int_{V} \rho + \oint_{\partial V} \mathbf{j} \cdot \hat{\mathbf{n}} = \\
   & = \dfrac{d}{dt} \int_{v_t} \rho - \oint_{\partial v_t } \rho \mathbf{u}_b \cdot \hat{\mathbf{n}} + \oint_{\partial v_t} \mathbf{j} \cdot \hat{\mathbf{n}} 
\end{aligned}$$

$$
    \dfrac{d}{dt} \int_{v_t} \rho + \oint_{\partial v_t} \underbrace{\rho (\mathbf{u} - \mathbf{u}_b)}_{\mathbf{j}^*} \cdot \hat{\mathbf{n}} 
$$

**Gauss's Law for the Field $\mathbf{d}(\mathbf{r},t)$.**

$$
    \oint_{\partial v_t} \mathbf{d} \cdot \mathbf{\hat{n}} = \int_{v_t} \rho
$$

**Gauss's Law for the Field $\mathbf{b}(\mathbf{r},t)$.**

$$
    \oint_{\partial v_t} \mathbf{b} \cdot \mathbf{\hat{n}} = 0
$$

**Faraday–Neumann–Lenz Law for Electromagnetic Induction.**

$$\begin{aligned}
   \mathbf{0} & = \oint_{\partial S} \mathbf{e} \cdot \hat{\mathbf{t}} + \dfrac{d}{dt} \int_{S} \mathbf{b} \cdot \hat{\mathbf{n}} = \\
    & = \oint_{\partial s_t} \mathbf{e} \cdot \hat{\mathbf{t}} + \dfrac{d}{dt} \int_{s_t} \mathbf{b} \cdot \hat{\mathbf{n}} - \int_{s_t} \underbrace{\nabla \cdot \mathbf{b}}_{=0} \, \mathbf{u}_b \cdot \hat{\mathbf{n}} + \oint_{s_t} \mathbf{u}_b \times \mathbf{b} \cdot \hat{\mathbf{t}} =  \\
\end{aligned}$$

$$
    \oint_{\partial s_t} \mathbf{e}^* \cdot \hat{\mathbf{t}} + \dfrac{d}{dt} \int_{s_t} \mathbf{b} \cdot \hat{\mathbf{n}} \ ,
$$
with the definition $\mathbf{e}^* := \mathbf{e} + \mathbf{u}_b \cdot \mathbf{b}$, already used in the expression of the Lorentz force law.

**Ampère–Maxwell Law.**

$$\begin{aligned}
    \mathbf{0} & = \oint_{\partial s_t} \mathbf{h} \cdot \hat{\mathbf{t}} - \dfrac{d}{dt} \int_{s_t} \mathbf{d} \cdot \hat{\mathbf{n}} - \int_{s_t} \mathbf{j} \cdot \hat{\mathbf{n}} = \\
    & = \oint_{\partial s_t} \mathbf{h} \cdot \hat{\mathbf{t}} - \dfrac{d}{dt} \int_{s_t} \mathbf{d} \cdot \hat{\mathbf{n}} + \int_{s_t} \underbrace{\nabla \cdot \mathbf{d}}_{=\rho} \, \mathbf{u}_b \cdot \hat{\mathbf{n}} - \oint_{s_t} \mathbf{u}_b \times \mathbf{d} \cdot \hat{\mathbf{t}} - \int_{s_t} \mathbf{j} \cdot \hat{\mathbf{n}} =  \\
\end{aligned}$$

$$
    \oint_{\partial s_t} \mathbf{h}^* \cdot \hat{\mathbf{t}} - \dfrac{d}{dt} \int_{s_t} \mathbf{b} \cdot \hat{\mathbf{n}} = \int_{s_t} \mathbf{j}^* \cdot \hat{\mathbf{n}} \ ,
$$

having defined $\mathbf{h}^* := \mathbf{h} - \mathbf{u}_b \times \mathbf{d}$, and using the previously introduced definition $\mathbf{j}^* := \mathbf{j} - \rho \mathbf{u}_b$.

Adding the definitions:

$$\rho^* = \rho$$  
$$\mathbf{d}^* = \mathbf{d}$$  
$$\mathbf{b}^* = \mathbf{b}$$

one obtains equations having the same form as those written for stationary domains in space, but which can be applied to moving domains. The definitions:

$$\begin{aligned}
\rho^* = \rho \qquad & , \qquad \mathbf{j}^* = \mathbf{j} - \rho \mathbf{u}_b \\
\mathbf{d}^* = \mathbf{d} \qquad & , \qquad \mathbf{e}^* = \mathbf{e} + \mathbf{u}_b \times \mathbf{b} \\
\mathbf{b}^* = \mathbf{b} \qquad & , \qquad \mathbf{h}^* = \mathbf{h} - \mathbf{u}_b \times \mathbf{d} \\
\end{aligned}$$

are nothing more than the transformation of the fields for two observers in relative motion, and correspond to the low-speed limit of Lorentz transformations from special relativity for velocities $|\mathbf{u}_b| \ll c$: in this procedure, the transformations for low relative speeds are obtained, as no transformation of spatial and temporal dimensions has been considered, unlike Einstein's theory of relativity.

**todo** Reference Galilean and Lorentz transformations for relativity in electromagnetism.

