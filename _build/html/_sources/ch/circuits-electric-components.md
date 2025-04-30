<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:circuits-electric:approx)=
# Circuit Approximation

Electrical engineering primarily deals with systems involving intense currents but low frequencies. In this operating regime, the Maxwell equations governing electromagnetic phenomena can be simplified:
1. In regions outside the walls of any capacitors present in the system, the time derivative of the displacement field flux is negligible.
2. The magnetic field $\vec{b}$ and its time derivative are relevant only in certain regions of space and are thus confined to components with inductances, such as electric motors.

Outside these regions, the Maxwell equations {eq}`eq:principles:maxwell` reduce to the steady-state equations:

$$\begin{cases}
  \Phi_{\partial V}(\vec{d}) = Q_f \\
  \Gamma_{\partial S}(\vec{e}) + \dot{\Phi}_S(\vec{b}) = 0 \\
  \Phi_{\partial V}(\vec{b}) = 0 \\
  \Gamma_{\partial S}(\vec{h}) - \dot{\Phi}_S(\vec{d}) = \Phi_S(\vec{j}_f)
\end{cases}
\qquad \rightarrow \qquad
\begin{cases}
  \Phi_{\partial V}(\vec{d}) = Q_f \\
  \Gamma_{\partial S}(\vec{e}) = 0 \\
  \Phi_{\partial V}(\vec{b}) = 0 \\
  \Gamma_{\partial S}(\vec{h}) = \Phi_S(\vec{j}_f)
\end{cases}$$ (eq:principles:maxwell:el-circuit)

At low frequencies,
- Electric components can be analyzed **"for their external effects"**: each component has its characteristic behavior determined by its nature and described by its constitutive equation, but it interfaces with the outside world only through the **electrical port terminals**, which in most cases are the electrical wires with which the component can be connected to other components in a circuit.
- The transmission of the electromagnetic field as electromagnetic waves can be neglected, and the power radiated through these waves is also negligible. The energy balance of the components of an electrical system can be reduced to the power transmitted through the electrical port terminals, which takes the form $P = \sum_{k \in \text{Ports}} v_k i_k$, as shown by [Energy balance in circuit approximation](classical-electromagnetism:circuits:energy)

  $$\dfrac{d E}{dt} = v i$$ (eq:el-circuit:power)

- Since electromagnetic waves are not transmitted, the low-frequency electromagnetic problem is greatly simplified compared to the general electromagnetic problem: while the general electromagnetic problem requires solving the electromagnetic field in all regions of space, the circuit approach allows—when applicable—considering only the electromagnetic components connected through conductors that replace the system.[^circuit-math:pde-ode]

[^circuit-math:pde-ode]: From a mathematical point of view, the general electromagnetic problem is governed by partial differential equations (PDEs), which are beyond the capabilities of a high school student. The circuit approach allows formulating the electromagnetic problem in terms of ordinary differential equations in the non-steady-state case and algebraic equations in the steady-state (or periodic) case, following appropriate transformations: not the simplest problem possible, but a problem that high school students can still tackle.

(physics-hs:electromagnetism:circuits-electric:electric-cable)=
## Electrical Wires
Within the circuit approximation, electrical wires with a small cross-section relative to the circuit dimensions can be treated as 1-dimensional elements, curves with geometric (mean line, cross-section) and physical (resistivity) properties.

The small cross-section allows neglecting the three-dimensional nature of the general problem and assuming that quantities are uniform across each section—or not very different from their average value: the average *drift* velocity $\vec{v}$ of the charges and thus the [current density](electric-current-density:def), $\vec{j} = \rho \vec{v}$, has the same direction as the local axis of the conductor.

The current can therefore be expressed as

$$i = \vec{j} \cdot \hat{n} A \simeq j A \ ,$$ (eq:cable:current-current-density)

where $\hat{n}$ denotes the normal to the cross-section, $A$ is the area of the wire's cross-section, and only the scalar value of the physical quantities needs to be considered if the cross-section is perpendicular to the wire's axis.

**todo** *add image*

(physics-hs:electromagnetism:circuits-electric:kirchhoff-laws)=
## Kirchhoff's Laws

Kirchhoff's laws transform the appropriately simplified governing equations of the electromagnetic problem within the low-frequency regime into the two fundamental laws of circuits.

**Node Law.** The sum of the currents entering a node in an electrical circuit is zero. This law is a consequence of the charge balance law {eq}`eq:principles:charge` for a system with zero volume—or a system that cannot accumulate charge, $\dot{Q}_V$, such as a wire in an electrical circuit operating at low frequency.

$$0 = \Phi_{\partial V}(\vec{j}) = \sum_{k} \vec{j}_k \cdot \hat{n}_k \, A_k = \sum_{k} i_k \ ,$$

where the sum is performed over all conductors $k$ connected to the node under consideration.

**Loop Law.** The sum of the voltages around a loop in an electrical circuit is zero in regions where the time derivative of the magnetic field flux is negligible—for example, outside electric motors and transformers. This law is a consequence of Faraday's law when the time derivative of the magnetic field flux is zero, allowing the electric field to be written in terms of the electric potential.

$$0 = \Gamma_{\partial S}(\vec{e}) = \sum_{k} \Delta v_k \ ,$$

where the sum is performed over all sides $k$ of the circuit loop under consideration.

(classical-electromagnetism:circuits-electric:components)=
## Components

This section presents the main components that can constitute a circuit. The following section analyzes some possible connections of these components and some elementary circuits.
The components are characterized by their constitutive law—determined by their nature and internal structure—which completely describes the electrical component "for its external effects," i.e., at the terminals of its electrical port, in terms of current $i$ and voltage difference across the terminals. For completeness, and to align with common practice, the two **sign conventions** for voltage difference and current are introduced for two classes of components:
- **Generators**, components that produce electrical power.
- **Loads**, components that—typically—absorb electrical power.

**todo** Add images of the two conventions

(physics-hs:electromagnetism:circuits-electric:components:resistor)=
### Electrical Resistance
The constitutive law of [linear electrical resistance](physics-hs:electromagnetism:electric-current:solids:conductor:ohm) is determined by Ohm's law {eq}`ohm:integral:first:R` for linear resistances:

$$v = R i \ ,$$

using the convention for loads.

(physics-hs:electromagnetism:circuits-electric:components:capacitor)=
### Capacitor
The constitutive law of a [capacitor](physics-hs:electromagnetism:electrostatics:capacitor) is:

$$i = C \dfrac{d v}{dt}$$

(physics-hs:electromagnetism:circuits-electric:components:inductor)=
### Inductor
The constitutive law of an inductor is:

$$v = L \dfrac{d i}{dt}$$

(physics-hs:electromagnetism:circuits-electric:components:generator-v)=
### Voltage Generator

$$v = e$$

(physics-hs:electromagnetism:circuits-electric:components:generator-i)=
### Current Generator

$$i = a$$

(physics-hs:electromagnetism:circuits-electric:components:diode)=
### Diode

**todo**
