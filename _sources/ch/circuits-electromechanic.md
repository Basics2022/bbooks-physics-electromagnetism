```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:circuits-electromechanic)=
# Circuiti elettromeccanici

Alcuni sistemi di interesse e di enorme diffusione nella società moderna sfruttano le interazioni tra componenti fenomeni elettromagnetici e meccanici: un esempio fondamentale sono le macchine elettriche, alcune delle quali possono operare sia come motore (con la potenza fornita dal sistema elettrico e convertita in potenza meccanica) sia come generatore di energia elettrica (convertendo potenza meccanica in potenza elettrica). 

In un sistema di induttori con mutua influenza, la differenza di tensione ai capi dell'induttore "potenziato" $i$ è

$$v_i = \dot{\psi}_i = \dfrac{d}{dt} \left( N_i \, \phi_i \right) \ .$$

Il flusso concatenato dipende dall'effetto di tutti gli induttori del sistema (e del campo magnetico generato da eventuali cause esterne al sistema),

$$\phi_i = \sum_{k} \phi_{ik} = \sum_{k} \frac{1}{\theta_{ik}} \, m_k \ ,$$

avendo indicato con $\theta_{ik}$ la riluttanza del circuito tra l'induttore potenziante $k$ e l'induttore potenziato $i$. Usando l'espressione della forza magneto-motrice $m_k = N_k \, i_k$, si può riscrivere l'espressione della differenza di tensione

$$v_i = \sum_k \frac{d}{dt} \left( \frac{N_i \, N_k}{\theta_{ik}} i_k \right) = \sum_k \frac{d}{dt} \left( L_{ik} \, i_k \right) \ .$$

In genereale, in circuiti elettromeccanici le riluttanze non sono dei parametri costanti del sistema ma dipendono dallo stato "meccanico" del sistema, descritto qui dalle variabili $\mathbf{x}$,

$$v_i = \sum_k \frac{d}{dt} \left( \frac{N_i \, N_k}{\theta_{ik}(\mathbf{x})} i_k \right) = \sum_k \frac{d}{dt} \left( L_{ik} (\mathbf{x}) \, i_k \right) \ .$$

$$\mathbf{v}(t) = \dfrac{d}{dt} \Big( \mathbf{L}(\mathbf{x}(t)) \, \mathbf{i}(t) \Big) \ .$$

La matrice di induttanza $\mathbf{L}$ è simmetrica **todo** *Dimostrazione*

## Sistemi elettromeccanici conservativi
Le equazioni che governano il sistema elettromeccanico, senza condensatori, in generale possono essere scritte come

$$\begin{cases}
 \mathbf{M} \ddot{\mathbf{x}} + \mathbf{D} \dot{\mathbf{x}} + \mathbf{K} \mathbf{x} = \mathbf{f}^{ext} + \mathbf{f}^{em} \\
 \dfrac{d}{dt} \left( \mathbf{L} \mathbf{i} \right) + \mathbf{R} \mathbf{i} = \mathbf{e}
\end{cases}$$

In termini di energia,

$$
0 = \dot{\mathbf{x}}^T \left[ \mathbf{M} \ddot{\mathbf{x}} + \mathbf{D} \dot{\mathbf{x}} + \mathbf{K} \mathbf{x} - \mathbf{f}^{ext} - \mathbf{f}^{em} \right] + \mathbf{i}^T \left[ \dfrac{d}{dt} \left( \mathbf{L} \mathbf{i} \right) + \mathbf{R} \mathbf{i} - \mathbf{e} \right]
$$

Nel caso di matrici di massa, smorzamento e rigidzza costanti, e usando la derivata del prodotto per ottenere un termine di derivata dell'energia degli induttori sfruttando la simmetria di $\mathbf{L}$,

$$ \begin{aligned}
\dfrac{d}{dt} \left[ \frac{1}{2} \mathbf{i}^T \mathbf{L} \mathbf{i} \right] 
  & = \mathbf{i}^T \dfrac{d}{dt} \left( \mathbf{L} \, \mathbf{i} \right) + \frac{1}{2} \mathbf{i}^T \dfrac{d \mathbf{L}}{dt} \mathbf{i} = \\
  & = \mathbf{i}^T \dfrac{d}{dt} \left( \mathbf{L} \, \mathbf{i} \right) + \sum_{a} \frac{1}{2} \mathbf{i}^T \dfrac{\partial \mathbf{L}}{\partial x_a} \mathbf{i} \, \dot{x}_a = \\
  & = \mathbf{i}^T \dfrac{d}{dt} \left( \mathbf{L} \, \mathbf{i} \right) + \nabla \left( \frac{1}{2} \mathbf{i}^T \mathbf{L} \mathbf{i} \right) \dot{\mathbf{x}}  \ .
\end{aligned}$$ (classical-electromagnetism:circuits-electromechanic:energy-mech-0)

si può scrivere un'equazione di bilancio dell'energia meccanica macroscopica, $E^{mec, int}$

$$
0 & = \dfrac{d}{dt} \left[ \dfrac{1}{2} \dot{\mathbf{x}}^T \mathbf{M} \dot{\mathbf{x}} + \dfrac{1}{2} \mathbf{x}^T \mathbf{K} \mathbf{x} + \dfrac{1}{2} \mathbf{i}^T \mathbf{L} \mathbf{i} \right] - \dot{\mathbf{x}}^T \left( \mathbf{f}^{em} - \nabla E^{ind}(\mathbf{x}, \mathbf{i})  \right) + \\
  & - \dot{\mathbf{x}}^T \mathbf{f}^{ext} - \mathbf{i}^T \mathbf{e} + \\
  & + \dot{\mathbf{x}}^T \mathbf{C} \dot{\mathbf{x}} + \mathbf{i}^T \mathbf{R} \mathbf{i} \ .
$$ 

Nell'ipotesi che il processo sia conservativo, si ricava la forma delle forze dovute ai fenomeni elettromagnetici,

$$\mathbf{f}^{em} = \nabla_{\mathbf{x}} E^{ind}(\mathbf{x}, \mathbf{i}) \ .$$ (classical-electromagnetism:circuits-electromechanic:f-em)


## Equazioni di governo
Usando l'espressione {eq}`classical-electromagnetism:circuits-electromechanic:f-em` delle azioni meccaniche dovute agli effetti elettromagnetici, del sistema sono

$$\begin{cases}
  \mathbf{M} \ddot{\mathbf{x}} + \mathbf{D} \dot{\mathbf{x}} + \mathbf{K} \mathbf{x} - \nabla_{\mathbf{x}} E^{ind}(\mathbf{x}, \mathbf{i})  = \mathbf{f}^{ext} \\
  \frac{d}{dt} \left( \mathbf{L}(\mathbf{x}) \mathbf{i} \right) + \mathbf{R} \mathbf{i} = \mathbf{e}
\end{cases}$$

o nel caso generale

$$\begin{cases}
  \mathbf{M} \ddot{\mathbf{x}} - \nabla_{\mathbf{x}} E^{ind} ( \mathbf{x}, \mathbf{i}) = \mathbf{f}^{ext} \\
  \frac{d}{dt} \left( \mathbf{L}(\mathbf{x}) \mathbf{i} \right) + \mathbf{R} \mathbf{i} = \mathbf{e}
\end{cases}$$


## Bilancio energetico

### Energia meccanica macroscopica
Usando l'espressione {eq}`classical-electromagnetism:circuits-electromechanic:f-em` delle azioni meccaniche dovute ai fenomeni elettromagnetici, si può riscrivere la relazione {eq}`classical-electromagnetism:circuits-electromechanic:energy-mech-0`, come un bilancio di energia meccanica macroscopica del sistema,

$$\dfrac{d}{dt} \left[ \dfrac{1}{2} \dot{\mathbf{x}}^T \mathbf{M} \dot{\mathbf{x}} + \dfrac{1}{2} \mathbf{x}^T \mathbf{K} \mathbf{x} + \dfrac{1}{2} \mathbf{i}^T \mathbf{L} \mathbf{i} \right] = \dot{\mathbf{x}}^T \mathbf{f}^{ext} + \mathbf{i}^T \mathbf{e} - \dot{\mathbf{x}}^T \mathbf{D} \dot{\mathbf{x}} - \mathbf{i}^T \mathbf{R} \mathbf{i} \ , $$

e quindi

$$\dot{E}^{mec} = P^{ext} - \dot{D} \ .$$

### Energia cinetica
L'energia meccanica macroscopica può essere scritta come la somma dell'energia cinetica e dell'energia potenziale interna del sistema, $E^{mec} = K + V^{int}$. La derivata nel tempo dell'energia potenziale delle azioni interne è l'opposto della potenza delle azioni interne conservative; la dissipazione è l'opposto della potenza delle azioni interne non-conservative. La potenza complessiva delle azioni interne può quindi essere scritta come

$$P^{int} = P^{int, c} + P^{int, nc} = - \dot{V}^{int} - \dot{D} \ ,$$

$$\dot{K} = \dot{E}^{mec} - \dot{V}^{int} = P^{ext} \underbrace{- \dot{D} - \dot{V}^{int}}_{=P^{int}} \  $$

### Energia totale
Il primo principio della termodinamica fornisce l'equazione di bilancio dell'energia totale di un sistema chiuso,

$$\dot{E}^{tot} = P^{ext} + \dot{Q}^{ext} \ .$$

### Energia interna
L'energia interna di un sistema è definita come la differenza dell'energia totale e dell'energia cinetica macroscopica, $E := E^{tot} - K$. L'equazione di bilancio dell'energia interna di un sistema chiuso è

$$\dot{E} = Q^{ext} - P^{int} \ .$$

### Energia interna termica (microscopica)
Se si definisce l'energia interna termica, corrispondente all'energia cinetica associata alle dinamiche microscopiche, come differenza tra energia interna e energia potenziale interna, $E^{th} = E - V^{int}$, l'equazione di bilancio dell'energia interna termica è

$$   \dot{E}^{th} = \dot{Q}^{ext} + \dot{D} \ . $$

```{dropdown} Dimostrazione
$$\begin{aligned}
  \dot{E}^{th} = \dot{E} - V^{int}
    & = \dot{Q}^{ext} - P^{int} - V^{int} = \\
    & = \dot{Q}^{ext} + \dot{D} + \dot{V}^{int} - \dot{V}^{int} = \\
    & = \dot{Q}^{ext} + \dot{D} \ .
\end{aligned}$$
```


**Con condensatori.** **todo**
```{dropdown} Equazioni
- **Leggi ai nodi.**

  $$0 = \sum_{k \in B_j} \alpha_{jk} \, i_{jk}$$

  $$\mathbf{A} \mathbf{i} = \mathbf{0}$$

- **Differenza di potenziale nodi-lati.**

  $$\mathbf{A}^T \mathbf{v}_{n} = \mathbf{v}$$

- **Nodo a terra.**

  $$\mathbf{v}_{\perp} = \mathbf{v}_0 \ .$$ 

- **Equazioni costitutive.**

  $$\begin{aligned}
    \mathbf{0} & = \mathbf{v}_R - \mathbf{R} \mathbf{i}_R & \text{resistenze} \\
    \mathbf{0} & = \mathbf{v}_L - \frac{d}{dt} \left( \mathbf{L} \mathbf{i}_L \right) & \text{induttanze} \\
    \mathbf{0} & = \frac{d}{dt} \left( C \mathbf{v}_C \right) - \mathbf{i}_C & \text{condensatori} \\
  \end{aligned}$$
```





