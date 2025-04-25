(classical-electromagnetism:electrical-engineering:three-phase)=
# Three-phase circuits


(classical-electromagnetism:electrical-engineering:three-phase:star-star)=
## Star-star network

```{list-table}
:header-rows: 0

* - ![](../media/star-star.png) 
  - ![](../media/star-star-e1.png) 

```

### General solution

Tension $v_{AB}$ between the centers of the stars $A$, $B$ 

$$v_{AB} = \dfrac{\sum_{g=1}^{3} Y_g e_g}{\sum_{i=1}^{4} Y_i} \ .$$

```{dropdown} Proof.
:open:

PSCE is used on the linear network, leaving only one tension generator on at a time, and then combining the results. 

**Tension generator $e_1$ on, $e_2 = e_3 = 0$ off.** Leaving $e_1$ on, and switching off $e_2 = e_3 = 0$, tension generator sees an equivalent impedance

$$\begin{aligned}
  Z_{eq,1}
  & = Z_1 + (Z_2 \parallel Z_3 \parallel Z_4) \\
  & = \dfrac{1}{Y_1} + \dfrac{1}{Y_2 + Y_3 + Y_4} = \dfrac{Y_{1234}}{Y_1 Y_{234}}  \ ,
\end{aligned}$$

so that:
- the current through the generator reads

   $$i_{1,1} = \dfrac{e_1}{Z_{eq,1}} = \frac{Y_1 Y_{234}}{Y_{1234}} e_1$$

- the currents through the other sides (acting as current dividers are):

   $$\begin{aligned}
      i_{2,1} & = -     \frac{Y_2}{Y_{234}} \, i_{1,1} = -     \frac{Y_1 Y_2}{Y_{1234}} e_1  \\
      i_{3,1} & = -     \frac{Y_3}{Y_{234}} \, i_{1,1} = -     \frac{Y_1 Y_3}{Y_{1234}} e_1  \\
      i_{4,1} & = \ \ \ \frac{Y_4}{Y_{234}} \, i_{1,1} = \ \ \ \frac{Y_1 Y_4}{Y_{1234}} e_1  \\
   \end{aligned}$$

- tension $v_{AB}$

   $$v_{AB,1} = e_1 - Z_1 i_{1,1} = \left( 1 - \frac{Y_{234}}{Y_{1234}} \right) e_1 = \frac{Y_1 e_1}{\sum_{k=1}^4 Y_k} \ . $$

**PSCE.** Exploiting the PSCE and the symmetry of the system, the expressions of currents in the phases, in the neutral and the center-center voltage seamlessly follow

$$\begin{aligned}
  i_1    & = \frac{Y_1 Y_{234}}{Y_{1234}} e_1 - \frac{Y_1 Y_2}{Y_{1234}} e_2 - \frac{Y_1 Y_3}{Y_{1234}} e_3 = \\
         & = Y_1 e_1 - \frac{Y_1}{Y_{1234}} \sum_{g=1}^{3} Y_g \, e_g \\
  i_2    & = Y_2 e_2 - \frac{Y_2}{Y_{1234}} \sum_{g=1}^{3} Y_g \, e_g \\
  i_3    & = Y_3 e_3 - \frac{Y_3}{Y_{1234}} \sum_{g=1}^{3} Y_g \, e_g \\
  i_4    & = \frac{Y_4}{Y_{1234}} \sum_{g=1}^{3} Y_g \, e_g \\
  v_{AB} & =  \frac{\sum_{g=1}^{3} Y_g \, e_g}{\sum_{k=1}^4 Y_k} \\
\end{aligned}$$

```


### Equilibrated generation and loads



### Extra connections

#### Phase-neutral connections
Connections of a phase with the neutral result in parallel impedence with the generators and/or the loads 

```{figure} ../media/star-star-parallel-connections.png

```

#### Phase-phase connections
Phase-phase connections don't influence the voltage $v_{AB}$ between the centers $A$, $B$.

**todo** *Write the proof.*

```{figure} ../media/star-star-extra-connections.png

```
