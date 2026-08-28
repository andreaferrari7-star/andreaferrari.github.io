---
tags: [crdial, cognitive-restructuring, cbt-dialogica, architettura-clinica, multi-turn-dialogue, llm-psicoterapia]
source_papers: ["2504.17238v1.pdf"]
---

# CRDIAL Framework

## Definizione Operativa
- Framework metodologico e computazionale progettato per strutturare interventi di **Ristrutturazione Cognitiva (Cognitive Restructuring, CR)** in agenti conversazionali e modelli linguistici di larga scala (LLM) attraverso dialoghi clinici multi-fase e multi-turno.
- **Utilità CBT:** Supera i limiti della mera riscrittura testuale (*text reframing*) e dei flussi a pattern rigido, articolando la seduta in due macro-fasi cliniche rigorose: (1) **Identificazione guidata dalla Teoria Cognitiva** (esplorazione gerarchica: pensieri automatici $\rightarrow$ credenze intermedie $\rightarrow$ credenze di base/distorsioni) e (2) **Ristrutturazione guidata dalla Defense Attorney Technique** (processo maieutico a tre stadi: Difesa, Accusa, Verdetto), integrando vincoli di strategie supportive a livello di singola frase e meccanismi multi-canale a ciclo continuo.

```mermaid
flowchart TD
    subgraph CRDIAL ["Framework CRDIAL"]
        direction TB
        subgraph Stage1 ["1. Identificazione (Cognitive Theory - Beck)"]
            S1_1["Esplorazione Pensieri Automatici (Automatic Thoughts)"]
            S1_2["Analisi Credenze Intermedie (Intermediate Beliefs)"]
            S1_3["Dissezione Credenze di Base / Distorsioni (Core Beliefs)"]
            S1_1 --> S1_2 --> S1_3
        end

        subgraph Stage2 ["2. Ristrutturazione (Defense Attorney Technique - de Oliveira)"]
            S2_1["Difesa (Defense): Raccolta Fatti a Supporto"]
            S2_2["Accusa (Prosecution): Confutazione Logico-Fattuale"]
            S2_3["Verdetto (Verdict): Valutazione Ristrutturazione"]
            S2_1 --> S2_2 --> S2_3
        end

        subgraph Support ["Vincoli Trasversali"]
            SS["Strategie Supportive Sentence-Level (Hill & Linehan)"]
            CS["Integrazione Senso Comune (ATOMIC 10x)"]
            MC["Multi-Channel & Loop Mechanism"]
        end

        Stage1 -->|Canali Multipli (≤3)| Stage2
        Stage2 -->|Loop Check| Stage1
        Support -.-> Stage1
        Support -.-> Stage2
    end
```

## Evidenze dalla Letteratura
- **Allineamento al Processo Psicoterapeutico Reale:** La formulazione standard della CBT (Beck, 1979, 2011) richiede una progressione graduale dalla superficie cognitiva alle strutture nucleari; CRDIAL traduce questa dinamica vincolando il self-chat e la generazione dell'LLM a non saltare fasi e a non imporre conclusioni premature (Zhou et al., 2025).
- **Gestione della Resistenza Emotiva:** Integrando 8 sotto-strategie di supporto emotivo (derivate da Hill, 2009 e Linehan, 2014) codificate frase per frase, il framework garantisce che ogni stimolo di sfida cognitiva sia bilanciato da validazione, rispecchiamento o empatia, riducendo le reazioni di rigetto (Zhou et al., 2025).
- **Adattamento alle Differenze Individuali:** Tramite la ramificazione multi-canale (fino a 3 distorsioni simultanee per problema) e la ricorsione ciclica (*loop*), CRDIAL garantisce la completezza della ristrutturazione, coprendo sistematicamente i bias associati (Zhou et al., 2025).

**Riferimenti Bibliografici:**
- Zhou, J., Chen, Y., Yin, J., Huang, Y., Shi, Y., Zhang, X., Peng, L., Zhang, R., Lv, T., Hu, Z., Wang, H., & Huang, M. (2025). CRISP: Cognitive Restructuring of Negative Thoughts through Multi-turn Supportive Dialogues. *arXiv preprint arXiv:2504.17238*. https://arxiv.org/abs/2504.17238
- Beck, A. T. (1979). *Cognitive therapy and the emotional disorders*. Penguin.
- Beck, J. S. (2011). *Cognitive behavior therapy: Basics and beyond*. Guilford Publications.

## Relazioni
- Vedi anche: [[zhou-et-al-2025]], [[defense-attorney-technique]], [[sentence-level-supportive-strategies]], [[multi-channel-loop-mechanism]], [[crispers-models-and-dataset]], [[active-ai-therapeutic-agent]], [[conversational-agents-mental-health]], [[digital-therapeutic-alliance]]
