# Riunione 05-08: Sviluppo Knowledge Base AI, Etica e Applicazioni Cliniche

**Summary**: Sintesi della discussione metodologica su architettura degli agenti didattici, transizione dal paradigma Human-in-the-loop a Human-in-the-reasoning, simulazione clinica di pazienti e sfide etiche/regolatorie nell'uso dell'IA in psicoterapia.
**Sources**: 05-08 Riunione_ Sviluppo Knowledge Base AI, Etica e Applicazioni Cliniche.txt
**Last updated**: 2026-08-27
---

## Sintesi dei Contenuti

### 1. Architettura della Knowledge Base e Sviluppo Agenti (Libet Prime)
- **Stato di avanzamento**: La Knowledge Base è attualmente strutturata per gli allievi dei primi due anni di specializzazione; è prevista l'integrazione di moduli per il 3° e 4° anno relativi ai pazienti complessi, all'adesione al trattamento e all'alleanza di lavoro.
- **Problematiche di rigidità algoritmica**: Durante il passaggio da *Libet Prime 1.0* a *1.1*, l'accumulo di istruzioni e vincoli sequenziali ha causato una regressione qualitativa, appiattendo le risposte dell'agente su scalette eccessivamente meccaniche.
- **Best practice di versioning**: Gli LLM tendono ad assegnare priorità gerarchica alle istruzioni aggiunte successivamente. È emerso che per migliorare un agente è preferibile crearne uno nuovo da zero (mantenendo versioni isolate e pulite) piuttosto che continuare a sovrascrivere o appesantire lo script originale.

### 2. Transizione verso il [[human-in-the-reasoning]]
- **Oltre lo Human-in-the-loop**: Viene proposta l'evoluzione dal semplice controllo a posteriori dell'output (supervisione passiva) verso una reale comprensione e guida congiunta dei processi inferenziali dell'IA (*Human-in-the-reasoning*).
- **Competenza metacognitiva**: Così come il terapeuta indaga le logiche e i bias di ragionamento del paziente, allo stesso modo deve apprendere come "ragiona" il modello linguistico, identificando la struttura dei pesi, i limiti della "scatola nera" e i meccanismi di simulazione del pensiero.

### 3. [[simulazione-pazienti-ai]] e Prompting Avanzato
- **Linee guida per i prompt clinici**: Riferimento a standard di trasparenza e prompt engineering (es. dichiarazioni tipo TRIPOD) che definiscono chiaramente il livello di astrazione richiesto (inferire, interpretare, descrivere).
- **Esplicitazione dei bias cognitivi**: Nella simulazione di pazienti virtuali, è fondamentale esplicitare nel prompt non solo i sintomi descrittivi ma gli specifici pattern di ragionamento disfunzionale (es. pensiero dicotomico, catastrofizzazione, dinamiche di alleanza). Questo previene risposte stereotipate e garantisce una simulazione psicologicamente realistica per il training degli studenti.
- **Testing economico**: Possibilità di sfruttare piattaforme accessibili (es. Gemini) per condurre studi pilota ed esperienze formative a basso costo per gli allievi.

### 4. Etica, Privacy e Bias nei Modelli Linguistici
- **Tutela della privacy e deontologia**: Rischi associati al caricamento indiscriminato di materiale clinico non anonimizzato (es. schede ABC o dati ipersensibili come l'orientamento sessuale). Necessità di protocolli rigorosi di de-identificazione.
- **Bias sistematici**: Evidenza di bias impliciti nei modelli (es. sovrastima della gravità clinica su vignette diagnostiche di disturbo borderline associate a soggetti femminili rispetto a soggetti maschili).
- **Governance e trasparenza**: Necessità di affiancare alla regolamentazione normativa una formazione sulle buone pratiche di interazione clinica con l'IA.

### 5. Ricerca Clinica e Digital Therapeutics (SaMD)
- **Progetto NHS / NIHR**: Analisi del progetto di ricerca del Prof. Delgadillo (Mindlight) per implementare l'IA nei percorsi clinici dell'NHS per ansia e depressione, con l'obiettivo di aumentare l'efficacia del 10% e ridurre i tassi di abbandono (dropout).
- **Digitalizzazione del protocollo Not-On-Track (CTS)**: Utilizzo dell'IA per monitorare precocemente i pazienti che non rispondono positivamente al trattamento standard e guidare terapeuta e paziente nelle procedure di recupero.
- **Requisiti Software as a Medical Device (SaMD)**: Complessità dei trial di validazione clinica (RCT) in cieco su popolazioni ampie e rappresentative per ottenere le certificazioni regolatorie (FDA / normative europee).

### 6. Proposta Formativa
- Pianificazione di un modulo/FAD per terapeuti articolato su tre pilastri:
  1. *Come funzionano e sono architettati gli LLM* (caratteristiche del ragionamento e limiti).
  2. *Come si costruiscono* (strutturazione modulare ed esplicitazione dei prompt).
  3. *Come si interrogano e si utilizzano eticamente* (gestione dei bias, privacy e interazione clinica).

## Related pages
- [[human-in-the-reasoning]]
- [[simulazione-pazienti-ai]]
- [[large-language-models]]
- [[prompting-in-psychology]]
- [[ai-research-ethics]]
