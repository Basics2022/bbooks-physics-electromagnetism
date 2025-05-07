(classical-electromagnetism:regimes:non-dimensional)=
# Non-dimensional equations of electromagnetism

Non-dimensional form of the equations of electromagnetism are derived here, defining every dimensional physical quantity as the product of a dimensional reference value and the non-dimensional quantity, $g = G \widetilde{g}$, or with a small abuse of notation to avoid writing lots of tildes and to keep lighter notation,

$$g = G g \ ,$$

using the same symbol to indicate the dimensional and the non-dimensional quantity. Here, capital letters are used for reference dimensional quantities.

This procedure allows to estimate the order of magnitude of the physical quantities involved in the problem: without any independent physical quantities, non-dimensional numbers are set equal to $1$, whenever it's possible. Only two equations, namely Ampére-Maxwell equation and the definition of the electric field with the EM potentials, contain 3 terms

**Continuity equation of electric charge.**

  $$\partial_t \rho + \nabla \cdot \vec{j} = 0$$

**Maxwell's equations.**

  $$\begin{cases}
    \nabla \cdot \vec{e} = \dfrac{\rho}{\varepsilon_0} \\
    \nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\ 
    \nabla \cdot \vec{b} = 0 \\
    \nabla \times \vec{b} - \frac{1}{c_0^2} \partial_t \vec{e} = \mu_0 \vec{j} 
  \end{cases}$$

**Constitutive laws**, here for linear isotropic medium

$$\begin{aligned}
  \vec{d} & = \varepsilon \vec{e} \\
  \vec{b} & = \mu         \vec{h} \\
\end{aligned}$$

**Potentials.**

   $$\begin{aligned}
      \vec{b} & = \nabla \times \vec{a} \\
      \vec{e} & = -\partial_t \vec{a} - \nabla \phi \\
   \end{aligned}$$

**Gauge.** Lorentz's gauge

$$0 = \dfrac{1}{c^2} \partial_t \phi + \nabla \cdot \vec{a}$$

**Wave equations.**

...

Assuming characteristic dimensions of the physical quantities involved in the problem exist, and allow to write the governing equations in non-dimensional form with contributions with (approximately at least) the same order of magnitude,

$$
\begin{aligned}
   &  F R \, \partial_t \rho_f + \dfrac{J}{L} \nabla \cdot \vec{j}_f = 0 \\ \\
   &  \dfrac{D}{L} \nabla \cdot \vec{d} - R \rho_f = 0 \\
   &  \dfrac{E}{L} \nabla \times \vec{e} + {B F} \, \partial_t \vec{b} = \vec{0} \\ 
   &  \dfrac{B}{L} \nabla \cdot \vec{b} = 0 \\
   &  \dfrac{H}{L} \nabla \times \vec{h} - F D \partial_t \vec{d} = J \, \vec{j}_f  \\ \\
   &  D \vec{d} = \varepsilon E \vec{e} \\
   &  B \vec{b} = \mu H \vec{h} \\ \\
   &  B \vec{b} = \dfrac{A}{L} \nabla \times \vec{a} \\
   &  E \vec{e} = - A F \, \partial_t \vec{a} - \frac{\Phi}{L} \nabla \phi \\ \\
   & \dfrac{A}{L} \nabla \cdot \vec{a} + \dfrac{F \Phi}{c_0^2} \partial_t \phi = 0
\end{aligned}
\qquad , \qquad
\begin{aligned}
   &  \partial_t \rho_f + \dfrac{J}{F L R} \nabla \cdot \vec{j}_f = 0 \\ \\
   &  \nabla \cdot \vec{d} - \dfrac{R L}{D} \rho_f = 0 \\
   &  \nabla \times \vec{e} + \frac{B F L}{E} \, \partial_t \vec{b} = \vec{0} \\ 
   &  \nabla \cdot \vec{b} = 0 \\
   &  \nabla \times \vec{h} - \dfrac{D L F}{H} \partial_t \vec{d} = \frac{J L}{H} \, \vec{j}_f  \\ \\
   &  \vec{d} = \frac{\varepsilon E}{D} \vec{e} \\
   &  \vec{b} = \frac{\mu H}{B} \vec{h} \\ \\
   &  \vec{b} = \dfrac{A}{B L} \nabla \times \vec{a} \\
   &  \vec{e} = \frac{\Phi}{E L} \left[ - \dfrac{A FL}{\Phi} \, \partial_t \vec{a} - \nabla \phi \right] \\ \\
   &  \nabla \cdot \vec{a} + \dfrac{F L \Phi}{A c_0^2} \partial_t \phi = 0
\end{aligned}
$$


All these relations but Ampére-Maxwell's law and the definition of the electric field in terms of the potentials contains at most two terms: these relations can be used to immediately find the relation between the scales of the problem (if they're not independent), by setting the non-dimensional numbers equal to $1$,

<!--  J & = f L R && \text{from charge continuity equation} \\ -->
$$\begin{aligned}
  J & = R F L                                &  \text{from contintuity} \\
  R & = \frac{D}{L}                          &  \text{from Gauss' law for $\vec{d}$} \\
  E & = B F L                                &  \text{from Faraday's law} \\
  D & = \varepsilon E                        &  \text{from $\vec{d} = \varepsilon \vec{e}$} \\
  B & = \mu H                                &  \text{from $\vec{b} = \mu         \vec{h}$} \\
  A & = B L                                  &  \text{from the definition $\vec{b} = \nabla \times \vec{a}$} \\
  A & = \dfrac{\Phi F L}{c_0^2}              &  \text{from Lorentz's gauge} \\
\end{aligned}$$ (eq:non-dim:c)

Using these definitions of the characteristic dimensions of the problem, the pairs of terms in Ampére-Maxwell law and in the the definition of the electric field are compared

$$\begin{aligned}
  \frac{D L F}{H}     & = \dfrac{\varepsilon \mu E L F}{B} = \left( \dfrac{FL}{c} \right)^2 \\
  \frac{A FL}{\Phi} & = \dfrac{\Phi F L}{c^2} \frac{FL}{\Phi} = \left(\dfrac{FL}{c}\right)^2 \\
\end{aligned}$$

<span style="color:red">**todo** *check obseration at the end of thi section*</span>

Setting equal to $1$ al the independent non-dimensional numbers, (**todo** *is it possible? Are they really independent*), including 

$$H = JL \qquad , \qquad \Phi = E L \ ,$$

the non-dimensional form of the equations of electromagnetism becomes

$$
\begin{aligned}
  & \text{continuity equation for charge}        &&  \partial_t \rho_f +  \nabla \cdot \vec{j}_f = 0 \\ \\
  & \text{Maxwell's equations}                   &&  \nabla \cdot \vec{d} - \rho_f = 0 \\
  &                                              &&  \nabla \times \vec{e} +  \partial_t \vec{b} = \vec{0} \\ 
  &                                              &&  \nabla \cdot \vec{b} = 0 \\
  &                                              &&  \nabla \times \vec{h} - \left(\dfrac{FL}{c}\right)^2 \partial_t \vec{d} = \, \vec{j}_f  \\ \\
  & \text{constitutive equations}                &&  \vec{d} = \vec{e} \\
  &                                              &&  \vec{b} = \vec{h} \\ \\
  & \text{EM potentials}                         &&  \vec{b} = \nabla \times \vec{a} \\
  &                                              &&  \vec{e} = - \left( \dfrac{FL}{c} \right)^2 \partial_t \vec{a} - \nabla \phi \\ \\
  & \text{Lorentz's gauge}                       &&  \nabla \cdot \vec{a} + \partial_t \phi = 0
\end{aligned}
$$ (eq:em:non-dimensional)

<span style="color:red">**todo** *check compatibility in the definition of the charactersitic physical quantities; need to distinguish steady and time-dependent terms?*</span>

<!--
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
  & = - \dfrac{\Phi}{E L} \left[ \nabla \phi + \left( \dfrac{F L}{c_0} \right)^2 \partial_t \vec{a} \right]
\end{aligned}$$
-->
