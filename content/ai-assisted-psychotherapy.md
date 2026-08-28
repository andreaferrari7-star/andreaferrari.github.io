# AI-Assisted Psychotherapy
**Summary**: Modello di integrazione di sistemi basati su intelligenza artificiale e [[large-language-models]] nei percorsi psicoterapeutici evidence-based (EBT). Descrive l'architettura di cooperazione uomo-macchina (dai compiti documentali al supporto agli esercizi inter-seduta), delineando limiti clinici, salvaguardie etiche e criteri di sicurezza.
**Sources**: 000.txt, 03-13 Avvio del Gruppo di Lavoro sull'Intelligenza Artificiale in Psicoterapia.txt
**Last updated**: 2026-08-27
---

## Definizione Operativa
L'**AI-Assisted Psychotherapy** (psicoterapia assistita dall'intelligenza artificiale) indica l'impiego strutturato di modelli linguistici avanzati ([[large-language-models]]), elaborazione del linguaggio naturale (NLP) e agenti software per potenziare, scalare e supportare l'erogazione di interventi psicologici evidence-based (EBT, quali CBT, CPT, Written Exposure Therapy).

A differenza dei chatbot consumer non regolamentati (spesso utilizzati dagli utenti tramite "wellness loopholes" senza garanzie cliniche), l'AI clinica assistita opera come infrastruttura di supporto al clinico o come estensione terapeutica supervisionata, integrandosi nei flussi di lavoro sanitari nel rispetto degli standard di riservatezza (HIPAA/BAA).

---

## Tassonomia di Autonomia Clinica: Il Paradigma "Self-Driving Car"
L'integrazione dell'AI nei contesti psicoterapeutici segue un percorso progressivo a stadi di maturità:

```
[Livello 1: AI-in-the-Loop]    --> [Livello 2: Clinician-on-the-Loop] --> [Livello 3: Autonomia Piena]
- Clinico alla guida                - Supervisione attiva del clinico        - Trattamento AI autonomo
- Scribing e note cliniche          - Supporto compiti inter-seduta          - Assessment e cura automatizzati
- Riduzione burnout                 - Simulazione clinica & training         - (Attualmente non applicabile)
```

1. **Livello 1: AI in the Loop (Clinico al comando primario)**:
   - L'AI assume compiti a basso rischio e ad alto carico burocratico: registrazione ambientale (*ambient listening*), trascrizione automatica e redazione di bozze di note cliniche per la cartella sanitaria elettronica (EHR).
   - Riduce il sovraccarico amministrativo e il burnout, consentendo al clinico di dedicare piena attenzione alla relazione terapeutica.
2. **Livello 2: Clinician on the Loop (Supervisione e co-pilotaggio)**:
   - L'AI assiste compiti intermedi guidati da protocolli manualizzati, come il supporto al paziente nello svolgimento dei compiti a casa (*Worksheet Helper* per CBT/CPT) o l'erogazione di feedback formativo simulato (*Therapy Trainer*).
   - Il terapeuta supervisiona tramite cruscotti digitali, intervenendo per validare gli output o gestire deviazioni cliniche ed emergenze.
3. **Livello 3: Trattamento Autonomo (Full Autonomous Treatment)**:
   - Valutazione psicodiagnostica, formulazione del caso, erogazione di interventi e adattamento dinamico eseguiti interamente dal sistema.
   - Attualmente confinato a sperimentazioni preliminari su sintomatologia lieve-moderata (es. RCT con LLM dedicati alla CBT a Dartmouth); non pronto per l'adozione clinica generale a causa di limiti epistemici, etici e normativi.

---

## Modelli Generici vs Purpose-Built Clinical AI
La ricerca evidenzia una divergenza sostanziale tra modelli LLM general-purpose e soluzioni cliniche dedicate:
- **LLM General-Purpose (es. GPT-4, Claude, Gemini)**: Addestrati su testi generici del web; producono dialoghi verosimili ma frammentari, invertono la sequenza logica dei protocolli manualizzati, omettono fasi cruciali di assessment e non dispongono di garanzie di riservatezza dei dati sanitari.
- **Purpose-Built Clinical AI**: Sistemi specificamente addestrati su trascrizioni cliniche annotate, manuali di trattamento ed esempi di interventi ad alta aderenza. Operano con controlli di sicurezza stringenti, monitoraggio continuo e conformità normativa (es. certificazioni FDA e framework etici APA).

---

## Funzioni Eseguibili e Limiti Strutturali
Dall'analisi delle linee guida professionali emergono chiaramente le competenze delegabili e i limiti invalicabili per i modelli linguistici:

### Competenze Delegabili all'AI:
- Erogazione scalabile di psicoeducazione standardizzata (disponibile 24/7).
- Approssimazione di empatia cognitiva e validazione linguistica di base.
- Riconoscimento di pattern testuali e marcatori linguistici di distress.
- Strutturazione e guida passo-passo negli esercizi di ristrutturazione cognitiva tra le sedute.
- Valutazione dell'aderenza ai protocolli ([[clinical-fidelity-assessment]]).

### Limiti Strutturali dell'AI (Necessità del Clinico Umano):
- Incapacità di stabilire un'autentica alleanza terapeutica umana (nonostante buone valutazioni di "alleanza digitale" percepita).
- Mancanza di decodifica e integrazione del comportamento non verbale e paraverbale complesso.
- Incapacità di gestire rotture e riparazioni dell'alleanza clinica (*rupture and repair*).
- Giudizio clinico ed euristico in contesti complessi, contraddittori o ad alta ambiguità.
- Responsabilità etica e deontologica vincolante.

---

## Sicurezza, Architetture Multi-Agente e Mitigazione del De-Skilling
1. **Architetture di Sicurezza Multi-Agente**: Separazione operativa tra l'agente che interagisce con l'utente (paziente o terapeuta) e sotto-agenti sentinella specializzati (*Safety Monitor* per intercettare ideazione suicidaria/autolesionismo; *Fidelity Monitor* per verificare la conformità al protocollo).
2. **Finestre di Contesto e Memoria a Lungo Termine**: Necessità di tracciare indicatori di rischio distribuiti su mesi di sedute, superando i limiti di oblio delle finestre di contesto standard.
3. **Prevenzione del De-Skilling Clinico**: Per evitare l'atrofia delle competenze dei terapeuti causata da suggerimenti automatizzati passivi, gli strumenti di supporto (es. *Coach AI*) sono progettati per stimolare la concettualizzazione del caso, la formulazione diagnostica e la riflessione critica.

## Related pages
- [[000]]
- [[03-13_Avvio_Gruppo_Lavoro_IA_Psicoterapia]]
- [[clinical-fidelity-assessment]]
- [[large-language-models]]
- [[ai-research-ethics]]
- [[prompting-in-psychology]]
- [[adamkovic-2025]]
