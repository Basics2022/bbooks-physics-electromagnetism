<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism\:waves\:plane-waves)=
# Plane Electromagnetic Waves

Harmonic decomposition of the electromagnetic field. The EM field can be written as the superposition of plane waves (Fourier decomposition)

$$\begin{aligned}
  \mathbf{e}(\mathbf{r},t) & = \mathbf{E} e^{i(\mathbf{k} \cdot \mathbf{r} - \omega t)} \\
  \mathbf{b}(\mathbf{r},t) & = \mathbf{B} e^{i(\mathbf{k} \cdot \mathbf{r} - \omega t)} \\
\end{aligned}$$

Introducing this decomposition into Maxwell's equations with no free charge and current

$$
\begin{cases}
 \nabla \cdot \mathbf{d} = 0 \\
 \nabla \times \mathbf{e} + \partial_t \mathbf{b} = \mathbf{0} \\
 \nabla \cdot \mathbf{b} = 0 \\
 \nabla \times \mathbf{h} - \partial_t \mathbf{d} = \mathbf{0}
\end{cases}
$$

we obtain

$$
\begin{cases}
 i \mathbf{k} \cdot \mathbf{D} = 0 \\
 i \mathbf{k} \times \mathbf{E} - i \omega \mathbf{B} = \mathbf{0} \\
 i \mathbf{k} \cdot \mathbf{B} = 0 \\
 i \mathbf{k} \times \mathbf{H} + i \omega \mathbf{D} = \mathbf{0}
\end{cases}
\quad \rightarrow \quad
\begin{cases}
 i \varepsilon \mathbf{k} \cdot \mathbf{E} = 0 \\
 i \mathbf{k} \times \mathbf{E} - i \omega \mathbf{B} = \mathbf{0} \\
 i \mathbf{k} \cdot \mathbf{B} = 0 \\
 i \dfrac{1}{\mu} \mathbf{k} \times \mathbf{B} + i \omega \varepsilon \mathbf{E} = \mathbf{0}
\end{cases}
$$

- From Gauss' equations for the electric and the magnetic field

   $$\mathbf{k} \perp \mathbf{E} \quad , \quad \mathbf{k} \perp \mathbf{B}$$

- From Faraday and Ampère-Maxwell equations

   $$\mathbf{B} = \dfrac{\mathbf{k}}{\omega} \times \mathbf{E}$$
   $$\mathbf{E} = - \dfrac{1}{\mu \varepsilon}\dfrac{\mathbf{k}}{\omega} \times \mathbf{B}$$

It follows that:

- $\mathbf{k}$, $\mathbf{E}$, $\mathbf{B}$ are orthogonal "RHS" set of vectors
- Relations between $\mathbf{E}$, $\mathbf{B}$, and $\mathbf{k}$ and the speed of light

    $$\begin{aligned}
      \mathbf{B} & = \dfrac{1}{c} \, \hat{\mathbf{k}} \times \mathbf{E} \\
      \mathbf{E} & = - c \, \hat{\mathbf{k}} \times \mathbf{B} \\
    \end{aligned}$$

    hold, with speed of light $c = \dfrac{1}{\sqrt{\mu \varepsilon}} = \dfrac{\omega}{|\mathbf{k}|}$, and unit vector $\hat{\mathbf{k}} = \dfrac{\mathbf{k}}{|\mathbf{k}|}$.

```{dropdown} Proof using vector algebra identity
Recalling $c^2 = \frac{1}{\mu \varepsilon}$ and

$$\mathbf{B} = \dfrac{\mathbf{k}}{\omega} \times \mathbf{E} = \dfrac{\mathbf{k}}{\omega} \times \left[ - c^2 \dfrac{\mathbf{k}}{\omega} \times \mathbf{B} \right] = - \dfrac{c^2 |\mathbf{k}|^2}{\omega^2} \hat{\mathbf{k}} \times \left( \hat{\mathbf{k}} \times \mathbf{B} \right)$$

Vector identity

$$\mathbf{a} \times (\mathbf{b} \times \mathbf{c}) = \varepsilon_{ijk} a_j \varepsilon_{klm} b_l c_m = \left( \delta_{il} \delta_{jm} - \delta_{im} \delta_{jl} \right) a_j \, b_l \, c_m = b_i a_m c_m - c_i a_m b_m = (\mathbf{a} \cdot \mathbf{c}) \mathbf{b} - (\mathbf{a} \cdot \mathbf{b}) \mathbf{c}$$

applied to $\hat{\mathbf{k}} \times \left( \hat{\mathbf{k}} \times \mathbf{B} \right)$ gives

$$
  \hat{\mathbf{k}} \times \left( \hat{\mathbf{k}} \times \mathbf{B} \right) = \underbrace{\left( \hat{\mathbf{k}} \dot \mathbf{B} \right)}_{=0 \text{ since $\mathbf{k} \perp \mathbf{B}$}} \hat{\mathbf{k}} - \underbrace{\left( \hat{\mathbf{k}} \cdot \hat{\mathbf{k}} \right)}_{= 1} \mathbf{B} = - \mathbf{B} \ ,
$$

and the original relation gives

$$\mathbf{B} = \mathbf{B} \dfrac{c^2 |\mathbf{k}|^2}{\omega^2} \ ,$$

and the relation between pulsation $\omega$, wave vector $\mathbf{k}$ and speed of light (EM radiation) $c$,

$$c = \dfrac{\omega}{|\mathbf{k}|} \ .$$

```

(classical-electromagnetism\:waves\:plane-waves\:snell)=
## Snell's Law at an Interface
Snell's law is derived here assuming isotropic linear media, so that

$$\begin{cases}
  \mathbf{d}(\mathbf{r},t) = \varepsilon \mathbf{e}(\mathbf{r},t) \\
  \mathbf{b}(\mathbf{r},t) = \mu         \mathbf{h}(\mathbf{r},t)
\end{cases}$$

and for harmonic plane EM waves

$$\begin{cases}
 \mathbf{e}(\mathbf{r}, t) = \mathbf{E}_{a} \, e^{i \left( \mathbf{k}_a \cdot \mathbf{r} - \omega t \right)} \\
 \mathbf{b}(\mathbf{r}, t) = \mathbf{B}_{a} \, e^{i \left( \mathbf{k}_a \cdot \mathbf{r} - \omega t \right)} \\
\end{cases}$$

$$\begin{aligned}
  \mathbf{B}_a & = \dfrac{1}{c} \, \hat{\mathbf{k}}_a \times \mathbf{E}_a \\
  \mathbf{E}_a & = - c \, \hat{\mathbf{k}}_a \times \mathbf{B}_a \\
\end{aligned}$$

being index $a$ representing the media involved: $a = 1$ for the medium with incident and reflected waves, $a = 2$ for the medium with the refracted wave.

[Jump conditions of electromagnetic field at an interface](classical-electromagnetism\:media\:jump) with no charge or current surface density are given by conditions {eq}`eq:em-jump:no-surf-density`,

$$\begin{cases}
  \varepsilon_1 e_{n,1} = \varepsilon_2 e_{n,2} \\
  e_{t_{\alpha},1} = e_{t_{\alpha},2}                                    & \quad , \quad \alpha=1:2 \\
  b_{n,1} = b_{n,2}  \\
  \dfrac{1}{\mu_1} b_{t_{\alpha},1} = \dfrac{1}{\mu_2} b_{t_{\alpha},2}  & \quad , \quad \alpha=1:2 \\
\end{cases}$$

Definition of some vectors: $\hat{\mathbf{n}}$ unit normal vector, $\mathbf{k}$ wave vector, $\hat{\mathbf{b}} = \dfrac{\hat{\mathbf{n}} \times \mathbf{k}}{|\hat{\mathbf{n}} \times \mathbf{k}|}$ (singular only for normal incident ray), $\hat{\mathbf{c}} = \dfrac{\hat{\mathbf{b}} \times \mathbf{k}}{|\hat{\mathbf{b}} \times \mathbf{k}|}$, $\hat{\mathbf{t}} = \dfrac{\hat{\mathbf{b}} \times \hat{\mathbf{n}}}{|\hat{\mathbf{b}} \times \hat{\mathbf{n}}|}$

Incident angle $\theta_{1,i}$ is the angle between $\hat{\mathbf{n}}$ and $\mathbf{k}$, s.t. $\hat{\mathbf{n}} \times \mathbf{k} = \hat{\mathbf{b}} \, k \, \sin \theta_{1,i}$.

$$\begin{cases}
  \hat{\mathbf{k}} = \quad \cos \theta_{1,i} \hat{\mathbf{n}} + \sin \theta_{1,i} \hat{\mathbf{t}} \\
  \hat{\mathbf{c}} =      -\sin \theta_{1,i} \hat{\mathbf{n}} + \cos \theta_{1,i} \hat{\mathbf{t}}
\end{cases}
\quad , \quad
\begin{cases}
  \hat{\mathbf{n}} = \cos \theta_{1,i} \hat{\mathbf{k}} - \sin \theta_{1,i} \hat{\mathbf{c}} \\
  \hat{\mathbf{t}} = \sin \theta_{1,i} \hat{\mathbf{k}} + \cos \theta_{1,i} \hat{\mathbf{c}}
\end{cases}$$

The electromagnetic field can be written as

$$\begin{aligned}
  \mathbf{E} & = E_b \hat{\mathbf{b}} + E_c \hat{\mathbf{c}} = \\
             & = E_b \hat{\mathbf{b}} - E_c \sin \theta_{1,i} \hat{\mathbf{n}} + E_c \cos \theta_{1,i} \hat{\mathbf{t}} \\
  \mathbf{B} & = B_b \hat{\mathbf{b}} + B_c \hat{\mathbf{c}} = \\
             & = \frac{E_c}{c} \hat{\mathbf{b}} - \frac{E_b}{c} \hat{\mathbf{c}} = \\
             & = \frac{E_c}{c} \hat{\mathbf{b}} + \frac{E_b}{c} \sin \theta_{1,i} \hat{\mathbf{n}} - \frac{E_b}{c} \cos \theta_{1,i} \hat{\mathbf{t}} \ .
\end{aligned}$$

so that jump relations become

$$\begin{cases}
  b: & \quad E_{b,1} = E_{b,2} \\
  n: & \quad \dots \\
  t: & \quad \dots \\
\end{cases}
\quad , \quad
\begin{cases}
  b: & \quad \dots \\
  n: & \quad \frac{E_{b,1}}{c_1} \sin \theta_{1,i} = \frac{E_{b,2}}{c_2} \sin \theta_{2,i}  \\
  t: & \quad \dots \\
\end{cases}$$

thus **Snell's law** follows

$$\frac{\sin \theta_{1,i}}{\sin \theta_{2,t}} = \frac{c_2}{c_1} = \frac{n_1}{n_2} \ .$$

**Incident, Reflected, and Refracted Wave.** The wave at the interface in medium 1 has the contribution of the incoming incident wave and the reflected one.

$$\begin{aligned}
\mathbf{e}_1(\mathbf{r},t)
& = \mathbf{e}_i(\mathbf{r},t) + \mathbf{e}_r(\mathbf{r},t) = \\
& = \mathbf{E}_{i} e^{i \left( \mathbf{k}_i \cdot \mathbf{r} - \omega t \right)} + \mathbf{E}_{r} e^{i \left( \mathbf{k}_r \cdot \mathbf{r} - \omega t \right)} = \\
& = \left( \mathbf{E}_{i} e^{i \mathbf{k}_i \cdot \mathbf{r}} + \mathbf{E}_{r} e^{i \mathbf{k}_r \cdot \mathbf{r} } \right) e^{-i \omega t}
\end{aligned}$$

with

$$\begin{aligned}
  \mathbf{k}_i & = k_{i,n} \hat{\mathbf{n}} + k_{i,t} \hat{\mathbf{t}} \\
  \mathbf{k}_r & = k_{r,n} \hat{\mathbf{n}} + k_{r,t} \hat{\mathbf{t}} \\
\end{aligned}$$

At the interface, $\mathbf{r}_s \cdot \hat{\mathbf{n}} = 0$, and thus

$$\begin{aligned}
  \mathbf{e}_1(\mathbf{r}_s, t) & = \left( \mathbf{E}_i e^{i k_{i,t} x_t} + \mathbf{E}_r e^{i k_{r,t} x_t} \right) e^{-i\omega t} \\
  \mathbf{e}_2(\mathbf{r}_s, t) & =        \mathbf{E}_t e^{i k_{t,t} x_t} e^{-i \omega t} \\
\end{aligned}$$

In order for the boundary conditions to be satisfied at all the points of the interface at each time,

  $$k_{i,t} = k_{r,t} = k_{t,t} \ .$$

Exploiting the relation between the pulsation, the wave-length, and the speed of light in media, $c_a = \frac{\omega}{|\mathbf{k}_a|} = \frac{c}{n_a}$,

$$|\mathbf{k}_i| = |\mathbf{k}_r| \qquad \rightarrow \qquad k_{r,n} = - k_{i,n}$$

$$\frac{|\mathbf{k}_2|}{|\mathbf{k}_1|} = \frac{c_1}{c_2}$$

$$\frac{k_{t,t}^2 + k_{t,n}^2}{k_{i,t}^2 + k_{i,n}^2} = \frac{c_1^2}{c_2^2}$$

$$
\begin{aligned}
  k_{i,n} & = \ \ \ |\mathbf{k}_i| \, \cos \theta_i \\
  k_{r,n} & = -     |\mathbf{k}_r| \, \cos \theta_r \\
  k_{t,n} & = \ \ \ |\mathbf{k}_t| \, \cos \theta_t \\
\end{aligned}
\quad , \quad
\begin{aligned}
  k_{i,t} & = \ \ \ |\mathbf{k}_i| \, \sin \theta_i \\
  k_{r,t} & = \ \ \ |\mathbf{k}_r| \, \sin \theta_r \\
  k_{t,t} & = \ \ \ |\mathbf{k}_t| \, \sin \theta_t \\
\end{aligned}
$$

$$\begin{cases}
 E_n: & \quad \varepsilon_1   \left( E_{i,c} \sin \theta_i + E_{r,c} \sin \theta_r \right) = \varepsilon_2   E_{t,c} \sin \theta_{t} \\
 E_t: & \quad                        E_{i,c} \cos \theta_i - E_{r,c} \cos \theta_r         =                 E_{t,c} \cos \theta_{t} \\
 E_b: & \quad                        E_{i,b}               + E_{r,b}                       =                 E_{t,b}                 \\
 B_n: & \quad                        B_{i,c} \sin \theta_i + B_{r,c} \sin \theta_r         =                 B_{t,c} \sin \theta_{t} \\
 B_t: & \quad \frac{1}{\mu_1} \left( B_{i,c} \cos \theta_i - B_{r,c} \cos \theta_r \right) = \frac{1}{\mu_2} B_{t,c} \cos \theta_{t} \\
 B_b: & \quad \frac{1}{\mu_1} \left( B_{i,b}               + B_{r,b}               \right) = \frac{1}{\mu_2} B_{t,b}                 \\
\end{cases}$$

Writing the magnetic field as a function of the wave-vector and the magnetic field, it's possible to write 2 decoupled systems of equations

$$\begin{cases}
 E_n: & \quad \varepsilon_1   \left( E_{i,c} \sin \theta_i + E_{r,c} \sin \theta_r \right) = \varepsilon_2   E_{t,c} \sin \theta_{t} \\
 E_t: & \quad                        E_{i,c} \cos \theta_i - E_{r,c} \cos \theta_r         =                 E_{t,c} \cos \theta_{t} \\
 B_b: & \quad \frac{1}{\mu_1} \left( \frac{E_{i,c}}{c_1}   + \frac{E_{r,c}}{c_1}   \right) = \frac{1}{\mu_2} \frac{E_{t,c}}{c_2}     \\
\end{cases}$$

$$\begin{cases}
 E_b: & \quad                        E_{i,b}               + E_{r,b}                       =                 E_{t,b}                 \\
 B_n: & \quad                        \frac{E_{i,b}}{c_1} \sin \theta_i + \frac{E_{r,b}}{c_1} \sin \theta_r         =                 \frac{E_{t,b}}{c_2} \sin \theta_{t} \\
 B_t: & \quad \frac{1}{\mu_1} \left( \frac{E_{i,b}}{c_1} \cos \theta_i - \frac{E_{r,b}}{c_1} \cos \theta_r \right) = \frac{1}{\mu_2} \frac{E_{t,b}}{c_2} \cos \theta_{t} \\
\end{cases}$$

The equations $E_n$ and $B_b$ are equivalent; $E_b$ and $B_n$ are equivalent as well, because of Snell's law. Thus, defining

$$
\begin{aligned}
  r_c & := \dfrac{E_{r,c}}{E_{i,c}} \\
  t_c & := \dfrac{E_{t,c}}{E_{i,c}} \\
\end{aligned}
\quad , \quad
\begin{aligned}
  r_b & := \dfrac{E_{r,b}}{E_{i,b}} \\
  t_b & := \dfrac{E_{t,b}}{E_{i,b}} \\
\end{aligned}
$$

and $\alpha_i := \frac{1}{\mu_i c_i}$. These systems of equations can be written as two uncoupled linear systems of equations,

(for P-polarization **todo** *change index from $c$ to $p$; for S-polarization **todo** *change index from $b$ to $s$*)

$$
& \begin{cases}
 E_t: & \quad  \cos \theta_i -  \cos \theta_r \, r_c = \cos \theta_{t} \, t_c \\
 B_b: & \quad  \alpha_1      +  \alpha_1      \, r_c =  \alpha_2       \, t_c \\
\end{cases}
\\
& \begin{cases}
 E_b: & \quad                          1 +                   r_b =  t_b \\
 B_t: & \quad  \alpha_1 \, \cos \theta_i -  \alpha_1 \, \cos \theta_r \, r_b = \alpha_2 \, \cos \theta_{t} \, t_b \\
\end{cases}
$$

Calling $\theta_i = \theta_r = \theta_1$, $\theta_2 = \theta_t$, these linear systems can be written using matrix formalism,

$$
& \begin{bmatrix} -1 & 1 \\ 1 & \frac{\alpha_2}{\alpha_1} \frac{\cos \theta_2}{\cos \theta_1} \end{bmatrix}
 \begin{bmatrix} r_b \\ t_b \end{bmatrix} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
\\
& \begin{bmatrix} 1 & \frac{\cos \theta_2}{\cos \theta_1} \\ -1 & \frac{\alpha_2}{\alpha_1} \end{bmatrix}
 \begin{bmatrix} r_c \\ t_c \end{bmatrix} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

**todo** *Analysis of the total reflection, forcing $t_x = 0$. Check signs before*

$$
\begin{bmatrix} 1 & \frac{\cos \theta_2}{\cos \theta_1} \\ -1 & \frac{\alpha_2}{\alpha_1} \end{bmatrix}
 \begin{bmatrix} r_c \\ t_c \end{bmatrix} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
\qquad \rightarrow \qquad
\begin{bmatrix} r_c \\ t_c \end{bmatrix} = \dfrac{1}{\frac{\alpha_2}{\alpha_1} + \frac{\cos \theta_2}{\cos \theta_1}} \begin{bmatrix} \frac{\alpha_2}{\alpha_1} & - \frac{\cos \theta_2}{\cos \theta_1} \\ 1 & 1  \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix}
= \begin{bmatrix} \frac{\alpha_2 \cos \theta_1 - \alpha_1 \cos \theta_2}{\alpha_2 \cos \theta_1 + \alpha_1 \cos \theta_2} \\ \frac{2 \alpha_1 \cos \theta_1}{\alpha_2 \cos \theta_1 + \alpha_1 \cos \theta_2} \end{bmatrix}
$$

$$
\begin{bmatrix} -1 & 1 \\ 1 & \frac{\alpha_2}{\alpha_1} \frac{\cos \theta_2}{\cos \theta_1} \end{bmatrix}
 \begin{bmatrix} r_b \\ t_b \end{bmatrix} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
\qquad \rightarrow \qquad
\begin{bmatrix} r_b \\ t_b \end{bmatrix} = \dfrac{1}{-\frac{\alpha_2}{\alpha_1} \frac{\cos \theta_2}{\cos \theta_1} - 1} \begin{bmatrix}  \frac{\alpha_2}{\alpha_1} \frac{\cos \theta_2}{\cos \theta_1} & -1 \\ -1 & -1  \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix}
= \begin{bmatrix} \frac{\alpha_1 \cos \theta_1 - \alpha_2 \cos \theta_2}{\alpha_1 \cos \theta_1 + \alpha_2 \cos \theta_2} \\ \frac{2 \alpha_1 \cos \theta_1}{\alpha_1 \cos \theta_1 + \alpha_2 \cos \theta_2} \end{bmatrix}
$$

<!--
that can be recast using Snell's law

$$\sin \theta_2 = \sin \theta_1 \frac{n_2}{n_1}$$

$$\cos \theta_2 = \sqrt{1 - \sin^2 \theta_2} = \sqrt{1 - \sin^2 \theta_1 \left( \frac{n_2}{n_1} \right)^2}$$
-->

that can be recast with the wave impedance $Z$,

$$\alpha_1 = \frac{1}{\mu_1 c_1} = \frac{\sqrt{\mu_1 \varepsilon_1}}{\mu_1} = \sqrt{\dfrac{\varepsilon_1}{\mu_1}} =: \frac{1}{Z_1} \ ,$$

$$
\begin{bmatrix} r_c \\ t_c \end{bmatrix} = \begin{bmatrix} \frac{Z_1 \cos \theta_1 - Z_2 \cos \theta_2}{Z_1 \cos \theta_1 + Z_2 \cos \theta_2} \\ \frac{2 Z_2 \cos \theta_1}{Z_1 \cos \theta_1 + Z_2 \cos \theta_2} \end{bmatrix}
$$

$$
\begin{bmatrix} r_b \\ t_b \end{bmatrix} = \begin{bmatrix} \frac{Z_2 \cos \theta_1 - Z_1 \cos \theta_2}{Z_2 \cos \theta_1 + Z_1 \cos \theta_2} \\ \frac{2 Z_2 \cos \theta_1}{Z_2 \cos \theta_1 + Z_1 \cos \theta_2} \end{bmatrix}
$$

**Energy Balance and Transmission Coefficients.** Energy balance for a domain collapsing on the interface reduces to power flux balance, namely

$$\oint_{\partial V} \mathbf{s} \cdot \hat{\mathbf{n}} = 0 \ ,$$

with $\mathbf{s} = \mathbf{e} \times \mathbf{h}$ the Poynting vector. For harmonic plane waves,

$$\begin{aligned}
  \mathbf{s}(\mathbf{r},t)
  & = \mathbf{e}(\mathbf{r},t) \times \mathbf{h}(\mathbf{r},t) = \\
  & = \frac{1}{\mu} \left[ \mathbf{E} e^{i(\mathbf{k} \cdot \mathbf{r} - \omega t)} + \mathbf{E}^* e^{-i(\mathbf{k} \cdot \mathbf{r} - \omega t)} \right] \times \left[ \mathbf{B} e^{i(\mathbf{k} \cdot \mathbf{r} - \omega t)} + \mathbf{B}^* e^{-i(\mathbf{k} \cdot \mathbf{r} - \omega t)}  \right] = \\
  & = \frac{1}{\mu} \left[ \, \mathbf{E} \times \mathbf{B} \, e^{i 2(\mathbf{k} \cdot \mathbf{r} - \omega t)} + c.c. \, \right] + \frac{1}{\mu} \left[ \, \mathbf{E} \times \mathbf{B}^* + c.c. \, \right] = \\
  & = \dots + \frac{1}{\mu} \mathbf{E} \times \left( \frac{1}{c} \hat{\mathbf{k}} \times \mathbf{E} \right)^* = \\
  & = \dots + \frac{1}{\mu c} \left( \mathbf{E} \cdot \mathbf{E}^* \right) \hat{\mathbf{k}} = \\
  & = \dots + \frac{1}{\mu c} | \mathbf{E} |^2 \hat{\mathbf{k}} \ .
  & = \dots + \alpha | \mathbf{E} |^2 \hat{\mathbf{k}} \ .
\end{aligned}$$

For each one of the two polarizations, the following holds ($\cos \theta$ comes from the dot product $\hat{k} \cdot \hat{n}$ appearing in the surface integral),

$$\alpha_1 \cos \theta_1 = \alpha_1 r_x^2 \, \cos \theta_1 + \alpha_2 t_x^2 \, \cos \theta_2 \ ,$$

i.e., the sum of reflected and transmitted power equals the incident power.

```{dropdown} Proof of the power balance, for P-polarization

**todo** Here $P$ is index $c$

Dividing by $\alpha_1 \cos  \theta_1$

$$\begin{aligned}
 & \frac{1}{\alpha_1 \cos \theta_1} \left( \alpha_1 r_p^2 \, \cos \theta_1 + \alpha_2 t_p^2 \, \cos \theta_2 \right) = \\
 & = \frac{\left(\alpha_1 \cos \theta_1 - \alpha_2 \cos \theta_2\right)^2}{\left(\alpha_1 \cos \theta_1 + \alpha_2 \cos \theta_2\right)^2} + \frac{\alpha_2 \cos \theta_2}{\alpha_1 \cos \theta_1} \frac{\left( 2 \alpha_1 \cos \theta_1 \right)^2}{\left( \alpha_1 \cos \theta_1 + \alpha_2 \cos \theta_2 \right)^2} = \\
  & = \dfrac{1}{\left( \alpha_1 \cos \theta_1 + \alpha_2 \cos \theta_2 \right)^2} \left[ \alpha_1^2 \cos^2 \theta_1 - 2 \alpha_1 \alpha_2 \cos \theta_1 \cos \theta_2 + \alpha_2^2 \cos^2 \theta_2 + 4 \alpha_1 \alpha_2 \cos \theta_1 \cos \theta_2 \right] = \\
  & = 1 \ .
\end{aligned}$$

```

