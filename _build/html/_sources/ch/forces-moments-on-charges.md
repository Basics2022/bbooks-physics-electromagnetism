<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:forces-moments)=
# Force, moment, and power on elementary charge distributions

## Force, moment and power on a point electric charge

Point electric charge with charge $q$ in a point $\vec{r}_P(t)$ at time $t$ where electromagnetic field is $\vec{e}(\vec{r},t)$, $\vec{b}(\vec{r},t)$:
- Lorentz's force

   $$\vec{F} = q \left( \vec{e}(\vec{r}_P(t), t) - \vec{b}(\vec{r}_P(t),t) \times \vec{v}_P(t) \right) \ ,$$

- zero moment, since it has no dimension (and assumed uniform or symmetric or... distribution of electric charge)

- power

   $$\begin{aligned}
     P & = \vec{v}_P(t) \cdot \vec{F} = \\
       & = \vec{v}_P(t) \cdot \, q \, \left( \vec{e}(\vec{r}_P(t), t) - \vec{b}(\vec{r}_P(t), t) \times \vec{v}_P(t) \right) = q \, \vec{v}_P(t) \cdot \vec{e}(\vec{r}_P(t),t) \ .
   \end{aligned}$$

## Force, moment and power on a electric dipole

Electric dipole with center $\vec{r}_C(t)$, axis $\vec{\ell}$, so that the positive charge $q$ is in $P_+ = C + \dfrac{\vec{\ell}}{2}$ and the negative charge is in $P_- = C - \dfrac{\vec{\ell}}{2}$, with $q \rightarrow +\infty$, $|\vec{\ell}| \rightarrow 0$, s.t. $q|\vec{\ell}| = |\vec{d}|$ finite.

**Kinematics and expansion of the field**

$$\vec{v}_{\pm} = \vec{v}_C \pm \vec{\omega} \times \frac{\vec{\ell}}{2}$$

$$\vec{e}(P_{\pm}) = \vec{e}\left( C \pm \dfrac{\vec{\ell}}{2} \right) = \vec{e}(C) \pm \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{e}(C) + o(|\vec{\ell}|)$$

$$\vec{b}(P_{\pm}) = \vec{b}\left( C \pm \dfrac{\vec{\ell}}{2} \right) = \vec{b}(C) \pm \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{b}(C) + o(|\vec{\ell}|)$$

**Net force.**

$$\begin{aligned}
  \vec{F} & = \vec{F}_+ + \vec{F}_- = \\
   & = q \left[ \vec{e}(P_+) - \vec{b}(P_+) \times \vec{v}_{+} \right] - q \left[ \vec{e}(P_-) - \vec{b}(P_-) \times \vec{v}_{-} \right] = \\
   & = q \left[ \vec{e}_C + \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{e}_C - \left( \vec{b}_C + \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{b}_C \right) \times \left( \vec{v}_C + \vec{\omega} \times \dfrac{\vec{\ell}}{2} \right) \right] + \\ 
   & - q \left[ \vec{e}_C - \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{e}_C - \left( \vec{b}_C - \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{b}_C \right) \times \left( \vec{v}_C - \vec{\omega} \times \dfrac{\vec{\ell}}{2} \right) \right] = \\
   & = q \vec{\ell} \cdot \nabla \vec{e}(C) - \left( q \vec{\ell} \cdot \nabla \vec{b}(C) \right) \times \vec{v}_C + \vec{b}(C) \times \left(  \vec{\omega} \times q \vec{\ell} \right) + o(|\vec{\ell}|)
\end{aligned}$$

**Net moment, w.r.t. $C$.**

$$\begin{aligned}
  \vec{M}_C
   & = \frac{\vec{\ell}}{2} \times \vec{F}_+ - \frac{\vec{\ell}}{2} \times \vec{F}_- = \\
   & = q \frac{\vec{\ell}}{2} \times \left[ \vec{e}(P_+) - \vec{b}(P_+) \times \vec{v}_{+} \right] + q \frac{\vec{\ell}}{2} \times \left[ \vec{e}(P_-) - \vec{b}(P_-) \times \vec{v}_{-} \right] = \\
   & = q \frac{\vec{\ell}}{2} \times \left[ \vec{e}_C + \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{e}_C - \left( \vec{b}_C + \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{b}_C \right) \times \left( \vec{v}_C + \vec{\omega} \times \dfrac{\vec{\ell}}{2} \right) \right] + \\ 
   & + q \frac{\vec{\ell}}{2} \times \left[ \vec{e}_C - \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{e}_C - \left( \vec{b}_C - \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{b}_C \right) \times \left( \vec{v}_C - \vec{\omega} \times \dfrac{\vec{\ell}}{2} \right) \right] = \\
   & = q \vec{\ell} \times \left[ \vec{e}_C - \vec{b}_C \times \vec{v}_C \right] + o(|\vec{\ell}|) \ .
\end{aligned}$$

**Power.**

$$\begin{aligned}
  P & = P_+ + P_- = \\
  & = \vec{F}_+ \cdot \vec{v}_+ + \vec{F}_- \cdot \vec{v}_- = \\
  & = q \, \left[ \vec{e}(P_+) - \vec{b}(P_+) \times \vec{v}_{+}  \right] \cdot \vec{v}_{+} 
    - q \, \left[ \vec{e}(P_-) - \vec{b}(P_-) \times \vec{v}_{-}  \right] \cdot \vec{v}_{-} = \\
  & = q \, \vec{e}(P_+) \cdot \vec{v}_{+} 
    - q \, \vec{e}(P_-) \cdot \vec{v}_{-} = \\
  & = q \, \left[ \vec{e}_C + \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{e}_C  \right] \cdot \left[ \vec{v}_C + \vec{\omega} \times \dfrac{\vec{\ell}}{2} \right] 
    - q \, \left[ \vec{e}_C - \dfrac{\vec{\ell}}{2} \cdot \nabla \vec{e}_C  \right] \cdot \left[ \vec{v}_C - \vec{\omega} \times \dfrac{\vec{\ell}}{2} \right] = \\
  & = \vec{e}_C \cdot \left( \vec{\omega} \times q \vec{\ell} \right) + \left( q \vec{\ell} \cdot \nabla \vec{e}_C \right) \cdot \vec{v}_C + o(|\vec{\ell}|^2) \ .
\end{aligned}$$


## Force, moment and power on a magnetic dipole

On an elementary magnetic dipole, modeled as a "small" circuit with current $i$ enclosing area $S$ and center $C$, with $S \rightarrow 0$, $i \rightarrow + \infty$ so that $i S \hat{n} := \vec{m}$ finite

**Force.**

$$\dots$$
$$\vec{F} = \nabla \vec{b}(C) \cdot \vec{m}$$

**Moment.**

$$\dots$$
$$\vec{M}_C = \vec{m} \times \vec{b}(C)$$

**Power.**

$$P = \vec{v}_C \cdot \nabla \vec{b}(C) \cdot \vec{m} + \vec{\omega} \cdot \vec{m} \times \vec{b}(C) \ .$$


## Energy balance

**todo** *Check and put charges, currents, and dipoles together with the electromagnetic field*

Ispirati dalle dimensioni fisiche dei campi elettromagnetici,

$$\begin{aligned}
\left[\mathbf{e}\right] = \frac{\text{force}}{\text{charge}} \qquad & , \qquad
[\mathbf{d}] = \frac{\text{charge}}{\text{length}^2} \\
[\mathbf{b}] = \frac{\text{force}\cdot\text{time}}{\text{charge}\cdot\text{length}} \qquad & , \qquad
[\mathbf{h}] = \frac{\text{charge}}{\text{time} \cdot \text{length}}
\end{aligned}$$
<!--$$[\varepsilon] = \frac{\text{charge}^2}{\text{force} \cdot \text{length}^2} = \frac{C^2}{N \ m^2}$$-->
<!--$$[\mu] = \frac{\text{charge}^2}{\text{force} \cdot \text{length}^2} = \frac{C^2}{N \ m^2}$$-->

$$\begin{aligned}
\left[\mathbf{e} \cdot \mathbf{d}\right] & = \frac{\text{force}}{\text{length}^2} = \frac{\text{energy}}{\text{length}^3} = [u] \\
[\mathbf{b} \cdot \mathbf{h}] & = \frac{\text{force}}{\text{length}^2} = \frac{\text{energy}}{\text{length}^3} = [u]
\end{aligned}$$

si può costruire la densità di volume di energia  (**todo** trovare motivazioni più convincenti, non basandosi solo sull'analisi dimensionale ma sul lavoro)

$$u = \frac{1}{2} \left( \mathbf{e} \cdot \mathbf{d} + \mathbf{b} \cdot \mathbf{h} \right) \ .$$

Si può calcolare la derivata parziale nel tempo della densità di energia, $u$, e usare le equazioni di Maxwell per ottenere un'equazione di bilancio dell'energia del campo elettromagnetico. Per un mezzo isotropo lineare, per il quale valgono le equazioni costitutive $\mathbf{d} = \varepsilon \mathbf{e}$, $\mathbf{b} = \mu \mathbf{h}$, la derivata parziale nel tempo dell'energia elettromagnetica può essere riscritta sfuttando la regola di derivazione del prodotto e le equazioni di Faraday-Lenz-Neumann e Ampére-Maxwell,

$$\begin{aligned}
\dfrac{\partial u}{\partial t} & = \dfrac{\partial}{\partial t}\left( \frac{1}{2} \mathbf{e} \cdot \mathbf{d} + \mathbf{b} \cdot \mathbf{h} \right) =  \qquad (...) \\
& = \mathbf{e} \cdot \partial_t \mathbf{d} + \mathbf{h} \cdot \partial_t \mathbf{b} = \\
& = \mathbf{e} \cdot (\nabla \times \mathbf{h} - \mathbf{j}) - \mathbf{h} \cdot \nabla \times \mathbf{e} \ .
\end{aligned}$$

L'ultimo termine può essere ulteriormente manipolato, usando l'identità vettoriale 

$$\begin{aligned}
\mathbf{e} \cdot \nabla \times \mathbf{h} - \mathbf{h} \cdot \nabla \times \mathbf{e} & = e_i \varepsilon_{ijk} \partial_j h_k - h_i \varepsilon_{ijk} \partial_j e_k = \qquad (i \rightarrow k, k \rightarrow i)\\
& = e_i \varepsilon_{ijk} \partial_j h_k - h_k \varepsilon_{kji} \partial_j e_i = \\
& = e_i \varepsilon_{ijk} \partial_j h_k + h_k \varepsilon_{ijk} \partial_j e_i = \\
& =  \partial_j (\varepsilon_{ijk} e_i  h_k ) = \\
& =  \partial_j (\varepsilon_{jki} e_i  h_k ) = \\
& = \nabla \cdot (\mathbf{h} \times \mathbf{e}) = - \nabla \cdot (\mathbf{e} \times \mathbf{h})
\end{aligned}$$

che permette di scrivere l'equazione del bilancio di energia elettromagnetica come,

$$\frac{\partial u }{\partial t} + \nabla \cdot \mathbf{s} = - \mathbf{e} \cdot \mathbf{j} \ ,$$

dove è stato definito il **vettore di Poynting**, o meglio il campo vettoriale di Poynting,

$$\mathbf{s}(\mathbf{r},t) := \mathbf{e}(\mathbf{r},t) \times \mathbf{h}(\mathbf{r},t) \ ,$$

che può essere identificato come un flusso di potenza per unità di superficie, comparendo sotto l'operatore di divergenza nel bilnacio di energia.

**todo.** Rimandare a una sezione in cui si mostra questa ultima affermazione passando dal bilancio differenziale al bilancio integrale e si usa il teorema della divergenza, $\int_V \nabla \cdot \mathbf{s} = \oint_{\partial V} \mathbf{s} \cdot \hat{\mathbf{n}}$.


```{dropdown} Bilancio di energia di cariche nel vuoto, o i materiali senza polarizzazione o magnetizzazione
:open:

**Moto di cariche puntiformi.**
L'equazione del moto di carica puntiforme $q_k$ nella posizione $\mathbf{r}_k(t)$ al tempo $t$ è

$$m_k \ddot{\mathbf{r}}_k = \mathbf{f}_k + \mathbf{f}_k^{em} \ ,$$

avendo riconosciuto i contributi di forza dovuti al campo elettromagnetico come $\mathbf{f}_k^{em}$ dagli altri. L'espressione della forza dovuta al campo elettromagnetico sulla carica $k$ è data dalla forza di Lorentz,

$$\mathbf{f}_k^{em}(t) = q_k \left[ \mathbf{e}(\mathbf{r_k}(t), t) - \mathbf{b}(\mathbf{r}_k(t), t) \times \dot{\mathbf{r}}_k(t) \right]$$

**Continuità della carica elettrica.** La densità di carica e di corrente elettrica di un insieme di cariche libere puntiformi macroscopiche può essere scritta come

$$\begin{aligned}
  \rho(\mathbf{r},t) & = \sum_k q_k \delta(\mathbf{r} - \mathbf{r}_k(t)) \\
  \mathbf{j}(\mathbf{r},t) & = \sum_k q_k \dot{\mathbf{r}}_k(t) \delta(\mathbf{r} - \mathbf{r}_k(t)) \ .
\end{aligned}$$

L'equazione di continuità della carica, $\partial_t \rho + \nabla \cdot \mathbf{j} = 0$, risulta quindi soddisfatta,

$$\begin{aligned}
  \partial_t \rho &  = - \sum_k q_k \, \partial_i \delta(\mathbf{r} - \mathbf{r}_k(t)) \, \dot{r}_{k,i} \\
  \partial_i j_i  &  =   \sum_k q_k \, \dot{r}_{k,i} \, \partial_i \delta(\mathbf{r} - \mathbf{r}_k(t)) \\
\end{aligned}$$

```




```{dropdown} Procedimento alternativo (e più generale?)

**todo** *In caso questo procedimento sia più generale, o più corretto, sostituire il procedimento precedente.*

La carica elementare in un volumetto $\Delta V$ è data da dal prodotto tra il volume e la densità volumetrica di carica, $\rho \Delta V$; la velocità media locale della carica elettrica è $\mathbf{v}$; la forza agente sulla carica elementare immersa in un campo elettromagnetico è determinata dalla formula di Lorentz, $\mathbf{f} \Delta V = \Delta V \rho \left( \mathbf{e} - \mathbf{b} \times \mathbf{v} \right)$. La potenza di questa forza è il prodotto scalare con la velocità media delle cariche, $\Delta V \mathbf{f} \cdot \mathbf{v}$

La potenza del campo elettromagnetico sul moto della carica elettrica per unità di volume è quindi 

$$\mathbf{v} \cdot \mathbf{f} = \rho \mathbf{v} \cdot \left( \mathbf{e} - \mathbf{b} \times \mathbf{v} \right) = \rho \mathbf{v} \cdot \mathbf{e} = \mathbf{j} \cdot \mathbf{e} \ .$$

**todo**
- discutere questo termine del bilancio di energia cinetica nel moto della carica elettrica
- questo termine compare con segno opposto nel bilancio dell'energia elettromagnetica del sistema
- dove compare la non-conservatività del problema in presenza di materiali dissipativi (come resistenza elettrica con $\mathbf{e} = \rho_R \mathbf{j}$?

Il termine $\mathbf{e} \cdot \mathbf{j}$ può essere manipolato usando le equazioni di Maxwell, e le relazioni

$$\begin{cases}
  \mathbf{d} = \varepsilon_0 \mathbf{e} + \mathbf{p} \\
  \mathbf{h} = \frac{\mathbf{b}}{\mu_0} - \mathbf{m} \\
\end{cases}$$

$$\begin{aligned}
  \mathbf{e} \cdot \mathbf{j} 
    & = \mathbf{e} \cdot \left( \nabla \times \mathbf{h} - \partial_t \mathbf{d} \right) = \\
    & = - \nabla \cdot \left( \mathbf{e} \times \mathbf{h} \right) + \mathbf{h} \cdot \nabla \times \mathbf{e} - \mathbf{e} \cdot \partial_t \mathbf{d} = \\
    & = - \nabla \cdot \left( \mathbf{e} \times \mathbf{h} \right) - \mathbf{h} \cdot \partial_t \mathbf{b} - \mathbf{e} \cdot \partial_t \mathbf{d} 
\end{aligned}$$

Gli ultimi due termini possono essere manipolati in diverse maniere,

$$\begin{aligned}
  \mathbf{e} \cdot \partial_t \mathbf{d}
    = \mathbf{e} \cdot \partial_t \left( \varepsilon_0 \mathbf{e} + \mathbf{p} \right) 
  & = \partial_t \left( \frac{1}{2} \varepsilon_0 \mathbf{e} \cdot \mathbf{e} \right) + \mathbf{e} \cdot \partial_t \mathbf{p} \\
  & = \partial_t \left( \frac{1}{2} \mathbf{e} \cdot \mathbf{d} \right) + \frac{1}{2} \left( \mathbf{e} \cdot \partial_t \mathbf{p} - \mathbf{p} \cdot \partial_t \mathbf{e} \right) \\
  & = \partial_t \left( \frac{1}{2 \varepsilon_0} \mathbf{d} \cdot \mathbf{d} \right) - \frac{\mathbf{p}}{\varepsilon_0} \cdot \partial_t \mathbf{d} \\
\end{aligned}$$

$$\begin{aligned}
  \mathbf{h} \cdot \partial_t \mathbf{b}
    = \mathbf{h} \cdot \partial_t \left( \mu_0 \mathbf{h} + \mu_0 \mathbf{m} \right) 
  & = \partial_t \left( \frac{1}{2} \mu_0 \mathbf{h} \cdot \mathbf{h} \right) + \mu_0 \mathbf{h} \cdot \partial_t \mathbf{m} \\
  & = \partial_t \left( \frac{1}{2} \mathbf{b} \cdot \mathbf{h} \right) + \frac{1}{2} \mu_0 \left( \mathbf{h} \cdot \partial_t \mathbf{m} - \mathbf{m} \cdot \partial_t \mathbf{h} \right) \\
  & = \partial_t \left( \frac{1}{2 \mu_0} \mathbf{b} \cdot \mathbf{b} \right) - \mathbf{m} \cdot \partial_t \mathbf{b} \\
\end{aligned}$$

Nel vuoto o in mezzi lineari $\mathbf{e} \cdot \partial_t \mathbf{p} - \mathbf{p} \cdot \partial_t \mathbf{e} = \mathbf{0}$, $\mathbf{h} \cdot \partial_t \mathbf{m} - \mathbf{m} \cdot \partial_t \mathbf{h} = \mathbf{0}$. Usando le seconde espressioni, si può riscrivere l'equazione dell'energia del campo elettromagnetico come

$$\begin{aligned}
  \partial_t \left( \frac{1}{2} \mathbf{e} \cdot \mathbf{d} + \frac{1}{2} \mathbf{b} \cdot \mathbf{h} \right) + \nabla \cdot \left( \mathbf{e} \times \mathbf{h} \right) & = - \ \mathbf{e} \cdot \mathbf{j} \ + \\
   & \quad - \frac{1}{2} \left[ \mathbf{e} \cdot \partial_t \mathbf{p} - \mathbf{p} \cdot \partial_t \mathbf{e} + \mu_0 \left(  \mathbf{h} \cdot \partial_t \mathbf{m} - \mathbf{m} \cdot \partial_t \mathbf{h} \right) \right]
\end{aligned}$$

o, usando le definizioni di densità di energia elettromagnetica $u$ e vettore di Poynting $\mathbf{s}$,

$$
  \partial_t u + \nabla \cdot \mathbf{s} =
    - \ \mathbf{e} \cdot \mathbf{j} \
    - \frac{1}{2} \left[ \mathbf{e} \cdot \partial_t \mathbf{p} - \mathbf{p} \cdot \partial_t \mathbf{e} + \mu_0 \left(  \mathbf{h} \cdot \partial_t \mathbf{m} - \mathbf{m} \cdot \partial_t \mathbf{h} \right) \right]
$$


```

