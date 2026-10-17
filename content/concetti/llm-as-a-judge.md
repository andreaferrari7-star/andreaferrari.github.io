---
tags: [llm-as-a-judge, valutazione, benchmarking, nlp-clinico, metrics]
tipo_fonte: scientifica
source_papers: ["2510.25384v1.pdf", "2510.03913v1.pdf", "2601.10970v2.pdf"]
---

# LLM-as-a-judge

## Definizione Operativa
- L'approccio "LLM-as-a-judge" prevede l'utilizzo di un Modello Linguistico di Grandi Dimensioni (LLM) avanzato (es. GPT-4o) per valutare, classificare o assegnare un punteggio all'output generato da un altro modello IA o a testi clinici, seguendo una specifica rubrica di valutazione.
- **Utilità CBT / Applicativa:** Consente di automatizzare e scalare la valutazione di dialoghi terapeutici simulati e delle abilità del terapeuta, riducendo i costi e i tempi della valutazione umana nella ricerca.

## Evidenze dalla Letteratura
- **Origine del metodo:** Zheng et al. (2023) hanno proposto e analizzato l'uso degli LLM come giudici su compiti conversazionali generali, con i benchmark MT-Bench e Chatbot Arena. Gli stessi autori documentano bias di posizione, di prolissità (*verbosity bias*) e di auto-preferenza verso risposte simili alle proprie.
- **Uso nella ricerca clinica:** PsychoLexTherapy è stato valutato con GPT-5 come giudice su criteri psicologici, terapeutici e linguistici, affiancando una valutazione umana di studenti di psicologia (Abbasi & Naderi, 2025). Nella simulazione di conflitti di coppia, Wang et al. (2026) usano GPT-4o con prompt di classificazione binaria separati per ogni dimensione.
- **Accordo con gli esperti umani in ambito terapeutico:** nella valutazione delle abilità del terapeuta in conversazioni sintetiche, la correlazione di Pearson con gli esperti clinici è risultata moderata per GPT-4o (r = 0,40) e Gemini-2.0-Flash (r = 0,41), bassa e non significativa per DeepSeek-V3 (r = 0,18) e nulla per GPT-4o-mini (Vu et al., 2025). L'accordo osservato sui compiti generali non si trasferisce quindi automaticamente alla valutazione clinica.
- **Limiti e mitigazioni:** il giudice automatico può introdurre bias sistematici. Wang et al. (2026) li riducono con prompt binari e rubriche esplicite per criterio, invece di giudizi olistici aperti; gli studi clinici affiancano comunque una valutazione umana (Abbasi & Naderi, 2025; Vu et al., 2025).

## Riferimenti Bibliografici
- Abbasi, M. A., & Naderi, H. (2025). *PsychoLexTherapy: Simulating reasoning in psychotherapy with small language models in Persian* (arXiv:2510.03913). arXiv.
- Vu, D. N. L., Tan, R., Moench, L., Francke, S. J., Woiwod, D., Thomas-Odenthal, F., Stroth, S., Kircher, T., Hermann, C., Dannlowski, U., Jamalabadi, H., & Ji, S. (2025). *Roleplaying with structure: Synthetic therapist-client conversation generation from questionnaires* (arXiv:2510.25384). arXiv.
- Wang, C., Chen, A., Bao, C., Jin, S., Swartz, H., Wu, T., Kraut, R. E., & Zhu, H. (2026). *Simulating couple conflict: Designing a multi-agent system for therapy training and practice* (arXiv:2601.10970). arXiv.
- Zheng, L., Chiang, W.-L., Sheng, Y., Zhuang, S., Wu, Z., Zhuang, Y., Lin, Z., Li, Z., Li, D., Xing, E., et al. (2023). Judging LLM-as-a-judge with MT-Bench and Chatbot Arena. *Advances in Neural Information Processing Systems*, *36*, 46595–46623.

## Relazioni
- Vedi anche: [[miti-framework-llm-evaluation]], [[ctrs-automated-evaluation]], [[counseling-benchmarks-evaluation]], [[2510-25384v1]], [[2510-03913v1]], [[2601-10970v2]]
