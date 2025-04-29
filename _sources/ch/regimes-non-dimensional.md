(classical-electromagnetism:regimes:non-dimensional)=
# Non-dimensional equations of electromagnetism

**Continuity equation of electric charge.**

  $$\partial_t \rho + \nabla \cdot \vec{j} = 0$$

**Maxwell's equations.**

  $$\begin{cases}
    \nabla \cdot \vec{e} = \dfrac{\rho}{\varepsilon_0} \\
    \nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\ 
    \nabla \cdot \vec{b} = 0 \\
    \nabla \times \vec{b} - \frac{1}{c_0^2} \partial_t \vec{e} = \mu_0 \vec{j} 
  \end{cases}$$

**Potentials.**

   $$\begin{aligned}
      \vec{b} & = \nabla \times \vec{a} \\
      \vec{e} & = -\partial_t \vec{a} - \nabla \phi \\
   \end{aligned}$$

**Gauge.**
**Wave equations.**


Assuming characteristic dimensions of the physical quantities involved in the problem exist, and allow to write the governing equations in non-dimensional form with contributions with (approximately at least) the same order of magnitude,

  $$
    f R \, \partial_t \rho + \dfrac{J}{L} \nabla \cdot \vec{j} = 0
  \qquad , \qquad
    \partial_t \rho + \dfrac{J}{f L R} \nabla \cdot \vec{j} = 0
  $$

  $$
  \begin{cases}
    \dfrac{E}{L} \nabla \cdot \vec{e} - \dfrac{R}{\varepsilon_0} \rho = 0 \\
    \dfrac{E}{L} \nabla \times \vec{e} + {B f} \, \partial_t \vec{b} = \vec{0} \\ 
    \dfrac{B}{L} \nabla \cdot \vec{b} = 0 \\
    \dfrac{B}{L} \nabla \times \vec{b} - \dfrac{E f}{c_0^2} \partial_t \vec{e} = \mu_0 J \, \vec{j} 
  \end{cases}
  \qquad , \qquad 
  \begin{cases}
    \nabla \cdot \vec{e} - \dfrac{R L}{\varepsilon_0 E} \rho = 0 \\
    \nabla \times \vec{e} + \dfrac{B f L}{E} \, \partial_t \vec{b} = \vec{0} \\ 
    \dfrac{B}{L} \nabla \cdot \vec{b} = 0 \\
    \nabla \times \vec{b} - \dfrac{E f L}{c_0^2 B} \partial_t \vec{e} = \dfrac{\mu_0 J L}{B} \, \vec{j} 
  \end{cases}
  $$

  $$
  \begin{aligned}
     B \vec{b} & = \dfrac{A}{L} \nabla \times \vec{a} \\
     E \vec{e} & = - A f \, \partial_t \vec{a} - \frac{\Phi}{L} \nabla \phi \\
  \end{aligned}
  \qquad , \qquad 
  \begin{aligned}
     \vec{b} & = \dfrac{A}{B L} \nabla \times \vec{a} \\
     \vec{e} & = - \dfrac{A f}{E} \, \partial_t \vec{a} - \frac{\Phi}{E L} \nabla \phi \\
  \end{aligned}
  $$

  $$
    \dfrac{A}{L} \nabla \cdot \vec{a} + \dfrac{f \Phi}{c_0^2} \partial_t \phi = 0
  \qquad , \qquad 
    \nabla \cdot \vec{a} + \frac{\Phi f L}{c_0^2 A} \partial_t \phi = 0
  $$

All these relations but Ampére-Maxwell's law and the definition of the electric field in terms of the potentials contains at most two terms: these relations can be used to immediately find the relation between the scales of the problem (if they're not independent), by setting the non-dimensional numbers equal to $1$,

<!--  J & = f L R && \text{from charge continuity equation} \\ -->
$$\begin{aligned}
  R & = \frac{\varepsilon_0 E}{L} && \text{from Gauss' law for $\vec{e}$} \\
  E & = B f L  && \text{from Faraday's law} \\
  A & = B L && \text{from the definition $\vec{b} = \nabla \times \vec{a}$} \\
  A & = \dfrac{\Phi f L}{c_0^2} && \text{from Lorentz's gauge} \\
\end{aligned}$$

while Ampére-Maxwell's equation and the definition of the electric field as a function of the electromagnetic potentials can be used to compare to define different regimes, comparing the non-dimensional numbers appearing in these relations

$$\begin{aligned}
  \nabla \times \vec{b} 
  & = \dfrac{\mu_0 J L}{B} \vec{j} + \dfrac{E f L}{c_0^2 B} \partial_t \vec{e}  = && (E = B f L) \\
  & = \dfrac{\mu_0 J L}{B} \vec{j} + \left(\dfrac{f L}{c_0}\right)^2 \partial_t \vec{e} = \\
  & = \dfrac{\mu_0 J L}{B} \left[ \vec{j} + \dfrac{B}{\mu_0 J L} \left(\dfrac{f L}{c_0}\right)^2 \partial_t \vec{e} \right] \\
\end{aligned}$$
$$\begin{aligned}
  \vec{e}
  & = - \dfrac{\Phi}{E L} \left[ \nabla \phi + \dfrac{A f L}{\Phi} \partial_t \vec{a} \right] = && \left( A = \dfrac{\Phi f L}{c_0^2} \right) \\ 
  & = - \dfrac{\Phi}{E L} \left[ \nabla \phi + \left( \dfrac{f L}{c_0} \right)^2 \partial_t \vec{a} \right]
\end{aligned}$$

