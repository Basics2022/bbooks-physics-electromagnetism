(classical-electromagnetism:electrostatics)=
# Electrostatics

Elextrostatics studies the electric phenomena in systems with stationary charges. Thus, current is identically zero $\vec{j} = \vec{0}$.

So far, this chapter contains random topics:

- [Governing equations of electrostatics](classical-electromagnetism:electrostatics:governing-equations)
- [Zero electric field insiede a conductor](classical-electromagnetism:electrostatics:zero-field-conductor)
- [Energy of a system of charges](classical-electromagnetism:electrostatics:energy-system-of-charges)

(classical-electromagnetism:electrostatics:governing-equations)=
## Governing equation of electrostatics

Electrostatics studies systems with no motion of charges, and thus no currents, $\vec{j} = \vec{0}$, and time dependency, $\partial_t \equiv 0$.

**Maxwell's equations.**

  $$\begin{cases}
    \nabla \cdot \vec{e} = \dfrac{\rho}{\varepsilon_0} \\
    \nabla \times \vec{e} = \vec{0} \\ 
    \nabla \cdot \vec{b} = 0 \\
    \nabla \times \vec{b} = \vec{0}
  \end{cases}$$

**Potentials.**

   $$\begin{aligned}
      \vec{b} & = \nabla \times \vec{a} \\
      \vec{e} & = - \nabla \phi \\
   \end{aligned}$$

As both the divergence and the curl of the magnetic field are zero, only constant and uniform magnetic field are allowed.
In absence of magnetic field, the problem is fully determined by the Gauss' law for the electric field and the steady condition of the Faraday's law, implying that the irrotational electric field can be written as the gradient of a scalar potential,

$$\vec{e} = - \nabla \varphi \ .$$

Introducing this expression into Gauss' law for the electric field, electrostatics can be formulated as a problem governed by a Laplace equation for the scalar potential

$$-\Delta \varphi = \dfrac{\rho}{\varepsilon_0} \ ,$$

supplied with the proper boundary conditions. **todo** *discuss boundary conditions...*

(classical-electromagnetism:electrostatics:zero-field-conductor)=
## Zero electric field inside a conductor

Studying the transient of the electric charge distribution inside a conductor,

$$\vec{e} = \rho_R \vec{j} \ ,$$

whose constitutive equation is

$$\vec{d} = \varepsilon \vec{e} \ ,$$

with free electric charge continuity equation

$$\partial_t \rho_f + \nabla \cdot \vec{j}_f = 0 \ ,$$

and Gauss equation for the displacement field 

$$\nabla \cdot \vec{d} = \rho_f \ .$$

$$\begin{aligned}
  \partial_t \rho_f
  & = - \nabla \cdot \vec{j}_f = \\
  & = - \nabla \cdot \left( \frac{1}{\rho_R} \vec{e} \right) = \\
  & = - \frac{1}{\rho_R \varepsilon} \nabla \cdot \vec{d} = \\
  & = - \frac{1}{\rho_R \varepsilon} \rho_f \ ,
\end{aligned}$$

having assumed uniform properties. The differential equation in the volume of the conductor provides the evolution of the electric charge in the volume $\rho(\mathbf{r},t)$, given the initial condition $\rho(\mathbf{r},0) = \rho_{f,0}(\mathbf{r})$

$$\partial_t \rho_f = - \frac{1}{\rho_R \varepsilon} \rho_f$$

$$\rho_f(\mathbf{r},t) = \rho_{f,0}(\mathbf{r}) \exp\left[ - \dfrac{t}{\rho_R \varepsilon} \right] \ .$$

For a conductor:
- $\varepsilon \sim \varepsilon_0 = 8.85 \cdot 10^{-12} \text{F} \text{m}^-1$
- $\rho_R \sim 10^{-7}  \Omega \, \text{m}$

so that the time constant (that can be thought as a characteristic time) of the process is

$$\tau = \rho_R \varepsilon \sim 8.85 \cdot 10^{-19} \, \text{s} \ , $$

and thus, after a very short period of time the volume charge density is approximately zero everywhere in the volume: it accumulates in a very thin surface layer.


```{dropdown} Proof

$$\partial_t \left( \rho_f e^{\frac{t}{\rho_R \varepsilon}} \right) = 0$$

$$\rho_f(\mathbf{r},t) e^{\frac{r}{\rho_R \varepsilon}} = a(\mathbf{r})$$

and appylying initial conditions in all the points of the domain, $\rho_{f}(\mathbf{r},0) = \rho_{f,0}(\mathbf{r})$, function $a(\mathbf{r})$ must be equal to $\rho_{f,0}(\mathbf{r})$ and the solution reads

$$\rho_f(\mathbf{r},t) = \rho_{f,0}(\mathbf{r}) \exp \left[ -\dfrac{t}{\rho_R \varepsilon} \right]$$

```

As charge density and current density is zero inside a conductor, the electric field is zero as well. Thus, the electrostatic potential is uniform inside a conductor in electrostatic regime.

(classical-electromagnetism:electrostatics:energy-system-of-charges)=
## Energy of a system of charges

This section discusses the electrostatic energy of a system of charges. The energy of the system of charges is computed using the external work done on the system required to build the final configuration of the system, see [here](https://basics2022.github.io/bbooks-physics-hs/ch/electromagnetism/electrostatics.html#energia-potenziale-di-una-distribuzione-di-cariche) for more details. The work done by external forces is equal and opposite in sign to the work done by internal forces, if the initial and final configurations are at rest (and thus, there's no change in kinetic energy between the initial and final configuration), and no dissipative actions occurs in the process. Positioning one charge after the other, the external force acting on the $n^{th}$ charge must equilibrate the sum of internal forces (Coulomb force) due to the $n-1$ charges previously arranged.

$$\begin{aligned}
  L^{ext}_{1} & = 0 \\
  L^{ext}_{2} & = \int_{P_\infty}^{P_2} \vec{F}_{21}(\vec{r}) \cdot d \vec{r} = - q_2 \int_{P_\infty}^{P_2} \vec{E}_{1}(\vec{r}) \cdot d \vec{r}
  = q_2 \Delta V_{21} = q_1 q_2 \Delta V^{(1)}_{21} \\
  \dots \\
  L^{ext}_{n} & = \int_{P_\infty}^{P_n} \sum_{i=1}^{n-1} \vec{F}_{ni}(\vec{r}) \cdot d \vec{r} = - q_n \int_{P_\infty}^{P_n} \sum_{i=1}^{n-1} \vec{E}_{i}(\vec{r}) \cdot d \vec{r} = \sum_{i=1}^{n-1} q_{n} q_{i} \Delta V^{(1)}_{ni} \\
\end{aligned}$$

so that

$$\begin{aligned}
  E 
  & = \sum_{i=1}^{n} L^{ext}_i = - \sum_{i=1}^{n} L^{int}_i = \\
  & = \sum_{n=1}^{N} \sum_{i=1}^{n-1} q_n q_i \Delta V_{ni}^{(1)} = \\
  & = \sum_{\{ i,j \}, i \ne j} q_j q_i \Delta V_{ji}^{(1)} = \\
  & = \sum_{  (i,j), i \ne j} \frac{1}{2} q_j q_i \Delta V_{ji}^{(1)} \ ,
\end{aligned}$$

with the $\{ i, j \}$ unordered pairs (i.e. not summing twice on $\{ i,k \}$ and $\{ k, i\}$) or ordered pairs $(i, k)$ (summing both $(i,k)$ and $(k,i)$), and $V_{ij}^{(1)} = V_{ji}^{(1)}$.

**Point charges.** 

$$\begin{aligned}
  \vec{F}_{ik} & = \frac{q_i q_k}{4 \pi \varepsilon} \frac{\vec{r}_i - \vec{r}_k}{|\vec{r}_i - \vec{r}_k|^3} \\
  \vec{E}_{k}(\vec{r}_i) & = \frac{q_k}{4 \pi \varepsilon} \frac{\vec{r}_i - \vec{r}_k}{|\vec{r}_i - \vec{r}_k|^3} \\
        V_{k}(\vec{r}_i) & = \frac{q_k}{4 \pi \varepsilon} \frac{1}{|\vec{r}_i - \vec{r}_k|} \\
        V_{ki}^{(1)} & = V_{ik}^{(1)} = \frac{1}{4 \pi \varepsilon} \frac{1}{|\vec{r}_i - \vec{r}_k|} \ .
\end{aligned}$$

(classical-electromagnetism:electrostatics:energy-system-of-charges:uniform-potential)=
### Systems with uniform potential

 The work done by an external force to move a charge $q$ from a region with electric potential $V_0 = 0$ to a system with electic potential $V$ reads

$$L^{ext} = q (V - V_0) = q V \ .$$

As an example, a **double layer of charges** (globally neutral) creates a potential difference across it. Assuming a piecewise uniform charge distribution,

| $x$ | $\rho(x)$ | $e(x)$ | $V(x)$  |
| :--- | :--- | :--- | :--- |
| $\in (-\infty,x_1]$ | $0$    | $0$                | $0$                    |
| $\in [x_1,0]$       | $-q$   | $-\frac{q}{\varepsilon}(x-x_1)$        | $ \frac{q}{2 \varepsilon}(x-x_1)^2$ |
| $\in [0,x_2]$       | $ q$   | $ \frac{q}{\varepsilon}(x-x_2)$        | $-\frac{q}{2 \varepsilon}(x-x_2)^2 + \frac{q}{2 \varepsilon}(x_1^2 + x_2^2)$ |
| $\in [x_2,+\infty)$ | $0$    | $0$                | $\frac{q}{2 \varepsilon}(x_1^2 + x_2^2)$                   |

with $\sigma = q x_2 = - q x_1 = \frac{Q}{S}$ the surface density $\left[ \frac{\text{charge}}{\text{length}^2} \right]$, for the global neutrality of the interface, $S$ the area of the interface and $Q$ the electric charge on its positive side. Thus the potential difference across the interface reads

$$V = \frac{q}{2 \varepsilon}(x_1^2 + x_2^2) = \frac{q}{2 \varepsilon} ( (-x_1)(-x_1) + x_2 x_2 ) = \frac{\sigma}{2 \varepsilon} (x_2 - x_1) = \frac{\sigma}{2} w = \frac{w}{2 \varepsilon S} Q \ .$$

The potential difference is a function of the charge $Q$. In order to move a charge $dQ$ from the negative to the positive side of the interface, with potential $V(Q)$, a work equal to 

$$d L = V(Q) dQ$$

is required. Assuming $w$, $\varepsilon$, $S$ as a constant, the work to transfer a total charge $\Delta Q_0 = Q_1 - Q_0$ starting from $Q_0$ reads

$$L = \int_{Q_0}^{Q_1} d L =  \int_{Q_0}^{Q_1} V(Q) dQ = \int_{Q_0}^{Q_1} \frac{w}{2 \varepsilon S} Q dQ = \frac{w}{4 \varepsilon S} \left( Q_1^2 - Q_0^2 \right) \ .$$


