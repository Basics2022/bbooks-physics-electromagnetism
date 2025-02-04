<!--
```{article-info}
:author: basics
:date: "{sub-ref}`today`"
:read-time: "{sub-ref}`wordcount-minutes` min read"
```
-->

(classical-electromagnetism:media)=
# Elettromagnetismo nella materia

**todo**

## Vuoto

I fenomeni elettromagnetici nel vuoto sono governati dalle equazioni di Maxwell nel vuoto,

$$\begin{cases}
\nabla \cdot \mathbf{e} = \frac{\rho}{\varepsilon_0} \\
\nabla \times \mathbf{e} + \partial_t \mathbf{b} = \mathbf{0} \\
\nabla \cdot \mathbf{b} = 0 \\
\nabla \times \mathbf{b} - \mu_0 \varepsilon_0 \partial_t \mathbf{e} = \mu_0 \mathbf{j}
\end{cases}$$

e dall'equazione della continuità della carica elettrica,

$$\partial_t \rho + \nabla \cdot \mathbf{j} = 0 \ .$$

## Mezzi continui

In generale, alcuni materiali rispondono a un campo elettromagnetico "esterno" imposto, con una polarizzazione e una magnetizzazione. In particolare, la polarizzazione elettrica di un materiale corrisponde a una separazione locale delle cariche elettriche dal punto di vista macroscopico equivalente a una densità di volume di dipoli, $\mathbf{p}(\mathbf{r}_0)$; la magnetizzazione corrisponde a un orientamento degli assi delle spire delle correnti amperiane dal punto di vista macroscopico equivalente a una densità di momento magnetico $\mathbf{m}(\mathbf{r}_0)$.


## Polarizzazione

### Singolo dipolo elettrico
Un dipolo elettrico discreto è formato da due cariche elettriche uguali e opposte $q$, $-q$, nei punti $P_+$, $P_- = P_+ \mathbf{l}$, nel limite $q \rightarrow +\infty$, $|\mathbf{l}| \rightarrow 0$ con $q |\mathbf{e}|$ finito.

Il campo elettrico (stazioario **todo** *controllare cosa succede nel caso non stazionario. Magari dopo aver derivato la soluzione generale del problema, come soluzione delle equazioni delle onde  in termini dei potenziali EM*) generato nel punto dello spazio $\mathbf{r}$ da un dipolo elettrico nel punto $\mathbf{r}_0$ viene calcolato come limite del campo elettrico generato da due cariche uguali e opposte $q^{\mp}$ nei punti $\mathbf{r}_0 \mp \frac{\mathbf{l}}{2}$,

$$\mathbf{e}(\mathbf{r}) = -\frac{q}{4 \pi \varepsilon_0} \frac{\mathbf{r} - \left( \mathbf{r}_0 - \frac{\mathbf{l}}{2} \right)}{\left|\mathbf{r} - \left( \mathbf{r}_0 - \frac{\mathbf{l}}{2} \right)\right|^3} + \frac{q}{4 \pi \varepsilon_0} \frac{\mathbf{r} - \left( \mathbf{r}_0 + \frac{\mathbf{l}}{2} \right)}{\left|\mathbf{r} - \left( \mathbf{r}_0 + \frac{\mathbf{l}}{2} \right)\right|^3} \ .$$

Usando la formula per la derivata dei termini

$$\partial_{\ell_k} \frac{x_i \pm \frac{\ell_i}{2}}{\left|\mathbf{x} \pm \frac{\mathbf{l}}{2} \right|^3} = \frac{1}{2} \left[ \pm \frac{\delta_{ik}}{r^3} - 3 r^{-4} \left( \pm \frac{x_k \pm \frac{\ell_k}{2}}{r} \right) \right]$$

$$\left. \partial_{\ell_k} \frac{x_i \pm \frac{\ell_i}{2}}{\left|\mathbf{x} \pm \frac{\mathbf{l}}{2} \right|^3} \right|_{\mathbf{l} = \mathbf{0}} = \mp \frac{1}{2} \left[ - \frac{\delta_{ik}}{|\mathbf{x}|^3} + 3 \left( \frac{x_k}{r^5} \right) \right] = \mp \frac{1}{2} \partial_{r_{0 k}} \frac{r_i - r_{0 i}}{|\mathbf{r} - \mathbf{r}_0|^3} = \mp \frac{1}{2} \nabla_{\mathbf{r}_0} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} $$

si ricava l'apporssimazione al primo ordine in $\mathbf{l}$ dei due termini

$$\begin{aligned}
  \frac{\mathbf{r} - \left( \mathbf{r}_0 \mp \frac{\mathbf{l}}{2} \right)}{\left|\mathbf{r} - \left( \mathbf{r}_0 \mp \frac{\mathbf{l}}{2} \right)\right|^3} 
  & = \frac{\mathbf{r} - \mathbf{r}_0 }{\left|\mathbf{r} - \mathbf{r}_0 \right|^3} \pm \mathbf{l} \cdot \frac{1}{2} \nabla_{\mathbf{r}_0} \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right) + o(|\mathbf{l}|)\\
\end{aligned}$$

e, definendo l'intensità del dipolo $\mathbf{P}_0 := q \mathbf{l}$ e facendo tendere le grandezze al limite desiderato, quella del campo elettrico

$$\begin{aligned}
  \mathbf{e}(\mathbf{r})
  & = - \frac{1}{4\pi \varepsilon_0} \, \mathbf{P}_0 \cdot \nabla_{\mathbf{r}_0}  \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right)   = \\
  & = - \frac{1}{4\pi \varepsilon_0} \left[ \frac{(\mathbf{r}-\mathbf{r}_0)(\mathbf{r}-\mathbf{r}_0)}{|\mathbf{r}-\mathbf{r}_0|^5} \cdot \mathbf{P}_0 - \frac{\mathbf{P}_0}{|\mathbf{r}-\mathbf{r}_0|^3} \right] = \\
  & = - \frac{1}{4\pi \varepsilon_0} \left[ \frac{(\mathbf{r}-\mathbf{r}_0) \otimes (\mathbf{r}-\mathbf{r}_0)}{|\mathbf{r}-\mathbf{r}_0|^5} - \frac{\mathbb{I}}{|\mathbf{r}-\mathbf{r}_0|^3} \right] \cdot \mathbf{P}_0 \ .
\end{aligned}$$

**todo** nel caso generale sarebbe necessario prestare attenzione all'ordine dei fattori nel prodotto tra vettori e tensori, ma in questo caso si può sfruttare la simmetria del tensore del secondo ordine (o delle operazioni).

### Distribuzione continua di dipoli

Una distribuzione di dipoli con densità di volume $\mathbf{p}(\mathbf{r_0})$, che produce il dipolo elementare $\Delta \mathbf{P}(\mathbf{r}_0) = \mathbf{p}(\mathbf{r}_0) dV_0$ nel volume $d V_0$, produce il campo elettrico

$$\mathbf{e}(\mathbf{r}) = \int_{\mathbf{r}_0 \in V_0} \frac{1}{4 \pi \varepsilon_0} \mathbf{p}(\mathbf{r}_0) \cdot \nabla_{\mathbf{r}_0}  \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right) \ , $$

la cui espressione può essere riscritta usando le regole di integrazione per parti

$$\begin{aligned}
\mathbf{e}(\mathbf{r})
  & = \int_{\mathbf{r}_0 \in V_0} \frac{1}{4 \pi \varepsilon_0} \mathbf{p}(\mathbf{r}_0) \cdot \nabla_{\mathbf{r}_0}  \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right) = \\
  & = \oint_{\mathbf{r}_0 \in \partial V_0} \frac{1}{4 \pi \varepsilon_0}  \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \underbrace{ \hat{\mathbf{n}}(\mathbf{r}_0) \cdot \mathbf{p}(\mathbf{r}_0) }_{ =: \sigma_P(\mathbf{r}_0)}  + \int_{\mathbf{r}_0 \in V_0} \frac{1}{4 \pi \varepsilon_0} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \underbrace{ \left( - \nabla_{\mathbf{r}_0} \cdot \mathbf{p}(\mathbf{r}_0) \right)}_{ =: \rho_P(\mathbf{r}_0) } \ , \\
\end{aligned}$$

avendo definito le densità di carica di polarizzazione superficiale $\sigma_P$ e di volume $\rho_P$ come le intensità delle sorgenti distribuite di campo elettrico, in analogia con l'espressione della legge di Coulomb.

### Riformulazione delle equazioni di Maxwell e della continuità della carica

L'equazione di Gauss determina la densità di flusso nel volume del campo elettrico $\mathbf{e}$,

$$\nabla \cdot \mathbf{e} = \frac{\rho}{\varepsilon_0} \ .$$

Scomponendo la densità di carica come somma delle **cariche libere** $\rho_f$ e delle **cariche di polarizzazione** $\rho_P := - \nabla \cdot \mathbf{p}$, si può rielaborare l'equazione di Gauss,

$$\begin{aligned}
 & \nabla \cdot \mathbf{e} = \frac{\rho_f + \rho_P}{\varepsilon_0} \\
 & \nabla \cdot \left( \varepsilon_0 \mathbf{e} + \mathbf{p} \right) = \rho_f \\ \\
 & \nabla \cdot \mathbf{d} = \rho_f \ ,
\end{aligned}$$

avendo introdotto il **campo di spostamento**, $\mathbf{d} := \varepsilon_0 \mathbf{e} + \mathbf{p}$.

La scomposizione della corrente elettrica come somma $\mathbf{j} = \mathbf{j}_f + \mathbf{j}_P$ della corrente libera $\mathbf{j}_f$ e corrente di polarizzazione $\mathbf{j}_P$, permette di rielaborare l'equazione della continuità della carica elettrica

$$\begin{aligned}
  0 & = \partial_t \rho + \nabla \cdot \mathbf{j} = \\
    & = \partial_t (\rho_f + \rho_P) + \nabla \cdot \left( \mathbf{j}_f + \mathbf{j}_P \right) = \\
    & = \partial_t \rho_f + \nabla \cdot  \mathbf{j}_f + \partial_t \rho_P + \nabla \cdot \mathbf{j}_P \ ,
\end{aligned}$$

e scrivere le equazioni di continuità per le due distribuzioni di carica (di natura diversa, si suppone che entrambe devono soddisfare la continuità della carica in maniera indipendente, se le cariche libere rimangono libere e le cariche di polarizzazione rimangono di polarizzazione),

$$\begin{aligned}
  & \partial_t \rho_f + \nabla \cdot \mathbf{j}_f = 0 \\
  & \partial_t \rho_P + \nabla \cdot \mathbf{j}_P = 0 \qquad \rightarrow \qquad 0 = \nabla \cdot (-\partial_t \mathbf{p} + \mathbf{j}_P) \qquad \rightarrow \qquad \mathbf{j}_P = \partial_t \mathbf{p}
\end{aligned}$$

**todo** *giustificare assenza di campo costante*

## Magnetizzazione

### Singolo momento magnetico (limite di una spira elementare)
Usando la legge di Biot-Savart, specializzato a un conduttore percorso da corrente $i(\mathbf{r}_0)$

$$\begin{aligned}
  d \mathbf{b}(\mathbf{r})
  & = - \frac{\mu}{4 \pi} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \times \mathbf{j}(\mathbf{r}_0) d V_0 = \\
  & = - \frac{\mu}{4 \pi} i(\mathbf{r}_0) \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \times \hat{\mathbf{t}}(\mathbf{r}_0) d \ell_0 \ ,
\end{aligned}$$

si può calcolare il campo magnetico generato da una spira con percorso $\ell_0 = \partial S_0$ sfruttando il PSCE

$$\begin{aligned}
  \mathbf{b}(\mathbf{r})
  & = \oint_{\ell_0} d \mathbf{b}(\mathbf{r}_0) = \\
  & = - \frac{\mu}{4 \pi} i_0 \oint_{\mathbf{r}_0 \in \ell_0} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \times \hat{\mathbf{t}}(\mathbf{r}_0)  = \\
  & =   \frac{\mu}{4 \pi} i_0 \int_{\mathbf{r}_0 \in S_0} \hat{\mathbf{n}}(\mathbf{r}_0) \cdot \nabla_{\mathbf{r}_0} \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right)
\end{aligned}$$

Il campo generato da spira elementare di superficie $S_0$ con normale $\hat{\mathbf{n}}_0$, usando il teorema della media, è

$$\mathbf{b}(\mathbf{r}) = \frac{\mu}{4 \pi} i_0 S_0 \hat{\mathbf{n}}_0 \cdot \nabla_{\mathbf{r}_0} \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right) + o(S_0)$$

e al tendere di $i_0 \rightarrow \infty$, $S_0 \rightarrow 0$ in modo tale da avere $\mathbf{M}_0 := i_0 S_0 \hat{\mathbf{n}}_0$

$$\begin{aligned}
 \mathbf{b}(\mathbf{r}) 
  & = \frac{\mu}{4 \pi} \mathbf{M}_0 \cdot \nabla_{\mathbf{r}_0} \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right) \\
  & = - \frac{\mu_0}{4\pi} \left[ \frac{(\mathbf{r}-\mathbf{r}_0)(\mathbf{r}-\mathbf{r}_0)}{|\mathbf{r}-\mathbf{r}_0|^5} \cdot \mathbf{M}_0 - \frac{\mathbf{M}_0}{|\mathbf{r}-\mathbf{r}_0|^3} \right] = \\
  & = - \frac{\mu_0}{4\pi} \left[ \frac{(\mathbf{r}-\mathbf{r}_0) \otimes (\mathbf{r}-\mathbf{r}_0)}{|\mathbf{r}-\mathbf{r}_0|^5} - \frac{\mathbb{I}}{|\mathbf{r}-\mathbf{r}_0|^3} \right] \cdot \mathbf{M}_0 \ .
\end{aligned}$$

**todo** Analogia con il campo elettrico prodotto da una distribuzione di dipoli.

```{dropdown} Dettagli 
$$\oint_{\partial S} A \, t_i = \int_S \varepsilon_{ijk} \, n_j \, \partial_k A
\qquad , \qquad 
  \oint_{\partial S} A \, \hat{\mathbf{t}} = \int_S \hat{\mathbf{n}} \times \nabla A$$

$$\begin{aligned}
\oint_{\mathbf{r}_0 \in \ell_0} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \times \hat{\mathbf{t}}(\mathbf{r}_0) d \ell_0 
  & = \oint_{\mathbf{r}_0 \in \ell_0} \varepsilon_{ijk} \frac{r_j - r_{0,j}}{|\mathbf{r} - \mathbf{r}_0|^3} \ t_k = \\
  & = \int_{\mathbf{r}_0 \in S_0} \varepsilon_{krs} n_r \partial^0_s \left( \varepsilon_{ijk} \frac{r_j - r_{0,j}}{|\mathbf{r} - \mathbf{r}_0|^3} \right) = \\
  & = \int_{\mathbf{r}_0 \in S_0} \left( \delta_{ir} \delta_{js} - \delta_{is} \delta_{jr} \right) n_r \partial^0_s \left( \frac{r_j - r_{0,j}}{|\mathbf{r} - \mathbf{r}_0|^3} \right) = \\
  & = \int_{\mathbf{r}_0 \in S_0} \left\{ n_i \underbrace{\partial^0_j \left( \frac{r_j - r_{0,j}}{|\mathbf{r} - \mathbf{r}_0|^3} \right)}_{=0} - n_j \partial^0_i \left( \frac{r_j - r_{0,j}}{|\mathbf{r} - \mathbf{r}_0|^3} \right) \right\} = \\
  & = - \int_{\mathbf{r}_0 \in S_0} n_j \partial^0_i \left( \frac{r_j - r_{0,j}}{|\mathbf{r} - \mathbf{r}_0|^3} \right) \ .
\end{aligned}$$
```

### Distribuzione continua di momento magnetico

Per calcolare il campo magnetico generato da una distribuzione di volume di momento magnetico si può procedere in analogia con quanto fatto per calcolare il campo elettrico generato da una distribuzione di dipoli

$$\begin{aligned}
\mathbf{b}(\mathbf{r})
  & = \int_{\mathbf{r}_0 \in V_0} \frac{\mu_0}{4 \pi } \mathbf{m}(\mathbf{r}_0) \cdot \nabla_{\mathbf{r}_0}  \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right) = \\
  & = \oint_{\mathbf{r}_0 \in \partial V_0} \frac{\mu_0}{4 \pi}  \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \hat{\mathbf{n}}(\mathbf{r}_0) \cdot \mathbf{m}(\mathbf{r}_0) + \int_{\mathbf{r}_0 \in V_0} \frac{\mu_0}{4 \pi} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \,\left( - \nabla_{\mathbf{r}_0} \cdot \mathbf{m}(\mathbf{r}_0) \right) \ , \\
\end{aligned}$$

ma senza ottenere un'analogia con l'espressione della legge di Biot-Savart che prevede il prodotto vettore tra il termine $\frac{\mathbf{r}- \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3}$ con una densità di corrente $\mathbf{j}(\mathbf{r}_0)$.

```{dropdown} Dettagli

Si può riscrivere

$$\begin{aligned}
  \oint_{\mathbf{r}_0 \in \partial V_0} & \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \times \left( \hat{\mathbf{n}}(\mathbf{r}_0) \times \mathbf{m}(\mathbf{r}_0) \right) \\
  & = \oint_{\mathbf{r}_0 \in \partial V_0} \varepsilon_{ijk} \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} \varepsilon_{krs} n_r m_s = \\
  & = \int_{\mathbf{r}_0 \in V_0} \left( \delta_{ir} \delta_{js} - \delta_{is} \delta_{jr} \right) \partial^0_r \left( \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} m_s \right) = \\
  & = \int_{\mathbf{r}_0 \in V_0} \left\{ \partial^0_i \left( \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} m_j \right) - \partial^0_j \left( \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} m_i \right)  \right\} = \\
  & = \int_{\mathbf{r}_0 \in V_0}
  \left\{ \partial^0_i \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} m_j 
         + \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} \partial^0_i m_j
         - \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} \partial^0_j m_i 
         - \underbrace{ \partial^0_j \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3}}_{=0} m_i 
  \right\} = \\
  & = \int_{\mathbf{r}_0 \in V_0}
  \left\{ \partial^0_i \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} m_j 
         + \varepsilon_{ijk} \varepsilon_{krs} \frac{r_j - r_{0,j}}{|\mathbf{r}-\mathbf{r}_0|^3} \partial^0_r m_s
  \right\} = \\
  & = \int_{\mathbf{r}_0 \in V_0}
  \left\{ \nabla_{\mathbf{r}_0} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r}-\mathbf{r}_0|^3} \cdot \mathbf{m}(\mathbf{r}_0) 
         + \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r}-\mathbf{r}_0|^3} \times \left( \nabla_{\mathbf{r}_0} \times \mathbf{m}(\mathbf{r}_0) \right)
  \right\} = \\
\end{aligned}$$

usando le identità del calcolo vettoriale,

$$\begin{aligned}
  \mathbf{a} \times (\mathbf{b} \times \mathbf{c}) & = \varepsilon_{ijk} a_j \varepsilon_{krs} b_r c_s = \\
  & = (\delta_{ir} \delta_{js} - \delta_{is} \delta_{jr}) a_j b_r c_s = \\
  & = a_j b_i c_j - c_i b_j a_j = \mathbf{b}(\mathbf{a} \cdot \mathbf{c}) - \mathbf{c} (\mathbf{a} \cdot \mathbf{b})
\end{aligned}$$

$$\begin{aligned}
 a_j \partial_i m_j - a_j \partial_j m_i
 & = (\delta_{ir} \delta_{js} - \delta_{is} \delta_{jr}) a_j \partial_r m_s = \\
 & = \varepsilon_{ijk} \varepsilon_{krs} a_j \partial_r m_s = \\
 & = \mathbf{a} \times \left( \nabla \times \mathbf{m} \right)
\end{aligned}$$

Il campo magnetico generato da una distribuzione di momento magnetico può quindi essere riscritto come

$$\begin{aligned}
\mathbf{b}(\mathbf{r})
  & = \int_{\mathbf{r}_0 \in V_0} \frac{\mu_0}{4 \pi } \mathbf{m}(\mathbf{r}_0) \cdot \nabla_{\mathbf{r}_0}  \left( \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \right) = \\
  & = - \frac{\mu_0}{4\pi} \oint_{\mathbf{r}_0 \in \partial V_0} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r} - \mathbf{r}_0|^3} \times \underbrace{ \left( - \hat{\mathbf{n}}(\mathbf{r}_0) \times \mathbf{m}(\mathbf{r}_0) \right) }_{\mathbf{j}^s_M}
  - \frac{\mu_0}{4 \pi} \int_{\mathbf{r}_0 \in V_0} \frac{\mathbf{r} - \mathbf{r}_0}{|\mathbf{r}-\mathbf{r}_0|^3} \times \underbrace{ \left(\nabla_{\mathbf{r}_0} \times \mathbf{m}(\mathbf{r}_0) \right)}_{\mathbf{j}_M} \ ,
\end{aligned}$$
avendo definito le densità di corrente di magnetizzazione superficiale $\mathbf{j}^s_M$ e di colume $\mathbf{j}_M$ come le intensità delle singolarità distribuite, in analogia con l'espressione della legge di Biot-Savart.

```

### Riformulazione delle equazioni di Maxwell e della continuità della carica

La legge di Ampére-Maxwell può essere riscritta

$$\begin{aligned}
 & \nabla \times \mathbf{b} - \mu_0 \varepsilon_0 \partial_t \mathbf{e} = \mu_0 \mathbf{j} \\
 & \nabla \times \mathbf{b} - \mu_0 \partial_t \left( \mathbf{d} - \mathbf{p} \right) = \mu_0 \left( \mathbf{j}_f + \mathbf{j}_P + \mathbf{j}_M \right) \\
 & \nabla \times \underbrace{\left( \mathbf{b} - \mu_0 \mathbf{m} \right)}_{=: \mu_0 \mathbf{h}} - \mu_0 \partial_t \mathbf{d} + \mu_0 \underbrace{\left( \partial_t \mathbf{p} - \mathbf{j}_P \right)}_{= \mathbf{0}} = \mu_0 \mathbf{j}_f  \\ \\
 & \nabla \times \mathbf{h} - \partial_t \mathbf{d} = \mathbf{j}_f
\end{aligned}$$

Dalla legge di continuità della corrente elettrica,

$$\partial_t \rho + \nabla \cdot \mathbf{j} = 0 \ ,$$

si ricava l'equazione di continuità per le cariche di magnetizzazione

$$\begin{aligned}
  0 & = \partial_t \rho_M + \nabla \cdot \mathbf{j}_M = \\
    & = \partial_t \rho_M + \underbrace{ \nabla \cdot \nabla \times \mathbf{m}}_{ \equiv \mathbf{0} } \ .
\end{aligned}$$


## Esempi
- conduttori
- ferromagentici e magnetismo debole (para-, dia-, anti-)

(classical-electromagnetism:media:jump)=
## Jump conditions
Differential form of Maxwell's equations

$$\begin{cases}
 \nabla \cdot \mathbf{d} = \rho_f \\
 \nabla \times \mathbf{e} + \partial_t \mathbf{b} = \mathbf{0} \\
 \nabla \cdot \mathbf{b} = 0 \\
 \nabla \times \mathbf{h} - \partial_t \mathbf{d} = \mathbf{j}_f
\end{cases}$$

Integral form of Maxwell's equations

$$\begin{cases}
 \displaystyle \oint_{\partial V} \mathbf{d} \cdot \hat{\mathbf{n}} = \int_{V} \rho_f \\
 \displaystyle \oint_{\partial S} \mathbf{e} \cdot \hat{\mathbf{t}} + \dfrac{d}{dt} \int_S \mathbf{b} \cdot \hat{\mathbf{n}} = 0 \\
 \displaystyle \oint_{\partial V} \mathbf{b} \cdot \hat{\mathbf{n}} = 0 \\
 \displaystyle \oint_{\partial S} \mathbf{h} \cdot \hat{\mathbf{t}} - \dfrac{d}{dt} \int_S \mathbf{d} \cdot \hat{\mathbf{n}} = \int_{S} \mathbf{j}_f \cdot \hat{\mathbf{n}} \\
\end{cases}$$

Letting $V$ and $S$ "collapsing on a discontinuity"...

$$\begin{cases}
  [ d_n ] = \sigma_f \\
  [ e_t ] = 0 \\
  [ b_n ] = 0 \\
  [ h_t ] = \iota_f \ ,
\end{cases}$$ (eq:em-jump)

being $\sigma_f$ and $\iota_f$ surface charge and current density, with physical dimension $\frac{\text{charge}}{\text{surface}}$, and $\frac{\text{current}}{\text{surface}}$ respectively. These contributions can be thought as Dirac delta contributions in volume density, namely

$$\rho(\mathbf{r},t) = \rho_0(\mathbf{r},t) + \sigma(\mathbf{r}_s,t) \delta_{1}(\mathbf{r}-\mathbf{r}_s) \ ,$$

being $\rho(\mathbf{r},t)$ the regular part of the volume density in all the points of the domain $\mathbf{r} \in V$, $\sigma(\mathbf{r}_s,t)$ the surface density on 2-dimensional surfaces $\mathbf{r}_s \in S$, $\delta_1()$ the Dirac's delta with physical dimension $\frac{1}{\text{length}}$.

If there's no free surface charge and currents, jump conditions form linear media become

$$\begin{cases}
  [ d_n ] = 0 \\
  [ e_t ] = 0 \\
  [ b_n ] = 0 \\
  [ h_t ] = 0 \ ,
\end{cases}
\qquad \rightarrow \qquad
\begin{cases}
  d_{n,1} = d_{n,2}  \quad \rightarrow \quad \varepsilon_1 e_{n,1} = \varepsilon_2 e_{n,2} \\
  e_{t,1} = e_{t,2}  \\
  b_{n,1} = b_{n,2}  \\
  h_{t,1} = h_{t,2}  \quad \rightarrow \quad \frac{1}{\mu_1} b_{t,1} = \frac{1}{\mu_2} b_{t,2} \\
\end{cases}
$$ (eq:em-jump:no-surf-density)







