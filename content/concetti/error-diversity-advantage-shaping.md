---
tags: [rlvr, training, edas, mode-collapse, ai-safety]
source_papers: ["2605.17333v1.pdf"]
---

# Error Diversity Advantage Shaping (EDAS)

## Definizione Operativa
- Modulo algoritmico *post-hoc* applicabile al Reinforcement Learning (RLVR) degli LLM, che ricalibra le penalità basandosi sulla distribuzione degli errori: amplifica la penalizzazione per gli errori dominanti/ripetitivi e attenua la penalità per errori esplorativi e rari.
- **Utilità CBT / Applicativa:** Similmente alle strategie CBT per de-biasare la fissazione cognitiva, EDAS costringe la rete neurale a non perseverare su pattern errati "comodi" (*error perseveration*). Applicato a modelli clinici, previene la convergenza su diagnosi errate stereotipate, mantenendo aperto lo spazio delle ipotesi.

## Evidenze dalla Letteratura
- **Efficacia:** Applicando EDAS a modelli open-source (es. Qwen3), si rileva una diminuzione drastica del collasso delle modalità di ragionamento e un aumento significativo delle probabilità di successo su problemi difficili, preservando un'alta diversità di traiettorie (Liu et al., 2026).

## Riferimenti Bibliografici
- Liu, W., Xu, Y., Xie, W., Zhu, Y., Dong, S., Wang, Z., Shao, W., Zhang, X., Yang, T., Duan, N., & Wang, J. (2026). Leveraging Error Diversity in Group Rollouts for Reinforcement Learning. *arXiv preprint arXiv:2605.17333*.

## Relazioni
- Vedi anche: [liu-et-al-2026](../liu-et-al-2026.md), [rlvr](rlvr.md)

