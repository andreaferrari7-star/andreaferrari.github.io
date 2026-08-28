---
tags: [coast-framework, clinical-prompting, prompt-engineering, scaffolding-cognitivo, subjectivity-assessment, contrastive-reasoning, schema-analysis, in-context-learning, few-shot-prompting, clinical-nlp, cbt-prompting]
source_papers: ["Clinical_AI_Blueprint.pdf"]
---

# Framework COAST e Prompting Clinico a Livelli di Astrazione

## Definizione Operativa
- Il **Framework COAST** è una metodologia strutturata di prompt engineering clinico progettata per proceduralizzare le richieste rivolte ai [[large-language-models]] (LLM) in contesti psicoterapeutici e di salute mentale, trasformando istruzioni vaghe in una rigida **impalcatura cognitiva (*cognitive scaffolding*)**.
- **La Struttura Pentapartita COAST:**
  1. **C - Context (Contesto):** Definizione del setting clinico, dell'orientamento teorico (es. CBT standard, ACT, terapia metacognitiva) e delle coordinate epidemiologico-anamnestiche.
  2. **O - Objective (Obiettivo):** Dichiarazione esplicita del target clinico dell'analisi (es. concettualizzazione del caso, estrazione di pensieri automatici disfunzionali, individuazione di trigger situazionali ed evitamenti).
  3. **A - Actions (Azioni):** Sequenza logico-metodologica vincolata di passi inferenziali che il modello deve eseguire in modo sequenziale.
  4. **S - Scenario (Scenario):** Vincoli anagrafici, elementi psicosociali, fattori di mantenimento e caratteristiche del paziente.
  5. **T - Task (Task):** Formato di output standardizzato e strutturato richiesto (es. note cliniche SOAP, schema ABC cognitivo, formulazione condivisa a tabella).
- **I Tre Livelli di Astrazione Deduttiva:** COAST vincola il ragionamento del modello a seguire una progressione a 3 stadi gerarchici (*Subjectivity Assessment* $\rightarrow$ *Contrastive Reasoning* $\rightarrow$ *Schema Analysis*), impedendo il salto prematuro a conclusioni diagnostiche affrettate (*premature closure*) e il tipico bias di problem-solving precoce dei modelli generativi commerciali.

```mermaid
flowchart TD
    subgraph COAST_Structure ["Architettura del Prompt COAST"]
        C["<b>Context</b><br/>Setting, orientamento teorico, coordinate cliniche"]
        O["<b>Objective</b><br/>Target analitico (concettualizzazione, bias, schemi)"]
        A["<b>Actions</b><br/>Step inferenziali sequenziali vincolati"]
        S["<b>Scenario</b><br/>Dati paziente, vincoli psicosociali, anamnesi"]
        T["<b>Task</b><br/>Output standardizzato (SOAP, ABC, tabelle)"]
        
        C --> O --> A --> S --> T
    end

    subgraph CognitiveScaffolding ["I 3 Livelli di Astrazione Inferenziale"]
        L1["<b>Livello 1: Subjectivity Assessment</b><br/>Separare rigorosamente i fatti empirici oggettivi dall'interpretazione soggettiva del paziente"]
        L2["<b>Livello 2: Contrastive Reasoning</b><br/>Generare ipotesi cliniche alternative divergenti e analisi pro/contro bilanciata"]
        L3["<b>Livello 3: Schema Analysis</b><br/>Inferire le credenze nucleari (Core Beliefs) e le distorsioni cognitive sottostanti"]
        
        L1 --> L2 --> L3
    end

    COAST_Structure --> CognitiveScaffolding
```

---

## I Tre Livelli di Astrazione nel Ragionamento Clinico Assistito

```mermaid
mindmap
  root((Scaffolding COAST))
    Livello 1: Subjectivity Assessment
      Isolamento Fatti Empirici
      Filtro Pregiudizio Soggettivo
      Mappatura Trigger Situazionali
    Livello 2: Contrastive Reasoning
      Ipotesi Primaria vs Alternativa
      Analisi Pro e Contro
      Contrasto Bias di Ancoraggio
    Livello 3: Schema Analysis
      Pensieri Automatici Negativi (NAT)
      Distorsioni Cognitive (es. Personalizzazione)
      Core Beliefs e Schemi di Sé
```

### Livello 1: Subjectivity Assessment (Valutazione della Soggettività)
- **Scopo:** Decontaminare i dati grezzi del paziente, separando nettamente i fatti oggettivi osservabili (es. *"Il responsabile non ha risposto alla mia email entro due ore"*) dalle interpretazioni, inferenze e proiezioni soggettive del paziente (es. *"Vuole licenziarmi e pensa che io sia incompetente"*).
- **Funzione Clinica:** Impedisce al modello di allinearsi acriticamente alla narrazione catastrofica del paziente, ponendo le basi per l'esame di realtà e la ristrutturazione cognitiva.

### Livello 2: Contrastive Reasoning (Ragionamento Contrastivo)
- **Scopo:** Forzare il modello linguistico a produrre molteplici ipotesi esplicative divergenti e plausibili per la medesima situazione clinica, valutandone criticamente le evidenze a favore e contrarie.
- **Funzione Clinica:** Neutralizza il naturale bias di conferma dell'algoritmo, sbloccando la fissità interpretativa del clinico in formazione e favorendo il pensiero differenziale prima di formulare la concettualizzazione definitiva.

### Livello 3: Schema Analysis (Analisi degli Schemi Profondi)
- **Scopo:** Identificare le distorsioni cognitive sistematiche (es. *Personalizzazione*, *Pensiero Dicotomico*, *Catastrofizzazione*, *Iper-generalizzazione*) e risalire induttivamente ai *Core Beliefs* e agli schemi maladattivi precoci sottostanti.
- **Funzione Clinica:** Eleva l'analisi dal livello puramente descrittivo/sintomatologico a quello eziopatogenetico e funzionale, in piena aderenza ai modelli CBT avanzati.

---

## Integrazione Metodologica: Few-Shot Prompting e In-Context Learning

```mermaid
flowchart LR
    Unstructured["Trascritto Clinico Disordinato & Rumoroso"] --> FewShotBlock["Prompt COAST + 2-3 Esempi Svolti (Mock-up SOAP / ABC)"]
    FewShotBlock --> LLM["In-Context Learning (LLM)"]
    LLM --> StructuredOut["Sintesi Clinica Rigorosa & Formattata ad Alta Fedeltà"]
```

- **Il Fallimento del Zero-Shot Astratto:** Fornire a un LLM indicazioni generiche in linguaggio naturale (*"Sii un buon terapeuta ed estrai i pensieri disfunzionali"*) genera risposte prolisse, ridondanti e instabili, con perdita di aderenza tassonomica.
- **In-Context Learning Strutturato:** L'inserimento nel prompt COAST di **2 o 3 coppie input-output (Few-Shot Prompting)** contenenti casi clinici fittizi risolti (ad esempio frammenti di seduta con relativa compilazione di schede SOAP o griglie ABC Beckiane) guida l'attenzione del modello verso la sintassi clinica desiderata, garantendo elevata consistenza e riproducibilità.

---

## Riferimenti Bibliografici
- *L'Intelligenza Artificiale Generativa in Psicoterapia: Dalla Scatola Nera alla Pratica Clinica Sicura* (`Clinical_AI_Blueprint.pdf`).
- Beck, J. S. (2020). *Cognitive Behavior Therapy: Basics and Beyond* (3rd ed.). Guilford Press.
- Bousquet, J., et al. (2024). Multi-agent exploratory thinking and demographic swapping for mitigating algorithmic diagnostic bias. *Journal of Medical Artificial Intelligence*.
- Wu, K., et al. (2025). The Avalanche Effect: How Chain-of-Thought Reasoning Degrades Performance on Unstructured Real-World Clinical Records. *Nature Digital Medicine*.

---

## Relazioni
- Scheda sintesi collegata: [[Clinical_AI_Blueprint]]
- Concetti correlati: [[mind-safe-framework]], [[patient-psi-simulazione-clinica]], [[chart-reporting-guideline]], [[cbt-dialogue-systems-and-tools]], [[llm-case-conceptualization-pipeline]], [[stepwise-cot]], [[audit-bias-llm-clinici]], [[deliberate-practice-in-psicoterapia-ia]].
