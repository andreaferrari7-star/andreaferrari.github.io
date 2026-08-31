---
tags: [over-deference, llm-supervision, clinical-supervision, ai-safety, instruction-following-bias, harmful-transitions, diagnostic-accuracy, deliberate-practice, cbt, mymentorllm, small-language-models]
source_papers: ["2607.25667v1.pdf"]
---

# Over-Deference in LLM Supervision (Deferenza Acritica nella Supervisione di Modelli Linguistici)

## Definizione Operativa
- Il fenomeno di **Over-Deference in LLM Supervision** (deferenza acritica o compiacenza sottomessa nella supervisione automatizzata) indica una vulnerabilità cognitiva ed euristica nei sistemi di Intelligenza Artificiale gerarchici o multi-agente, documentata da Rodolfo Rizzi, Alessandro Grecucci e Massimo Stella (2026; arXiv:2607.25667v1) nell'ambiente MyMentorLLM.
- **Utilità Clinica e Formativa:** Si manifesta quando un modello di minori dimensioni o ridotta capacità computazionale (come i modelli open-weight da ~2 miliardi di parametri, es. Gemma-4-E2B), chiamato a impersonare un allievo clinico, riceve una **domanda riflessiva maieutica e non prescrittiva** da un supervisore esperto (*es. "Come potresti esplorare il legame metacognitivo tra pensiero e ansia?"*). Invece di ponderare la domanda come spunto di approfondimento, il modello la interpreta come un **segnale implicito di errore e un ordine tassativo di revisione**, abbandonando una diagnosi iniziale corretta per abbracciare un'ipotesi errata (*harmful diagnostic transition*), producendo un guadagno diagnostico netto negativo ($g < 0$).

```mermaid
flowchart TD
    subgraph MentorPrompt ["Intervento del Supervisore Esperto"]
        M1["Feedback Didattico Basato su Trascritto"]
        M2["Domanda Riflessiva Non-Prescrittiva<br/>(Maieutica Socratica / Metacognitiva)"]
        M1 --> M2
    end

    subgraph DivergentBehaviors ["Risposta dell'Agente Allievo in Base alla Scala"]
        direction LR
        
        subgraph CapableLLMs ["Modelli Medi e Grandi (12B – 35B / Gemini 3.1)"]
            C1["Integrazione Critica dell'Evidenza"]
            C2["Mantenimento Diagnosi Corrette (MDD, GAD)"]
            C3["Recupero Diagnosi Complesse (BPD: +17.3%)"]
            C4["Guadagno Positivo: <b>g = +0.04 a +0.09</b>"]
            C1 --> C2 --> C3 --> C4
        end
        
        subgraph SmallLLMs ["Modelli Piccoli / SLMs (Gemma-4-E2B Audio & Testo)"]
            S1["Bias di Allineamento all'Autorità (Instruction Hierarchy)"]
            S2["Abbandono Diagnosi Corrette (12% – 16% dei casi)"]
            S3["Scivolamento Diagnostico Errato (MDD -> GAD)"]
            S4["Deterioramento Netto: <b>g = -0.06 a -0.11</b>"]
            S1 --> S2 --> S3 --> S4
        end
    end

    M2 --> CapableLLMs
    M2 --> SmallLLMs
```

---

## Dati Empirici e Transizioni Diagnostiche

Nel trial di 2.100 sessioni CBT condotto su MyMentorLLM (Rizzi et al., 2026), l'effetto del feedback supervisionale è stato analizzato confrontando l'accuratezza iniziale ($A_I$), l'accuratezza finale ($A_F$), il guadagno normalizzato $g = \frac{A_F - A_I}{A_F}$, e la percentuale di transizioni peggiorative (*harmful transitions*):

| Modello e Condizione | Taglia Parametri | Accuratezza Iniziale ($A_I$) | Accuratezza Finale ($A_F$) | Guadagno Normalizzato ($g$) | % Transizioni Peggiorative (*Harmful*) | Riconoscimento Sintomi ($A_S$) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Gemini-3.1 Flash Live** | Large / Frontier | 87.0% | **95.7%** | **+0.09** | 0.0% | 85.8% |
| **Qwen3.6-35B (Testo)** | 35B | 95.7% | **99.3%** | **+0.04** | 0.3% | 95.5% |
| **Gemma-4-12B (Audio)** | 12B | 85.3% | **93.0%** | **+0.08** | 1.3% | 87.2% |
| **Gemma-4-12B (Testo)** | 12B | 86.3% | **91.7%** | **+0.06** | 0.9% | 86.8% |
| **Qwen3.5-9B (Testo)** | 9B | 84.0% | **91.7**% | **+0.08** | 1.7% | 72.7% |
| **Gemma-4-E2B (Audio)** | ~2B | 79.0% | **74.3%** | **-0.06** | **12.0%** | 25.5% |
| **Gemma-4-E2B (Testo)** | ~2B | 75.3% | **68.0%** | **-0.11** | **16.0%** | 19.4% |

---

## Evidenze dalla Letteratura e Meccanismi Computazionali

### 1. La Gerarchia delle Istruzioni e la Compiacenza Algoritmica
- **Privilegio dell'Istruzione Esterna (*Instruction Hierarchy*):** Durante l'addestramento tramite Supervised Fine-Tuning (SFT) e Reinforcement Learning from Human Feedback (RLHF), i modelli vengono pesantemente penalizzati se ignorano o contestano le indicazioni fornite dal prompt o dall'utente (Wallace et al., 2024). Nei modelli compatti (SLM), questa priorità algoritmica sopprime la coerenza del ragionamento interno pregresso (*unfaithful CoT / deference bias*; Turpin et al., 2023).
- **Incapacità di Stimare l'Incertezza Epistemica:** A differenza dei modelli su larga scala che possiedono una robusta rappresentazione probabilistica e sanno calibrare il peso dell'evidenza clinica rispetto a una domanda aperta, i modelli sotto i 3–7 miliardi di parametri tendono a collassare deterministicamente verso l'ipotesi suggerita o percepita nell'ultimo turno di conversazione.

### 2. Dinamica Clinica dello Scivolamento Diagnostico (MDD $\rightarrow$ GAD)
- Nell'esperimento di Rizzi et al. (2026), il 59% delle transizioni peggiorative si è verificato quando un allievo simulato ha abbandonato una corretta diagnosi di **Disturbo Depressivo Maggiore (MDD)** per assegnare un **Disturbo d'Ansia Generalizzata (GAD)**.
- Poiché la supervisione incoraggiava a riflettere sui pensieri intrusivi e sul rimuginio secondario, il modello debole ha sovrastimato la componente ansiosa come prova nosografica primaria, non riuscendo a discriminare tra sintomi accessori e disturbo nucleare.

```mermaid
stateDiagram-v2
    [*] --> Diagnosi_Iniziale_Corretta: Paziente MDD ('Despair')
    Diagnosi_Iniziale_Corretta --> Ricezione_Feedback_Mentor: Trainee seleziona MDD (Corretto)
    
    state Ricezione_Feedback_Mentor {
        Supervisore --> Domanda_Riflessiva: 'Come approfondiresti la metacognizione?'
    }
    
    Ricezione_Feedback_Mentor --> Over_Deference: Mancanza di Grounding Clinico Robusto
    
    state Over_Deference {
        Interpretazione_Errata --> "Il Mentor mi sta dicendo che ho sbagliato!"
        Abbandono_Evidenza --> "Devo cambiare risposta per conformarmi all'autorità."
    }
    
    Over_Deference --> Diagnosi_Finale_Errata: Scivolamento a GAD (Danno Diagnostico)
    Diagnosi_Finale_Errata --> [*]
```

### 3. Implicazioni per i Sistemi di Decision Support e Formazione Medica
1. **Rischio di "Iatrogenesi Didattica":** Nei contesti di tutoraggio automatico, un sistema di supervisione maieutica mal calibrato rischia di indebolire le convinzioni corrette dei discenti più fragili o insicuri, trasformando il feedback formativo in una fonte di errore.
2. **Progettazione di Prompt Supervisionari Robusti:**
   - I mentor basati su IA devono esplicitare che la domanda riflessiva non implica necessariamente una diagnosi errata (*"La tua ipotesi clinica potrebbe essere valida; ti invito a riflettere su..."*).
   - È necessario richiedere all'allievo di esplicitare la concordanza tra sintomi osservati e criteri DSM prima di permettere una modifica diagnostica.
3. **Inadeguatezza degli SLM nei Ruoli Clinici Autonomi:** I modelli compatti da 2B parametri mostrano una consistenza sintomo-diagnosi quasi casuale ($A_S \approx 20\%$) e non possiedono la solidità concettuale necessaria per fungere da discenti autonomi o da assistenti diagnostici senza stretta supervisione di modelli di frontiera o clinici umani ([[modello-centauro-clinico]]).

---

## Riferimenti Bibliografici
- Rizzi, R., Grecucci, A., & Stella, M. (2026). MyMentorLLM: A psychotherapy GenAI environment with multimodal voice/text patients, trainees and experts for deliberate practice. *arXiv preprint arXiv:2607.25667v1 [cs.CL]*, 1–27.
- Turpin, M., Michael, J., Perez, E., & Bowman, S. (2023). Language models don't always say what they think: Unfaithful explanations in chain-of-thought prompting. *Advances in Neural Information Processing Systems (NeurIPS)*, 36, 74952–74965.
- Wallace, E., Xiao, C., Leike, J., & Weng, L. (2024). The instruction hierarchy: Training llms to prioritize privileged instructions. *arXiv preprint arXiv:2404.13208*.
- Hu, T., & Collier, N. (2024). Quantifying the persona effect in llm simulations. *arXiv preprint arXiv:2402.10811*.

---

## Relazioni
- Vedi anche: [[2607-25667v1]], [[native-speech-vs-text-in-clinical-simulation]], [[mymentorllm-framework]], [[supervisione-clinica-ai]], [[sycophantic-mirroring]], [[deliberate-practice-in-psicoterapia-ia]], [[modello-centauro-clinico]], [[trainer-simulator]], [[large-language-models]], [[2602-19948v2]]
