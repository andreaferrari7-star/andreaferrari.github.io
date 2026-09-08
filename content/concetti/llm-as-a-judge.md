---
tags: [llm-as-a-judge, valutazione, benchmarking, nlp-clinico, metrics]
source_papers: []
---

# LLM-as-a-judge

## Definizione Operativa
- L'approccio "LLM-as-a-judge" prevede l'utilizzo di un Modello Linguistico di Grandi Dimensioni (LLM) avanzato (es. GPT-4) per valutare, classificare o assegnare un punteggio all'output generato da un altro modello IA o a testi clinici, seguendo una specifica rubrica di valutazione.
- **Utilità CBT / Applicativa:** Consente di automatizzare e scalare la valutazione di dialoghi terapeutici simulati, aderenza ai protocolli CBT (es. tramite rubrica CTRS) e misurazioni di empatia, riducendo i costi e i tempi della supervisione umana nella ricerca.

## Evidenze dalla Letteratura
- Dati emersi: Gli LLM impiegati come giudici mostrano un'alta correlazione con i valutatori umani (spesso superiore all'80% di accordo) per task strutturati e ben delineati da rubriche di valutazione specifiche (Zheng et al., 2023).
- Limiti tecnici, bias e rischi specifici documentati: Rischio di bias posizionale, preferenza per risposte prolisse (verbosity bias), auto-conferma (preferenza per risposte generate dalla stessa famiglia di modelli) e incapacità di cogliere sfumature relazionali complesse o silenzi clinici. L'impiego come unico strumento di valutazione in ambiti clinici sensibili è sconsigliato.

## Riferimenti Bibliografici
- Zheng, L., Chiang, W. L., Ying, Y., et al. (2023). Judging LLM-as-a-judge with MT-Bench and Chatbot Arena. *arXiv preprint arXiv:2306.05685*.

## Relazioni
- Vedi anche: [[miti-framework-llm-evaluation]], [[ctrs-automated-evaluation]], [[counseling-benchmarks-evaluation]]
