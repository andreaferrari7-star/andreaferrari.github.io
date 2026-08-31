---
tags: [scoping-review, generative-ai, mental-health-chatbots, digital-mental-health, user-experience, safety-mechanisms, therapeutic-alliance, risk-mitigation, prisma-scr, human-in-the-loop, jbi-methodology]
source_papers: ["Generative AI Mental Health Chatbot Interventions - A Scoping Review of Safety and User Experience.pdf"]
---

# Generative AI Mental Health Chatbot Interventions: A Scoping Review of Safety and User Experience (Olisaeloka et al., 2026)

## Definizione Operativa
- **Scoping Review Sistematica PRISMA-ScR** condotta da Lotenna Olisaeloka, Chris Richardson, Angel Y. Wang, Richard Munthali e Daniel Vigo (Department of Psychiatry & School of Population and Public Health, Faculty of Medicine, University of British Columbia, Vancouver; protocollo registrato su OSF e pubblicato su *PLOS One*, 2026) che costituisce la **prima mappatura sistematica globale** mirata specificamente all'architettura computazionale, alle modalità di erogazione, agli esiti di **User Experience (UX)** e alle strategie di **mitigazione del rischio e sicurezza clinica** nei chatbot basati su Intelligenza Artificiale Generativa (*GenAI*) appositamente progettati per la salute mentale.
- **Campione ed Evidenze Sintetizzate:** Ricerca sistematica su 7 banche dati accademiche (MEDLINE, Scopus, PsycINFO, ACM Digital Library, IEEE Xplore, Google Scholar, Consensus) che ha censito 1.899 record, includendo **21 studi primari peer-reviewed** condotti in **11 Paesi** tra il 2023 e il 2025 (Cina n=4, Regno Unito n=4, USA n=3, Australia n=2, Germania n=1, Romania n=1, Kenya n=1, Kirghizistan n=1, Malesia n=1, Belgio n=1, Perù n=1).
- **Utilità Clinica e per la Ricerca in Psicoterapia Digitale:** 
  - Fornisce un quadro empirico dettagliato che supera le precedenti review focalizzate su LLM generalisti o chatbot tradizionali rule-based, esaminando interventi progettati ad hoc (*purpose-built*) per ansia, depressione, disturbo post-traumatico da stress (PTSD), demenza, disturbi dell'alimentazione e stress occupazionale.
  - Formalizza il duplice profilo della GenAI in salute mentale: **elevata promessa relazionale e alleanza percepita** (WAI-SR paragonabile a quella con terapeuti umani, 3.65-3.90/5) contrapposta al fenomeno del **[[relational-engagement-paradox-genai|Relational-Engagement Paradox]]** (drastico drop-out/attrition a medio-lungo termine: fino a -80% di retention a 6-8 settimane) e a gravi vulnerabilità di sicurezza (mancata gestione del rischio suicidario in modelli non specializzati, allucinazioni cliniche, scarsità di monitoraggio degli eventi avversi).
  - Dimostra l'imprescindibilità di un'architettura di sicurezza sociotecnica multilivello (**[[layered-safeguards-in-clinical-ai|Layered Safeguards]]**) che combina controlli algoritmici (fine-tuning clinico, RAG con soglie di astensione, filtri multilivello e classificatori di rischio), salvaguardie procedurali (onboarding, chiarimento del ruolo, co-design esperto) e governance operativa (supervisione *Human-in-the-Loop* e percorsi di escalation per le crisi).

## Evidenze dalla Letteratura
*(Contenuto riorganizzato dalle sezioni originali "Caratteristiche dei Sistemi...", "Tabella Comparativa...", "Analisi Approfondita...", "Architettura di Sicurezza...", "Lacune...")*

### 1. Condizioni Cliniche e Approcci Terapeutici
L'analisi evidenzia una forte focalizzazione sui disturbi internalizzanti (Ansia n=11, Depressione n=10) tramite framework CBT e Third-Wave (CBT, ACT, mindfulness). Gli approcci complementari includono psicologia positiva, terapia della reminiscenza, esposizione in realtà aumentata (PTSD) e arteterapia.

### 2. User Experience (UX) e il Paradosso di Ingaggio
Sebbene i chatbot GenAI ottengano punteggi elevati di accettabilità (3.8-4.6/5) e un'alleanza terapeutica (WAI-SR 3.65-3.90) comparabile ai terapeuti umani, si riscontra un **Relational-Engagement Paradox**: un'elevata soddisfazione iniziale seguita da un crollo drastico dell'attrition (retention -80% a 6-8 settimane in alcuni studi).

### 3. Architettura di Sicurezza (Layered Safeguards)
Le strategie di mitigazione si dividono in:
- **Algoritmiche:** Fine-tuning clinico, prompt engineering, RAG con soglie di astensione, filtri ML.
- **Procedurali:** Co-design multidisciplinare, onboarding trasparente, protocolli privacy.
- **Governance:** Human-in-the-Loop (HITL), escalation protocolli di crisi, monitoraggio eventi avversi.

### 4. Criticità Metodologiche
- Eterogeneità degli strumenti di valutazione (assenza di standardizzazione).
- Mancanza di metriche specifiche per rischi GenAI (es. AI psychosis, allucinazioni cliniche).
- Scarsa trasparenza architetturale e sui dati di deployment.

**Riferimenti Bibliografici:**
- Olisaeloka, L., Richardson, C., Wang, A. Y., Munthali, R., & Vigo, D. (2026). Generative AI Mental Health Chatbot Interventions: A Scoping Review of Safety and User Experience. *Department of Psychiatry, University of British Columbia*.
- Olisaeloka, L., Richardson, C., & Vigo, D. (2026). User experience and safety of generative AI-based mental health chatbots: Scoping review protocol. *PLOS ONE*, 21, e0341631. https://doi.org/10.17605/OSF.IO/HSNXA
- Campellone, T. R., et al. (2025). Safety and User Experience of a Generative Artificial Intelligence Digital Mental Health Intervention. *Journal of Medical Internet Research*, 27, e67365.
- Espinoza, F., et al. (2024). Supporting dementia caregivers in Peru through chatbots: generative AI vs structured conversations. *BCS Learning & Development*, 89–98.
- Habicht, J., et al. (2024). Closing the accessibility gap to mental health treatment with a personalized self-referral chatbot. *Nature Medicine*, 30, 595–602.
- Heinz, M. V., et al. (2025). Randomized Trial of a Generative AI Chatbot for Mental Health Treatment. *NEJM AI*, 2, AIoa2400802.
- Javanbakht, A., et al. (2024). Unreal that feels real: artificial intelligence-enhanced augmented reality for treating PTSD and anxiety disorders. *European Journal of Psychotraumatology*, 15, 2418248.
- Li, H., et al. (2023). Systematic review and meta-analysis of AI-based conversational agents for promoting mental health and well-being. *npj Digital Medicine*, 6, 1–14.
- Sabour, S., et al. (2023). A chatbot for mental health support: exploring the impact of Emohaa on reducing mental distress in China. *Frontiers in Digital Health*, 5, 1133987.
- Schäfer, L. M., et al. (2025). Exploring user characteristics, motives, and expectations and the therapeutic alliance in the mental health conversational AI Clare®: a baseline study. *Frontiers in Digital Health*, 7, 1576135.
- Vossen, W., et al. (2024). The effect of personalizing a psychotherapy conversational agent on therapeutic bond and usage intentions. In *Proceedings of the 29th International Conference on Intelligent User Interfaces* (pp. 761–771). ACM.

## Relazioni
- [[layered-safeguards-in-clinical-ai]]: Framework sociotecnico di salvaguardie multilivello.
- [[relational-engagement-paradox-genai]]: Analisi del divario tra alleanza iniziale e drop-out a lungo termine.
- [[clinical-readiness-gap-in-mh-chatbots]]: Divario tra scorrevolezza linguistica e validazione clinica.
- [[stepped-care-ai-integration]]: Integrazione di strumenti AI nei sistemi di cura blended.
- [[modello-centauro-clinico]]: Collaborazione Human-in-the-Loop.
- [[software-as-a-medical-device-salute-mentale]]: Inquadramento regolatorio SaMD.
- [[rag-in-psicoterapia]]: Impiego di RAG per ancorare le risposte a fonti cliniche verificate.
- [[cbt-dialogue-systems-and-tools]]: Architetture informatiche per tecniche cognitivo-comportamentali.
