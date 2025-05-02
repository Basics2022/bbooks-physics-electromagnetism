(classical-electromagnetism:systems-electromechanic:examples:dc-motor)=
# DC motors

Electric subsystem in potential regions

$$e = R i + v$$

Electromagnetic induction

$$v_L = -\int_{\ell} \vec{e} \cdot \hat{t} = - \oint_{\partial S} \vec{e} \cdot \hat{t} = \dfrac{d}{dt}\int_{S} \vec{b} \cdot \hat{n} $$

Mechanical sub-system

$$I \ddot{\alpha} = C^{em} + C^{load} \ ,$$

with $C^{em} = F b \cos \alpha$, and $F = i_L B a$.

**No commutation, neglecting the self-induction**. With no commutation, $i = i_L$, $v = v_L$ and thus the magnetic flux reads

$$\int_{S} \vec{b} \cdot \hat{n} = - B a b \sin \alpha = - B A \sin \alpha \ ,$$

so that its time derivative and the voltage different at the port reads

$$v_L = \dot{\alpha} B A \cos \alpha \ .$$

Current in the circuit reads

$$i = \dfrac{1}{R} \left( e - v \right) = \dfrac{1}{R} \left( e - \dot{\alpha} B A \cos \alpha \right) \ ,$$

electromagnetic torque

$$C^{em} = i_L B A \cos \alpha =  \dfrac{BA}{R} \cos \alpha \left( e - \dot{\alpha} B A \cos \alpha \right)$$

**With commutation.** $i_L = i \cdot \text{sign} \{ \cos \alpha \}$, $v = v_L \cdot \text{sign} \{ \cos \alpha \}$

$$\begin{aligned}
  C^{em} = i_L B A \cos \alpha
  & =  \text{sign} \{ \alpha \} \cdot \dfrac{BA}{R} \cos \alpha \left( e - \dot{\alpha} B A \cos \alpha \cdot \text{sign} \{ \alpha \} \right) = \\
  & = \dfrac{BA}{R} \left| \cos \alpha \right| \, e - \cos^2 \alpha  \dfrac{(BA)^2}{R} \, \dot{\alpha} \ .
\end{aligned}$$

**Multiple windings.** With $N$ windings equally spaced $\Delta \theta = \frac{\pi}{N}$, $\alpha_n = \alpha + \frac{n}{N} \pi$, are connected in series, quantities in the DC motor become so regular that can be approximated with their **average value** on a turn of the motor,

$$v = \dot{\alpha} B A \sum_{n} |\cos  \alpha_n| \simeq \dot{\alpha} \frac{2 N BA}{\pi}$$

$$i_L = i = \frac{1}{R}\left( e - \dfrac{2 N BA}{\pi} \dot{\alpha} \right) $$

$$\begin{aligned}
  C^{em} = i_L B A \sum_k \left| \cos \alpha_k \right|
  & \simeq \dfrac{2 N}{\pi} BA \dfrac{1}{R}  \left( e - \dfrac{2N}{\pi} BA \dot{\alpha} \right) = \\
  & =      \dfrac{1}{R} \dfrac{2 N BA}{\pi} e - \dfrac{1}{R} \left(\dfrac{2N BA}{\pi} \right)^2 \dot{\alpha} \ .
\end{aligned}$$
<!-- \dfrac{2 N}{\pi} \frac{BA}{R} e - \dfrac{N}{2} \dfrac{(BA)^2}{R} \dot{\alpha}$$ -->

The dynamical system of a brushed DC motor then are

$$\begin{aligned}
  I \ddot{\alpha} & = C^{load} + C^{em} \\ 
               e  & = R i + v
\end{aligned}$$

*Energy balance.* Multiplying the mechanical equation by $\dot{\alpha}$ and circuit equation by $i$,

$$\begin{aligned}
  0 
  & = \dot{\alpha} \left( I \ddot{\alpha} - C^{load} - C^{em} \right) - i \left( e - R i - v \right) = \\
  & = \dot{\alpha} \left( I \ddot{\alpha} - C^{load} - i \dfrac{2 N BA}{\pi}  \right) - i \left( e - R i - \dfrac{2 N B A}{\pi} \dot{\alpha} \right) = \\
  & = \dfrac{d}{dt} \left( \dfrac{1}{2} I \dot{\alpha}^2 \right) - C^{load} \dot{\alpha} + e i - R i^2 
\end{aligned}$$

energy balance equation can be written as

$$
  \dfrac{d}{dt} \left( \dfrac{1}{2} I \dot{\alpha}^2 \right) - R i^2 =  C^{load} \dot{\alpha} + e i \ ,
$$

where power of external actions on the system and the internal dissipation $R i^2$ equals the time derivative of the kinetic energy. Here the conversion of electromagnetic power to mechanical power is conservative, except for the dissipation loss in resistors.

**todo**
- better on average and different connections
- add pictures
- more on energy balance
- add self-inductance, being

   $$\begin{aligned}
     v_L = \dfrac{d \psi}{d t}
     & = \dfrac{d}{d t}\left( \widetilde{N} \phi \right) = \\
     & = \dfrac{d}{d t} \left( \widetilde{N} \left( B A \sin \alpha + \phi_d \right) \right) = \\
     & = \dfrac{d}{d t} \left( B A \widetilde{N} \sin \alpha \right) + \dfrac{d}{dt} \left( L i \right)  = \\
     & = \dot{\alpha} \, B A \widetilde{N} \cos \alpha + \dfrac{d}{dt} \left( L i \right) \ .
   \end{aligned}$$

   being $\phi_d = \dfrac{\widetilde{N} i}{\theta}$ the dispersed flux producing self-induction, and $L = \dfrac{\widetilde{N}^2}{\theta}$ the self-inductance. KVL equation on the electric circuit gives

   $$e = R i + v = R i + L \dfrac{d}{dt} (i ) + K \dot{\alpha} \ ,$$

   having introduced average quantities for multiple windings. **todo** define $\widetilde{N}$ for multiple windings

