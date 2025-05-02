(classical-electromagnetism:systems-electromechanic:examples:simple)=
# Electromechanic systems: first examples with induction

In this section first examples of electromechanical systems converting mechanical and electromagnetic power and viceversa exploiting **electromagnetic induction** are discussed. These examples can be interpreted as rudimentary models of motors or generators. Electromagnetic induction is governed by Faraday's law

$$\begin{aligned}
  0 
  & = \oint_{\partial s_t} \vec{e}^* \cdot \hat{t} + \dfrac{d}{dt} \int_{s_t} \vec{b} \cdot \hat{n} = \\
  & = \oint_{\partial s_t} \vec{e}   \cdot \hat{t} +               \int_{s_t} \partial_t \vec{b} \cdot \hat{n}  \ ,
\end{aligned}$$

as derived from integral form of governing equations on arbitrary domain $s_t$ (**todo** *add link*), that can move in space, with the definition of

$$\vec{e}^* = \vec{e} - \vec{b} \times \vec{v}_b \ ,$$

and $\vec{v}_b$ is the velocity of the point of the boundary of the surface $\partial s_t$. As shown in the examples of this section, a time-varying flux of the magnetic field may induce:
- **electromotive force** resulting in
  - voltage difference at the electric port of an open circuit, $v = \dfrac{d \psi(\vec{b})}{d t}$,
  - current in a closed loop, $i = \dfrac{v}{R} = \dfrac{1}{R} \dfrac{d \psi(\vec{b})}{d t}$,

  being the flux $\psi = N A B \cos \alpha$ of uniform magnetic field across a $N$-winding loop of area $A$ in a plane with unit normal vectro forming an angle $\alpha$ with the magnetic field;

- **force** on conductors, either moving conductors or conductors with electric current, governed by the expression of **Lorentz's force**,

   $$\vec{f} = \rho \vec{e} - \vec{j} \times \vec{b}$$
  
   or in integral form (elementary on the length of the conductor only) with no net charge

   $$d \vec{F} = - i \vec{b} \times \hat{t} \, d \ell \ .$$



## Simple loop with moving side in a constant and uniform magnetic field

Mechanical sub-system

$$m \ddot{x} = F^{ext} + F^{em}_x$$

Faraday's law (with Ohm's law $\vec{e}^* = \rho_R \vec{j}^*$, and negligible resistance of the circuit except for the section $l_R$; it's possible to use the equivalent form of Faraday's law, on the second line of the first equation of this section)

$$\begin{aligned}
  0 
  & = \oint_{\partial s_t} \vec{e}^* \cdot \hat{t} + \dfrac{d}{dt} \int_{s_t} \vec{b} \cdot \hat{n} = \\
  & = \int_{l_R} \vec{e}^* \cdot \hat{t} + \dfrac{d}{dt} \left( B a x \right) = \\
  & = R i + B a \dot{x} \ .
\end{aligned}$$

Faraday's experience, or consequence of Lorentz's force

$$F^{em}_x = i B a = - \dfrac{(B a)^2}{R} \dot{x} \ .$$

Inserting into the mechanical sub-system, even without self-inductance, the electromagnetic effects appears as a damping term

$$\begin{aligned}
  m \ddot{x} & = F^{ext} - \dfrac{(B a)^2}{R} \dot{x} \\ 
  m \ddot{x} + \dfrac{(B a)^2}{R} \dot{x} & = F^{ext} \\ 
\end{aligned}$$

**todo** 
- Show force acting on the moving side of the circuit starting from Lorentz's force
  - discuss the motion of a rod in a magnetic field, without connection to a circuit; discuss electric charge distribution
- as $\partial_t \vec{b} = 0$, it's possible to use potential $v$ to define the electromagnetic field $\vec{e} = - \nabla v$


## Rotating loop in a constant and uniform magnetic field

...

$$0 = R i + \dfrac{d}{dt} \left( A B \cos \alpha \right) \ ,$$

...

## Simple loop in a time-varying magnetic field

A time-dependent magnetic flux may induce electric current in an electric circuit...

...

Faraday's law (with Ohm's law $\vec{e}^* = \rho_R \vec{j}^*$, and negligible resistance of the circuit except for the section $l_R$;...)

$$\begin{aligned}
  0 
  & = \oint_{\partial s_t} \vec{e}^* \cdot \hat{t} + \dfrac{d}{dt} \int_{s_t} \vec{b} \cdot \hat{n} = \\
  & = \int_{l_R} \vec{e}^* \cdot \hat{t} + \dfrac{d}{dt} \left( B A \right) = \\
  & = R i + A \dot{B} \ ,
\end{aligned}$$

having here assumed that the area of the circuit is constant, and the circuit is planar in a plane with unit normal vector aligned with $\vec{b} = B(t) \hat{z}$




