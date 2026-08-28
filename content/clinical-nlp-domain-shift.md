---
tags: [domain-shift, nlp-clinico, transformers, validita-ecologica, bias-rappresentazione]
source_papers: ["10.1177_20552076261421688.pdf"]
---

# Clinical NLP Domain Shift

## Definizione Operativa
- Discrepanza semantica e statistica che emerge quando modelli linguistici pre-addestrati su testi informali dei social media vengono applicati all'ambiente clinico e psicoterapeutico formale.
- **Utilità CBT:** Previene l'errore di considerare i modelli linguistici validati su benchmark pubblici come pronti per la diagnosi o l'intervento autonomo su costrutti cognitivi complessi.

## Evidenze dalla Letteratura
- Modelli transformer specializzati (MentalBERT, MentalRoBERTa) ottengono elevate prestazioni classificatorie (F1 68–93%) su corpora social ma mostrano ridotta affidabilità nel cogliere il discorso clinico e la complessità psicopatologica reale (Rezaei et al., 2026).
- Oltre il 50% dei modelli pubblicati manca di metriche di calibrazione, interpretabilità post-hoc (SHAP, LIME) e audit di equità tra sottogruppi demografici, limitando la loro applicabilità a ruoli di screening e supporto decisionale (Rezaei et al., 2026).

**Riferimenti Bibliografici:**
- Rezaei, Z., Khorraminia, A., Shi, D., & Banad, Y. M. (2026). Network-based artificial intelligence in mental healthcare: A systematic review of chatbots, artificial intelligence/machine learning models and ethical considerations in global healthcare networks. *DIGITAL HEALTH*, 12, 1–30. https://doi.org/10.1177/20552076261421688

## Relazioni
- Vedi anche: [[10.1177_20552076261421688]], [[network-based-mental-healthcare]], [[audit-bias-llm-clinici]], [[large-language-models]], [[dual-validity-framework]]
