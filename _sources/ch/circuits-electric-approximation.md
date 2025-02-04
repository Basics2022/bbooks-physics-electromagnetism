<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:circuits-electric:approximation)=
# Validità dell'approccio circuitale

L'approccio circuitale consente di ridurre il problema elettromagnetico, in generale un problema di campo che richiede la soluzione di PDE, a un approccio "ai morsetti" **todo**, che richiede la soluzione di ODE.

Una rivisitazione dell'[equazione dell'energia](classical-electromagnetism:energy) permette di valutare i regimi in cui è possibile usare un approccio circuitale a un sistema elettromagnetico.

In particolare, nell'equazione di bilancio dell'energia elettromagnetica

$$\dfrac{d}{dt} \int_V u = \oint_{\partial V} \mathbf{s} \cdot \hat{\mathbf{n}} - \int_V \mathbf{j} \cdot \mathbf{e} \ ,$$

viene indagato il termine di flusso alla frontiera, ricordando la definizione di vettore di Poynting $\mathbf{s} := \mathbf{e} \times \mathbf{h}$, e riscrivendo i campi elettrico e magnetico in funzione dei potenziali elettromagnetici, $\mathbf{b} = \nabla \times \mathbf{a}$, $\mathbf{e} = - \nabla \varphi - \partial_t \mathbf{a} \ ,$

$$\begin{aligned}
  - \oint_{\partial V} \mathbf{s} \cdot \mathbf{\hat{n}}
  & = - \oint_{\partial V} \left(\mathbf{e} \times \mathbf{h} \right) \cdot \mathbf{\hat{n}} = \\
  & =   \oint_{\partial V} \left(\nabla \varphi + \partial_t \mathbf{a} \right) \times \mathbf{h}  \cdot \mathbf{\hat{n}} = \\
  & = ... \\
  & = \underbrace{\oint_{\partial V} \hat{\mathbf{n}} \cdot \nabla \times ( \varphi \mathbf{h} )}_{=0 \text{ (Stokes'thm **todo** check)}} - \oint_{\partial V} \varphi \hat{\mathbf{n}} \cdot \underbrace{\nabla \times \mathbf{h}}_{\partial_t \mathbf{d} + \mathbf{j}} + \oint_{\partial V} \hat{\mathbf{n}} \cdot \partial_t \mathbf{a} \times \mathbf{h} = \\
  & = - \oint_{\partial V} \varphi \mathbf{j} \cdot \hat{\mathbf{n}} - \oint_{\partial V} \hat{\mathbf{n}} \cdot \left( \partial_t \mathbf{d} + \mathbf{h} \times \partial_t \mathbf{a} \right) \ , 
\end{aligned}$$

e assumendo che il flusso di carica elettrica avvenga solo in corrispondenza di un numero finito di sezioni $S_k \in \partial V$ equipotenziali a potenziale $v_k = -\varphi_k$, costante sulle sezioni, e riconoscento il flusso di carica elettrica attraverso la sezione $S_k$ come la corrente $i_k = \int_{S_k} \mathbf{j} \cdot \hat{\mathbf{n}}$, si può scrivere

$$- \oint_{\partial V} \mathbf{s} \cdot \hat{\mathbf{n}} = \sum_k v_k \, i_k - \oint_{\partial V} \hat{\mathbf{n}} \cdot \left( \partial_t \mathbf{d} + \mathbf{h} \times \partial_t \mathbf{a} \right) \ .$$

Il bilancio di energia elettromagnetica del sistema può quindi essere riscritto come

$$\frac{d}{dt} \int_V u = \sum_k v_k \, i_k - \int_{V} \mathbf{j} \cdot \mathbf{e} - \oint_{\partial V} \hat{\mathbf{n}} \cdot \left( \partial_t \mathbf{d} + \mathbf{h} \times \partial_t \mathbf{a} \right) \ .$$

Nelle condizioni in cui l'ultimo termine è nullo o trascurabile (**todo** *quali? Spendere due parole sulla validità dell'approssimazione, con analisi dimensionale? Fare esempio in cui l'approssimazione non funziona*), la variazione di energia interna al sistema è dovuta alla differenza della potenza in ingresso ai morsetti, e la dissipazione all'interno del volume (ad esempio dovuta alla conduzione non ideale in conduttori con resistività finita),

$$\dot{E}^{em} = P^{ext, vi} - \dot{D} \ ,$$

con $\dot{D} \ge 0$ per il secondo principio della termodinamica **todo** *aggiungere riferimento, e discussione.*


