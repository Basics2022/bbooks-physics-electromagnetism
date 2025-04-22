<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:circuits-electric:induction)=
# Induzione elettromagnetica nell'approssimazione circuitale

E' possibile applicare l'approssimazione circuitale anche in presenza di regioni in cui non è possibile trascurare il termine $\partial_t \mathbf{b}$, come ad esempio circuiti elettromagnetici che coinvolgono trasformatori e/o motori o generatori elettrici.

In queste situazioni, se è possibile identificare una regione $V_0$ dello spazio connessa nella quale il termine $\partial_t \mathbf{b} = \mathbf{0}$, e quindi $\nabla \times \mathbf{e} = \mathbf{0}$, in $V_0$ è possibile definire il campo elettrico in termini di un potenziale $\varphi$,

$$\mathbf{e} = - \nabla \varphi \qquad , \qquad \mathbf{r} \in V_0 \ .$$

E' possibile calcolare le differenze di potenziale ai morsetti di un sistema in cui $\delta_t \mathbf{b} \ne 0$, racchiuso nel volume $V_k$, con la legge di Faraday,

$$\oint_{\ell_k} \mathbf{e} \cdot \hat{\mathbf{t}} = - \frac{d}{dt} \int_{S_k} \mathbf{b} \cdot \hat{\mathbf{n}} \ ,$$

dove il percorso chiuso $\ell_k = \ell_k^{cond} \cup \ell_k^{mors}$ descrive il conduttore in $V_k$ chiuso dalla linea geometrica tra i morsetti. Se si può trascurare la resistività del conduttore in $V_k$, $\int_{\ell_k^{cond}} \mathbf{e} \cdot \hat{\mathbf{t}} = 0$, la differenza di tensione ai morsetti vale

$$\Delta v_k = \int_{\ell^{mors}_k} \mathbf{e} \cdot \hat{\mathbf{t}} = - \frac{d}{dt} \int_{S_k} \mathbf{b} \cdot \hat{\mathbf{n}}$$



