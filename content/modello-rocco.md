---
tags: [prompt-engineering, cbt, clinical-reasoning, coast-framework, llm4cbt]
tipo_fonte: [scientifica, interna]
source_papers: ["Manuale_Tecnico_GenAI_Psicoterapia_CBT 1.md", "manuale_genai_cbt_libet.md", "10-02 Riunione_ Corso AI per terapeuti e valutazione software-Summary.md"]
---

# Modello R.O.C.C.O.

## Definizione Operativa
- Griglia operativa proprietaria a 5 campi (Ruolo, Obiettivo, Contesto, Criteri, Output) per la stesura materiale di prompt clinici, progettata per ridurre l'ambiguità pragmatica degli LLM. È descritta nel manuale tecnico del corso, materiale didattico interno del gruppo. Nel Modulo 1 del corso i partecipanti riscrivono un prompt spontaneo con l'acronimo ROCCO e confrontano gli output (cfr. [[10-02-riunione-corso-ai-terapeuti-software]]).
- **Utilità CBT:** Garantisce che l'intelligenza artificiale produca output terapeutici strutturati, sicuri (su dati de-identificati) e immediatamente azionabili in seduta, inibendo allucinazioni enciclopediche e violazioni deontologiche.

## Evidenze dalla Letteratura
- Il *Chain-of-Thought* non vincolato peggiora le prestazioni nell'86,3% dei 95 LLM valutati su 87 compiti con testi clinici reali (Wu et al., 2025). L'ipotesi che una griglia prescrittiva come R.O.C.C.O. contenga questo effetto non è stata verificata empiricamente [da verificare].
- Abdulnour et al. (2025) distinguono due modalità di collaborazione con l'IA: *Centauro*, in cui il clinico delega compiti definiti e a basso rischio e riserva a sé diagnosi e formulazione del caso, e *Cyborg*, in cui umano e IA lavorano in modo fuso su ogni compito, con un rischio clinico più alto. Gli autori segnalano anche il rischio di *deskilling* e *mis-skilling*. Una griglia che delimita il compito affidato all'IA, come R.O.C.C.O., è coerente con la modalità Centauro (cfr. [[human-in-the-reasoning]]).

## Riferimenti Bibliografici
- Abdulnour, R. E., Gin, B., & Boscardin, C. K. (2025). Educational strategies for clinical supervision of artificial intelligence use. *The New England Journal of Medicine*, *393*(8), 786–797. https://doi.org/10.1056/NEJMra2503232
- Wu, J., Xie, K., Gu, B., Krüger, N., Lin, K. J., & Yang, J. (2025). *Why chain of thought fails in clinical text understanding* (arXiv:2509.21933). arXiv. https://doi.org/10.48550/arXiv.2509.21933

## Relazioni
- Vedi anche: [[coast-framework-clinical-prompting]], [[LLM4CBT]], [[clinical-chain-of-thought-paradox]], [[stepwise-cot]], [[human-in-the-reasoning]], [[10-02-riunione-corso-ai-terapeuti-software]]
