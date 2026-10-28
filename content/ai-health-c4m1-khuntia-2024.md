---
tags: [ai-health-coursera, formazione, agenti-ia, rag, gestione-malattie-croniche, salute-mentale-digitale]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C4M1_JK_Dec29_2024_V1.0 (1).pdf"]
---

# AI for Healthcare Systems, C4M1: dai modelli agli agenti nell'IA sanitaria (Khuntia, 2024m)

## Definizione Operativa
- Materiale di approfondimento (36 pagine, versione 1.0 del 29 dicembre 2024) del primo modulo del corso 4 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]], su Coursera *AI Agents in Healthcare and Capstone*. Il frontespizio chiama il corso «AI Integration in Healthcare» e le intestazioni «Course 3, Module 3».
- Il modulo sostiene che i modelli producono conoscenza ma non agiscono. Servono agenti che trasformino le loro uscite in azioni dentro i flussi di lavoro. Distingue gli agenti dal RAG, li classifica per funzione, intelligenza e interazione e ne elenca molte applicazioni (Khuntia, 2024m).
- **Utilità CBT / Applicativa:** chiarisce una distinzione utile per valutare uno strumento. Un sistema RAG *recupera e sintetizza* conoscenza, per esempio da manuali e linee guida. Un agente *esegue compiti* in più passaggi con strumenti esterni: agende, cartelle, notifiche. Il secondo pone problemi di responsabilità molto maggiori. Vedi [[agenti-ia-sanita]].

## Evidenze dalla Letteratura

### I modelli nella gestione delle malattie
- Il modulo passa in rassegna l'uso dei cinque tipi di modelli in diverse condizioni: diabete, malattia renale cronica, cardiopatie, tumori, salute mentale, malattie infettive, malattie neurologiche, asma, ipertensione e BPCO (Khuntia, 2024m).
- Per la **salute mentale** cita (Khuntia, 2024m):
  - modelli cognitivi che riconoscono ansia e depressione da linguaggio, testi e dispositivi indossabili;
  - chatbot che «offrono supporto emotivo» e indirizzano alle risorse;
  - modelli predittivi del rischio suicidario e delle ricadute;
  - interventi che, secondo il modulo, «riducono lo stigma».
- Il limite comune è che i modelli «non possono agire direttamente»: un modello che prevede riammissioni non avvisa l'équipe e non avvia interventi (Khuntia, 2024m).

### Dai modelli agli agenti
- Gli agenti eseguono compiti in più passaggi, usano strumenti e prendono decisioni dinamiche (Khuntia, 2024m). Esempi:
  - agende che coordinano reparti e disponibilità;
  - monitoraggio dell'aderenza con promemoria;
  - triage nelle emergenze;
  - riallocazione dei letti in terapia intensiva.
- Secondo il modulo gli agenti affrontano tre problemi (Khuntia, 2024m):
  - l'**integrazione da parte di utenti non formati**: i medici spesso non sanno interpretare le uscite dell'IA;
  - il **«solismo diagnostico»**: gli LLM ragionerebbero bene da soli ma si integrano male nei flussi clinici;
  - il **problema dell'«ultimo miglio»**: le indicazioni dell'IA non si traducono in azioni.
- Gli agenti apprendono con metodi supervisionati, non supervisionati e per rinforzo. Usano l'NLP per le note cliniche e devono essere interoperabili. Sono presentati come «partner» che liberano tempo ai clinici e come strumenti che danno autonomia ai pazienti (Khuntia, 2024m).

### RAG e agenti
- **RAG:** riceve una domanda, recupera informazioni da fonti esterne (cartelle, letteratura, banche dati) e genera una risposta che le integra. È adatto quando servono informazioni accurate e aggiornate, per esempio nel supporto alla decisione o nei chatbot per pazienti con dati personali (Khuntia, 2024m).
- **Agente:** interpreta il compito, pianifica gli strumenti necessari ed esegue passo per passo con API verso cartelle, calcolatori e sistemi di comunicazione. È adatto ai compiti dinamici in più passaggi, come lettere di dimissione, prenotazioni, aderenza o pratiche assicurative (Khuntia, 2024m).
- Il modulo chiude con domande etiche: che cosa succede quando l'IA recupera informazioni sensibili o compie azioni autonome nei flussi clinici? (Khuntia, 2024m).

### Una tassonomia degli agenti
- Il modulo classifica gli agenti su tre assi (Khuntia, 2024m):
  - **funzione:** reattivi (allarme se la saturazione scende), proattivi (anticipano e programmano screening), interattivi (dialogo con il paziente), di monitoraggio (flussi continui, come la glicemia);
  - **intelligenza:** a riflesso semplice, basati su modello, che apprendono, cognitivi. Tra gli esempi di agenti cognitivi c'è la salute mentale, con «piani terapeutici personalizzati» e la predizione delle ricadute depressive;
  - **interazione:** autonomi (compiti amministrativi), collaborativi (affiancano il clinico mantenendone la supervisione), sistemi multi-agente (triage, letti e logistica coordinati), ibridi uomo-IA.
- Le applicazioni sono divise in quattro gruppi: orientate al compito, centrate sul paziente, di settore e di ricerca (Khuntia, 2024m).

### Gli esempi di agenti
- Per ogni condizione il modulo associa un agente. Per la salute mentale cita Woebot (CBT via testo, invio a un terapeuta se la situazione peggiora) ed Ellipsis Health (depressione e ansia dall'analisi della voce). Seguono decine di altri prodotti: Babylon Health, Qventus, MedAware, IBM Watson for Oncology, Sepsis Watch, Face2Gene, Ada Health, SkinVision, BlueDot, LactApp, Pillo Health, Overjet e altri (Khuntia, 2024m).

### Errori, limiti e divergenze con la wiki
- **LLM e medici:** il modulo afferma che gli LLM hanno mostrato capacità diagnostiche «eccezionali», «spesso superiori ai medici in studi controllati». La meta-analisi di Shan et al. (2025) su 30 studi trova invece che i medici superano gli LLM nella diagnosi principale (OR = 0,71; 71,8% contro 65,1%). Gli LLM si avvicinano o superano i medici solo nel triage e rispetto agli specializzandi in alcuni domini. Vedi [[diagnostic-accuracy-gap-llm-vs-physicians]].
- **Prodotti non verificati:** nelle ultime pagine, introdotte da una frase in stile chatbot («Here are some innovative or less-explored applications… that bring something new to the table»), compaiono molti nomi che non è stato possibile verificare: NutrAI, MyAIHealth, AutiBuddy, BloodTrack, EpiAI, EveAI, TeleCare ICU Assistant, ImagingPro AI, CareVoice, BioGen AI, HealthEquAI, HomeGuardian, RetinaGuard, MedSim AI, CardioBot, RehabBoost. Dato l'indizio di generazione automatica presente in tutta la serie, potrebbero essere invenzioni del modello [da verificare]. Non vanno citati come prodotti esistenti.
- **Prodotti dismessi:** Babylon Health è presentato come esempio di successo, ma risulta fallito nel 2023 [da verificare]. IBM Watson for Oncology è presentato come agente in uso [da verificare].
- **Woebot:** è descritto come agente NLP che riconosce ansia e depressione. Hua et al. (2025) classificano il Woebot originario tra i sistemi a regole. Vedi [[marketing-architecture-mismatch-in-mental-health-ai]].
- **Salute mentale senza cautele:** chatbot di supporto emotivo, predizione del rischio suicidario e agenti «cognitivi» che raccomandano piani terapeutici sono presentati senza discutere sicurezza, gestione delle crisi o validazione clinica. Vedi [[rischio-suicidario-ai-limits]] e [[conversational-agents-mental-health]].
- **Azioni cliniche automatiche:** nell'esempio del diabete l'agente regola la dose di insulina tramite microinfusore; in quello della malattia renale aggiusta i farmaci; nell'epilessia somministra farmaci di emergenza. La supervisione clinica non è discussa. Vedi [[tiered-autonomy-in-clinical-ai]].
- Il testo ripete più volte gli stessi contenuti, ha refusi («partnets», «aAgents», «Ongling») e non ha riferimenti bibliografici.

## Riferimenti Bibliografici
- Hua, Y., Siddals, S., Ma, Z., Galatzer-Levy, I., Xia, W., Hau, C., Na, H., Flathers, M., Linardon, J., Ayubcha, C., & Torous, J. (2025). Charting the evolution of artificial intelligence mental health chatbots from rule-based systems to large language models: A systematic review. *World Psychiatry*, *24*(3), 383–394. https://doi.org/10.1002/wps.21352
- Khuntia, J. (2024m). *Background materials for Course 4: AI integration in healthcare. Module 1: Models to agents in health AI* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-agents-in-healthcare-and-capstone
- Shan, G., Chen, X., Wang, C., Liu, L., Gu, Y., Jiang, H., & Shi, T. (2025). Comparing diagnostic accuracy of clinical professionals and large language models: Systematic review and meta-analysis. *JMIR Medical Informatics*, *13*, e64963. https://doi.org/10.2196/64963

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[agenti-ia-sanita]], [[rag-in-psicoterapia]], [[agent-harness-architecture]], [[diagnostic-accuracy-gap-llm-vs-physicians]], [[tiered-autonomy-in-clinical-ai]], [[conversational-agents-mental-health]], [[health-ai-landscape]], [[ai-health-c3m4-khuntia-2024]]
