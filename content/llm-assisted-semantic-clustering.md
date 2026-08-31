---
Summary: Metodologia ibrida per la sintesi della letteratura scientifica che combina Large Language Models con supervisione umana iterativa (Human-in-the-Loop) per raggruppare costrutti eterogenei in cluster semantici flessibili e gerarchici.
Sources: 1-s2.0-S0272735826000917-main.pdf
Last updated: 2026-08-27
---

# LLM-Assisted Semantic Clustering

## Definizione Operativa
L'**LLM-Assisted Semantic Clustering** è un approccio ibrido di classificazione ed estrazione concettuale progettato per mappare e sintetizzare corpora testuali ampi, non strutturati e frammentati (come le etichette di costrutti psicologici estratte da revisioni della letteratura).

A differenza degli algoritmi di clustering tradizionali (es. k-means o clustering gerarchico basato su distanze vettoriali di embedding), questa metodologia si caratterizza per:
1. **Flessibilità Semantica e Multi-appartenenza**: Consente assegnazioni "fuzzy" e multilivello in cui un singolo costrutto può appartenere a più cluster a differenti livelli di astrazione gerarchica.
2. **Human-in-the-Loop (HITL)**: Integra cicli iterativi di supervisione umana esperta (prompting few-shot, ispezione qualitativa, correzione di errori, fusione/divisione di cluster).
3. **Adattamento Progressivo**: La tassonomia concettuale evolve dinamicamente analizzando nuovi lotti di dati, evitando la rigidità di schemi teorici imposti a priori.

## Evidenze dalla Letteratura
Nello studio di [[1-s2-0-s0272735826000917-main|Hofmann et al. (2026)]], questo workflow è stato implementato con successo in Python utilizzando OpenAI GPT-5 nano:
- **Corpus**: 684 etichette uniche di processi terapeutici estratte da 778 studi di psicoterapia (2007–2025).
- **Workflow**: Suddivisione in blocchi da 100 frasi, vincolo su output JSON strutturato, raffinamento guidato da esempi teoricamente fondati e validazione deterministica finale per azzerare le allucinazioni.
- **Esito**: Generazione di 32 macro-cluster coerenti con i modelli teorici evidence-based (CBT, fattori comuni), riducendo drasticamente la frammentazione terminologica.

**Riferimenti Bibliografici:**
- [[1-s2-0-s0272735826000917-main|Hofmann, S. G., et al. (2026)]]. 

## Relazioni
- [[1-s2-0-s0272735826000917-main]]
- [[processes-of-change-in-psychotherapy]]
- [[structured-literature-reviews]]
- [[hybrid-ai-research-workflows]]
- [[llm-assisted-synthesis]]
- [[jingle-fallacy]]
- [[jangle-fallacy]]
