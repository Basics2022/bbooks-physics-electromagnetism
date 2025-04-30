(physics-hs:electromagnetism:circuits-electric:components:configurations)=
# Elementary circuits

(physics-hs:electromagnetism:circuits-electric:components:configurations:series-parallel)=
## Series and Parallel Connections

**Series Connection.** A series connection of linear passive components of the same type involves the same current passing through each component, $i_n = i, \forall n=1:N$, and the total voltage difference between the "input terminal" of the first element and the "output terminal" of the last element being the sum of the voltage differences, $v = \sum_{n=1:N} v_n$. Therefore:
- For resistors in series, $R_n$, the equivalent resistance is equal to the sum of the resistances:

   $$v = \sum_n v_n = \sum_n \left( R_n \, i_n \right) = \left( \sum_n R_n \right) i = R_{series} \, i \qquad \rightarrow \qquad R_{series} = \sum_n R_n$$

- For capacitors in series, $C_n$, the inverse of the equivalent capacitance is equal to the sum of the inverses of the capacitances:

   $$\dfrac{d v}{dt} = \sum_n \dfrac{d v_n}{dt} = \sum_n \left( \frac{1}{C_n} \, i_n \right) = \left( \sum_n \frac{1}{C_n} \right) i = \dfrac{1}{C_{series}} \, i \qquad \rightarrow \qquad \frac{1}{C_{series}} = \sum_n \frac{1}{C_n}$$

- For inductors in series, $L_n$, the equivalent inductance is equal to the sum of the inductances:

   $$v = \sum_n v_n = \sum_n \left( L_n \, \dfrac{d i_n}{d t} \right) = \left( \sum_n L_n \right) \dfrac{d i}{dt} = L_{series} \, \dfrac{d i}{dt} \qquad \rightarrow \qquad L_{series} = \sum_n L_n$$

Consequently, the resistance and inductance of series-connected resistors and inductors are greater than the maximum resistance/inductance in the system; the equivalent capacitance of series-connected capacitors is less than the minimum capacitance of the capacitors in the system.

**Parallel Connection.** A parallel connection of linear passive components of the same type involves the same voltage difference across the terminals of each component, $v_n = i, \forall n=1:N$, and the current through each component being generally different, with the sum of the currents equal to the current at the two extreme nodes of the connection, $\sum_{n=1:N} i_n = i$. Therefore:
- For resistors in parallel, $R_n$, the inverse of the equivalent resistance is equal to the sum of the inverses of the resistances:

   $$i = \sum_n i_n = \sum_n \left( \frac{1}{R_n} \, i_n \right) = \left( \sum_n \frac{1}{R_n} \right) i = \frac{1}{R_{\parallel}} \, i \qquad \rightarrow \qquad \frac{1}{R_{\parallel}} = \sum_n \frac{1}{R_n}$$

- For capacitors in parallel, $C_n$, the equivalent capacitance is equal to the sum of the capacitances:

   $$i = \sum_n i_n = \sum_n \left( C_n \, \dfrac{d v_n}{d t} \right) = \left( \sum_n C_n \right) \dfrac{d v}{dt} = C_{\parallel} \, \dfrac{d v}{dt} \qquad \rightarrow \qquad C_{\parallel} = \sum_n C_n$$

- For inductors in parallel, $L_n$, the inverse of the equivalent inductance is equal to the sum of the inverses of the inductances:

   $$\dfrac{d i}{dt} = \sum_n \dfrac{d i_n}{dt} = \sum_n \left( \frac{1}{L_n} \, v_n \right) = \left( \sum_n \frac{1}{L_n} \right) v = \dfrac{1}{L_{\parallel}} \, v \qquad \rightarrow \qquad \frac{1}{L_{\parallel}} = \sum_n \frac{1}{L_n}$$

Consequently, the resistance and inductance of parallel-connected resistors and inductors are less than the minimum resistance/inductance in the system; the equivalent capacitance of parallel-connected capacitors is greater than the maximum capacitance of the capacitors in the system.

(physics-hs:electromagnetism:circuits-electric:circuits)=
## Special Cases

(physics-hs:electromagnetism:circuits-electric:circuits:open)=
### Open Circuit
A circuit is open in the absence of a physical closure (with a wire) of a loop or behaves as such in the presence of a side through which the passage of electric current is impeded:

$$i = 0 \ .$$

(physics-hs:electromagnetism:circuits-electric:circuits:short)=
### Short Circuit
A short circuit occurs through a component with zero voltage drop:

$$v = 0 \ .$$

If a short circuit occurs in an entire loop, it is traversed by infinite current—in a linear model that does not consider the limits of validity; in reality, non-linear effects occur much earlier, or sparks, explosions, or other destructive effects—often characterized by zero resistance. **todo** *check the generality of this condition*


