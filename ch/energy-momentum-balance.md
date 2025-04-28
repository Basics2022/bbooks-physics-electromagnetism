(classical-electromagnetism:energy)=
# Energy and momentum balance in linear, local, isotropic, non-dispersive media

$$\begin{cases}
  \mathbf{d} = \varepsilon_0 \mathbf{e} + \mathbf{p} \\
  \mathbf{h} = \dfrac{1}{\mu_0} \mathbf{b} - \mathbf{m} \ .
\end{cases}$$

with 

$$\mathbf{d} = \varepsilon \mathbf{e} \qquad , \qquad \mathbf{h} = \dfrac{\mathbf{b}}{\mu}$$

Let $r$ be mass density, and $\vec{v}$ be charge velocity field, the equation of motion - momentum equation - of electric charges reads

$$r \frac{D \mathbf{v}}{D t} = \mathbf{f} \ ,$$

and the kinetic energy equation becomes

$$\mathbf{v} \cdot \mathbf{f} = r \mathbf{v} \cdot \frac{D \mathbf{v}}{D t} = r \dfrac{D}{Dt} \dfrac{|\mathbf{v}|^2}{2} \ ,$$

or using continuity equation for $r$, it can be recast in conservative form. The same term can be recast using the expression of Lorentz's force on electric charges in electromagnetic field (**is this the right way to evaluate power of bounded charges and currents? check it!**)

$$\mathbf{v} \cdot \mathbf{f} = \mathbf{v} \cdot \left[ \rho ( \mathbf{e} - \mathbf{b} \times \mathbf{v} ) \right] = \rho \mathbf{v} \cdot \mathbf{e} = \mathbf{e} \cdot \mathbf{j} \ ,$$

and furthered manipulated writing $\mathbf{j} = \mathbf{j}_f + \mathbf{j}_p + \mathbf{j}_m$ and using Maxwell's equations

$$\begin{aligned}
  \mathbf{e} \cdot \mathbf{j} 
  & = \mathbf{e} \cdot \left( \mathbf{j}_f + \mathbf{j}_p + \mathbf{j}_m \right) = \\
  & = \mathbf{e} \cdot \left( \nabla \times \mathbf{h} - \partial_t \mathbf{d} \right) + \mathbf{e} \cdot \partial_t \mathbf{p} + \mathbf{e} \cdot \nabla \times \mathbf{m} = \\
  & = \mathbf{e} \cdot \nabla \times \left( \mathbf{h} + \mathbf{m} \right) - \mathbf{e} \cdot \partial_t \left( \mathbf{d} - \mathbf{p} \right)  = \\
  & = \dfrac{1}{\mu_0} \mathbf{e} \cdot \nabla \times \mathbf{b} - \varepsilon_0 \mathbf{e} \cdot \partial_t \mathbf{e} = \\
  & = - \dfrac{1}{\mu_0} \nabla \cdot \left( \mathbf{e} \times \mathbf{b} \right) - \dfrac{\mathbf{b}}{\mu_0} \cdot \partial_t \mathbf{b} - \varepsilon_0 \mathbf{e} \cdot \partial_t \mathbf{e} = \\
\end{aligned}$$

$$\mathbf{e} \cdot \nabla \times \mathbf{h} = e_i \varepsilon_{ijk} \partial_j h_k = \partial_j \left( \varepsilon_{jki} h_k e_i \right) - \varepsilon_{ijk} h_k \partial_j e_i = - \nabla \cdot (\mathbf{e} \times \mathbf{h} ) + \mathbf{h} \cdot \nabla \times \mathbf{e} = - \nabla \cdot (\mathbf{e} \times \mathbf{h} ) - \mathbf{h} \cdot \partial_t \mathbf{b}$$

$$\begin{aligned}
  \mathbf{e} \cdot \mathbf{j}_f & = - \nabla \cdot ( \mathbf{e} \times \mathbf{h} ) - \mathbf{e} \cdot \partial_t \mathbf{d} - \mathbf{h} \cdot \partial_t \mathbf{b}
\end{aligned}$$

## Linear media - energy
For linear media, the energy of the electromagnetic field per unit volume reads

$$u = \dfrac{1}{2} \left( \mathbf{e} \cdot \mathbf{d} + \mathbf{h} \cdot \mathbf{b} \right)$$

so that the differential balance equation for the eneergy of the electromagnetic field becomes

$$\begin{aligned}
 \partial_t u + \nabla \cdot \mathbf{s} = - \mathbf{e} \cdot \mathbf{j} \ ,
\end{aligned}$$

with Poynting vector $\mathbf{s} := \mathbf{e} \times \mathbf{h}$, namely the momentum density of the electromagnetic field.

## Linear media - momentum

$$\partial_t \mathbf{s} = \partial_t s_i = \partial_t \left( \varepsilon_{ijk} e_j h_k \right)$$

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

$$\begin{aligned}
  \varepsilon_{ijk} e_j \partial_t h_k
  & =   \dfrac{1}{\mu} \varepsilon_{ijk} e_j \partial_t b_k = \\
  & = - \dfrac{1}{\mu} \varepsilon_{ijk} e_j \left( \varepsilon_{klm} \partial_l e_m \right) = \\
  & = - \dfrac{1}{\mu} \left( \delta_{il} \delta_{jm} - \delta_{im} \delta_{jl} \right) e_j \partial_l e_m =  \\
  & = - \dfrac{1}{\mu} \left( e_m \partial_i e_m - e_m \partial_m e_i \right) =  \\
  & = - \dfrac{1}{\mu} \left[ \partial_i \left(\frac{e_m e_m}{2}\right) -  \partial_m \left( e_m e_i \right) + \partial_m e_m \, e_i \right] = \\
  & = - \dfrac{1}{\varepsilon \mu} \left[ \partial_i \left(\frac{d_m e_m}{2}\right) - \partial_m \left( d_m e_i \right) + \rho^f \, e_i \right] \ .
\end{aligned}$$

so that

$$\partial_t s_i + c^2 \partial_m \left[ \dfrac{1}{2}\left( d_n e_n + h_n b_n \right) \delta_{mi} - \left( h_m b_i + d_m e_i \right) \right] = - c^2 \rho^f e_i + c^2 \varepsilon_{ijk} b_j j_k^f $$

or

$$\partial_t \mathbf{s} + c^2 \nabla \cdot \left[ \, \dfrac{1}{2} \left( \mathbf{d} \cdot \mathbf{e} + \mathbf{h} \cdot \mathbf{b} \right) \mathbb{I} - \left( \mathbf{d} \otimes \mathbf{e} + \mathbf{h} \otimes \mathbf{b} \right) \, \right] = - c^2 \left( \rho^f \mathbf{e} - \mathbf{b} \times \mathbf{j}^f \right)$$



$$\begin{cases}
& \partial_t u + \nabla \cdot \mathbf{s} = - \mathbf{e} \cdot \mathbf{j}^f \\
& \partial_t \mathbf{s} + c^2 \nabla \cdot \left[ \, u \mathbb{I} - \left( \mathbf{d} \otimes \mathbf{e} + \mathbf{h} \otimes \mathbf{b} \right) \, \right] = - c^2 \left( \mathbf{e} \, \rho^f - \mathbf{b} \times \mathbf{j}^f \right)
\end{cases}$$

**todo** *use this system to derive the 4-d formulation of special relativity in modern physics*

