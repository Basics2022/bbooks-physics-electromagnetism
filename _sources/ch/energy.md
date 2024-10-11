```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```

(classical-electromagnetism:energy)=
# Bilancio di energia

$$\begin{aligned}
\dfrac{\partial u}{\partial t} & = \dfrac{\partial}{\partial t}\left( \frac{1}{2} \mathbf{e} \cdot \mathbf{d} + \mathbf{b} \cdot \mathbf{h} \right) =  \qquad (...) \\
& = \mathbf{e} \cdot \partial_t \mathbf{d} + \mathbf{h} \cdot \partial_t \mathbf{b} = \\
& = \mathbf{e} \cdot (\nabla \times \mathbf{h} - \mathbf{j}) - \mathbf{h} \cdot \nabla \times \mathbf{e} = \\
\end{aligned}$$

Usando l'identità vettoriale 

$$\begin{aligned}
\mathbf{e} \cdot \nabla \times \mathbf{h} - \mathbf{h} \cdot \nabla \times \mathbf{e} & = e_i \varepsilon_{ijk} \partial_j h_k - h_i \varepsilon_{ijk} \partial_j e_k = \qquad (i \rightarrow k, k \rightarrow i)\\
& = e_i \varepsilon_{ijk} \partial_j h_k - h_k \varepsilon_{kji} \partial_j e_i = \\
& = e_i \varepsilon_{ijk} \partial_j h_k + h_k \varepsilon_{ijk} \partial_j e_i = \\
& =  \partial_j (\varepsilon_{ijk} e_i  h_k ) = \\
& =  \partial_j (\varepsilon_{jki} e_i  h_k ) = \\
& = \nabla \cdot (\mathbf{h} \times \mathbf{e})
& = - \nabla \cdot (\mathbf{e} \times \mathbf{h})
\end{aligned}$$

è possibile riscrivere il bilancio di energia come

$$\frac{\partial u }{\partial t} + \nabla \cdot \mathbf{s} = - \mathbf{e} \cdot \mathbf{j} \ ,$$

avendo definito il **vettore di Poynting**

$$\mathbf{s} := - \mathbf{e} \times \mathbf{h} \ ,$$

come flusso di energia per unità di superficie, comparendo sotto l'operazione di divergenza nel bilnacio di energia.

