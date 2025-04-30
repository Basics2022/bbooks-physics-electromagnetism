<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:circuits-electric:regimes)=
# Operating Regimes

**Steady, DC**

**Transient dynamics.**

**Periodic, AC**

(physics-hs:electromagnetism:circuits-electric:regimes:dc)=
## Steady-State Regime - Direct Current

The operating regime of a circuit in direct current involves the value of the electric current and the system variables being constant—in real life, "sufficiently constant."

In this operating regime, capacitors behave like [open circuits](physics-hs:electromagnetism:circuits-electric:circuits:open), since $i = C \frac{dv}{dt} = 0$; inductors behave like [short circuits](physics-hs:electromagnetism:circuits-electric:circuits:short), $v = L \frac{d i}{d t} = 0$.

(physics-hs:electromagnetism:circuits-electric:regimes:dt)=
## Transient Regime

Typical transient problems between two steady-state conditions include the dynamics of charging/discharging a capacitor following the closing/opening of a switch.

**RLC Circuit.** **todo**

(physics-hs:electromagnetism:circuits-electric:regimes:ac)=
## Periodic Regime - Alternating Current

The harmonic periodic regime is characteristic of the operation of electromagnetic circuits in alternating current, which is present in many modern electrical networks, from production (through generators) to transformation to high voltage for efficient long-distance transmission, to transformation to medium and then low voltage for distribution and use.

Using the formalism of **phasors** to represent harmonic periodic quantities at a constant frequency $f = \frac{\Omega}{2 \pi}$, one can write:

$$v(t) = V e^{-i \Omega t} \ ,$$

with $V \in \mathbb{C}$. **todo**

**Circuit Analysis.**

**Power Analysis.**

(physics-hs:electromagnetism:circuits-electric:regimes:conversion)=
## AC-DC and DC-AC Conversion

(physics-hs:electromagnetism:circuits-electric:regimes:conversion:rectifier)=
### AC $\rightarrow$ DC, Using Rectifiers

A Graetz bridge with diodes. Oscillations are reduced using capacitors and inductors.

(physics-hs:electromagnetism:circuits-electric:regimes:conversion:inverter)=
### DC $\rightarrow$ AC, Using Inverters


