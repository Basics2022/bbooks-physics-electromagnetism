(classical-electromagnetism:circuits-electromagnetic:transformer)=
# Transformer

- Magnetic field flux, assuming a uniform field or in terms of the average field:

  $$\phi = b \, A$$

- Magnetic field flux linked to $N$ windings:

  $$\psi = N \, \phi$$

- Relationship between the voltage at the inductor terminals and the linked flux, applying [Faraday's law to irrotational parts](classical-electromagnetism:circuits-electric:induction):

  $$v = \dot{\psi}$$

## Ideal Transformer

In the absence of stray fluxes and reluctance in the air gap, the loop law in the air gap implies:

$$0 = m_1 + m_2 = N_1 \, i_1 + N_2 \, i_2$$

The magnetic field flux can be written in terms of the flux linked to the windings:

$$\phi = \frac{\psi_1}{N_1} = \frac{\psi_2}{N_2}$$

The time derivative of this relation, with a constant number of windings over time, implies:

$$\frac{v_2}{N_2} = \frac{v_1}{N_1} \ .$$

## Transformer with Stray Fluxes

$$\begin{cases}
  \phi_1 - \phi_{1,d} = \phi \\
  \phi_2 - \phi_{2,d} = \phi \\
  m_1 = \theta_{1,d} \phi_{1,d} \\
  m_2 = \theta_{2,d} \phi_{2,d} \\
  m_1 + m_2 = 0
\end{cases}$$

$$\rightarrow \qquad 0 = m_1 + m_2 = N_1 \, i_1 + N_2 \, i_2$$

$$\begin{aligned}
  0 & = \phi_2 - \phi_1 - \phi_{2,d} + \phi_{1,d} \\
    & = \phi_2 - \phi_1 - \frac{m_2}{\theta_{2,d}} + \frac{m_1}{\theta_{1,d}} \\
\end{aligned}$$

$$\rightarrow \qquad \frac{\psi_2}{N_2} - \frac{m_2}{\theta_{2,d}} = \frac{\psi_1}{N_1} - \frac{m_1}{\theta_{1,d}} \ .$$

$$\rightarrow \qquad \frac{1}{N_2} \left( v_2 - \frac{N_2^2}{\theta_{2,d}} \dfrac{d i_2}{d t} \right) =
                     \frac{1}{N_1} \left( v_1 - \frac{N_1^2}{\theta_{1,d}} \dfrac{d i_1}{d t} \right)  \ .$$

## Transformer with Stray Fluxes and Reluctance $\theta_{Fe}$ in the Air Gap

$$\begin{cases}
  \phi_{1} - \phi_{1,d} = \phi \\
  \phi_{2} - \phi_{2,d} = \phi \\
  m_{1} = \theta_{1,d} \phi_{1,d} \\
  m_{2} = \theta_{2,d} \phi_{2,d} \\
  m_1 + m_2 = \theta_{Fe} \, \phi
\end{cases}$$

<span style="color:red">**todo** complete and verify the calculations; draw the equivalent circuit</span>

