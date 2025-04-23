(classical-electromagnetism:electrical-engineering:newtork-analysis:harmonic)=
# Network analysis of linear circuits - harmonic regime

The harmonic dynamics of a linear circuit can be evaluated in Fourier domain, or using complex numbers to represent harmonic functions. Using voltage signal as a reference for time phase,

$$\begin{aligned}
  v(t) & = V_{max} \cos (\Omega t) = \text{re} \{ V_{max} e^{i \Omega t} \} \\
  i(t) & = I_{max} \cos (\Omega t - \varphi_i) = \text{re} \{ I_{max} e^{i ( \Omega t + \varphi_i )} \} \\
\end{aligned}$$

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

as the integral of the harmonic term with period $\frac{T}{2}$ of the instantaneous power {eq}`eq:harmonic:power:instantaneous` is identically zero, and with the definition of the **effective voltage and current**,

$$V := \frac{V_{max}}{\sqrt{2}} \quad , \quad I := \frac{I_{max}}{\sqrt{2}} \ . $$

**Complex power.** Complex power of a dipole with impedence $Z$, $V =  Z I$

$$\begin{aligned}
  S 
  & := V I^* = |V|e^{i \varphi_V} |I| e^{-i \varphi_I} = |V| |I| e^{i(\varphi_V - \varphi_I)} = \\
  & = Z I I^* = Z |I|^2 = (R + i X ) |I|^2 = |Z||I|^2 e^{i \varphi_Z} = P + i Q \ ,
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
