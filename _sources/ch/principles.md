```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:principles)=
# Princìpi dell'elettromagnetismo classico

I progressi nello studio dei fenomeni elettromagnetici nel XIX secolo, permisero a James Clerk Maxwell di formulare quelle che oggi sono note con il nome di *equazioni di Maxwell* e possono essere considerate la prima formulazione consistente dei principi dell'elettromagnetismo classico, insieme alla legge di bilancio della carica e all'espressione della forza di Lorentz su una carica elettrica immersa in un campo elettromagnetico.

I principi in forma differenziale possono essere ricavati dai principi in forma integrale, più generici, se i campi soddisfano le necessarie condizioni di regolarità minima, che qualitativamente si possono enunciare come "tutte le operazioni svolte devono avere senso".

## Prinicipi in forma differenziale
**Conservazione della carica elettrica.**

$$\partial_t \rho + \nabla \cdot \mathbf{j} = 0 \ .$$

**Equazioni di Maxwell.**

$$\begin{cases}
 \nabla \cdot \mathbf{d} = \rho \\
 \nabla \times \mathbf{e} + \partial_t \mathbf{b} = \mathbf{0} \\ 
 \nabla \cdot \mathbf{b} = 0 \\
 \nabla \times \mathbf{h} - \partial_t \mathbf{d} = \mathbf{j} \\
\end{cases}$$

con la necessità di definire delle equazioni costitutive $\mathbf{d}(\mathbf{e}, \mathbf{b})$, $\mathbf{h}(\mathbf{e}, \mathbf{b})$.

**Forza di Lorentz.** La forza per unità di volume agente sulla carica elettrica presente in un punto $\mathbf{r}$ nello spazio è

$$\begin{aligned}
  \mathbf{f}(\mathbf{r},t) & = \rho(\mathbf{r},t) \, \mathbf{e}(\mathbf{r},t) - \mathbf{j}(\mathbf{r},t) \times \mathbf{b}(\mathbf{r},t) = \\
                           & = \rho(\mathbf{r},t) \left[ \mathbf{e}(\mathbf{r}) - \mathbf{v}(\mathbf{r},t) \times \mathbf{b}(\mathbf{r},t) \right] =  \\
                           & = \rho(\mathbf{r},t) \, \mathbf{e}^*(\mathbf{r},t) 
\end{aligned}$$

**todo.** controllare questa formula


## Principi in forma integrale: equazioni dell'elettromagnetismo e relatività galileiana

### Integrazione su volumi di controllo

La forma integrale dei principi dell'elettromagnetismo per volumi $V$ e superfici $S$ fissi nello spazio viene ricavata integrando le equazioni differenziali sui domini e usando il teorema della divergenza per ottenere termini di flusso, e il teorema del rotore per ottenere termini di circuitazione.

**Continuità della carica elettrica.**

$$
    \dfrac{d}{dt} \int_{V} \rho + \oint_{\partial V} \mathbf{j} \cdot \hat{\mathbf{n}}
$$

**Legge di Gauss per il campo $\mathbf{d}(\mathbf{r},t)$.**

$$
    \oint_{\partial V} \mathbf{d} \cdot \mathbf{\hat{n}} = \int_{V} \rho
$$

**Legge di Gauss per il campo $\mathbf{b}(\mathbf{r},t)$.**

$$
    \oint_{\partial V} \mathbf{b} \cdot \mathbf{\hat{n}} = 0
$$

**Legge di Faraday-Neumann-Lenz, per l'induzione elettromagnetica.**

$$
    \oint_{\partial S} \mathbf{e} \cdot \hat{\mathbf{t}} + \dfrac{d}{dt} \int_{S} \mathbf{b} \cdot \hat{\mathbf{n}} = \mathbf{0}
$$

**Legge di Ampére-Maxwell.**

$$
    \oint_{\partial S} \mathbf{h} \cdot \hat{\mathbf{t}} - \dfrac{d}{dt} \int_{S} \mathbf{b} \cdot \hat{\mathbf{n}} = \int_{S} \mathbf{j} \cdot \hat{\mathbf{n}} \ .
$$


### Integrazione su volumi arbitrari
Integrando su volumi e superfici in moto arbitario, si può ricavare la forma integrale dei princìpi dell'elettromagnetismo

**Equazione di continuità per la carica elettrica**

$$
    \dfrac{d}{dt} \int_{v_t}  \rho = \oint_{\partial v_t} \underbrace{\rho (\mathbf{u} - \mathbf{u}_b)}_{\mathbf{j}^*} \cdot \mathbf{\hat{n}}
$$

**Legge di Gauss per il campo $\mathbf{d}(\mathbf{r})$**

$$
    \oint_{\partial v_t} \mathbf{d} \cdot \mathbf{\hat{n}} = \int_{v_t} \rho
$$

**Legge di Gauss per il campo $\mathbf{b}(\mathbf{r})$**

$$
    \oint_{\partial v_t} \mathbf{b} \cdot \mathbf{\hat{n}} = 0
$$

**Legge di Faraday--Neumann--Lenz**

$$
\begin{aligned}
    0 & = \oint_{\partial s_t} \mathbf{e} \cdot \mathbf{\hat{t}} + \dfrac{d}{dt} \int_{s_t} \mathbf{b} \cdot \mathbf{\hat{n}} = \\
      & = \oint_{\partial s_t} \mathbf{e} \cdot \mathbf{\hat{t}} + \int_{s_t} \partial_t \mathbf{b} \cdot \mathbf{\hat{n}} + \oint_{\partial s_t} \mathbf{u}_b \times \mathbf{b} \cdot \mathbf{\hat{t}} = \qquad \text{(...)} \ = \\ 
      & = \int_{s_t} \partial_t \mathbf{b} \cdot \mathbf{\hat{n}} + \oint_{\partial s_t} \left[ \mathbf{e} - \mathbf{b} \times \mathbf{u}_b \right] \cdot \mathbf{\hat{t}} = \\
      & = \int_{s_t} \partial_t \mathbf{b} \cdot \mathbf{\hat{n}} + \oint_{\partial s_t} \mathbf{e}^* \cdot \mathbf{\hat{t}} = \\
\end{aligned}
$$

**Legge di Ampère--Maxwell**

$$
\begin{aligned}
    \oint_{s_t} \mathbf{j} \cdot \mathbf{\hat{n}} & = \oint_{\partial s_t} \mathbf{h} \cdot \mathbf{\hat{t}} - \dfrac{d}{dt} \int_{s_t} \mathbf{d} \cdot \mathbf{\hat{n}} = \\
      & = \oint_{\partial s_t} \mathbf{h} \cdot \mathbf{\hat{t}} - \int_{s_t} \partial_t \mathbf{d} \cdot \mathbf{\hat{n}} - \oint_{\partial s_t} \mathbf{u}_b \times \mathbf{d} \cdot \mathbf{\hat{t}} = \qquad \text{(...)} \ = \\ 
      & = \int_{s_t} \partial_t \mathbf{d} \cdot \mathbf{\hat{n}} + \oint_{\partial s_t} \left[ \mathbf{h} + \mathbf{d} \times \mathbf{u}_b \right] \cdot \mathbf{\hat{t}} = \\
      & = \int_{s_t} \partial_t \mathbf{d} \cdot \mathbf{\hat{n}} + \oint_{\partial s_t} \mathbf{h}^* \cdot \mathbf{\hat{t}} = \\
\end{aligned}
$$

**Forza di Lorentz**

$$\begin{aligned}
  \mathbf{F} = q \left( \mathbf{e} - \mathbf{u} \times \mathbf{b} \right) = q \, \mathbf{e}^*
\end{aligned}$$



- Equazioni di Maxwell:

    $$
        \begin{cases}
            &  \Phi_{\partial V^*}(\mathbf{d}^*) = Q_{V^*}^{int} \\
            &  \Gamma_{\partial S^*}(\mathbf{e}^*) + \dfrac{d}{dt}\Phi_{S^*}(\mathbf{b}^*) = 0 \\
            &  \Phi_{\partial V^*}(\mathbf{b}^*) = 0 \\
            &  \Gamma_{\partial S^*}(\mathbf{h}^*) - \dfrac{d}{dt}\Phi_{S^*}(\mathbf{d}^*) = \Phi_{S^*}(\mathbf{j}) \\
        \end{cases}
    $$

- continuità della carica elettrica

    $$
        \dfrac{d}{dt} Q_{V^*}^{int} + \Phi_{\partial V^*}(\mathbf{j}^*) = 0
    $$


