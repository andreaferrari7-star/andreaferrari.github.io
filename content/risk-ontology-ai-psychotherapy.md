---
tags: [ontologia-del-rischio, psicoterapia-ai, llm-safety, crisi-acute, valutazione-clinica, sicurezza-algoritmica]
source_papers: ["2505.15108v2.pdf"]
---

# Risk Ontology for AI Psychotherapy

## Definizione Operativa
- Modello ontologico e tassonomico strutturato a tre livelli gerarchici (Acute Crisis, In-Session Warning Signs, Potential Real-World Consequences) sviluppato da Steenstra e Bickmore (2025) per standardizzare la valutazione di sicurezza, la rilevazione di eventi avversi e la mitigazione dei rischi nell'erogazione di psicoterapia tramite agenti virtuali intelligenti e modelli linguistici.
- **Utilità CBT:** Fornisce criteri operativi per distinguere il disagio terapeutico transitorio e intenzionale (*intentional discomfort*, connaturato a tecniche CBT quali esposizione graduata, defusione o ristrutturazione cognitiva) dal danno iatrogeno (*unintentional harm*), integrando protocolli di sicurezza standardizzati per la gestione di emergenze e il monitoraggio degli schemi cognitivo-emotivi.

## Evidenze dalla Letteratura
- **Limite dei Benchmark Generici e Necessità di Valutazione Dinamica:** I benchmark di sicurezza standard per LLM (es. ALERT, SafetyBench) valutano proprietà lessicali statiche (tossicità, bias), risultando inefficaci nell'intercettare derive cliniche, rotture relazionali o amplificazioni di ideazioni disfunzionali nel corso di sessioni terapeutiche prolungate (Steenstra & Bickmore, 2025).
- **Architettura a Tre Livelli:**
  - *Livello 1 - Acute Crisis:* Rileva minacce imminenti di autolesionismo (*Imminent Harm to Self*), violenza verso terzi (*Imminent Harm to Others*) o psicosi/scompenso acuto (*Severe Psychological Decompensation*), vincolando l'agente a una sequenza standardizzata di 4 azioni: Assess -> De-escalate -> Recommend Emergency Services -> Request Human Consultation.
  - *Livello 2 - In-Session Warning Signs:* Monitora turno per turno su scala Likert a 5 punti le fluttuazioni di costrutti cognitivi, motivazionali e relazionali (es. disperazione, credenze nucleari, autoefficacia, ambivalenza, appartenenza frustrata) rispetto alla baseline del paziente.
  - *Livello 3 - Potential Real-World Consequences:* Valuta i danni tangibili post-sessione (suicidio, NSSI, dropout, vergogna/stigma, declino interpersonale) previsti causalmente dalle alterazioni dei segnali in sessione.
- **Casi d'Uso Operativi:** L'ontologia guida quattro scenari applicativi: 1) monitoraggio live di interazioni reali con trigger di interruzione automatica; 2) valutazione pre-clinica in ambienti di simulazione controllata (**SimPatient**); 3) benchmarking comparativo standardizzato tra modelli e versioni di LLM; 4) analisi delle cause primarie (*root-cause analysis*) per anomalie ed esiti inattesi (Steenstra & Bickmore, 2025).

**Riferimenti Bibliografici:**
- Steenstra, I., & Bickmore, T. (2025). A Risk Ontology for Evaluating AI-Powered Psychotherapy Virtual Agents. In *Preprint*, ACM, New York, NY, USA, 11 pages. https://doi.org/10.1145/3717511.3749286 / arXiv:2505.15108v2 [cs.CL]

## Relazioni
- Vedi anche: [[2505-15108v2]], [[in-session-warning-signs]], [[active-ai-therapeutic-agent]], [[clinical-fidelity-assessment]], [[ai-assisted-psychotherapy]], [[clinical-ai-simulation]]
