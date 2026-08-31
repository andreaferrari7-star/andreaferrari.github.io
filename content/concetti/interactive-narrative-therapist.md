---
title: Interactive Narrative Therapist (INT)
tags: [IA, Psicoterapia, Terapia Narrativa, RAG]
---

# Interactive Narrative Therapist (INT)

## Definizione Operativa
Framework architetturale basato su Large Language Models per la simulazione rigorosa di psicoterapeuti narrativi esperti. INT formalizza la progressione della seduta attraverso uno spazio di pianificazione gerarchico a due livelli (stadi terapeutici e livelli di riflessione intra-stadio) integrato con Retrieval-Augmented Generation (RAG) da un repository di interventi clinici esemplari.

Nella simulazione di colloqui terapeutici mediante [[large-language-models]], i modelli di role-playing diretto tendono a produrre risposte generiche, focalizzandosi eccessivamente sulla validazione empatica superficiale (*Reassuring*) e fallendo nel guidare il paziente verso la progressione terapeutica. L'**Interactive Narrative Therapist (INT)** (Feng et al., 2025) risolve questo problema traducendo la pratica clinica della terapia narrativa in un'architettura computazionale controllata da uno spazio di pianificazione formale $\Phi = (\mathcal{S}, \mathcal{L})$.

### Architettura a Due Livelli di Pianificazione

1. **Stage Planning ($\mathcal{S}$)**: Ad ogni turno $t$, la funzione di pianificazione $\Psi_S(H_t, C_t, \pi_{stage})$ valuta lo stato del dialogo e assegna uno dei 4 stadi progressivi:
    * $s_1$: Trust Building (Costruzione della Fiducia)
    * $s_2$: Problem Externalization (Esternalizzazione del Problema)
    * $s_3$: Re-authoring Conversation (Riscrivere la Narrazione)
    * $s_4$: Re-membering Conversation (Ri-membrare i Legami)

2. **Reflection Level Planning ($\mathcal{L}$)**: All'interno dello stadio $s_t$, la funzione $\Psi_L(s_t, H_t, C_t, \pi_{reflection})$ seleziona il micro-livello di ingaggio riflessivo $l_t^t \in \mathcal{L}_t$, consentendo una progressione calibrata.

### Retrieval-Augmented Generation (RAG) Guidato dallo Stato
Una volta identificato lo stato terapeutico $(s_t, l_t^t)$, INT interroga un database indicizzato di risposte cliniche esperte $\mathcal{E}$ per generare risposte vincolate a rispettare la posizione di *“decentered yet influential”*.

## Evidenze dalla Letteratura
Nei trial sperimentali con 230 partecipanti umani e 260 profili simulati:
* **Efficacia nelle Dimensioni Trasformative**: Rispetto a GPT-4o e Claude-3.7 in modalità role-playing, INT ottiene incrementi marcati nelle dimensioni avanzate della terapia: **Empowering (+0.36)**, **Transformative (+0.90)** e **Reconnecting (+0.88)**.
* **Raddoppio dei Marcatori di Cambiamento**: INT stimola quasi il doppio degli *Innovative Moments* di Livello 2 (azioni future e ridefinizione del sé) valutati tramite [[innovative-moment-assessment]].
* **Coinvolgimento del Paziente**: Produce dialoghi significativamente più lunghi (57 vs 42 turni medi) con risposte dell'utente più ricche e articolate (38.8 vs 31.5 parole per turno).

**Riferimenti Bibliografici:**
* Feng, et al. (2025). *Interactive Narrative Therapist*.
* White, M., & Epston, D. (1990). *Narrative Means to Therapeutic Ends*.
* White, M. (2007). *Maps of Narrative Practice*.

## Relazioni
- [[feng-et-al-2025]]
- [[terapia-narrativa-ia]]
- [[innovative-moment-assessment]]
- [[rag-in-psicoterapia]]
- [[clinical-fidelity-assessment]]
- [[simulazione-pazienti-ai]]
- [[process-of-change]]
