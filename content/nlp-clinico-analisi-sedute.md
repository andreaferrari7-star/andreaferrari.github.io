---
tags: [nlp-clinico, analisi-sedute, small-language-models, semantic-drift, process-based-therapy, on-device-ai]
source_papers: ["2511.22818v1.pdf", "2512.05836v1.pdf", "2510.03913v1.pdf"]
---

# NLP Clinico: Analisi delle Sedute e Modelli Locali (SLM)

## Definizione Operativa
- Utilizzo di modelli linguistici per analizzare e post-processare le trascrizioni di sedute terapeutiche reali (estrazione reti causali, riassunti clinici) e impiego di Small Language Models (SLM) in locale (*on-device*) per garantire la totale privacy dei dati sensibili del paziente.
- **Utilità CBT:** Offre al terapeuta strumenti automatici per redigere note di seduta, monitorare la fedeltà ai protocolli (es. Colloquio Motivazionale) e mappare le reti idiografiche cognitivo-comportamentali senza trasferire dati clinici protetti (PHI) su server cloud esterni.

## Evidenze dalla Letteratura
- **Sintesi di Seduta e Semantic Drift:** Nel riassumere lunghi colloqui terapeutici (es. Colloquio Motivazionale), gli LLM cloud-based subiscono una deriva semantica (*semantic drift*), perdendo la fedeltà clinica originale. Il "Progressive Prompting" (sintesi a step progressivi) migliora l'accuratezza del 32% rispetto all'approccio end-to-end (Kumar et al., 2025).
- **Estrazione Reti Personalizzate (PBT):** L'NLP può estrarre "Personalized Networks" (nodi cognitivi, emotivi e comportamentali e loro legami causali) direttamente dalle trascrizioni di seduta, supportando la concettualizzazione del caso in logica Process-Based Therapy (Ong et al., 2025).
- **Small Language Models e Privacy (On-Device):** Il framework *PsychoLexTherapy* dimostra che modelli "piccoli" in esecuzione locale (es. Gemma-3 4.3B) possono simulare percorsi di ragionamento clinico e mantenere una memoria a lungo termine strutturata (MemoBase), risolvendo alla radice le vulnerabilità della privacy e la dipendenza dalle API cloud (Abbasi & Naderi, 2025).

**Riferimenti Bibliografici:**
- Abbasi, M. A., & Naderi, H. (2025). PsychoLexTherapy: Simulating Reasoning in Psychotherapy with Small Language Models in Persian. *arXiv preprint arXiv:2510.03913v1*.
- Ong, C. W., et al. (2025). Using Large Language Models to Create Personalized Networks From Therapy Sessions. *arXiv preprint arXiv:2512.05836v1*.
- Kumar, V., Rajawat, P. S., & Ntoutsi, E. (2025). Mitigating semantic drift: Evaluating LLMs' efficacy in psychotherapy through MI dialogue summarization. *arXiv preprint arXiv:2511.22818v1*.

## Relazioni 
- Vedi anche: [[semantic-drift-in-therapy-llms]], [[process-based-therapy]], [[on-device-slm-mental-health]]
