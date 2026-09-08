---
tags: [rlvr, reasoning, llm-training, edas, mode-collapse]
source_papers: ["2605.17333v1.pdf"]
---

# Leveraging Error Diversity in Group Rollouts for Reinforcement Learning

## Definizione Operativa
- Presentazione di EDAS (*Error Diversity Advantage Shaping*), una tecnica di post-training RLVR (Reinforcement Learning from Verifiable Rewards) che penalizza la convergenza prematura del modello su un singolo tipo di errore e premia l'esplorazione di percorsi di ragionamento diversificati.
- **Utilità CBT / Applicativa:** La preservazione della "diversità degli errori" durante il training degli LLM ha implicazioni cliniche: previene il *mode collapse* algoritmico, un fenomeno analogo alla chiusura diagnostica prematura umana, in cui il modello si fossilizza su un singolo bias di ragionamento o "traiettoria clinica" errata. Modelli addestrati per mantenere percorsi di ragionamento diversificati risultano più robusti nell'esplorazione di ipotesi differenziali in compiti di *clinical reasoning*.

## Evidenze dalla Letteratura
- **Efficacia:** In compiti di ragionamento complesso e code generation, l'algoritmo EDAS migliora sistematicamente le prestazioni rispetto alle baseline standard (es. DAPO, GRPO) di 6.29 punti percentuali medi, mantenendo attivamente molteplici traiettorie esplorative anche su problemi ad altissima difficoltà (Liu et al., 2026).
- **Limiti:** L'equivalenza degli errori richiede l'estrazione simbolica dell'output (es. risultati matematici formali). L'adattamento a domini testuali aperti o di ragionamento clinico discorsivo richiede l'ingegnerizzazione manuale di funzioni di partizionamento per classificare in modo semantico gli "errori di ragionamento" (Liu et al., 2026).

## Riferimenti Bibliografici
- Liu, W., Xu, Y., Xie, W., Zhu, Y., Dong, S., Wang, Z., Shao, W., Zhang, X., Yang, T., Duan, N., & Wang, J. (2026). Leveraging Error Diversity in Group Rollouts for Reinforcement Learning. *arXiv preprint arXiv:2605.17333*.

## Relazioni
- Vedi anche: [[error-diversity-advantage-shaping]], [[rlvr]], [[clinical-chain-of-thought-paradox]]
