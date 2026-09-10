---
tags: [architecture, agent-harness, safety, governance]
source_papers: ["preprints202604.0428.v3.pdf"]
---

# Agent Harness Architecture

## Definizione Operativa
- L'infrastruttura software (middleware) che avvolge e governa l'esecuzione di un LLM per renderlo un agente autonomo affidabile. È formalizzata come un framework a 6 componenti: 1) Execution Loop, 2) Tool Registry, 3) Context Manager, 4) State Store, 5) Lifecycle Hooks, e 6) Evaluation Interface.
- **Utilità CBT / Applicativa:** Garantisce l'integrità del setting clinico algoritmico. Mentre il modello ragiona e genera testi, l'harness ne monitora i "side effects", previene il *context rot* (accumulo eccessivo di informazioni che degrada l'attenzione del modello) e impone rigidi protocolli di sicurezza tramite *lifecycle hooks* isolati, separando la logica clinica dalla governance dei rischi.

## Evidenze dalla Letteratura
- **Efficacia:** La variazione nell'architettura dell'harness produce variazioni di performance enormi, spesso superiori a quelle ottenute scalando i parametri del modello stesso. Il "harness-model coupling" spiega gran parte della varianza nei risultati dei benchmark odierni (Meng et al., 2026).

## Riferimenti Bibliografici
- Meng, Q., Wang, Y., Chen, L., Li, Y., Wu, W., Jiang, W., Wang, Q., Lu, C., Gao, Y., Wu, Y., & Hu, Y. (2026). Agent Harness for Large Language Model Agents: A Survey. *Preprints.org*, 202604.0428.v3. https://doi.org/10.20944/preprints202604.0428.v3

## Relazioni
- Vedi anche: [meng-et-al-2026](../meng-et-al-2026.md), [mcp-protocol](mcp-protocol.md)

