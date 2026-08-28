---
tags: [psychosis, schizophrenia, psychosocial-functioning, social-cognition, artificial-intelligence, machine-learning, digital-phenotyping, quality-of-life, predictive-modeling, clinical-psychiatry]
source_papers: ["fpsyt-16-1692177.pdf"]
---

# Intelligenza Artificiale nel Funzionamento Psicosociale della Psicosi (AI in Psychosocial Functioning in Psychosis)

## Definizione Operativa
- L'**Intelligenza Artificiale applicata al Funzionamento Psicosociale nella Psicosi** definisce l'impiego integrato di algoritmi di Machine Learning (supervisionato, causale ed ensemble), modelli di elaborazione del segnale vocale e sensoristica passiva (*digital phenotyping*) per la stima oggettiva, la predizione precoce e il monitoraggio continuo delle capacità funzionali, relazionali e occupazionali negli individui con disturbi dello spettro psicotico (Mok, Cheng & Chu, 2025; *Frontiers in Psychiatry*, doi: 10.3389/fpsyt.2025.1692177).
- **Superamento del Riduzionismo Diagnostico:** Rappresenta una fondamentale transizione clinico-computazionale: sposta il focus dell'IA dalla mera diagnosi nosografica binaria (schizofrenia vs controllo sano basata su neuroimaging acuto o genetica statica) verso la quantificazione dinamica della **recovery funzionale** (*social and occupational functioning*, *Theory of Mind*, qualità della vita percepita - QoL), fornendo ai clinici metriche predittive azionabili per personalizzare i percorsi riabilitativi e psicoterapeutici.

```mermaid
flowchart TD
    subgraph InputStreams ["1. Flussi di Dati Multidimensionali"]
        I1["Dati Clinici & Psicometrici<br/>(PANSS, BDI, TEPS, DUP)"]
        I2["Cognizione Sociale & Neurocognizione<br/>(ToM T.h.o.m.a.s, ER40, BLERT, MSCEIT)"]
        I3["Digital Phenotyping Passivo<br/>(Mobile sensing CrossCheck, Geolocation, Sleep)"]
        I4["Biomarker Vocali & Acustici<br/>(Pitch, Jitter, Formanti F1-F3, Shimmer)"]
    end

    subgraph ComputationalEngine ["2. Motore di Inferenza & Modellazione"]
        M1["Ensemble Learning & Feature Selection<br/>(Random Forest + LASSO, Bagging + M5 Prime)"]
        M2["Causal Discovery & Reti Probabilistiche<br/>(Greedy Fast Causal Inference, Bayesian Networks)"]
        M3["Reinforcement Learning Offline per Raccomandazioni<br/>(Batch Constrained Q-Learning - BCQ)"]
    end

    subgraph FunctionalOutcomes ["3. Target Psicosociali & Predizione"]
        O1["Autonomia Sociale & Lavorativa<br/>(GAF, PSP, SLOF, Tasso di impiego)"]
        O2["Decodifica Emozionale & Cognizione Sociale<br/>(Riconoscimento affetti, ToM di 1°/2°/3° ordine)"]
        O3["Qualità della Vita Soggettiva (QoL)<br/>(QLS, J-SQLS, Benessere percepito)"]
    end

    subgraph ClinicalAction ["4. Decisione Clinica & Intervento CBT"]
        A1["Stratificazione Precoce del Rischio di Disabilità"]
        A2["Scaffolding Riabilitativo Social Cognition Training (SCT)"]
        A3["Co-pilota Centauro: Raccomandazioni in Seduta"]
    end

    InputStreams --> ComputationalEngine
    ComputationalEngine --> FunctionalOutcomes
    FunctionalOutcomes --> ClinicalAction
```

---

## Evidenze Empiriche e Performance Computazionale

### 1. Accuratezza Predittiva Differenziale per Dominio
La meta-analisi di Mok et al. (2025) evidenzia che la capacità predittiva dei modelli di IA varia marcatamente in funzione del costrutto target e della tipologia di predittori impiegati:
- **Cognizione Sociale vs Esiti Funzionali nel Mondo Reale:** I modelli addestrati per discriminare o predire la cognizione sociale (riconoscimento delle micro-espressioni facciali su test ER40/BLERT, compiti di Theory of Mind) raggiungono un'accuratezza discriminativa significativamente più elevata (**AUC = 0.77**, 95% CI: 0.69–0.85) rispetto a quelli destinati a prevedere esiti psicosociali complessi e a lungo termine come il mantenimento dell'occupazione o il punteggio GAF (**AUC = 0.68**, 95% CI: 0.60–0.77; $p = 0.003$).
- **Gerarchia Predittiva dei Dati di Input:**
  1. *Sintomi Clinici & Affettivi:* Producono il minor errore di predizione (**RMSE = 7.10**, 95% CI: 5.78–8.43), confermandosi i predittori prossimali più potenti del livello funzionale;
  2. *Batterie Neurocognitive:* Presentano un errore intermedio (**RMSE = 8.17**, 95% CI: 7.36–8.99);
  3. *Biomarker Genetici & Poligenici:* Esibiscono l'errore predittivo più elevato (**RMSE = 9.19**, 95% CI: 7.96–10.41), indicando che i profili genomici da soli hanno una scarsa capacità di catturare la complessità del funzionamento psicosociale quotidiano.

```mermaid
flowchart LR
    subgraph PredictorPower ["Gerarchia di Accuratezza dei Predittori (RMSE Meta-Analitico)"]
        P1["Sintomi Clinici (PANSS, Umore)<br/>RMSE = 7.10 (Migliore Accuratezza)"]
        P2["Neurocognizione & ToM<br/>RMSE = 8.17 (Accuratezza Intermedia)"]
        P3["Biomarker Genetici & Poligenici<br/>RMSE = 9.19 (Massimo Errore / Minore Utilità)"]
        P1 -->|Superiore a| P2 -->|Superiore a| P3
    end
```

---

### 2. Architetture Ottimali: Il Ruolo di Ensemble e Feature Selection
- **Superiorità di Random Forest e Bagging:** L'applicazione di singoli alberi decisionali o di regressioni lineari non regolarizzate fallisce nella gestione della non-linearità e dell'eterogeneità tipica della clinica della psicosi. Gli algoritmi di *Random Forest (RF)* e *Bagging ensemble* combinati con metodi avanzati di selezione delle feature (*M5 Prime*, *LASSO*, *Recursive Feature Elimination*) ottengono sistematicamente le performance più elevate (Accuratezza fino al **79.5%**, AUC fino a **0.867**; Li et al., 2022; Lin et al., 2021a).
- **Risoluzione dell'Overfitting:** La selezione rigorosa delle feature riduce il rumore statistico generato da batterie di test eccessivamente ridondanti, isolando le variabili clinicamente determinanti.

---

### 3. Digital Phenotyping e Monitoraggio Continuo
- **Mobile Sensing Passivo (CrossCheck):** Attraverso la registrazione passiva dei pattern di mobilità GPS, dell'attività dell'accelerometro, dei log di chiamata/messaggistica e dell'uso del dispositivo, i modelli di regressione supervisionata (XGBoost, Support Vector Regression) stimano i livelli della *Social Functioning Scale (SFS)* con un margine di errore medio del ~10% (*MAE* 2.17–2.79; Wang et al., 2020).
- **Biomarker Acustici della Qualità della Vita:** L'analisi automatizzata delle proprietà prosodiche del parlato (frequenza fondamentale $F_0$, instabilità di ampiezza e micro-variazioni formanti) consente di rilevare precocemente peggioramenti soggettivi nella qualità della vita (*J-SQLS*), offrendo una misura ecologica che prescinde dalla compilazione attiva di questionari (Shibata et al., 2023).

---

## Matrice Comparativa dei Modelli di IA nella Psicosi

| Paradigma di IA | Ruolo Clinico | Vantaggi Principali | Rischi & Limiti Critici | Indicazione Clinica |
| :--- | :--- | :--- | :--- | :--- |
| **Supervised ML & Ensemble** (RF, SVM, Bagging) | Stratificazione del rischio funzionale e predizione del recovery | Elevata accuratezza (AUC 0.70–0.87), gestione di dati non lineari | Modelli statici, necessità di baseline strutturate | **Fortemente Raccomandato** per screening e pianificazione |
| **Causal Discovery & Bayesian Networks** | Identificazione di target terapeutici primari e gerarchie ToM | Spiegabilità causale, validazione di relazioni dirette vs spurie | Richiede campioni ampi e assunzioni di indipendenza | **Fondamentale** per la strutturazione dei protocolli CBT/SCT |
| **Digital Phenotyping** (Mobile & Audio Sensing) | Monitoraggio ecologico e continuativo tra le sedute | Rilevazione passiva in tempo reale, zero recall bias | Sfide di privacy, scarso transfer su pazienti con acuzie severa | **Consigliato** in fase di remissione o stabilizzazione |
| **Chatbot Conversazionali Autonomi (LLM)** | Psicoterapia o supporto conversazionale non supervisionato | Accessibilità 24/7, basso costo di erogazione | Rischio elevato di **AI Psychosis**, sicofanzia, rinforzo di deliri, stigma | **CONTROINDICATO** nella psicosi attiva senza clinico umano |
| **Co-pilota Centauro / Real-Time Recommendation** | Suggerimento argomenti e tecniche al terapeuta durante la seduta | Preserva l'alleanza terapeutica, potenzia la decisione umana | Accuratezza attuale moderata (64%), necessità di calibrazione | **Promettente** come supporto decisionale per il terapeuta |

---

## Implicazioni per la Psicoterapia Cognitivo-Comportamentale (CBT-p)

1. **Ottimizzazione delle Risorse Riabilitative:** La previsione algoritmica precoce del declino occupazionale permette di allocare percorsi intensivi di *Supported Employment* (es. modello IPS - *Individual Placement and Support*) ai pazienti con minore probabilità di recupero spontaneo.
2. **Personalizzazione del Social Cognition Training (SCT):** Individuando i cluster specifici di compromissione (es. deficit selettivo nella percezione facciale vs difficoltà nelle credenze ricorsive di secondo ordine), il terapeuta può calibrare esercizi di mentalizzazione su misura.
3. **Integrazione con il Modello Centauro:** L'IA non deve mai sostituirsi alla presenza incarnata del clinico. La relazione terapeutica rimane l'elemento insostituibile per l'elaborazione dei vissuti psicotici; gli strumenti computazionali operano come un co-pilota analitico per ridurre i punti ciechi diagnostici.

---

## Riferimenti Bibliografici
- Mok, C. H. Y., Cheng, C. P. W., & Chu, M. H. W. (2025). Application of artificial intelligence and psychosocial functioning in psychosis: a systematic review and meta-analysis. *Frontiers in Psychiatry*, 16, 1692177. https://doi.org/10.3389/fpsyt.2025.1692177
- Bosco, F. M., Colle, L., Salvini, R., & Gabbatore, I. (2024). A machine-learning approach to investigating the complexity of theory of mind in individuals with schizophrenia. *Heliyon*, 10(6), e30693. https://doi.org/10.1016/j.heliyon.2024.e30693
- Li, C., Wang, W., Guo, Q., Jiang, L., Qiao, K., Hu, Y., et al. (2022). Deep learning system for brain image-aided diagnosis of multiple major mental disorders. *bioRxiv*, 2022-06. https://doi.org/10.1101/2022.06.01.22275855
- Lin, B., Cecchi, G., & Bouneffouf, D. (2023). Psychotherapy AI companion with reinforcement learning recommendations and interpretable policy dynamics. In *Companion Proceedings of the ACM Web Conference 2023 (WWW '23)* (pp. 932–939). ACM. https://doi.org/10.1145/3543873.3587623
- Lin, E., Lin, C. H., & Lane, H. Y. (2021a). Applying a bagging ensemble machine learning approach to predict the functional outcome of schizophrenia with clinical symptoms and cognitive functions. *Scientific Reports*, 11, 6922. https://doi.org/10.1038/s41598-021-86382-0
- Miley, K., Meyer-Kalos, P., Ma, S., Bond, D. J., Kummerfeld, E., & Vinogradov, S. (2023). Causal pathways to social and occupational functioning in the first episode of schizophrenia: uncovering unmet treatment needs. *Psychological Medicine*, 53(5), 2041–2049. https://doi.org/10.1017/S0033291721003780
- Shibata, Y., Victorino, J. F., Natsuyama, T., Okamoto, N., Yoshimura, R., & Shibata, T. (2023). Estimation of subjective quality of life in schizophrenic patients using speech features. *Frontiers in Rehabilitation Sciences*, 4, 1121034. https://doi.org/10.3389/fresc.2023.1121034
- Wang, W., Mirjafari, S., Harari, G., Ben-Zeev, D., Brian, R., Choudhury, T., et al. (2020). Social sensing: Assessing social functioning of patients living with schizophrenia using mobile phone sensing. In *Proceedings of the 2020 CHI Conference on Human Factors in Computing Systems* (pp. 1–15). ACM. https://doi.org/10.1145/3313831.3376855

---

## Relazioni
- Vedi anche: [[fpsyt-16-1692177]], [[causal-discovery-psychosocial-targets]], [[modello-centauro-clinico]], [[ai-psychosis]], [[applied-theory-of-mind-llm]], [[synthetic-psychopathology]], [[multimodal-anxiety-detection-ai]], [[social-media-phenotyping-anxiety]], [[clinical-ai-simulation]], [[supervisione-clinica-ai]]
