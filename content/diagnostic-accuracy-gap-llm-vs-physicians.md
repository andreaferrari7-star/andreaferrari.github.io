---
tags: [diagnostic-accuracy, clinical-decision-support, large-language-models, physician-vs-ai, meta-analysis]
source_papers: ["medinform-v13-e64963.pdf"]
---

## Definizione Operativa
- Il **Diagnostic Accuracy Gap** definisce la discrepanza nelle prestazioni diagnostiche tra LLM e medici, rilevata in particolare nella diagnosi primaria rispetto al triage o alla diagnosi differenziale.
- **Utilità CBT / Applicativa:** Supporta il medico nella generazione di liste differenziali, riducendo il *premature closure bias*, ma richiede supervisione umana obbligatoria per la diagnosi definitiva.

## Evidenze dalla Letteratura
- Dati emersi: Meta-analisi (Shan et al., 2025) mostra una superiorità dei clinici umani nella diagnosi primaria ($\text{OR} = 0.71, P < .0001$), con successo globale $71.8\%$ (umani) vs $65.1\%$ (LLM).
- Limiti tecnici, bias e rischi: Gli LLM soffrono di iper-sicurezza (*overconfidence*), vulnerabilità al framing, e difficoltà nel gestire la conoscenza tacita (Polanyi's Paradox) e il ragionamento fisiopatologico (Shan et al., 2025; Ito et al., 2023).

## Riferimenti Bibliografici
- Shan, Y., et al. (2025). Diagnostic Accuracy Gap: Large Language Models vs Clinical Professionals. *Medical Informatics*, 13, e64963.

## Relazioni
- Vedi anche: [[single-correct-answer-fallacy-in-clinical-ai]], [[modello-centauro-clinico]], [[human-in-the-reasoning]]
