```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:circuits-electromagnetic:transformer)=
# Trasformatore

- flusso del campo magnetico, nell'ipotesi di campo uniforme, o in termini del campo medio

  $$\phi = b \, A$$

- flusso del campo magnetico concatenato a $N$ avvolgimenti

  $$\psi = N \, \phi$$

- relazione tra tensione ai morsetti dell'induttore e flusso concatenato, applicando la [legge di Faraday solo in parte irrotazionali](classical-electromagnetism:circuits-electric:induction)

  $$v = \dot{\psi}$$

## Trasformatore ideale

In assenza di flussi dispersi e riluttanza nel traferro, la legge alle maglie nel traferro implica

$$0 = m_1 + m_2 = N_1 \, i_1 + N_2 \, i_2$$

Il flusso del campo magnetico può essere scritto in funzione del flusso concatenato agli avvolgimenti,

$$\phi = \frac{\psi_1}{N_1} = \frac{\psi_2}{N_2}$$

La derivata nel tempo di questa relazione, con numero di avvolgimenti costanti nel tempo, implica

$$\frac{v_2}{N_2} = \frac{v_1}{N_1} \ .$$


## Trasformatore con flussi dispersi

$$\begin{cases}
 & \phi_1 - \phi_{1,d} = \phi \\
 & \phi_2 - \phi_{2,d} = \phi \\
 & m_1 = \theta_{1,d} \phi_{1,d} \\
 & m_2 = \theta_{2,d} \phi_{2,d} \\
 & m_1 + m_2 = 0
\end{cases}$$

$$\rightarrow \qquad 0 = m_1 + m_2 = N_1 \, i_1 + N_2 \, i_2$$

$$\begin{aligned}
  0 & = \phi_2 - \phi_1 - \phi_{2,d} + \phi_{1,d} \\
    & = \phi_2 - \phi_1 - \frac{m_2}{\theta_{2,d}} + \frac{m_1}{\theta_{1,d}} \\
    & = \frac{\psi_2}{N_2} - \frac{\psi_1}{N_1} + m_1 \left( \frac{1}{\theta_{1,d}} + \frac{1}{\theta_{2,d}} \right) \\
\end{aligned}$$

$$\rightarrow \qquad \frac{\psi_2}{N_2} = \frac{\psi_1}{N_1} - \left( \frac{1}{\theta_{1,d}} + \frac{1}{\theta_{2,d}} \right) \, m_1 \ .$$


## Trasformatore con flussi dispersi e riluttanza $\theta_{Fe}$ nel traferro

$$\begin{cases}
 & \phi_{1} - \phi_{1,d} = \phi \\
 & \phi_{2} - \phi_{2,d} = \phi \\
 & m_{1} = \theta_{1,d} \phi_{1,d} \\
 & m_{2} = \theta_{2,d} \phi_{2,d} \\
 & m_1   + m_{2} = \theta_{Fe} \, \phi
\end{cases}$$

<span style="color:red">**todo** finire e controllare i conti; disegnare circuito equivalente</span>

$$\begin{aligned}
  \frac{\psi_{2}}{N_{2}} & = \phi_2 = \\
                     & = \phi + \phi_{2,d} = \\
                     & = \phi + \frac{m_2}{\theta_{2,d}} = \\
                     & = \phi + \frac{1}{\theta_{2,d}} ( \theta_{Fe} \, \phi - m_1 ) = \\
                     & = \left( 1 + \frac{\theta_{Fe}}{\theta_{2,d}} \right) \, \phi - \frac{1}{\theta_{2,d}} m_1 = \\
                     & = \left( 1 + \frac{\theta_{Fe}}{\theta_{2,d}} \right) \, \left( \frac{\psi_1}{N_1} - \frac{m_1}{\theta_{1,d}} \right) - \frac{1}{\theta_{2,d}} m_1 = \\
\end{aligned}$$







