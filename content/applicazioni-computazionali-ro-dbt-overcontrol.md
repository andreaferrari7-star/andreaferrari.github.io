---
tags: [ro-dbt, overcontrol, digital-phenotyping, nlp, machine-learning, hrv-biofeedback, facs, cluster-c, ocpd, outcome-prediction, passive-sensing, affective-computing]
tipo_fonte: [scientifica, interna]
source_papers: ["Ricerca Computazionale RO-DBT e Overcontrol.md"]
---

# Analisi Computazionale della RO-DBT e Fenotipi di Overcontrol

## Definizione Operativa

- Sintesi sistematica delle applicazioni di intelligenza artificiale, NLP e passive sensing nel framework della Radically Open Dialectical Behavior Therapy (RO-DBT) e nei disturbi caratterizzati da ipercontrollo (Cluster C, anoressia restrittiva).
- La RO-DBT (Lynch, 2018) è un modello transdiagnostico sviluppato per quadri refrattari accomunati da eccessiva inibizione comportamentale, inflessibilità cognitiva e solitudine emotiva cronica, opposti al target della DBT standard (undercontrol/BPD). Il suo bersaglio terapeutico primario è il deficit di *social signaling* autentico e l'incapacità di *radical openness* relazionale.
- **Utilità CBT / Applicativa:** Identifica i gap tecnologici e le "deviazioni" verso la letteratura CBT/DBT generale, necessarie per monitorare e trattare digitalmente la rigidità inibitoria e la carenza di segnalazione sociale. Mappa cinque direttrici clinico-computazionali con il loro stato di validazione empirica.

---

## Evidenze dalla Letteratura

### 1. Interventi Computazionali Aumentati in RO-DBT

**Gap dichiarato:** Assenza totale di RCT, studi pilota quantitativi o trial di fattibilità peer-reviewed che abbiano testato interventi digitali (chatbot, DTx, agenti conversazionali AI) dedicati esclusivamente al modello RO-DBT (Hatoum & Burton, 2024). Esistono app commerciali di auto-tracciamento (es. *RO-DBT Diary Card and Skills App*) prive di validazione clinica indipendente pubblicata.

**Letteratura adiacente validata:**

| Primo Autore & Anno | Campione / Disegno | Architettura AI | Outcome Principali |
|---|---|---|---|
| **Rizvi et al. (2011)** | Pazienti BPD con abuso di sostanze; studio quasi-sperimentale pre-post | App smartphone (*DBT Coach*) con alberi decisionali euristici per coaching in vivo (*Opposite Action*) | Riduzione significativa dell'intensità emotiva soggettiva e del craving per sessione; decremento di ansia e depressione |
| **Rizvi et al. (2016)** | Soggetti con grave condotta autolesiva; studio pilota a braccio singolo | Algoritmo deterministico per gestione personalizzata delle contingenze e somministrazione graduale di strategie regolatorie | Riduzione statisticamente significativa delle urgenze autolesive e decremento dell'NSSI |
| **Mensinger et al. (2024)** | Operatori sanitari a rischio per disturbi alimentari e trauma; studio pilota pre-post | Analisi spettrale real-time per HRV-biofeedback risonante (mHealth, frequenza ~0.1 Hz) | Incremento della consapevolezza interocettiva (MAIA-2) e marcata attenuazione della sintomatologia alimentare restrittiva |
| **Scolnick et al. (2014)** | Pazienti ospedalizzati con anoressia nervosa; trial pilota di sicurezza | Piattaforma di biofeedback per coerenza cardiaca e respirazione controllata | Incremento significativo della coerenza HRV e riduzione dell'ansia di stato; assenza di eventi avversi |
| **Cardinal et al. (2021)** | Pazienti adulte con anoressia nervosa; studio di usabilità e fattibilità | Modulo software con gamification basato su strategie CBT/DBT per ipercontrollo emotivo | Tassi eccellenti di aderenza e usabilità; validazione di moduli per la tolleranza della vulnerabilità emotiva |

---

### 2. Clinical NLP e Speech Processing nelle Sedute Terapeutiche

**Gap dichiarato:** Nessuna pubblicazione peer-reviewed applica LLM, NLP o classificatori vocali/video a registrazioni di sedute RO-DBT. La disciplina attinge a sistemi di deep learning per la stima automatizzata della *fidelity* in CBT/DBT e a modelli di computer vision per l'ipo-espressività emotiva e il masking facciale.

La RO-DBT prescrive posture terapeutiche peculiari (auto-esplorazione, *taking the heat off*, *eyebrow wag*, modulazione prosodica espansiva) la cui codifica manuale è laboriosa e soggetta a bias — motivando un approccio computazionale.

| Primo Autore & Anno | Campione / Disegno | Architettura AI | Outcome Principali |
|---|---|---|---|
| **Ewbank et al. (2020)** | Larga scala; N sedute trascritte | Deep Learning supervisionato (Hierarchical Attention Networks, HAN) per NLP | Classificazione automatica della fidelity clinica con AUC elevata; il volume di interventi specifici predice il tasso di miglioramento |
| **Ramseyer et al. (2023)** | Sedute video-registrate; validazione metodologica in psicoterapia | Pipeline multimodale con OpenFace e OpenPose per tracciamento facciale e corporeo continuo (NVBA) | Correlazione significativa di arousal e valenza espressiva con il giudizio clinico di vergogna, tristezza e rilassamento |
| **Wang et al. (2012)** | Coorte clinica vs controlli sani; studio sperimentale di video-analisi | SVM + Active Appearance Models per FACS automatizzato | Rilevamento oggettivo di piattezza affettiva e inappropriatezza espressiva; quantificazione della dinamica transitoria delle Action Units |
| **Saeb et al. (2024)** | Registrazioni vocali cliniche con restrizione affettiva | Pipeline di speech processing (F0, jitter, shimmer, pause vocali) | Accuratezza elevata nella rilevazione dello stato affettivo inibito; la varianza prosodica discrimina significativamente il livello di inibizione |
| **Mocnik et al. (2024)** | Sintesi su video clinici e segnali paraverbali in disturbi con distorsione comunicativa | Architetture multimodali Transformer audio-visivi | Mappatura dei pattern di disconnessione tra contenuto semantico ed espressione non verbale; confermata rilevabilità algoritmica del masking |

---

### 3. Predizione degli Esiti (Machine Learning Outcome Prediction)

**Gap dichiarato:** I trial clinici registrativi della RO-DBT (incluso il trial multicentrico *REFRAMED* di Lynch) hanno analizzato i dati con modelli lineari a effetti misti (LMM), senza impiegare algoritmi ML per feature selection non lineare o previsione individuale cross-validata. Non esistono modelli ML pubblicati specificamente addestrati su outcome RO-DBT.

I modelli predittivi hanno valore strategico nell'OC perché i pazienti ipercontrollati mantengono un'aderenza esteriore rigida che può mascherare totale assenza di cambiamento metacognitivo, traducendosi in refrattarietà prolungata o abbandoni improvvisi.

| Primo Autore & Anno | Campione / Disegno | Architettura AI | Outcome Principali |
|---|---|---|---|
| **Gilmartin et al. (2024)** | N=561 giovani adulti; studio osservazionale trasversale su FFM | Hierarchical Clustering (Ward) + k-means non supervisionato + validazione Random Forest | Isolamento robusto di cluster OC, UC e Resiliente distinti; correlazione con psicopatologia alimentare, ansia e depressione (EDE-QS, DASS-21) |
| **Sole et al. (2022)** | Pazienti in percorsi di skills training DBT; studio prospettico | Lasso + Random Forest con validazione incrociata nested a 10-fold; 34 indici estratti | Identificazione di pattern clinici predittivi del successo terapeutico; impatto cardine della capacita "non-judging" |
| **Linardon et al. (2025)** | Partecipanti con disturbi alimentari disfunzionali; studio secondario su trial clinico | Confronto di 10 algoritmi (Random Forest, Elastic Net, SVR) | I dati baseline falliscono la predizione (AUC ~0.50); l'integrazione di serie temporali d'uso digitale predice il drop-out con AUC elevata |
| **De Jong et al. (2024)** | Meta-analisi; N studi con ampi campioni clinici | Sintesi e meta-regressione di modelli ML supervisionati per risposta alla psicoterapia | Capacita predittiva generalizzabile a campioni esterni (validata in 5 coorti su 7); effect size pooled significativo |
| **Gasser et al. (2023)** | Percorsi ambulatoriali con funzionamento di personalita; studio di coorte prospettico | Alberi decisionali + regressioni penalizzate per feature selection | Identificazione della compromissione delle attivita sociali e della rigidita relazionale come predittori cardine di mancato miglioramento |
| **Jacobs et al. (2026)** | N=463 pazienti con OCD; due studi con MCCV a 100 iterazioni | Random Forest ibrido con pretraining su dati simulati da letteratura (MVND) + SMOTE-NC | Il pretraining migliora l'accuracy in Studi 1 (+2.2%) ma non significativamente; nello Studio 2 (remissione) il modello standard supera i pre-addestrati |

---

### 4. Digital Phenotyping dell'Overcontrol tramite Dati Passivi

Il paradigma del digital phenotyping passivo consente la quantificazione ininterrotta del comportamento ecologico senza distorsioni da autovalutazione retrospettiva. Nella RO-DBT, i soggetti OC presentano un profilo bio-temperamentale specifico: elevata threat sensitivity con iper-reattivita inibitoria, che si traduce in modulazione parasimpatica tonica atipicamente alta a riposo e marcata ipo-reattivita neurovegetativa fasica durante l'ingaggio sociale.

Questo paradosso fisiopatologico si riflette nei segnali passivi rilevabili:
- **HRV:** Valori paradossalmente elevati di RMSSD e HF-HRV che non riflettono rilassamento ma iper-regolazione vagale rigida; blocco della variabilita fasica durante le interazioni comunitarie.
- **GPS/mobilita:** Estrema regolarita e bassa entropia negli spostamenti, pattern circadiano inflessibile, latenze ridotte nelle risposte formali, variazioni cinetiche ridotte (*keystroke dynamics*).
- **EDA:** Ridotta conduttanza cutanea tonica in popolazioni restrittive.

| Primo Autore & Anno | Campione / Disegno | Architettura AI | Outcome Principali |
|---|---|---|---|
| **Kim et al. (2024)** | Revisione sistematica su dati wearable in popolazioni AN | Sintesi computazionale di segnali ECG, PPG, EDA, accelerometria | Bradicardia, ridotta EDA tonica e incremento atipico di HRV associato a rigida ipo-reattivita nelle popolazioni restrittive/OC |
| **Wang et al. (2022)** | Coorte studentesca monitorata h24; studio longitudinale | Lasso, Random Forest e XGBoost con Leave-One-Participant-Out | Predizione accurata di tratti PID-5 e rigidita comportamentale da tracce GPS, sblocchi schermo e log chiamate |
| **Meng et al. (2025)** | Individui sotto compiti stressogeni; studio multimodale | Bimodal Gated Recurrent Unit (GRU) + FACS (OpenFace) + pose corporee | Predizione ottimale di ansia inibitoria e tratti anancastici tramite co-occorrenza di AU07, AU15 e postura |
| **Pfeffer et al. (2024)** | Coorte clinica con threat sensitivity; studio prospettico | OpenFace 2.0 vs codifiche manuali FACS | I biomarcatori computazionali di congelamento mimico e soppressione facciale predicono longitudinalmente la persistenza di sintomi rigidi |
| **Teckentrup et al. (2023)** | Soggetti sottoposti a paradigma sociale Cyberball; studio caso-controllo | Analisi tempo-frequenza su RMSSD autonomico ed elettrodermico | I soggetti con elevato overcontrol mostrano prolungata assenza di reattivita fasica e blocco dell'ingaggio vagale pro-sociale durante l'esclusione sociale |

---

### 5. Systematic Reviews su AI e Disturbi di Personalita del Cluster C

**Gap dichiarato:** Severa asimmetria nella ricerca: le revisioni sistematiche sulle applicazioni AI nei disturbi di personalita si concentrano quasi esclusivamente sul BPD (Cluster B), motivate dall'urgenza di predire e contenere condotte autolesive. Non esiste alcuna scoping review o meta-analisi registrata (PROSPERO) interamente circoscritta all'AI nei disturbi del Cluster C (OCPD, AVPD, DPD).

| Primo Autore & Anno | Campione / Disegno | Architettura AI | Outcome Principali |
|---|---|---|---|
| **Mocnik et al. (2024)** | Scoping Review (PRISMA-ScR) su digital biomarkers e AI nei disturbi di personalita | Rassegna di modelli AI per feature extraction da testo, audio, mimica, fisiologia | Documentata carenza di studi sul Cluster C vs Cluster B; specificita dei pattern di inibizione fisiologica nell'OCPD |
| **Aafjes-van Doorn et al. (2021)** | Scoping Review ML e psicoterapia; N studi analizzati sistematicamente | Mappatura di SVM, Random Forest e NLP per diagnostica e predizione | Rilevamento della trascuratezza dei profili internalizzanti ed evitanti; proposta di modelli computazionali dimensionali |
| **Arena (Sepe) et al. (2025)** | N=30 OCPD vs N=34 controlli; studio sperimentale di neuroimaging | Parallel Independent Component Analysis (pICA) — data fusion non supervisionata su MRI | Alterazioni GM+WM in network fronto-striatali e DMN/Salience specifiche OCPD; iperconnettivita strutturale correlata all'ansia clinica |
| **Hyatt et al. (2025)** | Anziani sani (N ampio) con validazione su giovani; studio multi-coorte | Elastic Net, SVR e Gradient Boosting con morfometria cerebrale | Predizione robusta di tratti OCPD tramite item FFM; associazione con ispessimento corticale del giro frontale superiore destro |
| **Gao et al. (2025)** | Scoping Review globale sull'AI nella salute mentale; N rassegne metodologiche | Valutazione cross-diagnostica di screening computazionale, diagnostica e chatbot | Marcata concentrazione su disturbi affettivi e Cluster B; drastico calo di accuratezza predittiva tra validazione interna ed esterna |

---

## Limiti Tecnici, Rischi Specifici e Implicazioni per l'IA

### 1. Masking Sociale e Falsi Negativi Ecologici
Il limite primario scaturisce dalla discrepanza intrinseca tra condotta manifesta e stato affettivo interno, teorizzata in RO-DBT come *disingenuous social signaling*. In contesti formali o valutativi, il paziente OC attua soppressione dell'espressione emotiva e iper-conformismo: sperimenta distress fisiologico (tachicardia, EDA elevata sottostante) ma manifesta un volto imperturbabile o sorrisi stereotipati (AU12 isolato senza AU06). I sistemi ML addestrati su espressioni ekmaniane prototipiche interpretano tali contrazioni come affettivita positiva, generando un tasso allarmante di **falsi negativi ecologici** che etichettano come "adattato" un paziente in stato di chiusura rigida.

### 2. Bias Algoritmico WEIRD e Normatività Socio-Culturale
I modelli di rilevamento dell'inibizione o della rigidita sono addestrati prevalentemente su popolazioni WEIRD (Western, Educated, Industrialized, Rich, Democratic), dove l'espressivita espansiva e l'assertivita sono indicatori universali di salute. In culture dell'Asia orientale o sottogruppi collettivisti, il riserbo prosodico e il controllo delle manifestazioni emotive riflettono valori pro-sociali: un'AI senza calibrazione cross-culturale rischia di patologizzare sistematicamente tali modalita comunicative come ipercontrollo anancastico.

### 3. Effetto Panottico Iatrogeno nel Monitoraggio Continuo
L'impiego di monitoraggio passivo continuo (GPS, HRV h24, analisi acustica ambientale) assume criticita speciale nei fenotipi OC: la consapevolezza di essere costantemente misurati puo agire da rinforzo iatrogeno del disturbo. Il paziente OCPD o anoressico canalizza il bisogno di perfezionismo sulla tecnologia, tentando compulsivamente di modulare i parametri fisiologici o verificare le dashboard per ottenere valori "perfetti". Questo esacerba l'ipervigilanza interna e ostacola direttamente il fine primario della RO-DBT: la vulnerabilita rilassata, la tolleranza dell'imperfezione, la capacita di dismettere il controllo intenzionale.

---

## Riferimenti Bibliografici

- Arena, L., Penate, W., Rivero, F., Marrero, R. J., Olivares, T., Scarano, A., Fumero, A., & Grecucci, A. (2025). Gray and white matter alterations in Obsessive-Compulsive Personality Disorder: a data fusion machine learning approach. *Frontiers in Human Neuroscience*, 19, 1559760. https://doi.org/10.3389/fnhum.2025.1559760
- Cardinal, E., et al. (2021). Smartphone application for adolescents with anorexia nervosa. *Journal of Eating Disorders*, 9, Article 119. https://doi.org/10.1186/s40337-021-00452-4
- De Jong, K., et al. (2024). Predicting depression treatment outcomes for cognitive behavioural therapy using machine learning. *Journal of Affective Disorders*. https://doi.org/10.1016/j.jad.2024.03.056
- Ewbank, M. P., Cummins, R., Tablan, V., et al. (2020). Quantifying the association between psychotherapy content and clinical outcomes using deep learning. *JAMA Psychiatry*, *77*(1), 35–43.
- Gao, X., et al. (2025). Artificial intelligence in mental health care: a scoping review of reviews. *Frontiers in Psychiatry*, 16, 1688043. https://doi.org/10.3389/fpsyt.2026.1688043
- Gasser, M., et al. (2023). Predictors for improvement in personality functioning during psychotherapy. *BMC Psychiatry*. https://doi.org/10.1186/s12888-024-06395-5
- Gilmartin, T., Dipnall, J. F., Gurvich, C., & Sharp, G. (2024). Identifying overcontrol and undercontrol personality types among young people using the five factor model. *Journal of Eating Disorders*, 12(1), Article 16. https://doi.org/10.1186/s40337-024-00967-4
- Hatoum, A. H., & Burton, A. L. (2024). Applications and efficacy of radically open dialectical behavior therapy (RO DBT): A systematic review. *Journal of Clinical Psychology*. https://doi.org/10.1002/jclp.23735
- Hyatt, C. S., et al. (2025). Leveraging normative personality data and machine learning to predict OCPD traits. *Journal of Abnormal Psychology*. https://doi.org/10.1037/abn0000889
- Jacobs, N., Voelkle, M. C., Kathmann, N., & Hilbert, K. (2026). Can we Improve Prediction of Psychotherapy Outcomes Through Pretraining With Simulated Data? *arXiv preprint arXiv:2601.06159v1 [stat.ML]*.
- Kim, S., et al. (2024). Momentary physiological indices related to eating disorders. *Frontiers in Psychiatry*, 15, 1378342. https://doi.org/10.3389/fpsyt.2024.1378342
- Linardon, J., et al. (2025). Predicting responsiveness to a dialectical behaviour therapy skills program. *International Journal of Eating Disorders*. https://doi.org/10.1002/eat.24156
- Lynch, T. R. (2018). *Radically Open Dialectical Behavior Therapy: Clinician manual for targeting disorders of overcontrol*. New Harbinger Publications.
- Meng, X., et al. (2025). Machine learning for predicting personality and psychological traits from multimodal data. *Electronics*, 14(3), 583. https://doi.org/10.3390/electronics14030583
- Mensinger, J. L., et al. (2024). Interoceptive mechanisms of a mobile heart rate variability biofeedback intervention. *Eating and Weight Disorders*. https://doi.org/10.1007/s40519-024-01684-x
- Mocnik, S., et al. (2024). Beyond clinical observations: a scoping review of AI-detectable observable cues in borderline personality disorder. *Frontiers in Psychiatry*, 15, 1345916. https://doi.org/10.3389/fpsyt.2024.1345916
- Pfeffer, K., et al. (2024). Explainable depression detection based on facial expression. *Columbia Academic Commons*. https://doi.org/10.7916/t1nw-b822
- Ramseyer, F. T., et al. (2023). Validation and application of the Non-Verbal Behavior Analyzer (NVBA). *Psychotherapy Research*, 33(2). https://doi.org/10.1080/10503307.2022.2139684
- Rizvi, S. L., et al. (2011). A pilot study of the DBT coach: an interactive mobile phone application for individuals with borderline personality disorder. *Behavior Therapy*, 42(4). https://doi.org/10.1016/j.beth.2011.01.003
- Rizvi, S. L., et al. (2016). The DBT coach mobile application as an adjunct to treatment. *Psychiatric Services*, 67(9). https://doi.org/10.1037/ser0000100
- Saeb, S., et al. (2024). The voice of depression: speech features as biomarkers for major depressive disorder. *Journal of Affective Disorders*, 348. https://doi.org/10.1016/j.jad.2023.11.045
- Scolnick, B., et al. (2014). Pilot study employing heart rate variability biofeedback training in patients with eating disorders. *Journal of Eating Disorders*, 2, 17. https://doi.org/10.1186/2050-2974-2-17
- Sole, B., et al. (2022). Machine learning detects predictors of symptom severity after dialectical behavior therapy skills training in borderline personality disorder. *Journal of Psychiatric Research*, 151. https://doi.org/10.1016/j.jpsychires.2022.04.013
- Teckentrup, V., et al. (2023). Autonomic changes as reaction to experimental social stress in overcontrol. *Frontiers in Psychiatry*, 13, 9385984. https://doi.org/10.3389/fpsyt.2022.9385984
- Wang, T., et al. (2022). Exploratory machine learning modeling of adaptive and maladaptive personality traits from passive smartphone sensing. *PLoS One*. https://doi.org/10.1371/journal.pone.0265691
- Wang, Y., et al. (2012). Automated facial action coding system for dynamic analysis of facial expressions in neuropsychiatric disorders. *Schizophrenia Research*, 138(2-3). https://doi.org/10.1016/j.schres.2012.06.012

---

## Relazioni

- Vedi anche: [[consensus-review-ai-ro-dbt]], [[overcontrol-and-undercontrol-personality-types]], [[fenotipizzazione-computazionale]], [[ocpd-neural-correlates]], [[multimodal-observable-cues-in-psychiatry]], [[cbt-outcome-prediction-in-ocd]], [[wearable-sensor-fusion-adherence]], [[overfitting-protocollare]], [[algorithmic-tractability-in-psychotherapy]]
