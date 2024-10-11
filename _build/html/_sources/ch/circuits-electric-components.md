```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:circuits-electric:components)=
# Componenti elementari dei circuiti elettrici

## Resistore ohmico
Un resistore di Ohm risulta dall'approssimazione circuitale di un materiale con equazione costitutiva lineare 

$$\mathbf{e} = \rho_R \, \mathbf{j} \ ,$$

tra il campo elettrico $\mathbf{e}$ e la densità di corrente $\mathbf{j}$, tramite la costante di proporzionalità $\rho_R$, la **resistività** del materiale. La corrente elettrica attraverso una sezione del componente è definita come il flusso di carica attraverso una sua sezione

$$i = \int_S \mathbf{j} \cdot \hat{\mathbf{t}} \simeq j \, A \ ,$$

Nell'ipotesi che il vettore densità di corrente si allineato con l'asse del componente e uniforme sulla sezione $A$, "piccola".
Se il materiale non è in grado di accumulare carica, il bilancio di carica elettrica si traduce nella continuità della corrente elettrica attraverso le sezioni del conduttore.

Utilizzando l'equazione costitutiva su un elemento di lunghezza elementare $d\mathbf{r} =\hat{\mathbf{t}} \, d \ell $, e assumendo che il campo elettrico sia allineato con l'asse del componente, $\mathbf{e} = e \hat{\mathbf{t}}$ si può scrivere il lavoro elementare per unità di carica come

$$\delta v = \mathbf{e} \cdot d \mathbf{r} =  e \, d\ell = \rho_R \, j \, d\ell =  \frac{\rho_R \, d\ell}{A} i \ .$$

Da questa ultima equazione seguono le due leggi di Ohm, per resistori lineari.

**Prima legge di Ohm.** La differenza di potenziale tra due sezioni di un resistore lineare è proporzionale alla corrente che passa attraverso di esso,

  $$\delta v = dR \, i \ .$$

**Seconda legge di Ohm.** La costante di proporzionalità che lega la differenza di potenziale e la corrente all'interno di un resistore ohmico, la **resistenza** del resistore, è proporzionale alla resistività e alla lunghezza del resistore, e inversamente proporzionale alla sua sezione,

  $$dR = \frac{\rho_R \ d\ell}{A} \ .$$

Se le proprietà sono uniformi nel resistore, si possono integrare le relazioni elementari per ottenere la relazione tra grandezze finite,

$$\Delta V = R \, i $$
$$R = \frac{\rho_R \ \ell}{A}$$

**todo** (perché si può usare il potenziale? Nelle mie note avevo usato il simbolo $v^*$, come se fosse una definizione leggermente diversa per incorporare movimento e instazionarietà, che si riduce a $v$ nel caso stazionario).

**Condensatore.**

**Induttore.**

**Generatore di tensione.**

**Generatore di corrente.**
