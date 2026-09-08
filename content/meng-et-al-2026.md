---
tags: [agent-harness, llm-infrastructure, evaluation, review]
source_papers: ["preprints202604.0428.v3.pdf"]
---

# Agent Harness for Large Language Model Agents: A Survey

## Definizione Operativa
- Prima revisione sistematica dedicata all'"Agent Harness", l'infrastruttura di governance in tempo reale che incapsula un LLM. L'harness è definito come una tupla a sei componenti: esecuzione (loop), registro strumenti (tool), gestione del contesto, persistenza di stato, hook del ciclo di vita e interfacce di valutazione.
- **Utilità CBT / Applicativa:** Nel contesto degli LLM clinici, l'harness è il middleware che trasforma un modello di linguaggio generico in uno psicoterapeuta virtuale "sicuro". Garantisce che le regole deontologiche (lifecycle hooks) vengano applicate prima delle risposte, che la memoria a lungo termine del paziente (state store) sia isolata e che l'accesso ai tool clinici (es. test psicometrici) sia validato.

## Evidenze dalla Letteratura
- **Efficacia:** La qualità e il design dell'harness impattano in modo decisivo (spesso più del modello sottostante) sull'affidabilità, la sicurezza e la misurabilità degli agenti IA. Modifiche all'harness possono produrre guadagni di performance fino al 10x e isolare comportamenti dannosi. Il report evidenzia come il *harness-model coupling* sia la causa principale della scarsa riproducibilità nei benchmark (Meng et al., 2026).
- **Limiti e Sfide:** Attualmente manca una standardizzazione completa per l'interoperabilità tra agenti e strumenti (nonostante iniziative come MCP e A2A), persistono vulnerabilità critiche di "memory poisoning", ed è assente un framework formale per la verifica della sicurezza del sistema combinato (modello + harness) (Meng et al., 2026).

## Riferimenti Bibliografici
- Meng, Q., Wang, Y., Chen, L., Li, Y., Wu, W., Jiang, W., Wang, Q., Lu, C., Gao, Y., Wu, Y., & Hu, Y. (2026). Agent Harness for Large Language Model Agents: A Survey. *Preprints.org*, 202604.0428.v3. https://doi.org/10.20944/preprints202604.0428.v3

## Relazioni
- Vedi anche: [[agent-harness-architecture]], [[mcp-protocol]], [[ai-safety]]
