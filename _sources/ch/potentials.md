```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:potentials)=
# Potenziali elettromagnetici

Partendo dalle equazioni di Maxwell, e in particolare dall'equazione di Gauss per il campo magnetico e dall'equazione di Faraday, si possono definire i potenziali elettrici.

$$0 = \nabla \cdot \mathbf{b} \qquad \rightarrow \qquad \mathbf{b} = \nabla \times \mathbf{a}$$

$$0 = \nabla \times \mathbf{e} + \partial_t \mathbf{b} = \nabla \times \mathbf{e} + \nabla \times \partial_t \mathbf{a} \qquad \rightarrow \qquad \mathbf{e} + \partial_t \mathbf{a} = \nabla \varphi$$

E' quindi possibile esprimere il campo elettrico e il campo magnetico come

$$\begin{aligned}
 \mathbf{e} & = \nabla \varphi - \partial_t \mathbf{a} \\
 \mathbf{b} & = \nabla \times \mathbf{a} \\
\end{aligned}$$

I potenziali sono definiti a meno di una condizione di gauge, un'ulteriore condzione che elimina ogni arbitrarietà nella definizione.
Ad esempio, il potenziale vettore è definito a meno del gradiente di una funzione scalare, poiché $\nabla \times \nabla f \equiv \mathbf{0}$, e quindi il potenziale $\tilde{\mathbf{a}} = \mathbf{a} + \nabla f$ produce lo stesso campo magnetico $\mathbf{b}$

$$\nabla \times \tilde{\mathbf{a}} = \nabla \times (\mathbf{a} + \nabla f) = \nabla \times \mathbf{a} \ .$$

**Condizione di gauge di Lorentz.** Per motivi che saranno più evidenti nella sezione sulle [onde elettromagnetiche](classical-electromagnetism:waves), una condizione di gauge conveniente è

$$\nabla \cdot \mathbf{a} + \frac{1}{c^2} \partial_t \varphi = 0$$

**Condizione di gauge di Coulomb.**

$$\nabla \cdot \mathbf{a} = 0$$




