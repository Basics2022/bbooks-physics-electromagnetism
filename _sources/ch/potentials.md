```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:potentials)=
# Potenziali elettromagnetici

E' possibile dimostrare che il sistema di equazioni di Maxwell e dell'equazione del bilancio della carica elettrica è un sistema sovra-determinato.
In particolare, è possibile dimostrare che, nota la distribuzione di carica e di densità di corrente - considerate come cause generanti il campo elettrico -, date le leggi costitutive del materiale, sono sufficienti 4 incognite per definire le 6 incognite (3 componenti, per due campi vettoriali) del problema.
E' possibile formulare quindi il problema in termini di un potenziale scalare $\varphi$ e un potenziale vettore $\mathbf{a}$ per ottenere, insieme a una condizione di gauge che elimini le due arbitrarietà (irrilevanti ai fini del calcolo dei campi fisici) restanti.

## Potenziale vettore e potenziale scalare

Partendo dalle equazioni di Maxwell si possono definire i potenziali del campo elettromagnetico. Usando l'equazione di Gauss per il campo magnetico si può introdurre il potenziale vettore $\mathbf{a}(\mathbf{r},t)$,

$$0 = \nabla \cdot \mathbf{b} \qquad \rightarrow \qquad \mathbf{b} = \nabla \times \mathbf{a} \ ,$$

poiché la divergenza di un rotore è identicamente nulla. Introducendo questa relazione nell'equazione di Faraday-Newumann-Lenz, nell'ipotesi di sufficiente regolarità dei campi che consenta di invertire l'ordine delle derivate,

$$0 = \nabla \times \mathbf{e} + \partial_t \mathbf{b} = \nabla \times \mathbf{e} +  \partial_t \nabla \times \mathbf{a} = \nabla \times (\mathbf{e} + \partial_t \mathbf{a}) \qquad \rightarrow \qquad \mathbf{e} + \partial_t \mathbf{a} = - \nabla \varphi \ ,$$

poichè il rotore di un gradiente è identicamente nulla. Le grandezze "fisiche" campo elettrico $\mathbf{e}(\mathbf{r},t)$ e campo magnetico $\mathbf{b}(mathbf{r},t)$ possono quindi essere scritte usando i pootenziali elettromagnetici come

$$\begin{cases}
 \mathbf{e} & = - \nabla \varphi - \partial_t \mathbf{a} \\
 \mathbf{b} & = \nabla \times \mathbf{a} \\
\end{cases}$$

## Gauge

I potenziali sono definiti a meno di una condizione di gauge, un'ulteriore condzione che elimina ogni arbitrarietà nella definizione.
Ad esempio, il potenziale vettore è definito a meno del gradiente di una funzione scalare, poiché $\nabla \times \nabla f \equiv \mathbf{0}$, e quindi il potenziale $\tilde{\mathbf{a}} = \mathbf{a} + \nabla f$ produce lo stesso campo magnetico $\mathbf{b}$

$$\nabla \times \tilde{\mathbf{a}} = \nabla \times (\mathbf{a} + \nabla f) = \nabla \times \mathbf{a} \ .$$

**Condizione di gauge di Lorentz.** Per motivi che saranno più evidenti nella sezione sulle [onde elettromagnetiche](classical-electromagnetism:waves), una condizione di gauge conveniente è

$$\nabla \cdot \mathbf{a} + \frac{1}{c^2} \partial_t \varphi = 0$$

**Condizione di gauge di Coulomb.**

$$\nabla \cdot \mathbf{a} = 0$$




