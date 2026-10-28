---
tags: [ai-health-coursera, formazione, analytics, modelli-predittivi, qualita-dei-dati, monitoraggio-modelli, implementazione]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C2M2_JK_Dec17_2024_V1.0 (4).pdf"]
---

# AI for Healthcare Systems, C2M2: l'analisi dei dati nel DIAD (Khuntia, 2024f)

## Definizione Operativa
- Materiale di approfondimento (16 pagine, versione 1.0 del 17 dicembre 2024) del secondo modulo del corso 2 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]]. Approfondisce lo stadio dell'analisi del [[diad-framework|framework DIAD]]: che cos'è un modello analitico, di quali elementi è fatto e perché l'IA non è una «soluzione rapida» (Khuntia, 2024f).
- **Utilità CBT / Applicativa:** dà a un clinico le domande da porre prima di adottare uno strumento predittivo. Quale problema risolve? Su quali dati è stato addestrato? Come è stato validato? Chi lo monitora e lo aggiorna? Vale anche per gli strumenti che stimano rischio o esito in salute mentale.

## Evidenze dalla Letteratura

### L'analisi come fondamento
- L'analisi dei dati collega il dato grezzo alla decisione in condizioni di incertezza. Il suo contributo più importante è integrare flussi oggi separati (cartelle elettroniche, dispositivi indossabili, imaging, esiti riferiti dal paziente) in un profilo unico. Questo permette di passare da cure episodiche a cure continue e preventive (Khuntia, 2024f).
- I modelli applicati a dati longitudinali possono cogliere segnali precoci, come una fibrillazione atriale o una disfunzione renale iniziale. Il loro valore dipende dalla qualità dei dati. Servono governance dei dati, strumenti trasparenti e comprensibili per clinici e pazienti, e alfabetizzazione ai dati dei professionisti (Khuntia, 2024f).

### Il mito dell'IA come soluzione rapida
- L'idea dell'IA come strumento da collegare e accendere, con risultati immediati, è secondo il modulo uno degli equivoci più diffusi in sanità. L'IA è un processo che richiede preparazione, collaborazione e revisione continua (Khuntia, 2024f).
- Le quattro condizioni di successo (Khuntia, 2024f):
  - **dati pronti:** dati di qualità, puliti, standardizzati e integrati («garbage in, garbage out»). Un modello di riammissione fallisce se le lettere di dimissione omettono il follow-up;
  - **problema definito:** un problema specifico e allineato agli obiettivi dell'organizzazione;
  - **collaborazione multidisciplinare:** tra data scientist, clinici, amministratori e informatici. Uno strumento accurato ma che disturba il flusso di lavoro del radiologo non produce valore;
  - **monitoraggio e riaddestramento continui:** un modello perde accuratezza quando cambiano popolazione, protocolli o linee guida.
- A queste si aggiungono fiducia, trasparenza e spiegabilità: come arriva il modello alla raccomandazione? I modelli addestrati su dati non rappresentativi perpetuano le disparità (Khuntia, 2024f).
- Il testo definisce l'IA «un investimento di breve termine e non una scorciatoia». Dal contesto si capisce che intendeva «di lungo termine»: il refuso rovescia il senso della frase.

### Che cos'è un modello analitico
- È uno strumento matematico o algoritmico che trasforma dati complessi in risultati utilizzabili, il «cervello digitale» di un sistema di IA. Si parte dall'esplorazione dei dati, per esempio i picchi stagionali di malattie respiratorie, e si applicano algoritmi come regressione, alberi decisionali o deep learning (Khuntia, 2024f).
- Gli usi illustrati sono quattro (Khuntia, 2024f):
  - prevedere le riammissioni entro 30 giorni, per programmare il follow-up;
  - personalizzare le cure croniche, per esempio l'insulina nel diabete;
  - passare da cure reattive a proattive, per esempio con segnali precoci nello scompenso cardiaco;
  - ottimizzare flussi, posti letto e scorte.

### Come funziona e di quali elementi è fatto
- Il modulo indica tre fasi centrali, addestramento, apprendimento e applicazione, inserite in un ecosistema più ampio (Khuntia, 2024f):
  - **preparazione dei dati:** per esempio unificare parametri vitali, esami e storia clinica per un modello sulla sepsi;
  - **validazione su dati mai visti:** con metriche come accuratezza, precisione e *recall* (sensibilità). Bisogna ridurre falsi positivi e falsi negativi senza sommergere i clinici di allarmi (*alert fatigue*);
  - **integrazione nel flusso clinico:** nella cartella elettronica, nei cruscotti, negli strumenti di supporto alla decisione;
  - **monitoraggio e riaddestramento:** con nuovi dati.
- Il modulo elenca sei elementi del modello (Khuntia, 2024f):
  - dati in ingresso;
  - variabili (*features*), con la possibilità di costruirne di composite, come un «punteggio di salute cardiaca»;
  - algoritmo: regressione per esiti continui, alberi per la classificazione, reti neurali per relazioni complesse;
  - addestramento, che regola iterativamente i parametri, per esempio i pesi di una rete, per ridurre l'errore;
  - output con le sue metriche;
  - ciclo di retroazione.

### Rapporto con la letteratura nella wiki
- Il principio del monitoraggio e del riaddestramento continui concorda con il passaggio dalla «validazione» alla valutazione continua sostenuto da TRIPOD+AI (Collins et al., 2024).
- Le metriche indicate dal modulo sono però solo di classificazione (accuratezza, precisione, *recall*). Mancano calibrazione e utilità clinica (beneficio netto), che la letteratura sui modelli predittivi considera indispensabili. Vedi [[clinical-prediction-model-evaluation]].
- Il modulo non ha riferimenti bibliografici.

## Riferimenti Bibliografici
- Collins, G. S., Moons, K. G. M., Dhiman, P., Riley, R. D., Beam, A. L., Van Calster, B., Ghassemi, M., Liu, X., Reitsma, J. B., van Smeden, M., Boulesteix, A.-L., Camaradou, J. C., Celi, L. A., Denaxas, S., Denniston, A. K., Glocker, B., Golub, R. M., Harvey, H., Heinze, G., . . . Logullo, P. (2024). TRIPOD+AI statement: Updated guidance for reporting clinical prediction models that use regression or machine learning methods. *BMJ*, *385*, Article e078378. https://doi.org/10.1136/bmj-2023-078378
- Khuntia, J. (2024f). *Background materials for Course 2: The data to decision path for infusion of AI in healthcare. Module 2: Emphasizing analytics in DIAD for healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/the-data-to-decision-path-for-infusion-of-ai-in-healthcare

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[diad-framework]], [[clinical-prediction-model-evaluation]], [[capacita-dinamiche-sistemi-sanitari]], [[proactive-surveillance-alert-fatigue]], [[dataset-integrity-and-contamination-in-medical-ai]], [[ai-health-c2m1-khuntia-2024]]
