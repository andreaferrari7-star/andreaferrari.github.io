---
tags: [ai-health-coursera, formazione, diad, data-mining, clinical-decision-support, llm, visualizzazione-dati]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C2M1_JK_Dec17_2024_V1.0 (2).pdf"]
---

# AI for Healthcare Systems, C2M1: il ruolo dell'IA nel processo DIAD (Khuntia, 2024e)

## Definizione Operativa
- Materiale di approfondimento (25 pagine, versione 1.0 del 17 dicembre 2024) del primo modulo del corso 2 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]], *The data to decision path for infusion of AI in healthcare*. Presenta il framework DIAD (*Data-Information-Analysis-Decision*) come percorso dai dati grezzi alla decisione e vi colloca IA, ML, LLM, data mining e visualizzazione (Khuntia, 2024e).
- **Utilità CBT / Applicativa:** il DIAD aiuta a capire in quale passaggio interviene uno strumento: raccolta del dato, organizzazione in informazione, analisi predittiva o supporto alla decisione. Ricorda anche che la decisione integra l'analisi con esperienza e competenza del clinico. Vedi [[diad-framework]].

## Evidenze dalla Letteratura

### Il framework DIAD
- Il modulo descrive quattro stadi (Khuntia, 2024e):
  - **dati:** provengono da cartelle cliniche elettroniche, dispositivi indossabili (frequenza cardiaca, sonno, attività, saturazione, glicemia), sistemi amministrativi (fatturazione, turni, scorte), registri di sanità pubblica e dati ambientali. I problemi sono qualità, standardizzazione, integrazione, affidabilità dei dispositivi e privacy;
  - **informazione:** il dato diventa informazione quando viene organizzato e contestualizzato, e risponde a «chi», «cosa», «dove». Esempi: la durata media della degenza o il tasso di infezioni;
  - **analisi (intelligence):** l'analisi dell'informazione porta a previsioni e collega «che cosa è successo» a «che cosa potrebbe succedere». Esempi: il rischio di riammissione o i picchi di ricovero stagionali;
  - **decisione:** integra dati, informazione e intelligence con esperienza e competenza.
- Il passaggio da uno stadio all'altro non è automatico: richiede impegno deliberato, strumenti e competenze. Il contesto dà valore al dato: una pressione arteriosa letta insieme a storia clinica, età e stile di vita indica un andamento ipertensivo e orienta la terapia (Khuntia, 2024e).
- IA, ML e soprattutto IA generativa e LLM automatizzano e affinano la trasformazione dei dati in conoscenza e la rendono accessibile in linguaggio naturale. Le questioni etiche sono integrità e sicurezza dei dati, inclusività e bias, che portano a intelligence distorta e decisioni inique (Khuntia, 2024e).

### IA, ML e LLM nella decisione clinica
- Gli esempi del modulo (Khuntia, 2024e):
  - rilevazione della fibrillazione atriale dall'ECG prima dei sintomi;
  - imaging oncologico, con DeepMind sulla mammografia descritto come «spesso» più preciso dei radiologi;
  - predizione del rischio di sepsi in pronto soccorso con allerta in tempo reale (Sepsis Watch);
  - triage delle immagini radiologiche;
  - controllo delle interazioni farmacologiche in farmacia.
- Agli LLM (GPT, Med-PaLM) il modulo attribuisce quattro funzioni: sintetizzare casi e letteratura sulle malattie rare, proporre terapie personalizzate (anche regimi chemioterapici calibrati sul profilo genetico), riassumere le nuove linee guida per l'aggiornamento professionale e interpretare le note cliniche (Khuntia, 2024e).
- Ripete che queste tecnologie «non sostituiscono i clinici ma ne potenziano le capacità». Chiede trasparenza, validazione rigorosa e audit periodici. Propone un esercizio: integrare con esame obiettivo e anamnesi il suggerimento di un modello che indica una probabile disfunzione tiroidea in un paziente con stanchezza e calo di peso (Khuntia, 2024e).

### Data mining, visualizzazione e tempo reale
- Il data mining attraversa gli stadi del DIAD (Khuntia, 2024e):
  - nello stadio dei dati: preelaborazione, classificazione e *clustering*, per esempio dei ricoveri respiratori invernali;
  - nell'analisi: regressione, alberi decisionali e modelli predittivi, per esempio per anticipare la neutropenia da chemioterapia e somministrare fattori di crescita;
  - nella decisione: riordino automatico delle scorte, turni del personale, supporto diagnostico, mappe di prevalenza per la sanità pubblica.
- La visualizzazione collega l'analisi alla decisione: cruscotti in tempo reale (posti letto, risorse, soddisfazione), mappe di calore e sovrapposizioni geografiche per epidemie e «deserti sanitari», portali che mostrano al paziente i propri dati. Gli strumenti citati sono Tableau e Power BI. Il tempo reale sposta il DIAD dall'analisi retrospettiva a quella proattiva, per esempio con i monitor in terapia intensiva (Khuntia, 2024e).
- Le basi tecniche sono i processi ETL (*Extract, Transform, Load*) e la pulizia dei dati (duplicati, valori mancanti, codifiche diverse), poi metodi statistici (regressione, test d'ipotesi) e ML: supervisionato per la riammissione, non supervisionato per i pattern di popolazione, deep learning per l'imaging. Gli strumenti sono R, Python (scikit-learn), SQL e ggplot2. Il framework migliora con cicli di retroazione tra decisori e analisti (Khuntia, 2024e).

### Limiti della fonte e divergenze con la wiki
- Il modulo attribuisce agli LLM la capacità di proporre regimi chemioterapici personalizzati che bilanciano efficacia e sicurezza. Nella review oncologica di Chen et al. (2025), invece, il 41,7% degli studi documenta bias, omissioni critiche o allucinazioni dei chatbot. Vedi [[ai-clinical-decision-support]].
- La superiorità di DeepMind sui radiologi è affermata senza fonte.
- Il vertice del framework è chiamato ora «decisione», ora «conoscenza». Il DIAD ricorda la gerarchia dati-informazione-conoscenza-saggezza della scienza dell'informazione, che il modulo non cita [da verificare].
- Mancano riferimenti bibliografici per tutti gli esempi.

## Riferimenti Bibliografici
- Chen, D., Avison, K., Alnassar, S., Huang, R. S., & Raman, S. (2025). Medical accuracy of artificial intelligence chatbots in oncology: a scoping review. *The Oncologist*, 30, oyaf038.
- Khuntia, J. (2024e). *Background materials for Course 2: The data to decision path for infusion of AI in healthcare. Module 1: The role of AI in the data-information-analysis-decision (DIAD) process in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/the-data-to-decision-path-for-infusion-of-ai-in-healthcare

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[diad-framework]], [[ai-clinical-decision-support]], [[large-language-models]], [[ai-health-c1m2-khuntia-2024]], [[ia-machine-learning-deep-learning]]
