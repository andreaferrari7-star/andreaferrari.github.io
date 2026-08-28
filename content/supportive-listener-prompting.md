---
tags: [supportive-listener, prompting, trauma-informed, psicoterapia-ai, llm-safety, empatia-artificiale, disclaimers-iatrogeni]
source_papers: ["2508.00847v1.pdf"]
---

# Supportive Listener Prompting

## Definizione Operativa
- Paradigma di ingegneria dei prompt e configurazione relazionale *trauma-informed* (Sahab et al., 2025) per modelli linguistici (LLM come GPT-4), finalizzato a fornire supporto psicologico ed emotivo di primo livello a popolazioni vulnerabili o esposte a traumi sistemici, evitando sia l'intrusività investigativa sia i rifiuti formali decontestualizzati.
- **Utilità CBT:** Previene l'effetto iatrogeno dei disclaimer standard rigidi e deflessivi ("Non posso aiutarti, rivolgiti a uno specialista"), che in contesti ad alto stigma generano senso di abbandono e incremento di ansia e depressione; calibra l'interazione su principi di ascolto attivo, accoglienza non giudicante, focalizzazione sull'utente ("you"), assenza di domande incalzanti o rievocative del trauma, e re-indirizzamento professionale introdotto in modo dolce e non invalidante solo dopo aver offerto contenimento emotivo.

## Evidenze dalla Letteratura
- **Vulnerabilità dei Prompt Standard e Disclaimer Rigidi:** I modelli out-of-the-box programmati con formule di sicurezza generiche per declinare responsabilità terapeutiche inducono una percezione di freddezza istituzionale che peggiora i sintomi ansioso-depressivi nei soggetti sofferenti ($d = -0.57$ nel trial controllato di Sahab et al., 2025).
- **Linee Guida del Paradigma Supportive Listener:**
  1. *Focalizzazione sull'Interlocutore (User-Centered):* Utilizzo preferenziale di pronomi di seconda persona ("you") rispetto a formule collettivizzanti ("we") o autoriferite, mantenendo l'attenzione centrata sui vissuti del paziente (Sahab et al., 2025).
  2. *Divieto di Pressioni Investigative (No Invasive / Trauma-Triggering Questions):* Divieto tassativo di incalzare l'utente con domande intrusive o spingerlo a rievocare ricordi traumatici, rispettandone le difese psicologiche e la privacy (Aldkheel & Zhou, 2023).
  3. *Accoglienza Non Giudicante:* Validazione incondizionata delle esperienze emotive e delle scelte personali, anche quando possono sembrare imprudenti.
  4. *Semplicità Lessicale e Compatibilità Multiculturale:* Utilizzo di un registro chiaro ed empatico, accessibile a parlanti non-madrelingua e consonante con culture comunicative ad alto contesto (*high-context cultures*).
  5. *Gradualità nell'Invio Specialistico:* Raccomandazione di consultare professionisti della salute mentale presentata in modo morbido e rassicurante (*"Nel frattempo sono qui per farti compagnia, non devi affrontare tutto da sola"*), riducendo l'impatto dello stigma sociale (Sahab et al., 2025).
- **Validazione Sperimentale (RCT su Donne Afghane):** L'applicazione di questo prompt a GPT-4 ha prodotto una riduzione statisticamente significativa dei punteggi HADS ($d = 0.47$), un incremento del tono positivo ($d = -1.63$) e un punteggio di risposta empatica RoPE significativamente superiore ($d = -0.76$) rispetto a GPT-4 standard (Sahab et al., 2025).

**Riferimenti Bibliografici:**
- Sahab, S., Haqbeen, J., Sapkota, D., & Ito, T. (2025). GPT Chatbots for Alleviating Anxiety and Depression: A Pilot Randomized Controlled Trial with Afghan Women. *arXiv preprint arXiv:2508.00847v1*, 1–13.
- Aldkheel, A. M., & Zhou, L. (2023). How to Support Domestic Violence Survivors with Conversational Agents: Meta Requirements and Design Principles. In *PACIS 2023*, Nanchang, China.

## Relazioni
- Vedi anche: [[2508.00847v1]], [[language-style-matching-human-ai]], [[simulated-empathy-vs-authentic-presence]], [[simulated-therapeutic-alliance]], [[conversational-agents-mental-health]], [[prompting-in-psychology]], [[ai-assisted-psychotherapy]]
