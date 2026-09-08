---
tags: [coast-framework, clinical-prompting, prompt-engineering, scaffolding-cognitivo, subjectivity-assessment, contrastive-reasoning, schema-analysis, in-context-learning, few-shot-prompting, clinical-nlp, cbt-prompting]
source_papers: ["Clinical_AI_Blueprint.pdf"]
---

## Definizione Operativa
- Metodologia di *prompt engineering* clinico che utilizza un'impalcatura cognitiva (*cognitive scaffolding*) strutturata per proceduralizzare le interazioni con LLM in psicoterapia.
- **Utilità CBT / Applicativa:** Stabilizza il ragionamento algoritmico evitando bias e chiusure premature, permettendo l'estrazione sistematica di pensieri disfunzionali e la concettualizzazione del caso attraverso tre livelli di astrazione.

## Evidenze dalla Letteratura
- Il framework riduce i bias di conferma e migliora la fedeltà tassonomica rispetto allo zero-shot, grazie all'uso di pochi esempi di riferimento (*few-shot prompting*) (Bousquet et al., 2024; Wu et al., 2025).
- Rischi documentati: il ragionamento *Chain-of-Thought* non strutturato può degradare le performance su record clinici reali (Wu et al., 2025).

## Riferimenti Bibliografici
- Beck, J. S. (2020). *Cognitive Behavior Therapy: Basics and Beyond* (3rd ed.). Guilford Press.
- Bousquet, J., et al. (2024). Multi-agent exploratory thinking and demographic swapping for mitigating algorithmic diagnostic bias. *Journal of Medical Artificial Intelligence*.
- Wu, K., et al. (2025). The Avalanche Effect: How Chain-of-Thought Reasoning Degrades Performance on Unstructured Real-World Clinical Records. *Nature Digital Medicine*.
- (Non specificato). *L'Intelligenza Artificiale Generativa in Psicoterapia: Dalla Scatola Nera alla Pratica Clinica Sicura* (Clinical_AI_Blueprint.pdf).

## Relazioni
- Vedi anche: [[clinical-ai-blueprint]], [[mind-safe-framework]], [[patient-psi-simulazione-clinica]], [[chart-reporting-guideline]], [[cbt-dialogue-systems-and-tools]], [[llm-case-conceptualization-pipeline]], [[stepwise-cot]], [[audit-bias-llm-clinici]], [[deliberate-practice-in-psicoterapia-ia]].
