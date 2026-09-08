---
tags: [layered-safeguards, clinical-safety, risk-mitigation, conversational-ai, mental-health-chatbots, hitl, samd, fda-guidelines, prompt-engineering, retrieval-augmented-generation, safety-net]
source_papers: ["Generative AI Mental Health Chatbot Interventions - A Scoping Review of Safety and User Experience.pdf"]
---

## Definizione Operativa
- Framework architetturale a "difesa in profondità" per governare rischi iatrogeni, allucinazioni cliniche e fallimenti di gestione emergenze nei sistemi di salute mentale conversazionali.
- **Utilità CBT / Applicativa:** Essenziale per trasformare i chatbot da semplici prototipi a dispositivi medici digitali certificati (SaMD), garantendo la sicurezza del paziente attraverso controlli algoritmici, procedurali e umani.

## Evidenze dalla Letteratura
- Dati emersi: Lo studio di Olisaeloka et al. (2026) ha analizzato 21 interventi, dimostrando l'inefficacia di guardrail basati su singoli prompt e la superiorità di pipeline multilivello. È necessaria una combinazione di fine-tuning su dataset clinici, RAG per ancoraggio fattuale e supervisione umana (HITL) per gestire le anomalie.
- Limiti tecnici, bias e rischi specifici: Il caso *HopeBot* (2024) evidenzia come il solo prompt engineering di sistema sia vulnerabile a jailbreak e incapace di rilevare il rischio suicidario. È critico il rischio di "over-flagging" o di risposte generiche pericolose senza escalation (Olisaeloka et al., 2026).

## Riferimenti Bibliografici
- Olisaeloka, L., Richardson, C., Wang, A. Y., Munthali, R., & Vigo, D. (2026). Generative AI Mental Health Chatbot Interventions: A Scoping Review of Safety and User Experience. *Department of Psychiatry, University of British Columbia*.
- Campellone, T. R., Flom, M., Montgomery, R. M., Bullard, L., Pirner, M. C., Pavez, A., et al. (2025). Safety and User Experience of a Generative Artificial Intelligence Digital Mental Health Intervention: Exploratory Randomized Controlled Trial. *Journal of Medical Internet Research*, 27, e67365.
- Heinz, M. V., Mackin, D. M., Trudeau, B. M., Bhattacharya, S., Wang, Y., Banta, H. A., et al. (2025). Randomized Trial of a Generative AI Chatbot for Mental Health Treatment. *NEJM AI*, 2, AIoa2400802.

## Relazioni
- Vedi anche: [[clinical-readiness-gap-in-mh-chatbots]], [[modello-centauro-clinico]], [[software-as-a-medical-device-salute-mentale]], [[rag-in-psicoterapia]]
