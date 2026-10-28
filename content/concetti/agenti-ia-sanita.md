---
tags: [agenti-ia, rag, autonomia, supervisione-umana, sanita-digitale, tassonomia]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C4M1_JK_Dec29_2024_V1.0 (1).pdf", "BackgroundMaterials_AI-Health_C4M2_JK_Dec29_2024_V1.0 (1).pdf"]
---

# Agenti di IA in sanità: dal modello all'azione

## Definizione Operativa
- Un agente di IA è un sistema che porta l'uscita di un modello dentro un flusso di lavoro e la trasforma in azioni. Interpreta un compito, pianifica gli strumenti necessari ed esegue più passaggi: interroga la cartella, prenota, avvisa l'équipe, aggiorna un piano. Il modello prevede; l'agente agisce (Khuntia, 2024m).
- **Utilità CBT / Applicativa:** in salute mentale la stessa tecnologia può fare due cose molto diverse. Può *informare*: un RAG che risponde su un protocollo citando il manuale. Oppure può *agire*: un agente che contatta il paziente, invia esercizi o segnala un rischio. Più l'agente agisce da solo, più servono limiti di autonomia, tracciabilità e supervisione. Vedi [[tiered-autonomy-in-clinical-ai]] e [[human-in-the-loop]].

## Evidenze dalla Letteratura

### Perché servono agenti
- Secondo Khuntia (2024m) gli agenti rispondono a tre problemi:
  - i clinici spesso non sono formati a interpretare le uscite dell'IA;
  - gli LLM funzionano bene in isolamento ma si integrano male nei flussi clinici, il «solismo diagnostico»;
  - le indicazioni dell'IA non si traducono in azioni, il problema dell'«ultimo miglio».

### RAG e agenti
- Il **RAG** recupera informazioni da fonti esterne e le integra nella risposta: arricchisce la *conoscenza*. L'**agente** pianifica ed esegue compiti con strumenti e API: produce *azioni* (Khuntia, 2024m).
- Per l'uso del RAG in psicoterapia (supervisione post-seduta, pazienti simulati, studio dei manuali) vedi [[rag-in-psicoterapia]]. Per l'infrastruttura che governa un agente basato su LLM (ciclo di esecuzione, registro degli strumenti, gestione del contesto, controlli di sicurezza) vedi [[agent-harness-architecture]].

### Una tassonomia
- **Funzione:** reattivi (rispondono a una soglia), proattivi (anticipano un rischio), interattivi (dialogano con l'utente), di monitoraggio (sorvegliano flussi continui) (Khuntia, 2024m).
- **Intelligenza:** a riflesso semplice, basati su modello, che apprendono, cognitivi (Khuntia, 2024m). Questa scala riprende la classificazione degli agenti dei manuali di IA, che il materiale non cita [da verificare].
- **Interazione:** autonomi, collaborativi (il clinico mantiene la supervisione), sistemi multi-agente, ibridi uomo-IA in cui il clinico resta al centro della decisione (Khuntia, 2024m).
- **Applicazioni:** orientate al compito, centrate sul paziente, di settore, di ricerca (Khuntia, 2024m).

### Sistemi multi-agente e «terza ondata»
- Nei sistemi multi-agente più agenti autonomi collaborano dividendosi i compiti: raccolta dei dati, assegnazione dei compiti, ottimizzazione distribuita, monitoraggio. Gli esempi tipici sono agende chirurgiche, pronto soccorso e malattie croniche. Gli ostacoli principali sono l'integrazione e la fiducia dei clinici in assenza di studi di validazione (Khuntia, 2024n).
- Gli stessi materiali descrivono l'IA in tre ondate: modelli predittivi, IA generativa, IA agentica. La terza è definita come capace di decidere «con un intervento umano minimo». Nello stesso modulo si afferma però che la diagnosi finale e il piano terapeutico restano responsabilità del clinico (Khuntia, 2024n). È il secondo principio a essere coerente con il quadro normativo europeo.

### Rischi e limiti
- Negli esempi dei materiali didattici gli agenti regolano l'insulina, aggiustano farmaci o somministrano terapie di emergenza senza che la supervisione clinica sia discussa (Khuntia, 2024m). Sono proprio i casi in cui l'autonomia va limitata e resa verificabile.
- I materiali presentano gli LLM come spesso superiori ai medici nella diagnosi. La meta-analisi di Shan et al. (2025) trova il contrario per la diagnosi principale. Vedi [[diagnostic-accuracy-gap-llm-vs-physicians]].
- Molti prodotti citati come esempi non sono verificabili o non risultano più attivi [da verificare]. Vedi [[ai-health-c4m1-khuntia-2024]].
- Per i sistemi con più agenti, l'opacità si somma tra i componenti. Vedi [[compound-opacity-in-multi-agent-systems]].

## Riferimenti Bibliografici
- Khuntia, J. (2024m). *Background materials for Course 4: AI integration in healthcare. Module 1: Models to agents in health AI* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-agents-in-healthcare-and-capstone
- Khuntia, J. (2024n). *Background materials for Course 4: AI integration in healthcare. Module 2: Health AI relevant design and ethics issues* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-agents-in-healthcare-and-capstone
- Shan, G., Chen, X., Wang, C., Liu, L., Gu, Y., Jiang, H., & Shi, T. (2025). Comparing diagnostic accuracy of clinical professionals and large language models: Systematic review and meta-analysis. *JMIR Medical Informatics*, *13*, e64963. https://doi.org/10.2196/64963

## Relazioni
- Vedi anche: [[ai-health-c4m1-khuntia-2024]], [[ai-health-c4m2-khuntia-2024]], [[value-sensitive-design-ia-sanitaria]], [[health-ai-landscape]], [[rag-in-psicoterapia]], [[agent-harness-architecture]], [[tiered-autonomy-in-clinical-ai]], [[human-in-the-loop]], [[compound-opacity-in-multi-agent-systems]], [[ai-for-healthcare-systems-khuntia-2024]]
