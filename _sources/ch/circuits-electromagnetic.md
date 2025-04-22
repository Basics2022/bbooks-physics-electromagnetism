<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:circuits-electromagnetic)=
# Circuiti elettromagnetici

Sotto opportune ipotesi è possibile usare un modello circuitale anche per sistemi elettromagnetici, come ad esempio i trasformatori, o i motori elettrici.

- legge di Gauss per il campo magnetico

  $$\nabla \cdot \mathbf{b} = 0$$

- legge di Ampére-Maxwell

  $$\nabla \times \mathbf{h} - \partial_t \mathbf{d} = \mathbf{j}$$

Si aggiungono le seguenti ipotesi:
- materiali lineari non-dissipativi e non-dispersivi $\mathbf{b} = \mu \mathbf{h}$ <span style="color:red">**todo** discutere questa ipotesi, insieme a isteresi materiali, cicli di magnetizzazione,...</span>.
- variazioni del campo $\mathbf{d}$ nel tempo trascurabili, $\partial_t \mathbf{d} = \mathbf{0}$.

La legge di Gauss del campo magnetico in forma integrale permette di scrivere la **legge ai nodi** del flusso del campo magnetico per i circuiti magnetici,

$$0 = \oint_{\partial V} \mathbf{b} \cdot \hat{\mathbf{n}} = \sum_k \phi_k \ .$$

La legge di Ampére-Maxwell in forma integrale considerando:
- un percorso incatenato con il solo induttore
  
  $$\int_{\ell_{ind}} \mathbf{h} \cdot \hat{\mathbf{t}} + \int_{\ell_{12}} \mathbf{h} \cdot \hat{\mathbf{t}} = \oint_{\ell_{1}} \mathbf{h} \cdot \hat{\mathbf{t}} = \int_{S^{ind}} \mathbf{j} \cdot \hat{\mathbf{n}} =  N i =: m$$

- un percorso incatenato con il traferro, aggirando l'induttore
  
  $$0 = \int_{\ell_{traf}} \mathbf{h} \cdot \hat{\mathbf{t}} + \int_{\ell_{21}} \hat{h} \cdot \hat{\mathbf{t}} = \sum_{k} h_k \ell_k + \int_{\ell_{21}} \hat{h} \cdot \hat{\mathbf{t}}$$

e sommando le due equazioni, riconoscendo che i due integrali di linea sullo stesso percorsoin versi opposti si annullano, si ottiene la **legge alle maglie** per i circuiti magnetici

$$\begin{aligned}
  m & = \int_{\ell_{ind}} \mathbf{h} \cdot \hat{\mathbf{t}} + \int_{\ell_{traf}} \mathbf{h} \cdot \hat{\mathbf{t}} = \\
    & \approx \sum_{k \in \ell} h_k \, \ell_k 
      = \sum_{k \in \ell} \frac{b_k}{\mu_k} \, \ell_k 
      = \sum_{k \in \ell} \frac{\ell_k}{\mu_k \, A_k} \, \phi_k  \ .
\end{aligned}$$

Le leggi di Kirchhoff per i circuiti magnetici sono quindi

$$\begin{cases}
  \sum_{k \in N_j} \phi_k = 0 \\ \\
  m_{\ell_i} = \sum_{k \in \ell_i} \theta_k \phi_k \ ,
\end{cases}$$

avendo introdotto la riluttanza $\theta_k = \frac{\ell_k}{\mu_k \, A_k}$, l'inverso della permeanza $\Lambda_k = \theta_k^{-1}$.



