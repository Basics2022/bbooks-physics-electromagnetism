(classical-electromagnetism:electrical-engineering:newtork-analysis:harmonic)=
# Network analysis of linear circuits - harmonic regime

The harmonic dynamics of a linear circuit can be evaluated in Fourier domain, or using complex numbers to represent harmonic functions,

$$\begin{aligned}
  v(t) & = V_{max} \cos (\Omega t + \varphi_v) = \text{re} \{ V_{max} e^{i (\Omega t + \varphi_v)} \} = \\
       & = \sqrt{2} V \cos (\Omega t + \varphi_v) = \sqrt{2} \, \text{re} \{ V e^{i (\Omega t + \varphi_v)} \} = \sqrt{2} \, \text{re} \{ v e^{i \Omega t} \} \\
  i(t) & = I_{max} \cos (\Omega t + \varphi_i) = \text{re} \{ I_{max} e^{j (\Omega t + \varphi_i)} \} = \\
       & = \sqrt{2} I \cos (\Omega t + \varphi_i) = \sqrt{2} \, \text{re} \{ I e^{j (\Omega t + \varphi_i)} \} = \sqrt{2} \, \text{re} \{ i e^{j \Omega t} \} \\
\end{aligned}$$

having anticipated the definition {prf:ref}`harmonic:effective-values` of effective tension $V$ and current $I$.

(classical-electromagnetism:electrical-engineering:newtork-analysis:harmonic:power)=
## Power
**Instantaneous power.**

$$\begin{aligned}
  P(t) 
  & = v(t) i(t) = \\
  & = V_{max} I_{max}  \cos (\Omega t )  \cos (\Omega t - \varphi_i) = \\ 
  & = \frac{1}{2} V_{max} I_{max} \left[ \cos \varphi_i +  \cos ( 2 \Omega t ) \right]  \\ 
\end{aligned}$$ (eq:harmonic:power:instantaneous)

having used [Werner's formula](https://basics2022.github.io/bbooks-math-miscellanea-hs/ch/trigonometry.html#werner),

$$\cos x \cos y = \frac{1}{2} \left[ \cos(x-y) + \cos(x+y) \right] \ .$$

and the property $\cos(-x) = \cos x$.

**Average power on a period.** Over a period $T = \frac{1}{f} = \frac{2 \pi}{\Omega}$

$$\overline{P} = \frac{1}{T} \int_{t=t_0}^{t_0+T} P(t) \, dt = \frac{V_{max} I_{max}}{2} = V I\ ,$$

as the integral of the harmonic term with period $\frac{T}{2}$ of the instantaneous power {eq}`eq:harmonic:power:instantaneous` is identically zero, and with the definition of the **effective voltage and current**

```{prf:definition} Effective voltage and current in AC
:label: harmonic:effective-values

Effective voltage and currents

$$V := \frac{V_{max}}{\sqrt{2}} \quad , \quad I := \frac{I_{max}}{\sqrt{2}} \ , $$

are defined as those voltage and current in DC providing the same value of average power.

```

**Complex power.** Complex power of a dipole with impedence $Z$, $v =  Z i$

$$\begin{aligned}
  S 
  & := v i^* = |v|e^{j \varphi_v} |i| e^{-j \varphi_i} = |v| |i| e^{j(\varphi_v - \varphi_i)} = \\
  & = Z i i^* = Z |i|^2 = (R + j X ) |i|^2 = |Z||i|^2 e^{j \varphi_Z} = P + j Q \ ,
\end{aligned}$$

with the active power $P$ and the reactive power $Q$

$$\begin{aligned}
  P & = \text{re}\{ S \} && = && |S| \cos \varphi_Z && = && \dots \\
  Q & = \text{im}\{ S \} && = && |S| \sin \varphi_Z && = && \dots \\
\end{aligned}$$

<!--
Or with time-varying signal in the complex domain

$$\begin{aligned}
  V(t) & = V e^{i\omega t} \\
  I(t) & = I e^{i\omega t} \\
\end{aligned}$$
-->
