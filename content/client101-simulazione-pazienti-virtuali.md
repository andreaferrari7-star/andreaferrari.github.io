---
tags: [client101, simulazione-pazienti, simulated-clients, liwc-validation, memory-assisted-prompt-editing, depressione-ansia, deliberate-practice, compliance-artificiale, stereotipia-clinica, ai-training-psicoterapia, cbt-simulation]
source_papers: ["Sunto articoli.docx.pdf"]
---

# Framework Client101 per la Simulazione di Pazienti Virtuali e Benchmarking Psicolinguistico

## Definizione Operativa
- Il **Framework Client101** (Cabrera Lozoya et al., 2025) è una piattaforma web interattiva basata su modelli linguistici generativi ([[large-language-models]], GPT-4) progettata per simulare **pazienti psicoterapeutici virtuali standardizzati**, destinata all'addestramento clinico e alla [[deliberate-practice-in-psicoterapia-ia|Deliberate Practice]] di psicologi, psichiatri e psicoterapeuti in formazione.
- **Evoluzione Storica dei Sistemi Dialogici:** Si colloca nella traiettoria evolutiva dei sistemi di simulazione in salute mentale, superando i limiti dei modelli basati su regole rigide (*ELIZA*, *PARRY*) e dei primi chatbot statistici (*ClientBot*):
  - *ELIZA (1966) / PARRY (1971):* Pattern matching superficiale, assenza di memoria contestuale.
  - *ClientBot (Tanana et al., 2019):* Dialoghi statistici limitati, frequenti rotture di coerenza logica.
  - *Client101 (2025):* Profili clinici ricchi basati su vignette CBT e linee guida NICE, coerenza multi-turno e validazione psicolinguistica avanzata.
- **Personas Cliniche Formalizzate:** Implementa due prototipi nosografici distinti:
  1. **"Alice":** Simulazione di Disturbo d'Ansia Generalizzato (GAD), caratterizzata da rimuginio, ipervigilanza e intolleranza dell'incertezza.
  2. **"Luke":** Simulazione di Disturbo Depressivo Maggiore (MDD), caratterizzato da anedonia, autosvalutazione, pensieri automatici negativi e ridotta energia.

```mermaid
flowchart TD
    subgraph DesignInputs ["Fonti Progettuali di Client101"]
        V1["Linee Guida Cliniche NICE"]
        V2["Vignette Cliniche CBT Standardizzate"]
        V3["Consulenza & Feedback di Psicoterapeuti Esperti"]
    end

    subgraph Architecture ["Architettura Computazionale Client101"]
        PE["System Prompt Engineering Specializzato"]
        MEM["Memory-Assisted Prompt Editing (Continuità di Sessione)"]
        GPT4["Motore Generativo GPT-4"]
        PE & MEM --> GPT4
    end

    subgraph SimulatedPersonas ["Pazienti Virtuali Simulati"]
        Alice["<b>Alice (GAD)</b><br/>Ansia generalizzata, rimuginio, anticipazione catastrofica"]
        Luke["<b>Luke (MDD)</b><br/>Depressione maggiore, senso di vuoto, autosvalutazione"]
    end

    DesignInputs --> Architecture
    GPT4 --> Alice & Luke
```

---

## Architettura Tecnica: Memory-Assisted Prompt Editing

Uno dei principali ostacoli storici nella simulazione di pazienti tramite LLM è la perdita progressiva del contesto clinico lungo la seduta (*semantic drift* e amnesia tematica).
- **Memory-Assisted Prompt Editing:** Client101 implementa un meccanismo dinamico che riassume e inietta periodicamente i punti cardine emersi nel dialogo (fatti biografici, credenze espresse, eventi scatenanti) all'interno del prompt di sistema di ogni turno.
- **Preservazione della Coerenza Narrativa:** Consente al paziente virtuale di ricordare eventi menzionati all'inizio del colloquio, reagire in modo coerente a ristrutturazioni cognitive e mantenere una traiettoria affettiva stabile per l'intera durata della sessione.

---

## Validazione Psicolinguistica Computazionale: Analisi LIWC

Gli autori hanno sottoposto le trascrizioni generate da Client101 a una rigorosa validazione empirica, confrontando le sessioni simulate condotte da 16 professionisti della salute mentale con un corpus di trascrizioni di sedute reali mediante l'analisi **LIWC** (*Linguistic Inquiry and Word Count*).

```mermaid
flowchart LR
    subgraph ComparisonLIWC ["Validazione Psicolinguistica LIWC"]
        RealData["Trascrizioni di Sedute Psicoterapeutiche Reali"]
        SyntheticData["Trascrizioni Sintetiche Client101 (Alice / Luke)"]
    end

    subgraph ResultsOverlap ["Marker ad Alta Fedeltà (Nessuna Differenza Statistica)"]
        M1["Pronomi personali di prima persona (I/me)"]
        M2["Focus temporale sul presente"]
        M3["Dimensioni cognitive, mentali e sociali"]
        M4["Marker lessicali di tristezza ed emozione negativa"]
    end

    subgraph ResultsDiscrepancy ["Anomalie & Discrepanze Rilevate dai Clinici"]
        D1["<b>Compliance Artificiale:</b> Eccessiva collaborazione, zero difese"]
        D2["<b>Amplificazione Caricaturale:</b> Sovra-rappresentazione stereotipata dei sintomi"]
        D3["<b>Rigidità Tematica:</b> Ancoraggio ostinato al prompt iniziale"]
    end

    RealData & SyntheticData --> ResultsOverlap
    SyntheticData --> ResultsDiscrepancy
```

### 1. Sovrapposizione Psicolinguistica Positiva
- I pattern linguistici profondi di Alice e Luke presentano una distribuzione statistica sovrapponibile a quella dei pazienti reali nelle categorie: *first-person pronouns*, *negative emotions*, *sadness*, *present focus* e *health references*.

### 2. Le Tre Anomalie Cliniche Emerse
Nonostante la fedeltà lessicale, la valutazione qualitativa dei clinici ha evidenziato tre limiti strutturali:
1. **Compliance Artificiale (*Artificial Compliance*):** I chatbot sono eccessivamente collaborativi, chiari e disponibili a seguire la guida del terapeuta. Manca la naturale resistenza al cambiamento, l'ambivalenza motivazionale e la complessità difensiva tipica della relazione terapeutica reale.
2. **Amplificazione Caricaturale (*Symptom Amplification*):** Il modello tende a concentrare ed esagerare continuamente i sintomi descritti nel prompt, generando risposte che rischiano di risultare stereotipate o 'da manuale'.
3. **Rigidità Tematica (*Algorithmic Rigidity*):** Il paziente virtuale fatica a deviare spontaneamente su argomenti contingenti o apparentemente scollegati, mantenendo una focalizzazione artificialmente ordinata sui soli temi della vignetta iniziale.

---

## Applicazioni Formative e Valore Pedagogico

```mermaid
flowchart TD
    Trainee["Allievo Terapeuta"] --> ChatInterface["Interfaccia Client101 (Seduta Simulata)"]
    ChatInterface --> Actions["Pratica Guidata di Competenze CBT"]
    
    subgraph CBTSkills ["Competenze Esercitate"]
        S1["Assessment Diagnostico e Anamnesi"]
        S2["Identificazione Pensieri Automatici"]
        S3["Questioning Socratico & Disputing"]
        S4["Assegnazione & Negoziazione Homework"]
    end
    
    Actions --> CBTSkills
    CBTSkills --> ClinicalNotes["Redazione Note Cliniche Post-Sessione"]
    ClinicalNotes --> Supervision["Revisione con Supervisore Umano"]
```

- **Palestra Clinica a Rischio Zero:** Permette ai terapeuti in formazione di esercitarsi ripetutamente sulla conduzione di colloqui diagnostici e tecniche di ristrutturazione cognitiva senza alcun rischio iatrogeno per persone reali.
- **Consapevolezza dell'Effetto ELIZA:** Il training con Client101 richiede che gli allievi siano formati sui limiti del simulatore, evitando che internalizzino un'idea distorta di paziente ideale, passivo e privo di resistenze.

---

## Related pages
- [[Sunto_articoli]]
- [[bolt-behavioral-assessment-framework]]
- [[patient-psi-simulazione-clinica]]
- [[deliberate-practice-in-psicoterapia-ia]]
- [[diagnosis-of-thought-framework]]
- [[clinical-fidelity-assessment]]
- [[large-language-models]]
- [[ai-assisted-psychotherapy]]
