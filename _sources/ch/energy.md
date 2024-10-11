```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:energy)=
# Bilancio di energia

Ispirati dalle dimensioni fisiche dei campi elettromagnetici,

$$\begin{aligned}
[\mathbf{e}] = \frac{\text{force}}{\text{charge}} \qquad & , \qquad
<!--$$[\varepsilon] = \frac{\text{charge}^2}{\text{force} \cdot \text{length}^2} = \frac{C^2}{N \ m^2}$$-->
[\mathbf{d}] = \frac{\text{charge}}{\text{length}^2} \\
[\mathbf{b}] = \frac{\text{force}\cdot\text{time}}{\text{charge}\cdot\text{length}} \qquad & , \qquad
<!--$$[\mu] = \frac{\text{charge}^2}{\text{force} \cdot \text{length}^2} = \frac{C^2}{N \ m^2}$$-->
[\mathbf{h}] = \frac{\text{charge}}{\text{time} \cdot \text{length}}
\end{aligned}$$

$$\begin{aligned}
[\mathbf{e} \cdot \mathbf{d}] & = \frac{\text{force}}{\text{length}^2} = \frac{\text{energy}}{\text{length}^3} = [u] \\
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

dove è stato definito il **vettore di Poynting**, o meglio il campo vettoriale di Poynting

$$\mathbf{s}(\mathbf{r},t) := - \mathbf{e}(\mathbf{r},t) \times \mathbf{h}(\mathbf{r},t) \ ,$$

che può essere identificato come un flusso di potenza per unità di superficie, comparendo sotto l'operatore di divergenza nel bilnacio di energia.

**todo.** Rimandare a una sezione in cui si mostra questa ultima affermazione passando dal bilancio differenziale al bilancio integrale e si usa il teorema della divergenza, $\int_V \nabla \cdot \mathbf{s} = \oint_{\partial V} \mathbf{s} \cdot \hat{\mathbf{n}}$.

