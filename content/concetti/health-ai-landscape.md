---
tags: [health-ai-landscape, governance-dei-dati, modelli-predittivi, agenti, implementazione, vincoli-etici]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C3M3_JK_Dec22_2024_V1.0 (1).pdf", "BackgroundMaterials_AI-Health_C3M4_JK_Dec22_2024_V1.0 pgd (1).pdf"]
---

# Health AI Landscape: la catena dai dati agli agenti

## Definizione Operativa
- Il *Health AI Landscape* è un quadro che descrive un sistema di IA sanitaria come una catena di sei elementi: dati (gestiti, ingegnerizzati, governati), analisi, algoritmi, modelli, agenti e processi organizzativi. La catena opera dentro un insieme di vincoli legali, etici, di sicurezza, trasparenza, bias, privacy e conformità (Khuntia, 2024k).
- **Utilità CBT / Applicativa:** dà una lista di controllo per valutare uno strumento di IA in un servizio di salute mentale:
  - da dove vengono i dati e chi li governa;
  - quale analisi e quale modello producono l'output, e come sono validati;
  - come l'output arriva al clinico o al paziente (l'agente);
  - come si inserisce nei flussi di lavoro;
  - quali vincoli lo regolano.
  Estende il [[diad-framework|framework DIAD]] con gli agenti e i processi organizzativi.

## Evidenze dalla Letteratura

### Gli elementi
- **Dati:** la gestione comprende selezione, reperimento, raccolta, archiviazione e sintesi. L'ingegneria comprende esplorazione, pulizia, normalizzazione, costruzione di variabili e standardizzazione. La governance comprende qualità, politiche, standard (HL7, FHIR), sicurezza e privacy, conformità e rischio (Khuntia, 2024k).
- **Analisi:** classificazione, regressione, *clustering*, riduzione di dimensionalità, anomalie, associazioni (Khuntia, 2024k). Vedi [[algoritmi-ml-sanita]].
- **Algoritmi:** supervisionati, non supervisionati, semi-supervisionati, per rinforzo, ensemble (Khuntia, 2024k).
- **Modelli:** il modulo ne distingue cinque tipi (Khuntia, 2024k):
  - descrittivi: che cosa è successo, cioè indicatori, andamenti, cruscotti;
  - diagnostici: perché è successo, cioè cause profonde e analisi delle prestazioni;
  - predittivi: che cosa succederà, cioè rischio di riammissione o diffusione di un'epidemia;
  - prescrittivi: che cosa conviene fare, cioè raccomandazioni di trattamento o organizzative;
  - cognitivi: imitano il ragionamento su dati non strutturati.
- **Agenti:** interfacce che portano l'output a chi lo usa. Si distinguono per funzione (monitoraggio, allerta, compiti amministrativi), per intelligenza (statica o adattiva) e per interazione: autonoma, oppure collaborativa con passaggio dei casi complessi al professionista (Khuntia, 2024k). Il corso 4 approfondisce gli agenti: vedi [[agenti-ia-sanita]].
- **Processi organizzativi:** allineamento ai flussi clinici, infrastruttura interoperabile e sicura, retroazione con riaddestramento e opinioni degli utenti, formazione e gestione del cambiamento (Khuntia, 2024k). Vedi [[capacita-dinamiche-sistemi-sanitari]].
- **Vincoli:** legali (HIPAA, GDPR, responsabilità), etici (equità, possibilità di contestare e scavalcare la decisione), di sicurezza (attacchi avversari), di trasparenza e spiegabilità, di gestione di bias e privacy, di conformità e documentazione (Khuntia, 2024k).

### Dallo sviluppo all'implementazione
- **Otto fasi di sviluppo:**
  1. raccolta e integrazione dei dati;
  2. preparazione e costruzione delle variabili;
  3. analisi esplorativa, anche dei bias;
  4. scelta del modello tra complessità, accuratezza e interpretabilità;
  5. addestramento e validazione incrociata;
  6. metriche scelte sul problema clinico, tenendo conto che l'accuratezza è fuorviante con classi sbilanciate;
  7. messa in produzione con monitoraggio della deriva dei dati;
  8. revisione iterativa (Khuntia, 2024l).
- **Dieci sfide:** qualità e interoperabilità dei dati, regolazione (soprattutto per i sistemi che continuano ad apprendere), spiegabilità, integrazione nei flussi di lavoro, bias, costi, privacy e sicurezza, monitoraggio, resistenza al cambiamento, scalabilità, con il calo di prestazioni passando da ospedali urbani a cliniche rurali (Khuntia, 2024l).
- **Contromisure principali:**
  - standard di interoperabilità (FHIR) e coinvolgimento precoce dei regolatori;
  - strumenti di spiegazione (SHAP, LIME) e, nelle applicazioni ad alto rischio, modelli più semplici e interpretabili;
  - introduzione graduale con progetti pilota;
  - audit dei bias e coinvolgimento delle comunità;
  - privacy differenziale e apprendimento federato;
  - riaddestramento e raccolta delle opinioni degli utenti;
  - adattamento locale (Khuntia, 2024l).
- **Supervisione umana:** nel confronto tra modelli Khuntia (2024l) elenca come limite dei modelli predittivi il fatto di lasciare la decisione al professionista. Nel quadro europeo e deontologico la supervisione umana è invece un requisito, non un limite (vedi [[human-in-the-loop]]).

### Limiti
- Il quadro è presentato in materiali didattici senza bibliografia, in parte probabilmente generati con IA e non revisionati. Vedi [[ai-health-c3m3-khuntia-2024]].
- Il passaggio dai modelli diagnostici alle affermazioni causali va trattato con cautela. L'analisi dei dati osservazionali non «valida» da sola un legame causale: servono metodi dedicati e assunzioni esplicite (Mok, Cheng, & Chu, 2025). Vedi [[causal-discovery-psychosocial-targets]].
- Per la governance dei dati in salute mentale nel contesto europeo vedi [[gdpr-governance-mental-health-ai]].

## Riferimenti Bibliografici
- Khuntia, J. (2024k). *Background materials for Course 3: AI integration in healthcare. Module 3: The craft of modeling for AI in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare
- Khuntia, J. (2024l). *Background materials for Course 3: AI integration in healthcare. Module 4: The craft of modeling for AI in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare
- Mok, C. H. Y., Cheng, C. P. W., & Chu, M. H. W. (2025). Application of artificial intelligence and psychosocial functioning in psychosis: a systematic review and meta-analysis. *Frontiers in Psychiatry*, 16, 1692177. https://doi.org/10.3389/fpsyt.2025.1692177

## Relazioni
- Vedi anche: [[ai-health-c3m3-khuntia-2024]], [[ai-health-c3m4-khuntia-2024]], [[human-in-the-loop]], [[diad-framework]], [[algoritmi-ml-sanita]], [[capacita-dinamiche-sistemi-sanitari]], [[causal-discovery-psychosocial-targets]], [[gdpr-governance-mental-health-ai]], [[ai-for-healthcare-systems-khuntia-2024]]
