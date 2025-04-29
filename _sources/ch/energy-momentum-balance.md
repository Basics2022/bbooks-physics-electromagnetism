(classical-electromagnetism:energy-momentum)=
# Energy and momentum balance in linear, local, isotropic, non-dispersive media

(classical-electromagnetism:energy-momentum:energy:differential)=
## Energy equation in differential form
In this section balance equations for the energy and the momentum of the system are derived for a linear, local, isotropic, homogeneous,... systems.

Power per unit volume of the Lorentz' force per unit volume acting on a charge distribution $\rho(\vec{r},t)$ with electric current density $\vec{j}(\vec{r},t)$ is

$$\begin{aligned}
  p(\vec{r},t) 
  & = \vec{f}(\vec{r},t) \cdot \vec{v}(\vec{r},t) = \\
  & = \left[ \rho(\vec{r},t) \, \vec{e}(\vec{r},t) - \vec{b}(\vec{r},t) \times \vec{v}(\vec{r},t) \right] \cdot \vec{v}(\vec{r},t) = \\
  & = \rho(\vec{r},t) \, \vec{e}(\vec{r},t) \cdot \vec{v}(\vec{r},t) = \\
  & = \vec{j}(\vec{r},t) \cdot \vec{e}(\vec{r},t) \ .
\end{aligned}$$

**Total charge and current.** Energy equation for **total charge and current**

<!--
$$\begin{aligned}
  \vec{j}_f \cdot \vec{e} & = && (1) \\
  & = \left( \nabla \times \vec{h} - \partial_t \vec{d} \right) \cdot \vec{e} = && (2) \\
  & = \nabla \cdot \left( \vec{h} \times \vec{e} \right) + \vec{h} \cdot \nabla \times \vec{e} - \partial_t \vec{d} \cdot \vec{e} = && (3) \\
  & = - \nabla \cdot \vec{s} - \vec{h} \cdot \partial_t \vec{b} - \partial_t \vec{d} \cdot \vec{e} \ ,
\end{aligned}$$
-->

$$\begin{aligned}
  \vec{j} \cdot \vec{e} & = && (1) \\
  & = \frac{1}{\mu_0} \left( \nabla \times \vec{b} - \varepsilon_0 \partial_t \vec{e} \right) \cdot \vec{e} = && (2) \\
  & = \nabla \cdot \left( \frac{ \vec{b} \times \vec{e} }{\mu_0} \right) + \frac{1}{\mu_0} \vec{b} \cdot \nabla \times \vec{e} - \varepsilon_0 \partial_t \vec{e} \cdot \vec{e} = && (3) \\
  & = - \nabla \cdot \vec{s} - \frac{1}{\mu_0} \vec{b} \cdot \partial_t \vec{b} - \varepsilon_0 \partial_t \vec{e} \cdot \vec{e} \ ,
\end{aligned}$$ (eq:energy:1)

using (1) Ampère-Maxwell's equation, (2) identity $\nabla \times \vec{b} \cdot \vec{e} =  \nabla \cdot \left( \vec{b} \times \vec{e} \right) + \vec{b} \cdot \nabla \times \vec{e}$[^poynting], (3) Faraday's law, and introducing the definition of the Poynting vector

$$\vec{s} := \frac{ \vec{e} \times \vec{b} }{\mu_0} \ .$$ (eq:energy:poynting-vector)

[^poynting]: $$\begin{aligned}
  \nabla \times \vec{h} \cdot \vec{e}
  & = e_i \varepsilon_{ijk} \partial_{j} h_k = \\
  & = \varepsilon_{ijk} \partial_{j} \left( e_i  h_k \right) - h_k \varepsilon_{ijk} \partial_{j} e_i = \\
  & = \partial_{j} \left( \varepsilon_{jki} h_k  e_i \right) + h_k \varepsilon_{kji} \partial_{j} e_i = \\
  & = \nabla \cdot \left( \vec{h} \times \vec{e} \right) + \vec{h} \cdot \nabla \times \vec{e}  \ .
\end{aligned}$$

Using the identity, $\vec{v} \cdot \partial_t \vec{v} = \partial_t \frac{|\vec{v}|^2}{2}$, energy equation {eq}`eq:energy:1` becomes

$$\partial_t u + \nabla \cdot \vec{s} = - \vec{j} \cdot \vec{e} \ ,$$ (eq:energy:2)

with the energy volume density,

$$ u := \frac{1}{2} \left( \varepsilon_0 \vec{e} \cdot \vec{e} + \frac{1}{\mu_0} \vec{b} \cdot \vec{b} \right) \ .$$ (eq:energy:density)

```{dropdown} Polarization current.

$$\begin{aligned}
  \vec{j}_P \cdot \vec{e} & = \\
  & = \partial_t \vec{p} \cdot \vec{e} \\
\end{aligned}$$

```

```{dropdown} Magnetization current.

$$\begin{aligned}
  \vec{j}_M \cdot \vec{e} & = \\
  & = \nabla \times \vec{m} \cdot \vec{e} \\
  & = \nabla \cdot \left( \vec{m} \times \vec{e} \right) + \vec{m} \cdot \nabla \times \vec{e} \\
  & = \nabla \cdot \left( \vec{m} \times \vec{e} \right) - \vec{m} \cdot \partial_t \vec{b} \\
\end{aligned}$$

```

```{dropdown} Free current.

$$\begin{aligned}
  \vec{j}_f \cdot \vec{e} & = \\
  & = \left( \nabla \times \vec{h} - \partial_t \vec{d} \right) \cdot \vec{e} \\
  & = \nabla \cdot \left( \vec{h} \times \vec{e} \right) + \vec{h} \cdot \nabla \times \vec{e} - \partial_t \vec{d} \cdot \vec{e} =  \\
  & = - \nabla \cdot \vec{S} - \vec{h} \cdot \partial_t \vec{b} - \partial_t \vec{d} \cdot \vec{e} \ 
\end{aligned}$$ (eq:energy:free-current)

```

(classical-electromagnetism:energy-momentum:energy:integral:control)=
## Energy equation in integral form - control volumes

Integral form of energy equation for a control volume $V$ can be derived integrating the differential balance equation {eq}`eq:energy:2` over $V$, 

$$\dfrac{d}{dt}\int_{V} u + \int_{V} \vec{e} \cdot \vec{j} = - \oint_{\partial V} \hat{n} \cdot \vec{s}  \ ,$$ (eq:energy:integral:1)

having used the divergence theorem to transform volume integral of the divergence of Poynting vector into a flux integral across the boundary $\partial V$ of the domain, and exploited the indepndence of $V$ from time to take the time derivative outside the integral (see reuls for integration over time-depending domains).

**Interpretation.** This equation has an immediate interpretation in terms of energy of the system and power (dissipated? and exchanged with the external environemnt) **todo** *discuss* 

This equation can be recast in different forms. One of them is particurarly useful later in this material to discuss energy balance in different regimes of electromagnetic systems and in circuit approximation and discuss the validity of the circuit approximation itself.
Manipulating the surface contribution, the energy equation {eq}`eq:energy:integral:1` can be recast as

$$\dfrac{d}{dt} \int_V u + \int_{V} \vec{e} \cdot \vec{j} = - \oint_{\partial V} \, \phi \vec{j} \cdot \hat{n} + \oint_{\partial V} \hat{n} \cdot \left[ \frac{1}{\mu_0} \partial_t \vec{a} \times \vec{b} + \varepsilon_0 \, \phi\, \partial_t \vec{e} \right] \ ,$$ (eq:energy:integral:2)

highlighting two contributions in the surface term:
- the first contribution can be recast as the common power flux at ports of circuits used in circuit approximations,

   $$- \oint_{\partial V} \, \phi \, \vec{j} \cdot \hat{n} = \sum_{k \in \text{wires}} \, v_k  i_k \ ,$$

- the second contribution is often negligible in electromagnetic systems with **low characteristic frequencies** and **non-large-scale** systems, as it will be discussed **todo** *add link*

```{dropdown} Boundary contribution to electromagnetic energy
:open:

$$\begin{aligned}
\oint_{\partial V} \hat{n} \cdot \vec{s} 
& = \dfrac{1}{\mu_0} \oint_{\partial V} \hat{n} \cdot \vec{e} \times \vec{b} = \\
& = \dfrac{1}{\mu_0} \oint_{\partial V} \hat{n} \cdot \left( -\partial_t \vec{a} - \nabla \phi \right) \times \vec{b} = \\
& = - \dfrac{1}{\mu_0} \oint_{\partial V} \hat{n} \cdot \left( \partial_t \vec{a} \times \vec{b} + \nabla \times ( \phi \, \vec{b} ) - \phi \nabla \times \vec{b} \right)  = \\
& = - \dfrac{1}{\mu_0} \oint_{\partial V} \hat{n} \cdot \left( \partial_t \vec{a} \times \vec{b} - \phi \, \left( \mu_0 \vec{j} + \varepsilon_0 \mu_0 \, \partial_t \vec{e} \right) \right)  = \\
& = \oint_{\partial V}  \phi \, \vec{j} \cdot \hat{n} - \oint_{\partial V} \hat{n} \cdot \left[ \frac{1}{\mu_0} \partial_t \vec{a} \times \vec{b}+  \varepsilon_0  \, \phi\, \partial_t \vec{e} \right] \ ,
\end{aligned}$$

where the integral of the flux of the curl across a closed surface goes to zero, assuming that curl theorem holds (**todo** does it hold?).


```


(classical-electromagnetism:energy-momentum:energy:integral:arbitrary)=
## Energy equation in integral form - arbitrary domains

<!--
Now, using the constitutive equations involving the definition of the polarization and magnetization field,

$$\begin{aligned}
  \vec{d} & = \varepsilon_0 \vec{e} + \vec{p} \\
  \vec{b} & = \mu_0 \vec{h} - \mu_0 \vec{m} \\
\end{aligned}$$

equation {eq}`eq:energy:1` becomes

$$\begin{aligned}
 -  \vec{j}_f \cdot \vec{e} & = && \\
  & = \nabla \cdot \vec{s} + \vec{h} \cdot \partial_t \vec{b} + \partial_t \vec{d} \cdot \vec{e} = \\ 
  & = \nabla \cdot \vec{s} + ... + \varepsilon_0 \partial_t \vec{e} \cdot \vec{e} + \partial_t \vec{p} \cdot \vec{e} = \\ 
\end{aligned}$$
-->




## Linear isotropic media 

Using constitutive equations of a linear isotropic medium

$$\begin{aligned}
  \vec{d} & = \varepsilon_0 \vec{e} + \vec{p} && = \varepsilon \, \vec{e} \\
  \vec{b} & = \mu_0 \vec{h} - \mu_0 \vec{m}   && = \mu         \, \vec{h} \ ,
\end{aligned}$$

it's possible to derive dynamical equations for the energy density and momentum due to free current only,

$$\begin{cases}
& \partial_t U + \nabla \cdot \vec{S} = - \vec{e} \cdot \vec{j}^f \\
& \partial_t \vec{S} + c^2 \nabla \cdot \left[ \, U \mathbb{I} - \left( \vec{d} \otimes \vec{e} + \vec{h} \otimes \vec{b} \right) \, \right] = - c^2 \left( \vec{e} \, \rho^f - \vec{b} \times \vec{j}^f \right)
\end{cases}$$

**todo** *use this system to derive the [4-d formulation of special relativity in modern physics](https://basics2022.github.io/bbooks-physics-modern/ch/relativity-special/notes.html#electromagnetism)*


### Energy equation

The products in the power equation of free current {eq}`eq:energy:free-current` becomes

$$\begin{aligned}
  \vec{h} \cdot \partial_t \vec{b} + \partial_t \vec{d} \cdot \vec{e} 
  & = \dfrac{1}{\mu} \, \vec{b} \cdot \partial_t \vec{b} + \varepsilon \partial_t \vec{e} \cdot \vec{e}  = \\
  & = \partial_t \left[ \dfrac{1}{2} \left( \dfrac{1}{\mu} \, \vec{b} \cdot \vec{b} + \varepsilon \vec{e} \cdot \vec{e} \right) \right] = \\
  & = \partial_t \left[ \dfrac{1}{2} \left( \vec{h} \cdot \vec{b} + \vec{e} \cdot \vec{d} \right) \right] = \partial_t U \ .
\end{aligned}$$

and $\vec{S} = \vec{e} \times \vec{h} = \frac{\vec{e} \times \vec{b}}{\mu}$.
For linear media, the energy of the electromagnetic field per unit volume due to free current only thus reads

$$\begin{aligned}
 \partial_t U + \nabla \cdot \vec{S} = - \vec{e} \cdot \vec{j}_f \ .
\end{aligned}$$

### Momentum

Taking the time derivative of the Poynting vector,

$$\begin{aligned}
  \partial_t \vec{S} = \partial_t S_i 
  & = \partial_t \left( \varepsilon_{ijk} e_j h_k \right) = \\
  & = \varepsilon_{ijk} \, \partial_t e_j \, h_k + \varepsilon_{ijk} \, e_j \, \partial_t h_k  \ ,
\end{aligned}$$

and using the product rule to evaluate time derivative

```{dropdown} $\varepsilon_{ijk} \, \partial_t e_j \, h_k$
$$\begin{aligned}
  \varepsilon_{ijk} \partial_t e_j h_k
  & = \dfrac{1}{\varepsilon} \varepsilon_{ijk} \partial_t d_j h_k \\
  & = \dfrac{1}{\varepsilon} \varepsilon_{ijk} \left(\varepsilon_{jlm} \partial_l h_m - j^f_j \right) h_k \\
  & = - \dfrac{1}{\varepsilon} \varepsilon_{ijk} \, j^f_j \, h_k + \dfrac{1}{\varepsilon} \varepsilon_{ijk} \varepsilon_{jlm} h_k \partial_l h_m \\
  & = - \dfrac{1}{\varepsilon} \varepsilon_{ijk} \, j^f_j \, h_k + \dfrac{1}{\varepsilon} \left( \delta_{im} \delta_{kl} - \delta_{il} \delta_{km} \right) h_k \partial_l h_m =  \\
  & = - \dfrac{1}{\varepsilon} \varepsilon_{ijk} \, j^f_j \, h_k + \dfrac{1}{\varepsilon} \left( h_m \partial_m h_i - h_m \partial_i h_m \right) =  \\
  & = - \dfrac{1}{\varepsilon} \varepsilon_{ijk} \, j^f_j \, h_k + \dfrac{1}{\varepsilon} \left[ \partial_m ( h_m  h_i ) - \partial_m h_m \, h_i - \partial_i \left( \frac{h_m h_m}{2} \right) \right] =  \\
  & = \dfrac{1}{\varepsilon \mu} \varepsilon_{ijk} \, b_j \, j^f_k + \dfrac{1}{\varepsilon \mu} \left[ \partial_m ( b_m  h_i ) - \underbrace{\partial_m b_m}_{=0} \, h_i - \partial_i \left( \frac{h_m b_m}{2} \right) \right] =  \\
\end{aligned}$$
```

```{dropdown} $\varepsilon_{ijk} \, e_j \, \partial_t h_k$
$$\begin{aligned}
  \varepsilon_{ijk} e_j \partial_t h_k
  & =   \dfrac{1}{\mu} \varepsilon_{ijk} e_j \partial_t b_k = \\
  & = - \dfrac{1}{\mu} \varepsilon_{ijk} e_j \left( \varepsilon_{klm} \partial_l e_m \right) = \\
  & = - \dfrac{1}{\mu} \left( \delta_{il} \delta_{jm} - \delta_{im} \delta_{jl} \right) e_j \partial_l e_m =  \\
  & = - \dfrac{1}{\mu} \left( e_m \partial_i e_m - e_m \partial_m e_i \right) =  \\
  & = - \dfrac{1}{\mu} \left[ \partial_i \left(\frac{e_m e_m}{2}\right) -  \partial_m \left( e_m e_i \right) + \partial_m e_m \, e_i \right] = \\
  & = - \dfrac{1}{\varepsilon \mu} \left[ \partial_i \left(\frac{d_m e_m}{2}\right) - \partial_m \left( d_m e_i \right) + \rho^f \, e_i \right] \ .
\end{aligned}$$
```

the dynamical equation for the Poynting vector $\vec{S}$ reads

$$\partial_t S_i + c^2 \partial_m \left[ \dfrac{1}{2}\left( d_n e_n + h_n b_n \right) \delta_{mi} - \left( h_m b_i + d_m e_i \right) \right] = - c^2 \rho^f e_i + c^2 \varepsilon_{ijk} b_j j_k^f $$

or with vector notation

$$\partial_t \vec{S} + c^2 \nabla \cdot \left[ \, \dfrac{1}{2} \left( \vec{d} \cdot \vec{e} + \vec{h} \cdot \vec{b} \right) \mathbb{I} - \left( \vec{d} \otimes \vec{e} + \vec{h} \otimes \vec{b} \right) \, \right] = - c^2 \left( \rho^f \vec{e} - \vec{b} \times \vec{j}^f \right) \ .$$


