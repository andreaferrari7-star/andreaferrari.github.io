---
tags: [prompt-engineering, cbt, clinical-reasoning, coast-framework, llm4cbt]
source_papers: ["Manuale_Tecnico_GenAI_Psicoterapia_CBT 1.md", "manuale_genai_cbt_libet.md"]
---

# Modello R.O.C.C.O.

## Definizione Operativa
- Griglia operativa proprietaria a 5 campi (Ruolo, Obiettivo, Contesto, Criteri, Output) per la stesura materiale di prompt clinici, progettata per ridurre l'ambiguità pragmatica degli LLM.
- **Utilità CBT:** Garantisce che l'intelligenza artificiale produca output terapeutici strutturati, sicuri (su dati de-identificati) e immediatamente azionabili in seduta, inibendo allucinazioni enciclopediche e violazioni deontologiche.

## Evidenze dalla Letteratura
- Il confinamento strutturato dei prompt tramite griglie prescrittive previene il deterioramento inferenziale e l'accumulo di errori intrinseco al *Chain-of-Thought* clinico non vincolato (Wu et al., 2025).
- L'adozione di griglie prescrittive come il Modello R.O.C.C.O. supporta il modello euristico *Centauro*, favorendo la delega selettiva di micro-task all'IA per mitigare il rischio di *deskilling* e di *automation bias* nel terapeuta (Abdulnour et al., 2025).

**Riferimenti Bibliografici:**
- Manuale Tecnico: L'Applicazione dell'AI Generativa nella Psicoterapia Cognitivo-Comportamentale (CBT). (n.d.).
- Abdulnour, R.-E., et al. (2025). Human-in-the-Reasoning: Centaur vs Cyborg Approaches. *NEJM AI*.
- Wu, K., et al. (2025). Why Chain of Thought Fails in Clinical Text Understanding. *arXiv:2509.21933*.

## Relazioni 
- Vedi anche: [[coast-framework-clinical-prompting]], [[LLM4CBT]], [[clinical-chain-of-thought-paradox]], [[stepwise-cot]]
