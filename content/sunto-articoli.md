---
tags:
  - prompt-engineering
  - clinical-nlp
  - bolt-framework
  - diagnosis-of-thought
  - client101
  - mind-safe
  - reporting-guidelines
  - tripod-llm
  - chart-statement
  - elevate-genai
  - gamer-statement
  - mi-clear-llm
  - refine-guideline
  - rlhf-bias
  - simulated-patients
  - cbt-simulation
tipo_fonte: [scientifica, interna]
source_papers:
  - Sunto articoli.docx.pdf
---

# Sunto Articoli: Prompt Engineering, Simulazione Clinica e Standard di Reporting per l'IA in Salute Mentale

## Definizione Operativa
Il documento articola due macro-filoni di ricerca sull'integrazione dei Large Language Models (LLM) nella pratica clinica e biomedica:

1.  **Prompt Engineering come Variabile Clinica**: Il prompt non è solo un input tecnico, ma un'architettura che modula le inferenze cliniche, incarna teorie terapeutiche (CBT, ACT, ecc.) e regola la dinamica relazionale.
2.  **Standard di Reporting e Trasparenza**: L'esigenza di protocolli (TRIPOD-LLM, CHART, ecc.) per documentare sistematicamente prompt, stochasticità, dati di training e supervisione umana, garantendo trasferibilità scientifica.

## Evidenze dalla Letteratura

### Ricerca 1: Prompting, Modelli Clinici e Simulazione
*   **Prompt come veicolo di teoria**: La qualità clinica dipende dalla configurazione del prompt (es. *expert psychiatrist* vs. *wellness coach*). Framework come *Diagnosis of Thought (DoT)* (Chen et al., 2023) guidano l'LLM in processi sequenziali (subjectivity assessment, contrastive reasoning, schema analysis) migliorando l'accuratezza.
*   **Valutazione (Framework BOLT)**: Gli LLM tendono spontaneamente a uno stile di "bassa qualità" (RLHF advice-giving bias), con un eccesso di soluzioni premature. Il framework BOLT (Chiu et al., 2024) formalizza la valutazione quantitativa su tecniche cliniche e comportamenti.
*   **Simulazione e Sicurezza**: *Client101* (Cabrera Lozoya et al., 2025) utilizza pazienti virtuali per la formazione clinica. *MIND-SAFE* (Boit & Patil, 2025) propone un'architettura multilivello che integra triage del rischio acuto, RAG (Retrieval-Augmented Generation) e supervisione umana continua.

### Ricerca 4: Reporting Guidelines
La rassegna analizza le linee guida internazionali per la trasparenza degli LLM in sanità:

*   **TRIPOD-LLM (2025)**: Validazione modulare per modelli in biomedicina.
*   **CHART Statement (2025)**: Focalizzato su chatbot di consulenza sanitaria.
*   **ELEVATE-GenAI (2025)**: Focalizzato su esiti clinici ed economia sanitaria (HEOR).
*   **GAMER Statement (2025)**: Trasparenza dell'AI nel workflow di ricerca.
*   **MI-CLEAR-LLM (2025)**: Controllo della stochasticità e accuratezza diagnostica.
*   **REFINE Statement (2026)**: Integrità dei Foundation Models nella ricerca clinica.

### Riferimenti Bibliografici
*   Boit, S., & Patil, R. (2025). A prompt engineering framework for large language model-based mental health chatbots: MIND-SAFE. *JMIR Mental Health*.
*   Cabrera Lozoya, D., Conway, M., De Duro, E. S., et al. (2025). Leveraging large language models for simulated psychotherapy client interactions: Development and usability study of Client 101. *JMIR Medical Education*, *11*(1), e68056. https://doi.org/10.2196/68056
*   Chen, Z., Lu, Y., & Wang, W. Y. (2023). Empowering psychotherapy with large language models: Cognitive distortion detection through diagnosis of thought prompting. In *Findings of the Association for Computational Linguistics: EMNLP 2023*. Association for Computational Linguistics.
*   Chiu, Y. Y., Sharma, A., Lin, I. W., & Althoff, T. (2024). *A computational framework for behavioral assessment of LLM therapists* (arXiv:2401.00820). arXiv.
*   Filienko, D., Wang, Y., El Jazmi, C., Xie, S., Cohen, T., De Cock, M., & Yuwen, W. (2024). *Toward large language models as a therapeutic tool: Comparing prompting techniques to improve GPT-delivered problem-solving therapy* (arXiv:2409.00112). arXiv.
*   Grabb, D. (2023). The impact of prompt engineering in large language model performance: A psychiatric example. *Journal of Medical Artificial Intelligence*, *6*, 20. https://doi.org/10.21037/jmai-23-71
*   Meskó, B. (2023). Prompt engineering as an important emerging skill for medical professionals: Tutorial. *Journal of Medical Internet Research*, *25*, e50638.

## Relazioni
*   **Relazione tra pilastri**: Esiste una necessità di convergenza tra l'ingegnerizzazione del prompt (Ricerca 1) e l'adozione rigorosa degli standard di reporting (Ricerca 4) per garantire la sicurezza del paziente.
*   **Workflow**: L'utilizzo dell'IA richiede un approccio *Human-in-the-Loop* costante, dove l'IA supporta il clinico (concettualizzazione, simulazione) senza sostituire la responsabilità relazionale.
