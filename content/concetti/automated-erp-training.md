---
tags:
  - erp
  - cbt
  - ocd
  - simulation
  - training
  - exposure-hierarchy
  - human-in-the-loop
source_papers:
  - "AI_in_OCD.pdf"
  - "40501_2025_Article_359.pdf"
---

# Automated ERP Training

## Definizione Operativa
- **Inquadramento Clinico-Tecnico:** L'applicazione di modelli di intelligenza artificiale generativa (LLM) e agenti simulati per potenziare, scalare e supervisionare la formazione dei clinici nell'Esposizione con Prevenzione della Risposta (ERP - *Exposure and Response Prevention*), intervento cognitivo-comportamentale d'elezione e *gold standard* per il Disturbo Ossessivo-Compulsivo (OCD).
- **Architettura del Sistema:** Il paradigma combina:
  1. *Pazienti Virtuali Simulati:* Modelli generativi addestrati/promptati per simulare profili ossessivi realistici, variando livelli di insight, resistenza all'esposizione ed emissione di compulsioni neutralizzanti.
  2. *Supervisore / Consulente AI:* Moduli di feedback in tempo reale (es. *TherapyTrainer*, Stade et al., 2024) che valutano la fedeltà al protocollo ERP da parte del terapeuta in formazione.
  3. *Generatore di Gerarchie Espositive:* Strumenti di supporto decisionale clinico (*clinical decision support*) capaci di generare gerarchie SUDS (Subjective Units of Distress Scale) altamente personalizzate e graduate (Bernstein et al., 2025).

## Evidenze dalla Letteratura

### Efficacia e Vantaggi Clinici
- **Superamento del Collo di Bottiglia Formativo:** Sebbene l'ERP sia il trattamento di prima linea raccomandato dalle linee guida (APA), la sua disponibilità è drammaticamente limitata a livello globale per via della carenza di terapeuti con formazione specialistica accreditata. I ritardi nell'accesso alla cura evidence-based raggiungono in media i 17 anni (Kim et al., 2025). L'Automated ERP Training permette una *deliberate practice* scalabile, riducendo l'onere orario dei supervisori umani esperti e democratizzando le competenze espositive.
- **Validità delle Gerarchie Generate:** Test empirici (Bernstein et al., 2025) hanno dimostrato che ChatGPT-4 genera gerarchie di esposizione valutate da esperti clinici come eccellenti in termini di appropriatezza, specificità, variabilità e utilità clinica per target ossessivi specifici (es. timore di contaminazione, pensieri aggressivi o tabù).
- **Potenziamento dell'Aderenza tra le Sedute:** I sistemi digitali e conversazionali possono assistere il paziente tra le sedute nel monitoraggio dell'astensione dai rituali durante i compiti di esposizione (*homework adherence*), fattore predittivo chiave dell'esito della CBT per l'OCD (Wheaton & Chen, 2021; Kim et al., 2025).

### Limiti e Rischi Iatrogeni
- **Rischio Reassurance-Seeking (Ricerca di Rassicurazione):** Se impiegati direttamente dal paziente senza mediazione professionale, gli agenti LLM possono essere strumentalizzati come fonte inesauribile di rassicurazione verbale (es. richieste compulsive di conferma su contaminazioni o timori di colpa), trasformando l'interazione in un rituale neutralizzante che rinforza il circolo vizioso ossessivo.
- **Necessità del Presidio Umano (Human-in-the-Loop):** L'integrazione di questi strumenti deve rimanere ancorata a un modello clinico collaborativo, in cui il terapeuta umano supervisiona costantemente le gerarchie e le interazioni, validandone la sicurezza clinica ed etica prima dell'applicazione in vivo.

## Riferimenti Bibliografici
- Bernstein, E. E., Jaroszewski, A. C., Jacoby, R. J., Bailen, N. H., Ragan, J., Usmani, A., & Wilhelm, S. (2025). Feasibility of using ChatGPT to generate exposure hierarchies for treating obsessive-compulsive disorder. *Behavior Therapy*. https://doi.org/10.1016/j.beth.2025.02.005
- Foa, E. B., Yadin, E., & Lichner, T. K. (2012). *Exposure and response (ritual) prevention for obsessive-compulsive disorder: Therapist guide*. Oxford University Press.
- Kim, J., Gonzalez Pacheco, J. P., Golden, A., Aboujaoude, E., van Roessel, P., Gandhi, A., Mukunda, P., Avanesyan, T., Xue, H., Adeli, E., Kim, J. P., Saggar, M., Wiltsey Stirman, S., Kuhn, E., Supekar, K., Pohl, K. M., & Rodriguez, C. I. (2025). Artificial Intelligence in Obsessive-Compulsive Disorder: A Systematic Review. *Current Treatment Options in Psychiatry*, 12, 23. https://doi.org/10.1007/s40501-025-00359-8
- Stade, B., Eichstaedt, J. C., Kaysen, D., Salecha, A., Greenberger, A., Singhvi, S., & Stirman, S. W. (2024). *TherapyTrainer: using AI to train therapists in written exposure therapy*. OSF Preprints. https://doi.org/10.31219/osf.io/wx93m

## Relazioni
- [kim-et-al-2025](../kim-et-al-2025.md)
- [client101-simulazione-pazienti-virtuali](../client101-simulazione-pazienti-virtuali.md)
- [exposure-interruption-mechanism](exposure-interruption-mechanism.md)
- [deliberate-practice-in-psicoterapia-ia](deliberate-practice-in-psicoterapia-ia.md)
- [cbt](cbt.md)
- [supervisione-clinica-ai](supervisione-clinica-ai.md)

