---
tags:
  - ai-assisted-psychotherapy
  - CBT
  - large-language-models
  - evidence-based-psychotherapy
source_papers:
  - 000
  - 03-13_Avvio_Gruppo_Lavoro_IA_Psicoterapia
---

# AI-Assisted Psychotherapy

## Definizione Operativa
- Sintesi: Modello di integrazione di sistemi basati su intelligenza artificiale, [[large-language-models]] (LLM), elaborazione del linguaggio naturale (NLP) e agenti software nei percorsi psicoterapeutici evidence-based (EBT). Descrive un'architettura di cooperazione uomo-macchina che opera come infrastruttura di supporto al clinico o come estensione terapeutica supervisionata, integrandosi nei flussi di lavoro sanitari nel rispetto degli standard di riservatezza (HIPAA/BAA). Si distingue nettamente dai chatbot consumer non regolamentati (usati tramite "wellness loopholes") per le sue rigorose salvaguardie etiche, i limiti clinici definiti e i criteri di sicurezza che portano il sistema ad occuparsi da compiti documentali fino al supporto agli esercizi inter-seduta. 
- **Utilità CBT:** Potenzia e scala l'erogazione di interventi come la CBT, la CPT e la Written Exposure Therapy. Supporta la strutturazione e funge da guida passo-passo negli esercizi di ristrutturazione cognitiva tra le sedute. Inoltre, agisce come *Worksheet Helper* per lo svolgimento dei compiti a casa e provvede all'erogazione di psicoeducazione standardizzata scalabile (disponibile 24/7).

## Evidenze dalla Letteratura

### Tassonomia di Autonomia Clinica: Il Paradigma "Self-Driving Car"
L'integrazione dell'AI segue un percorso progressivo a stadi di maturità [1, 2]:
- **Livello 1: AI in the Loop (Clinico al comando primario)**. Assunzione di compiti a basso rischio e ad alto carico burocratico come registrazione ambientale (*ambient listening*), trascrizione automatica e redazione di bozze di note cliniche per la cartella sanitaria elettronica (EHR). L'obiettivo primario è ridurre il burnout amministrativo per permettere al clinico di dedicare piena attenzione alla relazione terapeutica [1].
- **Livello 2: Clinician on the Loop (Supervisione e co-pilotaggio)**. L'AI assiste compiti intermedi guidati da protocolli manualizzati (es. supporto ai pazienti per i compiti a casa o feedback formativo simulato tramite *Therapy Trainer*). Il terapeuta supervisiona attivamente tramite cruscotti digitali, intervenendo per validare gli output o gestire deviazioni cliniche ed emergenze [1].
- **Livello 3: Trattamento Autonomo (Full Autonomous Treatment)**. Valutazione psicodiagnostica, formulazione del caso, erogazione di interventi e adattamento dinamico eseguiti interamente dal sistema. Ad oggi è confinato a sperimentazioni preliminari su sintomatologia lieve-moderata (es. RCT con LLM dedicati alla CBT a Dartmouth); attualmente non applicabile per l'adozione clinica a causa di limiti epistemici, normativi ed etici [1, 2].

### Modelli Generici vs Purpose-Built Clinical AI
La ricerca evidenzia una sostanziale differenza tra gli strumenti a disposizione [1, 2]:
- **LLM General-Purpose (es. GPT-4, Claude, Gemini)**: Addestrati su testi generici del web; possono produrre dialoghi verosimili ma frammentari. Spesso invertono la sequenza logica dei protocolli manualizzati, omettono fasi cruciali di assessment e non dispongono di garanzie di riservatezza dei dati sanitari [1].
- **Purpose-Built Clinical AI**: Sistemi specificamente addestrati su trascrizioni cliniche annotate, manuali di trattamento ed esempi di interventi ad alta aderenza. Operano con controlli di sicurezza stringenti, monitoraggio continuo e conformità normativa (es. certificazioni FDA e framework etici APA) [1, 2].

### Funzioni Eseguibili e Limiti Strutturali
Dall'analisi delle linee guida professionali emergono competenze delegabili e limiti invalicabili per i modelli linguistici [1, 2]:
- **Competenze Delegabili all'AI**: Erogazione scalabile di psicoeducazione (24/7), approssimazione di empatia cognitiva e validazione linguistica di base, riconoscimento di pattern e marcatori testuali di distress, strutturazione guidata di esercizi di ristrutturazione cognitiva tra le sedute, e valutazione dell'aderenza ai protocolli ([[clinical-fidelity-assessment]]).
- **Limiti Strutturali dell'AI (Necessità del Clinico Umano)**: Incapacità di stabilire un'autentica alleanza terapeutica umana (nonostante buone valutazioni di "alleanza digitale" percepita), mancanza di decodifica e integrazione del comportamento non verbale e paraverbale complesso. L'AI è incapace di gestire le rotture e le riparazioni dell'alleanza clinica (*rupture and repair*), non possiede giudizio euristico o clinico in contesti complessi e ad alta ambiguità, ed è priva di responsabilità etica e deontologica vincolante [1, 2].

### Sicurezza, Architetture Multi-Agente e Mitigazione del De-Skilling
Le evidenze sottolineano la necessità di cautele strutturali [1]:
- **Architetture di Sicurezza Multi-Agente**: Separazione operativa tra agente che interagisce con l'utente (paziente o terapeuta) e sotto-agenti sentinella specializzati (*Safety Monitor* per intercettare ideazione suicidaria/autolesionismo; *Fidelity Monitor* per verificare la conformità al protocollo) [1].
- **Finestre di Contesto e Memoria a Lungo Termine**: Necessità di tracciare indicatori di rischio distribuiti su mesi di sedute, superando i limiti di oblio tipici delle finestre di contesto standard [1, 2].
- **Prevenzione del De-Skilling Clinico**: Per evitare l'atrofia delle competenze dei terapeuti causata da suggerimenti automatizzati passivi, gli strumenti di supporto (es. *Coach AI*) sono progettati per stimolare la concettualizzazione del caso, la formulazione diagnostica e la riflessione critica [1].

**Riferimenti Bibliografici:**
- [1] 000.txt
- [2] 03-13 Avvio del Gruppo di Lavoro sull'Intelligenza Artificiale in Psicoterapia.txt

## Relazioni
- [[000]]
- [[03-13_Avvio_Gruppo_Lavoro_IA_Psicoterapia]]
- [[clinical-fidelity-assessment]]
- [[large-language-models]]
- [[ai-research-ethics]]
- [[prompting-in-psychology]]
- [[adamkovic-2025]]
