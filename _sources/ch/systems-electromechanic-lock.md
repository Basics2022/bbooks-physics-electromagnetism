(classical-electromagnetism:systems-electromechanic:examples:lock)=
# Electromechanic lock

## C-shaped magnetic circuit

Mechanical sub-system

$$m \ddot{x} + c \dot{x} + k x = F^{ext} + F^{em}$$

Electromagnetic sub-system, with no dispersed flux and non-negligible reactance of the ferromagnetic medium

$$\begin{aligned}
  e   & = R i + v_L \\
  v_L & = \dfrac{d \psi}{dt} = \dfrac{d \left( N \phi \right)}{d t} \\
  N i = m & = \left( \theta_{Fe} + 2 \theta_0(x) \right) \phi = \\
          & = \left( \theta_{Fe} + 2 \dfrac{x}{\mu_0 A} \right) \phi \ .
\end{aligned}$$

Assuming no dispersed flux and conservative conversion of electromagnetic power to mechanical power, the expression of the force $F^{em}$ acting on the mechanical system due to electromagnetic phenomena is derived from energy balance equation,

$$\begin{aligned}
  0 
  & = \dot{x} \left( m \ddot{x} + c \dot{x} + k x - F^{ext} - F^{em} \right) + i \left( R i - e + \dfrac{d}{dt} \left( \dfrac{N^2}{\theta(x)} \, i \right) \right) \\
  & = \dot{x} \left( m \ddot{x} + c \dot{x} + k x - F^{ext} - F^{em} \right) + i \left( R i - e + \dfrac{d}{dt} \left( L(x) \, i \right) \right) \\
  & = \dfrac{d}{dt} \left( \dfrac{1}{2} m \dot{x}^2 + \dfrac{1}{2} k x^2 + \dfrac{1}{2} L i^2 \right) + c \dot{x}^2 + R i^2 - \dot{x} F^{ext} - e i - \dot{x} \left( F^{em} - \partial_x \left( \dfrac{1}{2} L i^2 \right) \right)
\end{aligned}$$

$$\begin{aligned}
  F^{em} = \dfrac{1}{2} \partial_x L i^2
  & = - \dfrac{1}{2} \dfrac{N^2}{\theta^2(x)} \theta'(x) i^2 = \\
  & = - \dfrac{1}{2} \dfrac{N^2 i^2}{\theta^2(x)} \dfrac{2}{\mu_0 A} = \\
  & = - \dfrac{1}{2} \dfrac{N^2 i^2}{\left( \theta_{Fe} + \frac{2 x}{\mu_0 A} \right)^2} \dfrac{2}{\mu_0 A} = \\
  & = - 2 \dfrac{1}{2 \mu_0 A} \phi^2(x,i) \ ,
\end{aligned}$$

so that the force produce by each of the two gaps is

$$F^{em}_{gap} = -\dfrac{\phi^2(x,i)}{2 \mu_0 A} \ .$$

**todo**
- Find general expression of the force at each gap. Is it possible to find such an expression?
- Example: electromagnetic lock
