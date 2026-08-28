# LLM-Assisted Semantic Clustering
**Summary**: Metodologia ibrida per la sintesi della letteratura scientifica che combina Large Language Models con supervisione umana iterativa (Human-in-the-Loop) per raggruppare costrutti eterogenei in cluster semantici flessibili e gerarchici.
**Sources**: 1-s2.0-S0272735826000917-main.pdf
**Last updated**: 2026-08-27
---

## Definizione e Razionale Metodologico
L'**LLM-Assisted Semantic Clustering** è un approccio ibrido di classificazione ed estrazione concettuale progettato per mappare e sintetizzare corpora testuali ampi, non strutturati e frammentati (come le etichette di costrutti psicologici estratte da revisioni della letteratura).

A differenza degli algoritmi di clustering tradizionali ("hard" clustering deterministico come k-means o clustering gerarchico puramente basato su distanze vettoriali di embedding):
1. **Flessibilità Semantica e Multi-appartenenza**: Consente assegnazioni "fuzzy" e multilivello in cui un singolo costrutto o frase può appartenere a più cluster a differenti livelli di astrazione gerarchica, rispecchiando la natura multidimensionale dei costrutti psicologici e clinici.
2. **Human-in-the-Loop (HITL)**: Integra cicli iterativi di supervisione umana esperta (prompting few-shot, ispezione qualitativa degli output, correzione di errori di categorizzazione, fusione o divisione di cluster e rimozione di allucinazioni).
3. **Adattamento Progressivo**: La tassonomia concettuale evolve dinamicamente man mano che nuovi lotti di dati vengono analizzati dal modello linguistico, evitando la rigidità di schemi teorici imposti arbitrariamente a priori.

## Applicazione nella Ricerca Clinica
Nello studio di [[1-s2.0-S0272735826000917-main|Hofmann et al. (2026)]], questo workflow è stato implementato con successo in Python utilizzando OpenAI GPT-5 nano:
- **Corpus**: 684 etichette uniche di processi terapeutici estratte da 778 studi di psicoterapia (2007–2025).
- **Workflow**: Suddivisione in blocchi da 100 frasi, vincolo su output JSON strutturato, raffinamento guidato da esempi teoricamente fondati (es. separazione tra *reappraisal* cognitivo e costrutti di *positive psychology*), e validazione deterministica finale contro il dizionario originale delle frasi per azzerare le allucinazioni.
- **Esito**: Generazione di 32 macro-cluster coerenti con i modelli teorici evidence-based (come CBT e fattori comuni), riducendo drasticamente la frammentazione terminologica senza perdere specificità clinica.

## Vantaggi e Sfide
- **Vantaggi**: Scalabilità su migliaia di record testuali, coerenza semantica superiore rispetto all'estrazione manuale isolata, riduzione dei bias soggettivi di un singolo ricercatore.
- **Sfide e Limiti**: Dipendenza dai giudizi interpretativi del team di ricerca nella fase di supervisione; rischio di cluster con confini sfumati che richiedono successiva validazione psicometrica o fattoriale.

## Related pages
- [[1-s2.0-S0272735826000917-main]]
- [[processes-of-change-in-psychotherapy]]
- [[structured-literature-reviews]]
- [[hybrid-ai-research-workflows]]
- [[llm-assisted-synthesis]]
- [[jingle-fallacy]]
- [[jangle-fallacy]]
