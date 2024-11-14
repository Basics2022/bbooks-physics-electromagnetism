```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:energy)=
# Bilancio di energia del campo elettromagnetico

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

```{dropdown} Procedimento alternativo (e più generale?)
:open:

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

