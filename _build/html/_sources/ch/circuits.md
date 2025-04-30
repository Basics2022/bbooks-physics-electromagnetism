(classical-electromagnetism:electrical-engineering)=
# Circuit Approximation

Circuit approximation of electromagnetic systems is a good approximation of electromagnetic phenomena in **slow regime** of systems of **moderate dimension**, allowing to reduce the complexity of the problem: while the electromagnetism is a "field" physical phenomenon governed by system of PDEs, circuit approximation allows to build models governed by ODEs for non-stationary problems, and algebraic equations for stationary problems.

Under the assumptions of circuit approximation, components of the electromagnetic field don't radiate EM energy through waves, but involve electromagnetic field confined in space, and interface with other components typically through electric ports made of conductor wires - or with actions on mechanical elements for electro-mechanical systems.

[**Energy balance**](classical-electromagnetism:circuits:energy). Under the assumptions of circuit approximation, discussed later, electromagnetic energy balance equation {eq}`eq:energy:integral:2` for electomagnetic systems may reduce to

 $$\dfrac{d U}{dt} + \sum_{k \in \text{Resistors}} R_k i_k^2 = \sum_{j \in \text{Wires}} v_j i_j \ ,$$

where resistors produce power dissipation, $\dot{D} \ge 0$, and the electromagnetic energy $U$ is the sum of the contributions stored in conservative elements like capacitors and inductors,

$$U = \sum_{i \in \text{Capacitors}} \frac{1}{2} C_i v_i^2 + \sum_{j \in \text{Inductors}} \dfrac{1}{2} L_j i_j^2 \ ,$$

or, defining $P^{vi, ext}$ the power exchanged with the external environment through the ports,

$$\dot{U} = P^{vi, ext} - \dot{D} \ .$$

[**Electric circuits**](classical-electromagnetism:circuits-electric). Elementary components of electric circuits are discussed and their constitutive equations relating the current through the component and the voltage difference at their ports are derived from the equations of electromagnetism. First, circuits with no unsteady flux of the magnetic field are discussed, along with Kirchhoff's laws; then time-varying magnetic flux in a confined regions of the domain and electromagnetic induction in electric circuits is discussed.

[**Electromagnetic circuits**](classical-electromagnetism:circuits-electromagnetic). Circuit approximation of electromagnetic circuit is discussed for systems working in slow regimes, where the contribution of the displacement current density is negligible, $\partial_t \vec{d} = 0$. Kirchhoff law's for magnetic circuits are stated in terms of magnetic flux, magnetomotive force and reluctance, under the (**strong?** no hysteresis) assumption of linear and non dispersive constitutive law, $\vec{b} = \mu \vec{h}$. Electromagnetic models of transformers are discussed. 

[**Electromechanical systems**](classical-electromagnetism:circuits-electromechanic). Electromagnetic and mechanical phenomena interact in electromechanical systems. These systems usually convert electrical inputsto create mechanical power (e.g. electric motors), or viceversa convert mechanical power into electromagnetic energy or power (e.g. electric generators).

[**Network analysis**](classical-electromagnetism:electrical-engineering:newtork-analysis). Classical methods in the analyses are discussed. This section contains [**exercises with solution**](classical-electromagnetism:electrical-engineering-exercises) taken from exams at Politecnico di Milano.

<!--
**Electric Circuits**

- **Validity Conditions for Circuit Approximation:**
  - The dimensions of the circuit are much smaller than the wavelength of the electromagnetic waves involved.
  - The frequency of the signals is low enough that the propagation delay is negligible.
  - The electric and magnetic fields are confined within the circuit components.

- **Basic Components:** resistors (R); capacitors (C); inductors (L); voltage and current sources; switches; non-linear components: diodes, transistors,...

- **Operating Regimes:**
  - **Steady State (DC):** The circuit parameters (voltage, current) do not change over time.
  - **Harmonic (AC):** The circuit parameters vary sinusoidally with time.
  - **Transient:** The circuit parameters change over time, typically due to a change in input or initial conditions.

**Electromagnetic Circuits**

- **Validity Conditions for Circuit Approximation:**
  - term $\partial_t \vec{d}$ negligible,...**todo** *as an integral condition on a system? Discussion in terms of energy?*

- **Example: Transformers**
  - Transformers operate on the principle of electromagnetic induction.
  - They are used to step up or step down voltages and currents in AC circuits.
  - The circuit approximation is valid as long as the frequency of the AC signal is within the designed range of the transformer.

**Electro-Magneto-Mechanical Circuits**

- **Examples:**
  - **Simple Circuits:** Basic circuits involving electromagnetic and mechanical components, such as a moving coil in a magnetic field.
  - **Electric Motors:** Convert electrical energy into mechanical energy.
  - **Generators:** Convert mechanical energy into electrical energy.

- **Key Concepts:**
  - Interaction between electrical and mechanical components.
  - Energy conversion and efficiency.
  - Dynamic behavior and control of electromechanical systems.
-->
