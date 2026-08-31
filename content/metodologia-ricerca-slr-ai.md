---
tags: [metodologia-ricerca, scientific-forecasting, slr, bibliometria, dual-validity, pseudoreplication]
source_papers: ["2603.27146v3.pdf", "2605.24351v1.pdf", "2507.04491v2.pdf"]
---

# Metodologia della Ricerca e SLR con IA

## Definizione Operativa
- Corpus di metodologie e framework normativi per integrare i Large Language Models (LLM) nella ricerca scientifica e psicologica. Riguarda tre ambiti principali: (1) le Revisioni Sistematiche della Letteratura (SLR) ibride, (2) la simulazione e generazione di proposte di ricerca (*Scientific Forecasting*), e (3) i protocolli di rigore metodologico per condurre esperimenti sulle/con le IA.
- **Utilità CBT:** Fornisce a ricercatori e clinici le linee guida per accelerare in modo sicuro la sintesi delle evidenze (necessaria per aggiornare i protocolli terapeutici continui), assicurando che i dati estratti dall'IA siano esenti da pseudoreplicazione e che i test sperimentali non misurino artefatti sintattici (*measurement phantoms*).

## Evidenze dalla Letteratura
- **Scientific Forecasting e Generazione Proposte:** Modelli specializzati come *AI-Scientist* addestrati tramite *Time-Sliced Scientific Forecasting* (previsione della letteratura dell'anno +1$ avendo accesso solo a $) e *Stepwise Citation-Grounded Reasoning* riescono a formulare ipotesi di ricerca che anticipano validamente i futuri orientamenti accademici. Tali modelli sono stati validati tramite il metrico quantitativo *Future Alignment Score* (FAS) (Wang et al., 2026).
- **Cluster Bibliometrici Ibridi per SLR:** Nelle revisioni sistematiche (SLR) massive, la letteratura raccomanda un approccio ibrido uomo-macchina. Metodi algoritmici classici estraggono la rete e i cluster di citazioni oggettivi (garantendo l'integrità strutturale), mentre l'LLM viene impiegato esclusivamente a valle per sintetizzare e descrivere semanticamente i nodi del cluster (Camelo-Guerrero & Diaz-Rodriguez, 2026).
- **Workflow Guidati dalla Validità (Dual-Validity):** L'utilizzo degli LLM come soggetti sperimentali in psicologia è soggetto a gravi bias metodologici. Banali parafrasi nei prompt possono invertire i risultati dei test psicologici del modello. Per ovviare a questo, Lin (2026) ha introdotto un workflow rigoroso in 6 stadi basato sul *Dual-Validity Framework*, imponendo tecniche statistiche correttive (es. *Generalized Estimating Equations*) per neutralizzare la pseudoreplicazione causata dai campionamenti testuali interdipendenti.

**Riferimenti Bibliografici:**
- Camelo-Guerrero, A., & Diaz-Rodriguez, J. (2026). How much structure do LLMs need? Evaluating LLMs for bibliometric cluster description. *arXiv preprint arXiv:2605.24351v1*.
- Lin, Z. (2026). A validity-guided workflow for robust large language model research in psychology. *Behavior Research Methods*, 58, 216.
- Wang, H., et al. (2026). Learning to Predict Future-Aligned Research Proposals with Language Models. *arXiv preprint arXiv:2603.27146v3*.

## Relazioni 
- Vedi anche: [[dual-validity-framework]], [[future-alignment-score]], [[time-sliced-scientific-forecasting]], [[measurement-phantoms]], [[structured-literature-reviews]]
