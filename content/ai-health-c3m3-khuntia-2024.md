---
tags: [ai-health-coursera, formazione, health-ai-landscape, governance-dei-dati, modelli-descrittivi, modelli-diagnostici, causalita]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C3M3_JK_Dec22_2024_V1.0 (1).pdf"]
---

# AI for Healthcare Systems, C3M3: la modellazione per l'IA in sanità, parte 1 (Khuntia, 2024k)

## Definizione Operativa
- Materiale di approfondimento (44 pagine, versione 1.0 del 22 dicembre 2024) del terzo modulo del corso 3 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]]. Il file era stato nominato C3M2 per errore ed è stato rinominato dall'utente; le intestazioni di pagina lo chiamano «Module 2».
- Presenta il quadro integrato *Health AI Landscape*, dove dati, analisi, algoritmi, modelli, agenti e processi organizzativi operano dentro un insieme di vincoli. Approfondisce poi due tipi di modelli: descrittivi e diagnostici (Khuntia, 2024k).
- **Utilità CBT / Applicativa:** il quadro mostra che un chatbot o un sistema di allerta è solo l'ultimo anello di una catena: dati governati, analisi, modelli validati, integrazione nei processi, vincoli legali ed etici. Valutare uno strumento significa interrogare ogni anello. Vedi [[health-ai-landscape]].

## Evidenze dalla Letteratura

### Il quadro *Health AI Landscape*
- **Dati**, articolati in tre attività (Khuntia, 2024k):
  - *gestione:* selezione (anche di cosa escludere), reperimento da cartelle elettroniche, imaging, dispositivi indossabili e biobanche come la UK Biobank, raccolta automatica (con FHIR contro i silos), archiviazione conforme a HIPAA, sintesi in formati unificati;
  - *ingegneria:* esplorazione, pulizia e imputazione, normalizzazione delle unità, costruzione di variabili (per esempio la media glicemica settimanale), standardizzazione delle scale;
  - *governance:* qualità, politiche di accesso, standard (HL7, FHIR), sicurezza e privacy (cifratura, anonimizzazione o pseudonimizzazione), conformità e gestione del rischio. Opera a livello di struttura, nazionale (Office for Civil Rights, European Data Protection Board) e di consorzi.
- **Analisi:** classificazione, regressione, *clustering*, riduzione di dimensionalità (PCA, t-SNE), rilevazione di anomalie, associazioni. Tra gli esempi di classificazione il modulo cita la salute mentale: riconoscere segni di depressione o ansia dalla voce e dai testi, classificare gli utenti dei social media a rischio di ideazione suicidaria, stimare lo stress dalla variabilità cardiaca (Khuntia, 2024k).
- **Algoritmi:** supervisionati, non supervisionati, semi-supervisionati, per rinforzo, ensemble (Khuntia, 2024k).
- **Modelli:** descrittivi (che cosa è successo), diagnostici (perché), predittivi (che cosa succederà), prescrittivi (che cosa fare) e cognitivi, che imitano il ragionamento umano su dati non strutturati. L'esempio citato per i cognitivi è IBM Watson in oncologia (Khuntia, 2024k).
- **Agenti:** interfacce che rendono operative le uscite dei modelli. Il modulo li classifica secondo tre dimensioni (Khuntia, 2024k):
  - *funzione:* per esempio l'allerta per la sepsi di Sepsis Watch;
  - *intelligenza:* statica, a regole, oppure adattiva;
  - *interazione:* autonoma, come gli assistenti virtuali fuori orario, o collaborativa, come i chatbot che passano i casi complessi al personale.
- **Processi organizzativi:** allineamento con gli obiettivi clinici e i flussi di lavoro, infrastruttura interoperabile e sicura, cicli di retroazione con riaddestramento e opinioni degli utenti, gestione del cambiamento, formazione (Khuntia, 2024k).
- **Vincoli:** il modulo ne elenca sei (Khuntia, 2024k):
  - legali: HIPAA, GDPR, responsabilità;
  - etici: equità, dignità, possibilità per clinici e pazienti di contestare o scavalcare la decisione;
  - di sicurezza: cifratura, autenticazione, attacchi avversari;
  - di trasparenza e spiegabilità;
  - di gestione di bias e privacy, con audit dei bias;
  - di conformità, con documentazione di dati, algoritmi e criteri.
  L'esempio integrato è un sistema per la sepsi.

### Modelli descrittivi
- Il modulo indica tre funzioni (Khuntia, 2024k):
  - aggregare e riassumere dati da fonti diverse in indicatori (degenza media, riammissioni, tempi di attesa);
  - individuare andamenti stagionali, pattern di progressione e segmenti di pazienti;
  - visualizzare con cruscotti in tempo reale, mappe geografiche e grafici interattivi (Tableau, Power BI, ArcGIS).
- Le tecniche indicate sono ETL, analisi di frequenze e distribuzioni e monitoraggio in tempo reale. Gli usi sono operazioni ospedaliere, sanità pubblica e ricerca (Khuntia, 2024k).

### Modelli diagnostici
- **Analisi delle cause profonde:** risalire alle cause di un fenomeno, come un aumento delle infezioni post-operatorie legato a turni con poco personale e minore aderenza ai protocolli (Khuntia, 2024k).
- **Correlazione e causalità:** il modulo avverte che confonderle porta a interventi sbagliati. L'esempio è che una degenza lunga si associa a esiti peggiori perché i pazienti più gravi restano di più, non perché la degenza causi l'esito. Il modulo attribuisce all'IA la capacità di «validare legami causali» (Khuntia, 2024k).
- **Analisi delle prestazioni:** efficacia di interventi e flussi, per esempio un farmaco che funziona meglio negli adulti che negli anziani (Khuntia, 2024k).
- Le applicazioni citate (Khuntia, 2024k):
  - cause delle riammissioni, compresi i determinanti sociali;
  - soddisfazione dei pazienti;
  - errori diagnostici, che possono colpire di più donne e minoranze perché poco rappresentate in linee guida e dati;
  - controllo delle infezioni;
  - malattie croniche nei quartieri a basso reddito;
  - colli di bottiglia operativi.

### Errori, limiti e divergenze con la wiki
- **Seconda traccia di generazione automatica:** a pagina 19 il testo si chiude con «Let me know if further elaboration is required!». È la stessa traccia trovata in C3M1.
- **Incoerenza sulla causalità:** a pagina 18 l'analisi delle associazioni «fornisce indicazioni sulla causalità»; a pagina 39 lo stesso modulo spiega che correlazione e causalità vanno distinte. Anche quando le distingue, dice che l'IA «valida» i legami causali senza indicare i metodi necessari. La wiki documenta che servono algoritmi di scoperta causale e modelli strutturali dedicati, con assunzioni esplicite, per separare cause dirette, cause mediate e associazioni spurie (Mok, Cheng, & Chu, 2025). Vedi [[causal-discovery-psychosocial-targets]].
- **Ideazione suicidaria dai social media:** l'esempio è presentato come applicazione riuscita, senza accennare a falsi positivi, privacy o consenso. Per i limiti dell'IA nella gestione del rischio suicidario vedi [[rischio-suicidario-ai-limits]].
- **IBM Watson:** è citato come modello cognitivo di riferimento in oncologia. Il suo uso clinico è stato oggetto di critiche documentate [da verificare].
- Il modulo non ha riferimenti bibliografici. I casi sono ipotetici, introdotti da «AI might…».

## Riferimenti Bibliografici
- Khuntia, J. (2024k). *Background materials for Course 3: AI integration in healthcare. Module 3: The craft of modeling for AI in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare
- Mok, C. H. Y., Cheng, C. P. W., & Chu, M. H. W. (2025). Application of artificial intelligence and psychosocial functioning in psychosis: a systematic review and meta-analysis. *Frontiers in Psychiatry*, 16, 1692177. https://doi.org/10.3389/fpsyt.2025.1692177

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[health-ai-landscape]], [[diad-framework]], [[causal-discovery-psychosocial-targets]], [[rischio-suicidario-ai-limits]], [[gdpr-governance-mental-health-ai]], [[algoritmi-ml-sanita]], [[ai-health-c3m2-khuntia-2024]]
