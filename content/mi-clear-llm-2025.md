---
tags: [mi-clear-llm, reporting-guidelines, accuracy-reports, large-language-models, healthcare-ai, medical-imaging, radiology-ai, api-access, local-deployment, open-source-llm, prompt-engineering, stochasticity-management, test-data-independence, research-transparency]
source_papers: ["MI-CLEAR-LLM_2025.pdf"]
---

## Definizione Operativa
- Il **MI-CLEAR-LLM (2025 Updates)** è una linea guida metodologica standardizzata per garantire trasparenza, completezza e riproducibilità negli studi clinici che valutano l'accuratezza diagnostica di LLM e LMM in sanità.
- **Utilità CBT / Applicativa:** Fornisce un framework rigoroso per valutare l'interazione con LLM via API e modelli locali, prevenendo il data leakage e documentando la stocasticità dei modelli, essenziale per la validazione clinica e regolatoria.

## Evidenze dalla Letteratura
- Dati emersi: Gli studi recenti (Park et al., 2025) evidenziano che oltre il 60% delle pubblicazioni omette parametri cruciali di stocasticità o dettagli di versione, minando la riproducibilità. L'aggiornamento 2025 colma il gap relativo a modelli open-source e API rispetto alla versione 2024.
- Limiti tecnici, bias e rischi specifici documentati: Il fenomeno della *prompt brittleness* (Lee et al., 2024) e la contaminazione da dati di training (data leakage) rappresentano rischi critici che il framework mira a mitigare attraverso l'obbligo di trasparenza metodologica.

## Riferimenti Bibliografici
- Park, S. H., Suh, C. H., Lee, J. H., Tejani, A. S., You, S. C., Kahn, C. E., Jr., & Moy, L. (2025). Minimum reporting items for clear evaluation of accuracy reports of large language models in healthcare (MI-CLEAR-LLM): 2025 updates. *Korean Journal of Radiology*, 26(12), 1123–1132. https://doi.org/10.3348/kjr.2025.1522

## Relazioni
- Vedi anche: [TRIPOD-LLM](concetti/TRIPOD-LLM.md), [DEAL](concetti/DEAL.md), [chart-reporting-guideline](chart-reporting-guideline.md), [stochasticity-management-in-clinical-llms](stochasticity-management-in-clinical-llms.md), [clinical-fidelity-assessment](clinical-fidelity-assessment.md)

