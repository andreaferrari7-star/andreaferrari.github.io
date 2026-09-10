---
tags: [rlvr, reinforcement-learning, reasoning, formal-verification]
source_papers: ["2605.17333v1.pdf"]
---

# Reinforcement Learning from Verifiable Rewards (RLVR)

## Definizione Operativa
- Paradigma di addestramento post-training in cui i reward vengono assegnati sulla base della correttezza verificabile oggettivamente (es. risoluzione di un'equazione o output di un compilatore) anziché su feedback umani soggettivi (RLHF).
- **Utilità CBT / Applicativa:** Sebbene nativo delle scienze esatte, il paradigma RLVR sta ispirando framework di validazione per i ragionamenti clinici tramite "verificatori formali" (es. aderenza alle linee guida DSM o assenza di allucinazioni oggettive nei referti), riducendo la dipendenza dal costoso *human-in-the-loop* durante l'addestramento dei modelli sanitari.

## Evidenze dalla Letteratura
- **Vantaggi e Limiti:** L'RLVR standard assegna reward binari (corretto/errato) ignorando le informazioni sulla traiettoria. Se combinato con tecniche di mantenimento della diversità (come EDAS), evita il collasso su un singolo percorso e favorisce l'emersione di capacità di ragionamento complesse (*chain-of-thought* prolungata) (Liu et al., 2026).

## Riferimenti Bibliografici
- Liu, W., Xu, Y., Xie, W., Zhu, Y., Dong, S., Wang, Z., Shao, W., Zhang, X., Yang, T., Duan, N., & Wang, J. (2026). Leveraging Error Diversity in Group Rollouts for Reinforcement Learning. *arXiv preprint arXiv:2605.17333*.

## Relazioni
- Vedi anche: [error-diversity-advantage-shaping](error-diversity-advantage-shaping.md), [llm-as-a-judge](llm-as-a-judge.md), [clinical-fidelity-assessment](../clinical-fidelity-assessment.md)

