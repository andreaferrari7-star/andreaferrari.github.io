---
tags: [scoping-review, slr, metodologia-ricerca, ai-assistita, criteria-centric, data-triangulation, human-in-the-loop]
source_papers: ["JML_1001.pdf", "2605.24351v1.pdf"]
---

# Buone Pratiche per Scoping Review Assistite da IA

## Definizione Operativa
- Framework di raccomandazioni e linee guida procedurali per integrare modelli linguistici di grandi dimensioni (LLM) ed elaborazioni bibliometriche nella conduzione di Scoping Review e Revisioni Strutturate della Letteratura (SLR).
- **Utilità CBT:** Permette a ricercatori clinici e psicoterapeuti di mappare e aggiornare rapidamente la base di evidenze empiriche (EBM) su protocolli terapeutici complessi, garantendo la replicabilità metodologica ed eliminando il rischio di allucinazioni scientifiche o distorsioni nel campionamento degli studi.

## Evidenze dalla Letteratura
- **Paradigma Criteria-Centric e Governance:** L'integrazione della GenAI deve essere guidata da criteri etici e normativi di qualità (Integrità, Trasparenza, Riproducibilità, Rigore) anziché dalle mutevoli capacità tecniche contingenti dei modelli (*capability-centric*). L'autore umano rimane il solo responsabile legale ed epistemologico dell'opera, con divieto di attribuzione di co-autorato all'IA (Tingelhoff et al., 2024).
- **Matrice dei Task (Aree Consentite vs Vietate):**
  - *Task Consentiti ad Assistenza:* Familiarizzazione preliminare con il dominio, ottimizzazione della sintassi delle query booleane per database eterogenei, tracciamento citazionale avanzato (backward/forward citation con embedding semantici) e screening iniziale dei pattern (Tingelhoff et al., 2024).
  - *Task a Divieto di Delega (Human-Only):* Stesura del protocollo di revisione, formulazione autonoma di scope e parole chiave (per evitare l'*anchoring bias* algoritmico), valutazione qualitativa della solidità metodologica dei paper e redazione non supervisionata delle sintesi teoriche (Tingelhoff et al., 2024).
- **Workflow Ibrido Struttura-Semantica:** Per gestire volumi massivi di letteratura preservando l'integrità formale, è raccomandato un approccio ibrido in cui algoritmi bibliometrici classici estraggono la topologia e i cluster citazionali oggettivi, mentre i modelli LLM vengono usati a valle solo per descrivere e riassumere semanticamente i nodi individuati (Camelo-Guerrero & Diaz-Rodriguez, 2026).
- **Metodo Operativo di Triangolazione e Saturazione:** 
  - *Between-Tool Triangulation:* Esecuzione dei medesimi prompt su molteplici motori accademici indipendenti (es. Scite, Elicit, SciSpace) per superare i limiti di database chiusi o non esaustivi (Tingelhoff et al., 2024).
  - *Saturazione Induttiva:* Codifica iterativa degli estratti fino al raggiungimento della saturazione concettuale, definita come l'emersione di meno del 5% di nuovi codici per round (Tingelhoff et al., 2024).

**Riferimenti Bibliografici:**
- Camelo-Guerrero, A., & Diaz-Rodriguez, J. (2026). How much structure do LLMs need? Evaluating LLMs for bibliometric cluster description. *arXiv preprint arXiv:2605.24351v1*.
- Tingelhoff, F., Brugger, M., & Leimeister, J. M. (2024). A guide for structured literature reviews in business research: The state-of-the-art and how to integrate generative artificial intelligence. *Journal of Information Technology*, 1–23. https://doi.org/10.1177/02683962241304105

## Relazioni 
- Vedi anche: [[jml-1001]], [[metodologia-ricerca-slr-ai]], [[criteria-centric-genai-integration]], [[structured-literature-reviews]]
