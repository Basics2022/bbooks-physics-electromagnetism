(classical-electromagnetism:electrical-engineering:newtork-analysis)=
# Network analysis of linear circuits

Dynamical equations of a linear circuit can be written as a general linear state-space model

$$\begin{cases}
  \mathbf{M} \dot{\mathbf{x}} = \mathbf{A} \mathbf{x} + \mathbf{B} \mathbf{u} \\
  \mathbf{y} = \mathbf{C} \mathbf{x} + \mathbf{D} \mathbf{u} \\
\end{cases}$$

The mathematical problem is a system of DAE (dynamical-algebraic equations), as it includes:
- constitutive equations of the linear components
- Kirchhoff laws for current at nodes and voltage in loops

Thus matrix $\mathbf{M}$ is likely to be singular, here vector $\mathbf{x}$ contains both dynamical (like voltage across a capacitor or current through an inductor) and algebraic grid variables, current and voltages whose time derivative doesn't appear explicitly in the system of DAE.

**Different representations.** Possible choices of the unknowns:
1. current through any side, voltage at any node
2. loop currents, voltage drops across any side.
3. ... *any other (linear) combination on the physical quantities*

(classical-electromagnetism:electrical-engineering:newtork-analysis:thevenin)=
## Thevenin equivalent

**One-port.** Thevenin's theorem states that any linear circuit can be reduced to a single voltage source and a single impedance in series.

(classical-electromagnetism:electrical-engineering:newtork-analysis:thevenin:1-port)=
### One-port circuit

As the goal of Thevenin's theorem is to find the constitutive equation of the network as $v(i)$, the network is connected to an external current generator that prescribes $i$ and the voltage $v$ at the port is evaluated.

The input of the extended network is 

$$\mathbf{u} = ( \mathbf{u}_{gen}, i ) \ ,$$

while the output is, or at least contains, the voltage $v$

$$\mathbf{y} = \mathbf{C} \mathbf{x} + \mathbf{D} \mathbf{u} \ .$$

The linear system can be written in Laplace domain as 

$$\begin{cases}
  s \mathbf{M} \mathbf{x} - \mathbf{M} \mathbf{x}_0  = \mathbf{A} \mathbf{x} + \mathbf{B} \mathbf{u} \\
  \mathbf{y} = \mathbf{C} \mathbf{x} + \mathbf{D} \mathbf{u} \\
\end{cases}$$

The state and the output are the sum of the free response to non-zero initial conditions and forced response,

$$\begin{cases}
  \mathbf{x} = (s \mathbf{M} - \mathbf{A})^{-1} \mathbf{M} \mathbf{x}_0 + (s \mathbf{M} - \mathbf{A})^{-1} \mathbf{B} \mathbf{u} \\
  \mathbf{y} = \mathbf{C} (s \mathbf{M} - \mathbf{A})^{-1} \mathbf{M} \mathbf{x}_0 + \left[ \mathbf{C} (s \mathbf{M} - \mathbf{A})^{-1} \mathbf{B} + \mathbf{D} \right] \mathbf{u} \\
\end{cases}$$

Forced response can be further manipulated exploiting PSCE, evaluating the effect of one input at a time, setting all the other inputs equal to zero.
- the effect of setting the input of the external current generator, $i = 0$, is equivalent to evaluate the system with an open circuit at the port
- the effect of setting equal to zero a tension generator, $e = 0$, is equivalent to a short-circuit on the same side
- the effect of setting equal to zero a current generator, $a = 0$, is equivalent to an open circuit on the same side

If the system is **asymptotically stable**, the free response is approximately zero when the **transient dynamics is over**, and the output equals the forced output. Introducing the transfer function 

 $$\mathbf{G}(s) = [ \ \mathbf{G}_{gen}(s) \quad \mathbf{G}_i(s) \ ] \ ,$$

 the input-output relation reads

$$\begin{aligned}
   v = \mathbf{G}(s) \mathbf{u}
   & = \mathbf{G}_{gen}(s) \mathbf{u}_{gen} + G_i(s) \, i = \\
   & = v_{Th}(s) - Z_{Th}(s) i(s) \ ,
\end{aligned}$$

having recast it as Thevenin's theorem defining the voltage $v_{Th}$ and the impedance $Z_{Th}$ of the equivalent circuit,

 $$\begin{aligned}
   v_{Th} & := \mathbf{G}_{gen}(s) \mathbf{u}_{gen}(s) \\
   Z_{Th}(s) & := - G_i(s)
\end{aligned}$$


(classical-electromagnetism:electrical-engineering:newtork-analysis:thevenin:n-port)=
### Many-port circuit

$$\mathbf{v} = \mathbf{G}_{gen}(s) \mathbf{u}_{gen} + \mathbf{G}_i(s) \mathbf{i} = \mathbf{v}_{Th} - \mathbf{Z}_{Th} \mathbf{i} \ .$$


(classical-electromagnetism:electrical-engineering:newtork-analysis:norton)=
## Norton equivalent

