---
tags: [simulazione-clinica, pazienti-virtuali, multi-agent, deliberate-practice, synthetic-data, cbt]
source_papers: ["2607.25667v1.pdf", "2601.10970v2.pdf", "2510.25384v1.pdf", "2504.17238v1.pdf"]
---

# Simulazione Clinica e Pazienti Virtuali (Multi-Agent Systems)

## Definizione Operativa
- Utilizzo di architetture Multi-Agent basate su LLM per simulare in modo interattivo pazienti, dinamiche relazionali complesse (es. conflitti di coppia) e supervisori clinici, creando ambienti di "Pratica Deliberata" (*Deliberate Practice*) per il training dei terapeuti o per la generazione di dataset sintetici sicuri.
- **Utilità CBT:** Consente ai terapeuti in formazione di esercitarsi su casi complessi o resistenti senza rischio iatrogeno per pazienti reali, ricevendo un feedback formativo immediato (es. scoring CTRS) da un supervisore algoritmico. Inoltre, l'impiego di agenti sintetici permette di costruire dataset di dialoghi clinici aggirando i limiti e i vincoli normativi legati alla privacy dei dati reali.

## Evidenze dalla Letteratura
- **Ambienti di Deliberate Practice Multimodali:** Piattaforme come *MyMentorLLM* integrano pazienti simulati e un "Expert Agent" in veste di supervisore clinico in modalità multimodale (voce/testo), offrendo al tirocinante feedback in tempo reale sull'aderenza al protocollo CBT e misurando le competenze tramite la scala standardizzata CTRS (*Cognitive Therapy Rating Scale*) (Rizzi et al., 2026).
- **Simulazione Relazionale e Multi-Party:** Le architetture avanzate (come il framework *Sense-Plan-Act*) estendono la simulazione oltre il singolo individuo, orchestrando complesse dinamiche multi-agente (ad esempio, terapie di coppia basate sul pattern Demand-Withdraw). In questi scenari, gli agenti modificano dinamicamente i propri tratti in risposta agli interventi del terapeuta in training (Wang et al., 2026).
- **Generazione di Dati Sintetici Privacy-Compliant:** Framework come *SQPsych* (Li et al., 2025) trasformano set di questionari clinici strutturati in fluidi dialoghi sintetici medico-paziente tramite architetture dual-agent (terapeuta-IA e paziente-IA), garantendo l'anonimato assoluto pur conservando un'elevata fedeltà clinica necessaria per il training di altri modelli.
- **Dialoghi Terapeutici Strutturati a Ciclo Continuo:** Strumenti come *CRISP* dimostrano la capacità dei modelli di gestire protocolli di Ristrutturazione Cognitiva multi-turno. Impiegando tecniche complesse (es. *Defense Attorney Technique*) e meccanismi a ciclo continuo, superano i limiti delle interazioni "one-shot" e offrono un simulacro relazionale clinicamente efficace (es. riduzione dell'affetto negativo misurato tramite PANAS) (Zhou et al., 2025).

**Riferimenti Bibliografici:**
- Li, Z., et al. (2025). Roleplaying with Structure: Synthetic Therapist-Client Conversation Generation from Questionnaires. *arXiv preprint arXiv:2510.25384v1*.
- Rizzi, A., et al. (2026). MyMentorLLM: A Psychotherapy GenAI Environment with Multimodal Voice/Text Patients, Trainees and Experts for Deliberate Practice. *arXiv preprint arXiv:2607.25667v1*.
- Wang, J., et al. (2026). Simulating Couple Conflict: Designing A Multi-Agent System for Therapy Training and Practice. *arXiv preprint arXiv:2601.10970v2*.
- Zhou, J., et al. (2025). CRISP: Cognitive Restructuring of Negative Thoughts through Multi-turn Supportive Dialogues. *arXiv preprint arXiv:2504.17238*.

## Relazioni 
- Vedi anche: [[patient-psi-simulazione-clinica]], [[multi-party-interaction-simulation]], [[synthetic-clinical-dialogues]], [[trainer-simulator]], [[sqpsych-framework]]
