---
tags: [prompt-engineering, clinical-nlp, bolt-framework, diagnosis-of-thought, client101, mind-safe, reporting-guidelines, tripod-llm, chart-statement, elevate-genai, gamer-statement, mi-clear-llm, refine-guideline, rlhf-bias, simulated-patients, cbt-simulation]
source_papers: ["Sunto articoli.docx.pdf"]
---

# Sunto Articoli: Prompt Engineering, Simulazione Clinica e Standard di Reporting per l'IA in Salute Mentale

## Definizione Operativa
Il documento articola due macro-filoni di ricerca sull'integrazione dei Large Language Models (LLM) nella pratica clinica e biomedica:
1. **Prompt Engineering come Variabile Clinica**: Il prompt non è solo un input tecnico, ma un'architettura che modula le inferenze cliniche, incarna teorie terapeutiche (CBT, ACT, etc.) e regola la dinamica relazionale.
2. **Standard di Reporting e Trasparenza**: L'esigenza di protocolli (TRIPOD-LLM, CHART, etc.) per documentare sistematicamente prompt, stochasticità, dati di training e supervisione umana, garantendo trasferibilità scientifica.

## Evidenze dalla Letteratura

### Ricerca 1: Prompting, Modelli Clinici e Simulazione
- **Prompt come veicolo di teoria**: La qualità clinica dipende dalla configurazione del prompt (es. *expert psychiatrist* vs. *wellness coach*). Framework come *Diagnosis of Thought (DoT)* (Chen et al., 2023) guidano l'LLM in processi sequenziali (subjectivity assessment, contrastive reasoning, schema analysis) migliorando l'accuratezza.
- **Valutazione (Framework BOLT)**: Gli LLM tendono spontaneamente a uno stile di "bassa qualità" (RLHF advice-giving bias), con un eccesso di soluzioni premature. Il framework BOLT (Chiu et al., 2024) formalizza la valutazione quantitativa su tecniche cliniche e comportamenti.
- **Simulazione e Sicurezza**: *Client101* (Cabrera Lozoya et al., 2025) utilizza pazienti virtuali per la formazione clinica. *MIND-SAFE* (Boit & Patil, 2025) propone un'architettura multilivello che integra triage del rischio acuto, RAG (Retrieval-Augmented Generation) e supervisione umana continua.

### Ricerca 4: Reporting Guidelines
La rassegna analizza le linee guida internazionali per la trasparenza degli LLM in sanità:
- **TRIPOD-LLM (2025)**: Validazione modulare per modelli in biomedicina.
- **CHART Statement (2025)**: Focalizzato su chatbot di consulenza sanitaria.
- **ELEVATE-GenAI (2025)**: Focalizzato su esiti clinici ed economia sanitaria (HEOR).
- **GAMER Statement (2025)**: Trasparenza dell'AI nel workflow di ricerca.
- **MI-CLEAR-LLM (2025)**: Controllo della stochasticità e accuratezza diagnostica.
- **REFINE Statement (2026)**: Integrità dei Foundation Models nella ricerca clinica.

**Riferimenti Bibliografici:**
- Boit, A., & Patil, A. (2025). *MIND-SAFE Framework*.
- Cabrera Lozoya, et al. (2025). *Client101: Simulazione Pazienti Virtuali*.
- Chen, Lu, & Wang (2023). *Diagnosis of Thought (DoT)*, EMNLP.
- Chiu, et al. (2024). *BOLT Behavioral Assessment Framework*.
- Filienko, et al. (2024). *PST and Prompting Experiment*.
- Grabb (2023). *Prompting in Clinical Psychiatry*.
- Meskó, et al. (2023). *AI Literacy in Healthcare*.

## Relazioni
- **Relazione tra pilastri**: Esiste una necessità di convergenza tra l'ingegnerizzazione del prompt (Ricerca 1) e l'adozione rigorosa degli standard di reporting (Ricerca 4) per garantire la sicurezza del paziente.
- **Workflow**: L'utilizzo dell'IA richiede un approccio *Human-in-the-Loop* costante, dove l'IA supporta il clinico (concettualizzazione, simulazione) senza sostituire la responsabilità relazionale.
