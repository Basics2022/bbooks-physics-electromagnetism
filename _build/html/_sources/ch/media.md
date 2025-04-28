<!--
```{article-info}
\:author: basics
\:date: "{sub-ref}`today`"
\:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:media)=
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
\nabla \cdot \vec{e} = \frac{\rho}{\varepsilon_0} \\
\nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\
\nabla \cdot \vec{b} = 0 \\
\nabla \times \vec{b} - \mu_0 \varepsilon_0 \partial_t \vec{e} = \mu_0 \vec{j}
\end{cases}$$

and more precisely 

- into Gauss' law for the electric field

  $$\begin{aligned}
    & 0  = \nabla \cdot \vec{e} - \frac{\rho}{\varepsilon_0} = \nabla \cdot \vec{e} - \frac{\rho_f - \nabla \cdot \vec{p}}{\varepsilon_0}  \\ \\
    & \rightarrow \qquad \nabla \cdot \vec{d} = \rho_f \ ,
  \end{aligned}$$

  with $\vec{d} = \varepsilon_0 \vec{e} + \vec{p}$ defined as the **displacement field**. 

- into continuity equation

  $$
    0 
    & = \partial_t \rho + \nabla \cdot \vec{j} = \\
    & = \partial_t \rho_f + \nabla \cdot \vec{j}_f + \partial_t \rho_b + \nabla \cdot ( \vec{j}_P + \nabla \times \vec{j}_M ) = \\
  $$

  since $\nabla \cdot \nabla \times \vec{m} \equiv 0$, and keeping separated the contributions of free and bound charges,

  $$\begin{aligned}
     & \partial_t \rho_f + \nabla \cdot \vec{j}_f = 0 \\
     & \partial_t \rho_P + \nabla \cdot \vec{j}_P = 0 \\ \\
     & \rightarrow \qquad \vec{j}_P = \partial_t \vec{p} \ .
  \end{aligned}$$


- and into Ampére-Maxwell's law
  
  $$\begin{aligned}
    \vec{0}
    & = \nabla \times \vec{b} - \mu_0 \varepsilon_0 \partial_t \vec{e} - \mu_0 \vec{j} = \\
    & = \nabla \times \vec{b} - \mu_0 \, \partial_t \left( \vec{d} - \vec{p} \right) - \mu_0 \vec{j}_f - \mu_0 \partial_t \vec{p} - \mu_0 \nabla \times \vec{m} \\
    & = \nabla \times \left( \vec{b} - \mu_0 \vec{m} \right) - \ mu_0 \, \partial_t \vec{d} - \mu_0 \vec{j}_f \\ \\ 
    & \rightarrow \qquad \nabla \times \vec{h}  - \, \partial_t \vec{d} = \vec{j}_f \ ,
  \end{aligned}$$

  where $\vec{h} := \vec{b} - \mu_0 \vec{m}$, the **magnetic field strength**.

## Continuous Media

In general, some materials respond to an imposed "external" electromagnetic field with polarization and magnetization. In particular, the electric polarization of a material corresponds to a local separation of electric charges, macroscopically equivalent to a volume density of dipoles, $\vec{p}(\vec{r}_0)$; magnetization corresponds to an orientation of the axes of Amperian current loops, macroscopically equivalent to a density of magnetic moment $\vec{m}(\vec{r}_0)$.

(classical-electromagnetism:media:polarization)=
## Polarization

### Single Electric Dipole
A discrete electric dipole is formed by two equal and opposite electric charges $q$, $-q$, at points $P_+$, $P_- = P_+ \vec{l}$, in the limit $q \rightarrow +\infty$, $|\vec{l}| \rightarrow 0$ with $q |\vec{l}|$ finite.

The electric field (stationary **todo** *check what happens in the non-stationary case. Perhaps after deriving the general solution to the problem, as a solution to the wave equations in terms of EM potentials*) generated at the point in space $\vec{r}$ by an electric dipole at the point $\vec{r}_0$ is calculated as the limit of the electric field generated by two equal and opposite charges $q^{\mp}$ at the points $\vec{r}_0 \mp \frac{\vec{l}}{2}$,

$$\vec{e}(\vec{r}) = -\frac{q}{4 \pi \varepsilon_0} \frac{\vec{r} - \left( \vec{r}_0 - \frac{\vec{l}}{2} \right)}{\left|\vec{r} - \left( \vec{r}_0 - \frac{\vec{l}}{2} \right)\right|^3} + \frac{q}{4 \pi \varepsilon_0} \frac{\vec{r} - \left( \vec{r}_0 + \frac{\vec{l}}{2} \right)}{\left|\vec{r} - \left( \vec{r}_0 + \frac{\vec{l}}{2} \right)\right|^3} \ .$$

Using the formula for the derivative of the terms

$$\partial_{\ell_k} \frac{x_i \pm \frac{\ell_i}{2}}{\left|\vec{x} \pm \frac{\vec{l}}{2} \right|^3} = \frac{1}{2} \left[ \pm \frac{\delta_{ik}}{r^3} - 3 r^{-4} \left( \pm \frac{x_k \pm \frac{\ell_k}{2}}{r} \right) \right]$$

$$\left. \partial_{\ell_k} \frac{x_i \pm \frac{\ell_i}{2}}{\left|\vec{x} \pm \frac{\vec{l}}{2} \right|^3} \right|_{\vec{l} = \vec{0}} = \mp \frac{1}{2} \left[ - \frac{\delta_{ik}}{|\vec{x}|^3} + 3 \left( \frac{x_k}{r^5} \right) \right] = \mp \frac{1}{2} \partial_{r_{0 k}} \frac{r_i - r_{0 i}}{|\vec{r} - \vec{r}_0|^3} = \mp \frac{1}{2} \nabla_{\vec{r}_0} \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} $$

we derive the first-order approximation in $\vec{l}$ of the two terms

$$\begin{aligned}
  \frac{\vec{r} - \left( \vec{r}_0 \mp \frac{\vec{l}}{2} \right)}{\left|\vec{r} - \left( \vec{r}_0 \mp \frac{\vec{l}}{2} \right)\right|^3}
  & = \frac{\vec{r} - \vec{r}_0 }{\left|\vec{r} - \vec{r}_0 \right|^3} \pm \vec{l} \cdot \frac{1}{2} \nabla_{\vec{r}_0} \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right) + o(|\vec{l}|)\\
\end{aligned}$$

and, defining the dipole intensity $\vec{P}_0 := q \vec{l}$ and taking the quantities to the desired limit, that of the electric field

$$\begin{aligned}
  \vec{e}(\vec{r})
  & = - \frac{1}{4\pi \varepsilon_0} \, \vec{P}_0 \cdot \nabla_{\vec{r}_0}  \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right)   = \\
  & = - \frac{1}{4\pi \varepsilon_0} \left[ \frac{(\vec{r}-\vec{r}_0)(\vec{r}-\vec{r}_0)}{|\vec{r}-\vec{r}_0|^5} \cdot \vec{P}_0 - \frac{\vec{P}_0}{|\vec{r}-\vec{r}_0|^3} \right] = \\
  & = - \frac{1}{4\pi \varepsilon_0} \left[ \frac{(\vec{r}-\vec{r}_0) \otimes (\vec{r}-\vec{r}_0)}{|\vec{r}-\vec{r}_0|^5} - \frac{\mathbb{I}}{|\vec{r}-\vec{r}_0|^3} \right] \cdot \vec{P}_0 \ .
\end{aligned}$$

**todo** In the general case, it would be necessary to pay attention to the order of the factors in the product between vectors and tensors, but in this case, the symmetry of the second-order tensor (or of the operations) can be exploited.

### Continuous Distribution of Dipoles

A distribution of dipoles with volume density $\vec{p}(\vec{r_0})$, which produces the elementary dipole $\Delta \vec{P}(\vec{r}_0) = \vec{p}(\vec{r}_0) dV_0$ in the volume $d V_0$, produces the electric field

$$\vec{e}(\vec{r}) = \int_{\vec{r}_0 \in V_0} \frac{1}{4 \pi \varepsilon_0} \vec{p}(\vec{r}_0) \cdot \nabla_{\vec{r}_0}  \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right) \ , $$

whose expression can be rewritten using the rules of integration by parts

$$\begin{aligned}
\vec{e}(\vec{r})
  & = \int_{\vec{r}_0 \in V_0} \frac{1}{4 \pi \varepsilon_0} \vec{p}(\vec{r}_0) \cdot \nabla_{\vec{r}_0}  \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right) = \\
  & = \oint_{\vec{r}_0 \in \partial V_0} \frac{1}{4 \pi \varepsilon_0}  \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \underbrace{ \hat{\vec{n}}(\vec{r}_0) \cdot \vec{p}(\vec{r}_0) }_{ =: \sigma_P(\vec{r}_0)}  + \int_{\vec{r}_0 \in V_0} \frac{1}{4 \pi \varepsilon_0} \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \underbrace{ \left( - \nabla_{\vec{r}_0} \cdot \vec{p}(\vec{r}_0) \right)}_{ =: \rho_P(\vec{r}_0) } \ , \\
\end{aligned}$$

having defined the surface polarization charge density $\sigma_P$ and the volume polarization charge density $\rho_P$ as the intensities of the distributed sources of the electric field, in analogy with the expression of Coulomb's law.

### Reformulation of Maxwell's Equations and Charge Continuity

Gauss's equation determines the volume flux density of the electric field $\vec{e}$,

$$\nabla \cdot \vec{e} = \frac{\rho}{\varepsilon_0} \ .$$

By decomposing the charge density as the sum of **free charges** $\rho_f$ and **polarization charges** $\rho_P := - \nabla \cdot \vec{p}$, we can rework Gauss's equation,

$$\begin{aligned}
 & \nabla \cdot \vec{e} = \frac{\rho_f + \rho_P}{\varepsilon_0} \\
 & \nabla \cdot \left( \varepsilon_0 \vec{e} + \vec{p} \right) = \rho_f \\ \\
 & \nabla \cdot \vec{d} = \rho_f \ ,
\end{aligned}$$

having introduced the **displacement field**, $\vec{d} := \varepsilon_0 \vec{e} + \vec{p}$.

The decomposition of the electric current as the sum $\vec{j} = \vec{j}_f + \vec{j}_P$ of the free current $\vec{j}_f$ and the polarization current $\vec{j}_P$, allows us to rework the continuity equation of electric charge

$$\begin{aligned}
  0 & = \partial_t \rho + \nabla \cdot \vec{j} = \\
    & = \partial_t (\rho_f + \rho_P) + \nabla \cdot \left( \vec{j}_f + \vec{j}_P \right) = \\
    & = \partial_t \rho_f + \nabla \cdot  \vec{j}_f + \partial_t \rho_P + \nabla \cdot \vec{j}_P \ ,
\end{aligned}$$

and write the continuity equations for the two charge distributions (of different nature, it is assumed that both must satisfy charge continuity independently, if free charges remain free and polarization charges remain polarization charges),

$$\begin{aligned}
  & \partial_t \rho_f + \nabla \cdot \vec{j}_f = 0 \\
  & \partial_t \rho_P + \nabla \cdot \vec{j}_P = 0 \qquad \rightarrow \qquad 0 = \nabla \cdot (-\partial_t \vec{p} + \vec{j}_P) \qquad \rightarrow \qquad \vec{j}_P = \partial_t \vec{p}
\end{aligned}$$

**todo** *justify absence of constant field*

(classical-electromagnetism:media:magnetization)=
## Magnetization

### Single Magnetic Moment (Limit of an Elementary Loop)
Using the Biot-Savart law, specialized for a conductor carrying current $i(\vec{r}_0)$

$$\begin{aligned}
  d \vec{b}(\vec{r})
  & = - \frac{\mu}{4 \pi} \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \times \vec{j}(\vec{r}_0) d V_0 = \\
  & = - \frac{\mu}{4 \pi} i(\vec{r}_0) \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \times \hat{\vec{t}}(\vec{r}_0) d \ell_0 \ ,
\end{aligned}$$

we can calculate the magnetic field generated by a loop with path $\ell_0 = \partial S_0$ using the PSCE

$$\begin{aligned}
  \vec{b}(\vec{r})
  & = \oint_{\ell_0} d \vec{b}(\vec{r}_0) = \\
  & = - \frac{\mu}{4 \pi} i_0 \oint_{\vec{r}_0 \in \ell_0} \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \times \hat{\vec{t}}(\vec{r}_0)  = \\
  & =   \frac{\mu}{4 \pi} i_0 \int_{\vec{r}_0 \in S_0} \hat{\vec{n}}(\vec{r}_0) \cdot \nabla_{\vec{r}_0} \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right)
\end{aligned}$$

The field generated by an elementary loop of surface $S_0$ with normal $\hat{\vec{n}}_0$, using the mean value theorem, is

$$\vec{b}(\vec{r}) = \frac{\mu}{4 \pi} i_0 S_0 \hat{\vec{n}}_0 \cdot \nabla_{\vec{r}_0} \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right) + o(S_0)$$

and as $i_0 \rightarrow \infty$, $S_0 \rightarrow 0$ such that $\vec{M}_0 := i_0 S_0 \hat{\vec{n}}_0$

$$\begin{aligned}
 \vec{b}(\vec{r})
  & = \frac{\mu}{4 \pi} \vec{M}_0 \cdot \nabla_{\vec{r}_0} \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right) \\
  & = - \frac{\mu_0}{4\pi} \left[ \frac{(\vec{r}-\vec{r}_0)(\vec{r}-\vec{r}_0)}{|\vec{r}-\vec{r}_0|^5} \cdot \vec{M}_0 - \frac{\vec{M}_0}{|\vec{r}-\vec{r}_0|^3} \right] = \\
  & = - \frac{\mu_0}{4\pi} \left[ \frac{(\vec{r}-\vec{r}_0) \otimes (\vec{r}-\vec{r}_0)}{|\vec{r}-\vec{r}_0|^5} - \frac{\mathbb{I}}{|\vec{r}-\vec{r}_0|^3} \right] \cdot \vec{M}_0 \ .
\end{aligned}$$

**todo** Analogy with the electric field produced by a distribution of dipoles.

```{dropdown} Details
$$\oint_{\partial S} A \, t_i = \int_S \varepsilon_{ijk} \, n_j \, \partial_k A
\qquad , \qquad
  \oint_{\partial S} A \, \hat{\vec{t}} = \int_S \hat{\vec{n}} \times \nabla A$$

$$\begin{aligned}
\oint_{\vec{r}_0 \in \ell_0} \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \times \hat{\vec{t}}(\vec{r}_0) d \ell_0
  & = \oint_{\vec{r}_0 \in \ell_0} \varepsilon_{ijk} \frac{r_j - r_{0,j}}{|\vec{r} - \vec{r}_0|^3}  t_k = \\
  & = \int_{\vec{r}_0 \in S_0} \varepsilon_{krs} n_r \partial^0_s \left( \varepsilon_{ijk} \frac{r_j - r_{0,j}}{|\vec{r} - \vec{r}_0|^3} \right) = \\
  & = \int_{\vec{r}_0 \in S_0} \left( \delta_{ir} \delta_{js} - \delta_{is} \delta_{jr} \right) n_r \partial^0_s \left( \frac{r_j - r_{0,j}}{|\vec{r} - \vec{r}_0|^3} \right) = \\
  & = \int_{\vec{r}_0 \in S_0} \left\{ n_i \underbrace{\partial^0_j \left( \frac{r_j - r_{0,j}}{|\vec{r} - \vec{r}_0|^3} \right)}_{=0} - n_j \partial^0_i \left( \frac{r_j - r_{0,j}}{|\vec{r} - \vec{r}_0|^3} \right) \right\} = \\
  & = - \int_{\vec{r}_0 \in S_0} n_j \partial^0_i \left( \frac{r_j - r_{0,j}}{|\vec{r} - \vec{r}_0|^3} \right) \ .
\end{aligned}$$
```

### Continuous Distribution of Magnetic Moment

To calculate the magnetic field generated by a volume distribution of magnetic moment, we can proceed in analogy with what was done to calculate the electric field generated by a distribution of dipoles

$$\begin{aligned}
\vec{b}(\vec{r})
  & = \int_{\vec{r}_0 \in V_0} \frac{\mu_0}{4 \pi } \vec{m}(\vec{r}_0) \cdot \nabla_{\vec{r}_0}  \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right) = \\
  & = \oint_{\vec{r}_0 \in \partial V_0} \frac{\mu_0}{4 \pi}  \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \hat{\vec{n}}(\vec{r}_0) \cdot \vec{m}(\vec{r}_0) + \int_{\vec{r}_0 \in V_0} \frac{\mu_0}{4 \pi} \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \,\left( - \nabla_{\vec{r}_0} \cdot \vec{m}(\vec{r}_0) \right) \ , \\
\end{aligned}$$

but without obtaining an analogy with the expression of the Biot-Savart law, which involves the cross product between the term $\frac{\vec{r}- \vec{r}_0}{|\vec{r} - \vec{r}_0|^3}$ and a current density $\vec{j}(\vec{r}_0)$.

```{dropdown} Details

We can rewrite

$$\begin{aligned}
  \oint_{\vec{r}_0 \in \partial V_0} & \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \times \left( \hat{\vec{n}}(\vec{r}_0) \times \vec{m}(\vec{r}_0) \right) \\
  & = \oint_{\vec{r}_0 \in \partial V_0} \varepsilon_{ijk} \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} \varepsilon_{krs} n_r m_s = \\
  & = \int_{\vec{r}_0 \in V_0} \left( \delta_{ir} \delta_{js} - \delta_{is} \delta_{jr} \right) \partial^0_r \left( \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} m_s \right) = \\
  & = \int_{\vec{r}_0 \in V_0} \left\{ \partial^0_i \left( \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} m_j \right) - \partial^0_j \left( \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} m_i \right)  \right\} = \\
  & = \int_{\vec{r}_0 \in V_0}
  \left\{ \partial^0_i \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} m_j
         + \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} \partial^0_i m_j
         - \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} \partial^0_j m_i
         - \underbrace{ \partial^0_j \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3}}_{=0} m_i
  \right\} = \\
  & = \int_{\vec{r}_0 \in V_0}
  \left\{ \partial^0_i \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} m_j
         + \varepsilon_{ijk} \varepsilon_{krs} \frac{r_j - r_{0,j}}{|\vec{r}-\vec{r}_0|^3} \partial^0_r m_s
  \right\} = \\
  & = \int_{\vec{r}_0 \in V_0}
  \left\{ \nabla_{\vec{r}_0} \frac{\vec{r} - \vec{r}_0}{|\vec{r}-\vec{r}_0|^3} \cdot \vec{m}(\vec{r}_0)
         + \frac{\vec{r} - \vec{r}_0}{|\vec{r}-\vec{r}_0|^3} \times \left( \nabla_{\vec{r}_0} \times \vec{m}(\vec{r}_0) \right)
  \right\} = \\
\end{aligned}$$

using vector calculus identities,

$$\begin{aligned}
  \vec{a} \times (\vec{b} \times \vec{c}) & = \varepsilon_{ijk} a_j \varepsilon_{krs} b_r c_s = \\
  & = (\delta_{ir} \delta_{js} - \delta_{is} \delta_{jr}) a_j b_r c_s = \\
  & = a_j b_i c_j - c_i b_j a_j = \vec{b}(\vec{a} \cdot \vec{c}) - \vec{c} (\vec{a} \cdot \vec{b})
\end{aligned}$$

$$\begin{aligned}
 a_j \partial_i m_j - a_j \partial_j m_i
 & = (\delta_{ir} \delta_{js} - \delta_{is} \delta_{jr}) a_j \partial_r m_s = \\
 & = \varepsilon_{ijk} \varepsilon_{krs} a_j \partial_r m_s = \\
 & = \vec{a} \times \left( \nabla \times \vec{m} \right)
\end{aligned}$$

The magnetic field generated by a distribution of magnetic moment can therefore be rewritten as

$$\begin{aligned}
\vec{b}(\vec{r})
  & = \int_{\vec{r}_0 \in V_0} \frac{\mu_0}{4 \pi } \vec{m}(\vec{r}_0) \cdot \nabla_{\vec{r}_0}  \left( \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \right) = \\
  & = - \frac{\mu_0}{4\pi} \oint_{\vec{r}_0 \in \partial V_0} \frac{\vec{r} - \vec{r}_0}{|\vec{r} - \vec{r}_0|^3} \times \underbrace{ \left( - \hat{\vec{n}}(\vec{r}_0) \times \vec{m}(\vec{r}_0) \right) }_{\vec{j}^s_M}
  - \frac{\mu_0}{4 \pi} \int_{\vec{r}_0 \in V_0} \frac{\vec{r} - \vec{r}_0}{|\vec{r}-\vec{r}_0|^3} \times \underbrace{ \left(\nabla_{\vec{r}_0} \times \vec{m}(\vec{r}_0) \right)}_{\vec{j}_M} \ ,
\end{aligned}$$

having defined the surface magnetization current density $\vec{j}^s_M$ and the volume magnetization current density $\vec{j}_M$ as the intensities of the distributed singularities, in analogy with the expression of the Biot-Savart law.

```

### Reformulation of Maxwell's Equations and Charge Continuity

The Ampère-Maxwell law can be rewritten

$$\begin{aligned}
 & \nabla \times \vec{b} - \mu_0 \varepsilon_0 \partial_t \vec{e} = \mu_0 \vec{j} \\
 & \nabla \times \vec{b} - \mu_0 \partial_t \left( \vec{d} - \vec{p} \right) = \mu_0 \left( \vec{j}_f + \vec{j}_P + \vec{j}_M \right) \\
 & \nabla \times \underbrace{\left( \vec{b} - \mu_0 \vec{m} \right)}_{=: \mu_0 \vec{h}} - \mu_0 \partial_t \vec{d} + \mu_0 \underbrace{\left( \partial_t \vec{p} - \vec{j}_P \right)}_{= \vec{0}} = \mu_0 \vec{j}_f  \\ \\
 & \nabla \times \vec{h} - \partial_t \vec{d} = \vec{j}_f
\end{aligned}$$

From the continuity equation of electric current,

$$\partial_t \rho + \nabla \cdot \vec{j} = 0 \ ,$$

we derive the continuity equation for magnetization charges

$$\begin{aligned}
  0 & = \partial_t \rho_M + \nabla \cdot \vec{j}_M = \\
    & = \partial_t \rho_M + \underbrace{ \nabla \cdot \nabla \times \vec{m}}_{ \equiv \vec{0} } \ .
\end{aligned}$$

## Examples
- conductors
- ferromagnetic and weak magnetism (para-, dia-, anti-)

(classical-electromagnetism:media:jump)=
## Jump Conditions
Differential form of Maxwell's equations

$$\begin{cases}
 \nabla \cdot \vec{d} = \rho_f \\
 \nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\
 \nabla \cdot \vec{b} = 0 \\
 \nabla \times \vec{h} - \partial_t \vec{d} = \vec{j}_f
\end{cases}$$

Integral form of Maxwell's equations

$$\begin{cases}
 \displaystyle \oint_{\partial V} \vec{d} \cdot \hat{\vec{n}} = \int_{V} \rho_f \\
 \displaystyle \oint_{\partial S} \vec{e} \cdot \hat{\vec{t}} + \dfrac{d}{dt} \int_S \vec{b} \cdot \hat{\vec{n}} = 0 \\
 \displaystyle \oint_{\partial V} \vec{b} \cdot \hat{\vec{n}} = 0 \\
 \displaystyle \oint_{\partial S} \vec{h} \cdot \hat{\vec{t}} - \dfrac{d}{dt} \int_S \vec{d} \cdot \hat{\vec{n}} = \int_{S} \vec{j}_f \cdot \hat{\vec{n}} \\
\end{cases}$$

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

