---
tags: [ro-dbt, overcontrol, artificial-intelligence, machine-learning, digital-phenotyping, nlp, cluster-c, ocpd, outcome-prediction, passive-sensing, hrv-biofeedback, facs, eating-disorders, transdiagnostico, rassegna]
tipo_fonte: [scientifica, interna]
source_papers: ["Ricerca Computazionale RO-DBT e Overcontrol.md", "Agisci_come_un_Information_Specialist_e_ricercator.pdf", "40337_2024_Article_967.pdf", "fnhum-19-1559760.pdf", "2601.06159v1.pdf", "mjiri-39-30.pdf", "mhealth-2024-1-e63316.pdf"]
---

# Rassegna degli Studi: IA per la Comprensione e il Trattamento dell'Ipercontrollo

## Definizione Operativa

- Rassegna sistematica degli studi in cui metodi di intelligenza artificiale (machine learning, NLP, affective computing, digital phenotyping) sono stati impiegati per incrementare la comprensione e il trattamento delle problematiche da ipercontrollo (*overcontrol*, OC): un fenotipo transdiagnostico di personalita caratterizzato da eccessiva inibizione comportamentale, perfezionismo rigido e mascheramento emotivo cronico, teorizzato e trattato nel quadro della Radically Open Dialectical Behavior Therapy (RO-DBT; Lynch, 2018).
- **Utilita CBT / Applicativa:** Sintetizza sei linee di ricerca computazionale che convergono sul fenotipo OC — pur in assenza di letteratura AI nativa specifica per la RO-DBT — per orientare ricercatori e clinici verso le evidenze esistenti, i gap critici e i rischi iatrogeni specifici dell'applicazione tecnologica a questo profilo.

> **Nota metodologica:** La wiki non contiene fonti dedicate a trial RO-DBT computazionali. La rassegna e costruita per traslazione da quattro corpora adiacenti: (1) DBT standard e psicoterapia strutturata; (2) disturbi con fenotipo OC (anoressia nervosa, OCD, OCPD); (3) analisi computazionale della personalita di Cluster C; (4) digital phenotyping dei segnali fisiologici e comportamentali dell'inibizione.

---

## Evidenze dalla Letteratura

### Linea 1 — Fenotipizzazione Computazionale dei Tipi di Personalita (Cluster Analysis)

La fenotipizzazione computazionale non supervisionata dei tipi di personalita costituisce il fondamento empirico per identificare e isolare il fenotipo OC all'interno di dataset psicometrici complessi.

**Contributo principale:** La cluster analysis gerarchica (metodo di Ward) + k-means applicata alle 30 faccette dell'FFM (N=561 giovani adulti) isola empiricamente tre cluster distinti: Overcontrol (33,7%), Undercontrol (29,5%) e Resiliente (36,8%). Il cluster OC presenta elevato nevroticismo internalizzante (ansia, vergogna, timidezza sociale, vulnerabilita allo stress), ridotta estroversione, coscienziosita doveristica e rigida aderenza morale. L'analisi a livello di faccette e nettamente superiore ai 5 domini generali dell'FFM nell'intercettare differenze cliniche qualitative (Gilmartin et al., 2024).

**Evidenze associate:**
- Entrambi i profili OC (44%) e UC (52,4%) superano la soglia clinica EDE-QS ≥ 15 vs il 21% dei resilienti (chi-quadro = 43.57, p < 0.001); il profilo UC mostra specificamente condotte disinibite (abbuffate, purging, esercizio compulsivo) assenti nell'OC (Gilmartin et al., 2024).
- Appartenenza a OC o UC predice significativamente maggiori livelli DASS-21 nelle regressioni multivariate (Gilmartin et al., 2024).
- Modelli Elastic Net, SVR e Gradient Boosting predicono tratti OCPD da dati FFM normativi con associazione all'ispessimento corticale del giro frontale superiore destro (Hyatt et al., 2025).

**Limite chiave:** Campione di convenienza, disegno trasversale, dataset non clinico; l'approccio unsupervised non permette validazione esterna su coorti indipendenti.

---

### Linea 2 — Neuroimaging e Machine Learning per i Correlati Cerebrali dell'OCPD

L'applicazione di tecniche di ML al neuroimaging strutturale ha prodotto le prime evidenze di correlati neurali specifici dell'OCPD, distinti dall'OCD.

**Contributo principale:** Parallel Independent Component Analysis (pICA) — approccio non supervisionato di data fusion su MRI strutturale (materia grigia e bianca) — su N=30 pazienti OCPD vs N=34 controlli. Il network GM-05 (DMN + Salience Network: cingolato anteriore, giro frontale mediale, insula) mostra volume maggiore negli OCPD, direttamente correlato ai livelli di ansia clinica. Questo profilo di iperconnettivita strutturale — distinto dai circuiti cortico-striatali orbitofrontali dell'OCD — riflette ruminazione, introspezione eccessiva e disorganizzazione del controllo cognitivo (Arena/Sepe et al., 2025).

**Implicazione clinica:** Fornisce razionale neurobiologico per la pervasivita e la resistenza al cambiamento dei tratti OC in terapia. La rigidita non e solo cognitiva ma strutturalmente inscritta nei circuiti dell'elaborazione autoreferenziale.

**Limite chiave:** N=30; campione sbilanciato (73% donne); assenza di correlazioni con dati funzionali task-based.

---

### Linea 3 — Predizione degli Esiti della CBT tramite ML

I modelli predittivi supervisionati rivelano pattern critici per la gestione computazionale dell'OC.

**Contributi principali:**

| Studio | Metodo | Target | Risultato chiave |
|---|---|---|---|
| Gilmartin et al. (2024) | Hierarchical Clustering + k-means + RF | Fenotipizzazione OC/UC in FFM | Cluster OC distinto e clinicamente significativo |
| Sole et al. (2022) | Lasso + Random Forest, nested 10-fold CV | Risposta a DBT skills training (BPD) | "Non-judging" e parametri dinamici predicono il successo; rilevante per OC |
| Linardon et al. (2025) | 10 algoritmi (RF, Elastic Net, SVR) | Drop-out da DBT skills in disturbi alimentari | Baseline fallisce (AUC ~0.50); serie temporali digitali predicono il drop-out efficacemente |
| De Jong et al. (2024) | Meta-analisi di modelli ML supervisionati | Risposta alla psicoterapia strutturata | Capacita predittiva generalizzabile in 5/7 coorti |
| Gasser et al. (2023) | Alberi decisionali + regressioni penalizzate | Funzionamento di personalita in psicoterapia | Rigidita relazionale e compromissione sociale = predittori cardine di mancato miglioramento |
| Jacobs et al. (2026) | Random Forest ibrido + pretraining MVND + MCCV (100 iter.) | Risposta e remissione CBT nell'OCD | Pretraining da letteratura: +2.2% acc. (Studio 1, non significativo); degrada in Studio 2; scarsita di statistiche sottogruppo = collo di bottiglia principale |
| Bennemann et al. (2022) | Random Forest vs regressioni lineari | Dropout in psicoterapia ambulatoriale | RF identifica dropout al 63.4%, superiore ai modelli lineari classici |

**Pattern critico per l'OC:** I pazienti ipercontrollati mantengono un'aderenza esteriore rigida ai programmi terapeutici che puo mascherare totale assenza di cambiamento metacognitivo — rendendo la predizione del dropout e della non-risposta particolarmente urgente e difficile.

---

### Linea 4 — Digital Phenotyping dell'Overcontrol tramite Dati Passivi

Il sensing passivo continuo quantifica il fenotipo OC tramite segnali biologici e comportamentali rilevati ecologicamente, senza distorsioni da autovalutazione retrospettiva.

**Firma biologica paradossale dell'OC:**
- HRV elevata (RMSSD, HF-HRV) a riposo non come indicatore di rilassamento, ma come iper-regolazione vagale rigida e non adattiva. Il blocco della variabilita fasica durante stimoli di ingaggio sociale distingue l'OC dai profili resilienti (Teckentrup et al., 2023).
- Bradicardia e ridotta EDA tonica nelle popolazioni restrittive/OC (Kim et al., 2024).

**Firma comportamentale passiva dell'OC:**
- Estrema regolarita GPS (bassa entropia spaziale), pattern circadiano inflessibile, latenze ridotte nelle risposte formali, variazioni cinetiche ridotte alla tastiera (*keystroke dynamics*) — tutti indicatori oggettivi di perfezionismo e controllo motorio esasperato (Wang et al., 2022).

| Studio | Metodo | Outcome |
|---|---|---|
| Kim et al. (2024) | Revisione sistematica wearable in AN | Bradicardia, EDA ridotta e HRV atipicamente elevata nelle popolazioni OC/restrittive |
| Wang et al. (2022) | Lasso + RF + XGBoost, Leave-One-Participant-Out | Predizione accurata di tratti PID-5 e rigidita da GPS, sblocchi schermo, log chiamate |
| Meng et al. (2025) | Bimodal GRU + FACS (OpenFace) + posture | Predizione ottimale di ansia inibitoria e tratti anancastici da co-occorrenza AU07, AU15 e postura |
| Pfeffer et al. (2024) | OpenFace 2.0 vs codifiche manuali FACS | Congelamento mimico e soppressione facciale predicono longitudinalmente sintomi rigidi |
| Teckentrup et al. (2023) | Analisi tempo-frequenza RMSSD + EDA (paradigma Cyberball) | I soggetti OC mostrano assenza di reattivita fasica e blocco dell'ingaggio vagale durante l'esclusione sociale |

---

### Linea 5 — Clinical NLP, Speech Processing e Fidelity Computazionale

I costrutti centrali del "social signaling" OC — varianza prosodica, uso dei pronomi, non-fluency, ipo-espressivita mimica — sono gia codificabili computazionalmente, pur in assenza di studi specifici su sedute RO-DBT.

**Contributi principali:**
- **Pronomi e non-fluency:** L'uso di pronomi di prima persona e le disfluenze verbali sono marker NLP dell'alleanza terapeutica (Ryu et al., 2023). Nell'OC, la soppressione del riferimento egoriferito segnala distanza emotiva — variabile computazionalmente intercettabile.
- **Acustica vocale (F0, jitter, shimmer):** La varianza della frequenza fondamentale discrimina con elevata accuratezza il livello di inibizione affettiva (Saeb et al., 2024).
- **Fidelity computazionale:** Sistemi HAN (deep learning su NLP) classificano automaticamente la fidelity clinica del terapeuta con AUC elevata; il volume di interventi specifici predice il miglioramento del paziente (Ewbank et al., 2020).
- **FACS + OpenFace:** Pipeline multimodali (OpenFace, OpenPose, SVM + Active Appearance Models) quantificano piattezza affettiva, inappropriatezza espressiva e masking facciale (Wang et al., 2012; Ramseyer et al., 2023; Mocnik et al., 2024).
- **Architetture multimodali:** I modelli Transformer audio-visivi mappano la disconnessione tra contenuto semantico ed espressione non verbale — la firma centrale del *disingenuous social signaling* OC (Mocnik et al., 2024).

**Limite strutturale:** Nessun modello e stato applicato a sedute RO-DBT. Le architetture solo-testo mancano di validita ecologica per l'OC, che esprime il mascheramento primariamente nel canale prosodicofacciale (Ryu et al., 2023).

---

### Linea 6 — Interventi Digitali e App per Disturbi Adiacenti all'OC

| Studio | Intervento | Target | Risultato |
|---|---|---|---|
| Mensinger et al. (2024) | HRV-biofeedback mHealth (~0.1 Hz) | Operatori sanitari a rischio per disturbi alimentari | Incremento consapevolezza interocettiva (MAIA-2), attenuazione sintomatologia restrittiva |
| Scolnick et al. (2014) | Biofeedback coerenza cardiaca | Pazienti ospedalizzati con anoressia nervosa | Incremento HRV e riduzione ansia di stato; fattibilita e sicurezza confermate |
| Cardinal et al. (2021) | App gamificata CBT/DBT per ipercontrollo emotivo | Pazienti adulte con anoressia nervosa | Aderenza eccellente; validazione moduli per tolleranza della vulnerabilita emotiva |
| Mohammadi et al. (2025) | Blended CBT (face-to-face + app web) vs CBT standard | Perfezionismo maladattivo in studenti universitari | Equivalenza terapeutica; apertura a scalabilita digitale per il tratto OC |
| Lee Yoon Li et al. (2024) | App mHealth (Intellect) per ERP autoguidata | OCD subclinico in studenti universitari | Efficacia non moderata negativamente dal perfezionismo maladattivo — utile in profili OC con OCD subclinico |

---

## Limiti Critici e Rischi Specifici per i Fenotipi OC

### 1. Falsi Negativi Ecologici da Masking Sociale
I sistemi ML per il riconoscimento delle emozioni, addestrati su espressioni ekmaniane prototipiche, interpretano il sorriso di acquiescenza OC (AU12 senza AU06, senza attivazione dell'orbicolare dell'occhio) come affettivita positiva — classificando come "adattato" un paziente in stato di chiusura rigida o sofferenza inibita. Questo introduce un tasso allarmante di falsi negativi ecologici (Mocnik et al., 2024).

### 2. Effetto Panottico Iatrogeno nel Monitoraggio Continuo
La consapevolezza di essere costantemente misurati da sensori e algoritmi puo agire da rinforzo iatrogeno dell'ipercontrollo: il paziente OCPD o anoressico canalizza il bisogno di perfezionismo sul controllo ossessivo dei parametri fisiologici (dashboard HRV, GPS, sonno). Questo esacerba l'ipervigilanza interna e ostacola direttamente il fine primario della RO-DBT — dismettere il controllo intenzionale e tollerare l'imperfezione.

### 3. Bias WEIRD e Normatività Culturale
I modelli sono calibrati su norme espressive occidentali; in culture collettiviste il riserbo prosodico e il controllo delle emozioni riflettono valori pro-sociali. L'AI rischia di classificare tali modalita come ipercontrollo anancastico, incorrendo in patologizzazione algoritmica etnocentrica.

### 4. Gap di Letteratura Strutturale
- Assenza totale di RCT o trial peer-reviewed su chatbot/DTx dedicati esclusivamente alla RO-DBT (Hatoum & Burton, 2024).
- Nessuna scoping review o meta-analisi registrata (PROSPERO) esclusivamente sui disturbi di Cluster C (Gao et al., 2025).
- I trial RO-DBT hanno impiegato esclusivamente LMM, senza ML per feature selection o predizione individuale.
- Nessun modello NLP/speech applicato a sedute RO-DBT.

---

## Riferimenti Bibliografici

- Arena, L., Penate, W., Rivero, F., Marrero, R. J., Olivares, T., Scarano, A., Fumero, A., & Grecucci, A. (2025). Gray and white matter alterations in Obsessive-Compulsive Personality Disorder: a data fusion machine learning approach. *Frontiers in Human Neuroscience*, 19, 1559760. https://doi.org/10.3389/fnhum.2025.1559760
- Bennemann, B., Schwartz, B., Giesemann, J., & Lutz, W. (2022). Predicting patients who will drop out of out-patient psychotherapy using machine learning algorithms. *The British Journal of Psychiatry*, 220, 192–201. https://doi.org/10.1192/bjp.2022.17
- Cardinal, E., et al. (2021). Smartphone application for adolescents with anorexia nervosa. *Journal of Eating Disorders*, 9, Article 119. https://doi.org/10.1186/s40337-021-00452-4
- De Jong, K., et al. (2024). Predicting depression treatment outcomes for cognitive behavioural therapy using machine learning. *Journal of Affective Disorders*. https://doi.org/10.1016/j.jad.2024.03.056
- Ewbank, M. P., et al. (2020). Quantifying the association between psychotherapist competence and patient outcomes. *JAMA Psychiatry*, 77(4). https://doi.org/10.1001/jamapsychiatry.2019.2664
- Gao, X., et al. (2025). Artificial intelligence in mental health care: a scoping review of reviews. *Frontiers in Psychiatry*, 16, 1688043. https://doi.org/10.3389/fpsyt.2026.1688043
- Gasser, M., et al. (2023). Predictors for improvement in personality functioning during psychotherapy. *BMC Psychiatry*. https://doi.org/10.1186/s12888-024-06395-5
- Gilmartin, T., Dipnall, J. F., Gurvich, C., & Sharp, G. (2024). Identifying overcontrol and undercontrol personality types among young people using the five factor model. *Journal of Eating Disorders*, 12(1), Article 16. https://doi.org/10.1186/s40337-024-00967-4
- Hatoum, A. H., & Burton, A. L. (2024). Applications and efficacy of radically open dialectical behavior therapy (RO DBT): A systematic review. *Journal of Clinical Psychology*. https://doi.org/10.1002/jclp.23735
- Hyatt, C. S., et al. (2025). Leveraging normative personality data and machine learning to predict OCPD traits. *Journal of Abnormal Psychology*. https://doi.org/10.1037/abn0000889
- Jacobs, N., Voelkle, M. C., Kathmann, N., & Hilbert, K. (2026). Can we improve prediction of psychotherapy outcomes through pretraining with simulated data? *arXiv preprint arXiv:2601.06159v1 [stat.ML]*.
- Kim, S., et al. (2024). Momentary physiological indices related to eating disorders: a wearable review. *Frontiers in Psychiatry*, 15, 1378342. https://doi.org/10.3389/fpsyt.2024.1378342
- Lee Yoon Li, M., Lee Si Min, S., & Sundermann, O. (2024). Efficacy of the mHealth App Intellect in improving subclinical OCD: RCT with 4-week follow-up. *JMIR Mhealth Uhealth*, 12, e63316. https://doi.org/10.2196/63316
- Linardon, J., et al. (2025). Predicting responsiveness to a dialectical behaviour therapy skills program. *International Journal of Eating Disorders*. https://doi.org/10.1002/eat.24156
- Lynch, T. R. (2018). *Radically Open Dialectical Behavior Therapy: Clinician manual for targeting disorders of overcontrol*. New Harbinger Publications.
- Meng, X., et al. (2025). Machine learning for predicting personality and psychological traits from multimodal data. *Electronics*, 14(3), 583. https://doi.org/10.3390/electronics14030583
- Mensinger, J. L., et al. (2024). Interoceptive mechanisms of a mobile heart rate variability biofeedback intervention. *Eating and Weight Disorders*. https://doi.org/10.1007/s40519-024-01684-x
- Mocnik, S., Smrke, U., Mlakar, I., Mocnik, G., Gregoric Kumperschak, H., & Plohl, N. (2024). Beyond clinical observations: a scoping review of AI-detectable observable cues in borderline personality disorder. *Frontiers in Psychiatry*, 15, 1345916. https://doi.org/10.3389/fpsyt.2024.1345916
- Mohammadi, G., Asgharnezhadfarid, A., Zahedi Tajrishi, K., Gharraee, B., & Moloodi, R. (2025). Comparative effectiveness of face-to-face CBT and blended CBT on maladaptive perfectionism. *Medical Journal of the Islamic Republic of Iran*, 39, 30. https://doi.org/10.47176/mjiri.39.30
- Pfeffer, K., et al. (2024). Explainable depression detection based on facial expression. *Columbia Academic Commons*. https://doi.org/10.7916/t1nw-b822
- Ramseyer, F. T., et al. (2023). Validation and application of the Non-Verbal Behavior Analyzer (NVBA). *Psychotherapy Research*, 33(2). https://doi.org/10.1080/10503307.2022.2139684
- Ryu, J., Heisig, S., McLaughlin, C., Katz, M., Mayberg, H., & Gu, X. (2023). A natural language processing approach reveals first-person pronoun usage and non-fluency as markers of therapeutic alliance. *iScience*, 26. https://doi.org/10.1016/j.isci.2023.106860
- Saeb, S., et al. (2024). The voice of depression: speech features as biomarkers for major depressive disorder. *Journal of Affective Disorders*, 348. https://doi.org/10.1016/j.jad.2023.11.045
- Scolnick, B., et al. (2014). Pilot study employing heart rate variability biofeedback training in patients with eating disorders. *Journal of Eating Disorders*, 2, 17. https://doi.org/10.1186/2050-2974-2-17
- Sole, B., et al. (2022). Machine learning detects predictors of symptom severity after DBT skills training in BPD. *Journal of Psychiatric Research*, 151. https://doi.org/10.1016/j.jpsychires.2022.04.013
- Teckentrup, V., et al. (2023). Autonomic changes as reaction to experimental social stress in overcontrol. *Frontiers in Psychiatry*, 13. https://doi.org/10.3389/fpsyt.2022.9385984
- Wang, T., et al. (2022). Exploratory machine learning modeling of adaptive and maladaptive personality traits from passive smartphone sensing. *PLoS One*. https://doi.org/10.1371/journal.pone.0265691
- Wang, Y., et al. (2012). Automated facial action coding system for dynamic analysis of facial expressions in neuropsychiatric disorders. *Schizophrenia Research*, 138(2-3). https://doi.org/10.1016/j.schres.2012.06.012

---

## Relazioni

- Vedi anche: [[applicazioni-computazionali-ro-dbt-overcontrol]], [[consensus-review-ai-ro-dbt]], [[overcontrol-and-undercontrol-personality-types]], [[fenotipizzazione-computazionale]], [[ocpd-neural-correlates]], [[multimodal-observable-cues-in-psychiatry]], [[maladaptive-perfectionism]], [[self-guided-mhealth-ocd]], [[gilmartin-et-al-2024]], [[arena-et-al-2025]], [[algorithmic-tractability-in-psychotherapy]], [[bollettino-iperlab-intherapy-n01-1]]
