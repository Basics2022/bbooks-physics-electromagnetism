(classical-electromagnetism:electrical-engineering-exercises:harmonic)=
# Harmonic regime of linear electrical grids

````{exercise} Exam 2025-02-11, Exercise 2.
:label: exam-25-02-11-exe-02

```{figure} ../media/exam-2025-02-11-ese-02.png
```

```{dropdown} Solution

First [one-port equivalent Thevenin circuit](classical-electromagnetism:electrical-engineering:newtork-analysis:thevenin:1-port) of the circuit with port $A-B$ is evaluated, then [power flow in harmonic regime](classical-electromagnetism:electrical-engineering:newtork-analysis:harmonic:power) is discussed.

**Thevenin equivalent: voltage.** With open circuit in $A-B$, current $a$ flows in the lower branch and in impedence $Z_1$. Clockwise loop currents $i_1$ and $i_2$ flows in the left and right loop respectively. Kirchhoff voltage laws in the left and right loops give

$$\begin{aligned}
  0 & = e_1 - Z_L (i_1 + a) - (R_1 + Z_C) i_1 \\
  0 & = -e_2 - Z_2 (i_2 + a) - Z_3 i_2 \\
\end{aligned}
\quad \rightarrow \quad
\begin{aligned}
  i_1 & = \frac{e_1 - Z_L a}{Z_L + Z_C + R_1} \\
  i_2 & = -\frac{e_2 + Z_2 a}{Z_2 + Z_3} \\
\end{aligned}$$

and thus using Kirchhoff voltage law on the loop with nodes $A-B$ and closing through $Z_1$ and $R_1$,

$$V_{Th} = R_1 i_1 + Z_1 a = \dots$$


**Thevenin equivalent: impedence.** Opening circuit at the current generator, and replace tension generators with short circuits, the equivalent impedence is

$$Z_{Th} = ( (Z_C + Z_L) \parallel R_1) + Z_1 \ .$$

**Equivalent circuit.** Kirchhoff voltage law on the equivalent circuit reads

$$0 = V_{Th} - Z_{Th} i - Z_{x} i = 0 \ ,$$

and thus

$$I = \frac{V_{Th}}{Z_{Th} + Z_{x}} = \dots$$

**Power.** Complex power reads

$$S = V I^* = Z_x |I|^2 = \frac{Z_x}{|Z_{Th} + Z_x|^2} |V_{th}|^2 \ ,$$

Writing the impedence as $Z_x = R_x + i X_x$, the active power reads

$$P = \frac{ R_x }{ (R_{Th} + R_x)^2 + (X_{Th} + X_x)^2} |V_{Th}|^2 \ .$$

With the physical constraints $R \ge 0$, the problem is a constrained optimization problem of finding the maximum value of the function $P(R_x, X_x)$ subject to the constraint $R_x \ge 0$,

$$\text{find } \ \max_{R_x, X_x} P(R_x, X_x) \qquad \text{s.t.} \qquad R_x \ge 0 \ .$$

The denominator is the sum of two non negative terms, one function of $R_x$ and one function of $X_x$. The independent variable $X_x$ only appears in this term at the denominator, so that this term must vanish at the solution of the optimization problem, and thus

$$\widetilde{X}_x = - X_{Th} \ .$$

The remaining term is a function of $R_x$ only and proportional to

$$f(R_x) = \frac{R_x}{(R_{Th} + R_x)^2} \ .$$

Local extremes of this function is attained where

$$\begin{aligned}
  0 = f'(R_x) 
  & = \frac{(R_{Th} + R_x)^2 - 2 R_x (R_{Th} + R_x))}{(R_{Th} + R_x)^4} = \\
  & = \frac{R_{Th}^2 - R_x^2 }{(R_{Th} + R_x)^4} \\
\end{aligned}$$

and thus, within the physical limit of the problem, the local and global maximum of the function (check that $f''(\widetilde{R}_x) < 0$), is attained for

$$\begin{aligned}
  \widetilde{R}_{x} & = R_{Th} \\
  \widetilde{Z}_{x} & = R_{Th} - i X_{Th}
\end{aligned}$$

and the maximum active power is

$$P_{max} = P(\widetilde{Z}_x) = \frac{|V_{Th}|^2}{4 R_{Th} } \ .$$

while the reactive power in this condition reads

$$Q = - \frac{ X_{Th} }{4 R^2_{Th}} |V_{Th}|^2 \ .$$

```

````


````{exercise} Exam 2025-02-11, Exercise 3.
:label: exam-25-02-11-exe-03

```{figure} ../media/exam-2025-02-11-ese-03.png
```

```{dropdown} Solution

First [power flow in harmonic regime](classical-electromagnetism:electrical-engineering:newtork-analysis:harmonic:power) is used to calculate load impedence, then the electrical circuit is solved, and the power on the tension generator is computed.

**Load impedence $Z_L$**. Load impedence appears in the load constitutive equation $V_L = Z_L I_L$, and can be evalauted from data about complex power,

$$
   S_L  & = |S_L| e^{i \phi_L} = V_L I_L^* = Z_L |I|^2 = \frac{1}{Z_L^*} |V_L|^2 \\ 
$$

$$Z_L = \frac{|V_L|^2}{|S_L|} e^{i \varphi_L}$$

**Current $I_s$.** From data of load power, it's possible to evaluate the current $I_s$. The current $I_L$ through the load reads

$$S_L = V_L I_L^* \qquad \rightarrow \qquad I_L = \frac{S_L^*}{V_L^*} = \frac{|S_L|}{|V_L|} e^{i(-\phi_L + \phi_V)}$$

The three parallel sides act as current divider so that

$$I_L = \frac{(R_3+Z_L)^{-1}}{(R_3+Z_L)^{-1} + ( (i X_1 ) \parallel (R_2 + i X_2) )^{-1}} I_s$$

and thus

$$I_s = |I_s| e^{i \varphi_{I_s}} = \dots$$

**Equivalent circuit.** The impedence of the circuit powered by the tension generatore is

$$Z_{eq} = R_1 + ( i X_1 \parallel (R_2 + i X_2) \parallel (R_3 + Z_L) ) \ .$$

Given the equivalent impedance, and the current $I_s$ the voltage across the tension generator is

$$E_s = Z_{eq} I_s = |E_s| e^{i \varphi_{E_s}} \dots \ .$$

and the power factor is $\cos \varphi_s = \dots$, where

$$\varphi_s = \varphi_{E_s} - \varphi_{I_s} = \dots \ . $$



```

````


````{exercise} Exam 2025-01-22, Exercise 2.
:label: exam-25-01-22-exe-02

```{figure} ../media/exam-2025-01-22-ese-02.png
```

```{dropdown} Solution

First [one-port equivalent Thevenin circuit](classical-electromagnetism:electrical-engineering:newtork-analysis:thevenin:1-port) of the circuit with port $A-B$ is evaluated, then the equivalent circuit is solved to find the tension $v(t)$ across the current generator, and [power flow in harmonic regime](classical-electromagnetism:electrical-engineering:newtork-analysis:harmonic:power) is discussed.

**Thevenin equivalent: voltage.** With an open circuit, the network can be split into two parts: the triangle in the upper-left side and the section in the right part.

In the triangular part, a current $I_{a}$ flows in counter-clockwise direction, while current $I_b$ flows in the right part in clockwise direction,

$$\begin{aligned}
  I_a & = \frac{E_1}{Z_1 + Z_2} \\
  I_b & = \frac{E_2 + i \Omega L_5 A_2}{Z_4 + Z_5 + Z_3} \\
\end{aligned}$$

as 

$$E_2 + \bigg( Z_4 + Z_3 \underbrace{- i \frac{1}{\Omega C_5} + i \Omega L_5}_{=Z_5} \bigg) I_b + i \Omega L_5 A_2 = 0 \ . $$

with $Z_k$ being the impedence of the $k$-th side. Thevenin voltage thus reads

$$\begin{aligned}
  V_{Th} & = E_2 - Z_3 I_b + Z_2 I_a \\ 
\end{aligned}$$

**Thevenin equivalent: impedence.** Equivalent impedence reads

$$Z_{Th} = (Z_1 \parallel Z_2 + ( Z_3 \parallel (Z_4 + Z_5)))$$

**Equivalent circuit.** Prescribed current $A_1$ flows in the equivalent circuit, and the voltage across the current generator is evaluated with Krichhoff voltage law

$$V_{A_1} - V_{Th} - Z_{Th} A_1 = 0 \ ,$$

$$V_{A_1} = V_{Th} + Z_{Th} A_1 = |V_A| e^{i \varphi_{V_{A_1}}} \ .$$

Signal in time is reconstructed using using the relation between effective and maximum amplitude of the oscillation and evaluating the real part of the signal $|V_{A_1}| e^{i(\Omega t + \varphi_{V_{A_1}})}$

$$v_{A_1}(t) = \sqrt{2} |V_{A_1}| \cos(\Omega t + \varphi_{V_{A_1}}) \ .$$

**Poer.** Using definitions of [power in circuits in harmonic regime](classical-electromagnetism:electrical-engineering:newtork-analysis:harmonic:power),

$$\begin{aligned}
   S_{A_1}  & = V_{A_1} I_{A_1}^* \\
  |S_{A_1}| & = |V_{A_1}| |I_{A_1}| \\
   P_{A_1}  & = \text{re} \{ S_{A_1} \} \\
   Q_{A_1}  & = \text{im} \{ S_{A_1} \} \\
\end{aligned}$$


```

````


````{exercise} Exam 2024-09-06, Exercise 2.
:label: exam-24-09-06-exe-02

```{figure} ../media/exam-2024-09-06-ese-02.png
```

```{dropdown} Solution - todo
:open:



```

````

````{exercise} Exam 2024-07-22, Exercise 2.
:label: exam-24-07-22-exe-02

```{figure} ../media/exam-2024-07-22-ese-02.png
```

```{dropdown} Solution - todo
:open:



```

````

