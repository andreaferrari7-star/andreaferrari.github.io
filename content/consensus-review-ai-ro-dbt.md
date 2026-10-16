---
tags: [ro-dbt, overcontrol, artificial-intelligence, cluster-c, outcome-prediction, nlp, digital-phenotyping, literature-gap, systematic-review, machine-learning]
tipo_fonte: [scientifica, interna]
source_papers: ["Agisci_come_un_Information_Specialist_e_ricercator.pdf"]
---

# Stato dell'Arte su AI, RO-DBT e Overcontrol (Consensus Review)

## Definizione Operativa

- Revisione sintetica dello stato della letteratura che esplora i gap e le opportunita dell'impiego di NLP, predizione di outcome, sensing passivo e IA generativa nella RO-DBT e per i fenotipi di overcontrol/Cluster C.
- **Utilita CBT / Applicativa:** Mappa sistematicamente i "confini operativi" dell'AI applicata all'ipercontrollo, distinguendo: (a) dove esistono evidenze validate; (b) dove il clinico/ricercatore deve attingere a letteratura adiacente per analogia; (c) dove il gap e totale e la ricerca e urgente.

---

## Evidenze dalla Letteratura

### Gap Fondamentale: Assenza di Letteratura AI Nativa per la RO-DBT

Il gap piu grave e strutturale riguarda l'assenza quasi completa di RCT o studi clinici validati peer-reviewed che applichino IA generativa, NLP o predittori ML specificamente alle sessioni o al modello manualizzato della RO-DBT (Hatoum & Burton, 2024). Non esistono modelli ML pubblicati addestrati su dati RO-DBT, ne sistemi conversazionali validati per il trattamento dei fenotipi OC. I trial registrativi della RO-DBT (incluso il multicentrico *REFRAMED* di Lynch) hanno impiegato esclusivamente modelli statistici classici (LMM).

Di conseguenza, l'intera architettura computazionale per l'overcontrol deve essere costruita "per traslazione" da quattro corpora adiacenti: (1) DBT standard e psicoterapia strutturata; (2) disturbi con fenotipo OC (anoressia nervosa, OCD, OCPD); (3) analisi computazionale della personalita di Cluster C; (4) digital phenotyping dei segnali fisiologici e comportamentali dell'inibizione.

---

### Area 1 — ML per la Predizione degli Esiti Psicoterapeutici

I modelli predittivi supervisionati e non supervisionati rivelano tre pattern critici per l'OC:

- **Feature baseline insufficienti:** I dati demografici e le scale autosomministrate al baseline falliscono la predizione (AUC ~0.50), mentre l'integrazione di serie temporali d'uso digitale e parametri dinamici longitudinali predice efficacemente il drop-out (AUC elevata) (Linardon et al., 2025).
- **Fenotipizzazione computazionale:** La cluster analysis non supervisionata (hierarchical clustering + k-means) sulle 30 faccette del FFM isola empiricamente i cluster OC, UC e Resiliente come fenotipi distinti con psicopatologia e traiettorie differenziali (Gilmartin et al., 2024). L'analisi a livello di faccette e nettamente superiore ai 5 domini generali.
- **Random Forest e modelli ensemble:** Superano le regressioni lineari per identificare tassi di dropout e risposta al trattamento quando integrano parametri dinamici come la capacita di "non-judging" — variabile rilevante specificamente per i fenotipi OC (Sole et al., 2022; Bennemann et al., 2022). Giesemann et al. (2023) riportano Random Forest con identificazione del dropout al 63.4%, superiore ai modelli lineari classici.
- **Rigidita relazionale come predittore cardine:** La compromissione delle attivita sociali e la rigidita relazionale — marker centrali dell'ipercontrollo — emergono come predittori primari di mancato miglioramento in modelli basati su alberi decisionali e regressioni penalizzate (Gasser et al., 2023).
- **Generalizzabilita esterna:** La validazione esterna su coorti ampie (N > 300) rimane rara; una meta-analisi recente ha dimostrato capacita predittiva generalizzabile in 5 coorti su 7 (De Jong et al., 2024).

---

### Area 2 — NLP e Speech Processing in Psicoterapia

I costrutti adiacenti al "social signaling" dell'OC — alleanza terapeutica, non-fluency verbale, uso dei pronomi di prima persona, varianza prosodica — sono gia codificabili tramite marker linguistici e acustici (Ryu et al., 2023; Saeb et al., 2024):

- **Pronomi e non-fluency:** L'uso di pronomi di prima persona singolare (io, me) e le disfluenze verbali sono stati identificati come marker dell'alleanza terapeutica tramite NLP (Ryu et al., 2023). Questi costrutti sono direttamente rilevanti per l'overcontrol, dove la soppressione del riferimento egoriferito segnala distanza emotiva.
- **Acustica vocale:** La varianza della frequenza fondamentale (F0), il jitter, lo shimmer e la durata delle pause discriminano con elevata accuratezza il livello di inibizione affettiva nei campioni clinici (Saeb et al., 2024).
- **Limiti architetturali:** Le architetture limitate al solo testo mancano di validita ecologica per l'OC perche trascurano prosodia e faccialita — canali in cui l'overcontrol esprime primariamente il suo mascheramento (Ryu et al., 2023). Questo giustifica l'approccio multimodale.
- **Fidelity computazionale:** Sistemi di deep learning (HAN) classificano automaticamente la fidelity clinica del terapeuta con AUC elevata; il volume di interventi specifici predice il tasso di miglioramento del paziente (Ewbank et al., 2020).

---

### Area 3 — Digital Phenotyping e HRV

Sebbene l'HRV sia la misura piu citata per quantificare la self-regulation, l'overcontrol esibisce relazioni feature-costrutto non lineari e paradossali che rendono necessario un approccio item-level (Lekkas et al., 2023; Shen et al., 2025):

- **Paradosso HRV dell'OC:** I pazienti OC mostrano valori paradossalmente elevati di RMSSD e HF-HRV a riposo — non indicatori di rilassamento ma di iper-regolazione vagale rigida non adattiva. La distinzione rispetto al profilo UC o resiliente richiede la misurazione della *reattivita fasica* durante stimoli di ingaggio sociale (Teckentrup et al., 2023).
- **Feature item-level vs score totali:** Passare da score totali di HRV o GPS a predizione basata su feature/item granulari e cruciale per la sensoristica passiva nei fenotipi OC (Lekkas et al., 2023).
- **Firma passiva dell'OC:** Estrema regolarita GPS (bassa entropia spaziale), pattern circadiano inflessibile, ridotte variazioni cinetiche (*keystroke dynamics*), bradicardia e ridotta EDA tonica nei campioni restrittivi (Kim et al., 2024; Wang et al., 2022).
- **Tratti PID-5 da smartphone:** Lasso, Random Forest e XGBoost predicono accuratamente tratti maladattivi dimensionali (PID-5) da tracce di mobilita GPS, sblocchi schermo e log chiamate (Wang et al., 2022).

---

### Area 4 — Cluster C: Asimmetria e Gap della Ricerca

Esiste un grave "literature gap" a favore del Cluster B (BPD) rispetto al Cluster C (OCPD, AVPD, DPD):
- Nessuna scoping review o meta-analisi circoscritta esclusivamente all'AI nei disturbi di Cluster C e stata registrata su PROSPERO (Mocnik et al., 2024; Gao et al., 2025).
- La ricerca di neuroimaging con ML ha comunque isolato alterazioni strutturali OCPD-specifiche in network fronto-striatali e DMN/Salience (Arena/Sepe et al., 2025), e tratti OCPD predibili da dati FFM normativi tramite Elastic Net, SVR e Gradient Boosting (Hyatt et al., 2025).
- La concentrazione della ricerca su disturbi affettivi e Cluster B introduce un sistematico reporting bias: i modelli AI sono spesso ottimizzati per rispondere ai comportamenti impulsivi, acuti e misurabili del discontrollo emotivo, piuttosto che alla rigidita cronica e inibita dell'overcontrol (Aafjes-van Doorn et al., 2021).

---

### Area 5 — Rischi Specifici per i Fenotipi OC

Tre rischi clinicamente critici distinguono l'AI applicata all'overcontrol rispetto agli altri fenotipi:

1. **Falsi negativi ecologici da masking:** I sistemi CV/ML addestrati su espressioni ekmaniane prototipiche etichettano il sorriso di acquiescenza OC (AU12 senza AU06) come affettivita positiva, classificando come "adattato" un paziente in stato di chiusura rigida.
2. **Effetto Panottico iatrogeno:** Il monitoraggio digitale continuo puo diventare un amplificatore iatrogeno dell'ipercontrollo, permettendo al paziente OC di canalizzare il perfezionismo sul controllo ossessivo dei parametri fisiologici (dashboard HRV, GPS, sonno). Questo ostacola direttamente il target primario della RO-DBT: dismettere il controllo intenzionale.
3. **Bias WEIRD e normatività culturale:** I modelli di rilevamento dell'inibizione sono calibrati su norme espressive occidentali; in culture collettiviste il riserbo prosodico e il controllo delle emozioni riflettono valori pro-sociali, non patologia. L'AI rischia di patologizzare sistematicamente tali modalita comunicative come ipercontrollo anancastico.

---

## Riferimenti Bibliografici

- Aafjes-van Doorn, K., et al. (2021). Machine learning in psychotherapy research and practice. *Psychotherapy Research*, 31(4). https://doi.org/10.1080/10503307.2021.1898372
- Arena, L., Penate, W., Rivero, F., Marrero, R. J., Olivares, T., Scarano, A., Fumero, A., & Grecucci, A. (2025). Gray and white matter alterations in OCPD: a data fusion machine learning approach. *Frontiers in Human Neuroscience*, 19, 1559760. https://doi.org/10.3389/fnhum.2025.1559760
- Bennemann, B., Schwartz, B., Giesemann, J., & Lutz, W. (2022). Predicting patients who will drop out of out-patient psychotherapy using machine learning algorithms. *The British Journal of Psychiatry*, 220, 192–201. https://doi.org/10.1192/bjp.2022.17
- De Jong, K., et al. (2024). Predicting depression treatment outcomes for CBT using machine learning. *Journal of Affective Disorders*. https://doi.org/10.1016/j.jad.2024.03.056
- Ewbank, M. P., et al. (2020). Quantifying the association between psychotherapist competence and patient outcomes. *JAMA Psychiatry*, 77(4). https://doi.org/10.1001/jamapsychiatry.2019.2664
- Gao, X., et al. (2025). Artificial intelligence in mental health care: a scoping review of reviews. *Frontiers in Psychiatry*, 16, 1688043. https://doi.org/10.3389/fpsyt.2026.1688043
- Gasser, M., et al. (2023). Predictors for improvement in personality functioning during psychotherapy. *BMC Psychiatry*. https://doi.org/10.1186/s12888-024-06395-5
- Gilmartin, T., Dipnall, J. F., Gurvich, C., & Sharp, G. (2024). Identifying overcontrol and undercontrol personality types among young people using the five factor model. *Journal of Eating Disorders*, 12(1). https://doi.org/10.1186/s40337-024-00967-4
- Hatoum, A. H., & Burton, A. L. (2024). Applications and efficacy of radically open dialectical behavior therapy (RO DBT): A systematic review. *Journal of Clinical Psychology*. https://doi.org/10.1002/jclp.23735
- Hyatt, C. S., et al. (2025). Leveraging normative personality data and machine learning to predict OCPD traits. *Journal of Abnormal Psychology*. https://doi.org/10.1037/abn0000889
- Kim, S., et al. (2024). Momentary physiological indices related to eating disorders — a wearable review. *Frontiers in Psychiatry*, 15, 1378342. https://doi.org/10.3389/fpsyt.2024.1378342
- Lekkas, D., Gyorda, J. A., Price, G. D., & Jacobson, N. (2023). Depression deconstructed: wearables and passive digital phenotyping for analyzing individual symptoms. *Behaviour Research and Therapy*, 168. https://doi.org/10.1016/j.brat.2023.104382
- Linardon, J., et al. (2025). Predicting responsiveness to a DBT skills program. *International Journal of Eating Disorders*. https://doi.org/10.1002/eat.24156
- Lynch, T. R. (2018). *Radically Open Dialectical Behavior Therapy: Clinician manual for targeting disorders of overcontrol*. New Harbinger Publications.
- Mocnik, S., et al. (2024). Beyond clinical observations: a scoping review of AI-detectable observable cues in BPD. *Frontiers in Psychiatry*, 15, 1345916. https://doi.org/10.3389/fpsyt.2024.1345916
- Ryu, J., Heisig, S., McLaughlin, C., Katz, M., Mayberg, H., & Gu, X. (2023). A natural language processing approach reveals first-person pronoun usage and non-fluency as markers of therapeutic alliance. *iScience*, 26. https://doi.org/10.1016/j.isci.2023.106860
- Saeb, S., et al. (2024). The voice of depression: speech features as biomarkers for major depressive disorder. *Journal of Affective Disorders*, 348. https://doi.org/10.1016/j.jad.2023.11.045
- Sole, B., et al. (2022). Machine learning detects predictors of symptom severity after DBT skills training in BPD. *Journal of Psychiatric Research*, 151. https://doi.org/10.1016/j.jpsychires.2022.04.013
- Teckentrup, V., et al. (2023). Autonomic changes as reaction to experimental social stress in overcontrol. *Frontiers in Psychiatry*, 13. https://doi.org/10.3389/fpsyt.2022.9385984
- Wang, T., et al. (2022). Exploratory machine learning modeling of adaptive and maladaptive personality traits from passive smartphone sensing. *PLoS One*. https://doi.org/10.1371/journal.pone.0265691

---

## Relazioni

- Vedi anche: [[applicazioni-computazionali-ro-dbt-overcontrol]], [[overcontrol-and-undercontrol-personality-types]], [[fenotipizzazione-computazionale]], [[ocpd-neural-correlates]], [[multimodal-observable-cues-in-psychiatry]], [[algorithmic-tractability-in-psychotherapy]], [[cbt-outcome-prediction-in-ocd]]
