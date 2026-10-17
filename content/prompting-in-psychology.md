---
tags: [prompt-engineering, few-shot, zero-shot, temperatura, simulazione]
tipo_fonte: scientifica
source_papers: ["final_textbook_genAIinpsychologyresearchandtraining.pdf", "informatics-12-00029.pdf"]
---

# Prompting in Psychology

## Definizione Operativa
- Ingegnerizzazione e calibrazione sistematica degli input testuali (ruoli, esempi few-shot, parametri di campionamento) per orientare l'elaborazione degli LLM in ambito psicologico.
- **Utilità CBT:** Consente di impostare prompt per addestrare modelli a fungere da co-terapeuti virtuali per la simulazione di colloqui o per generare ristrutturazioni cognitive alternative.

## Evidenze dalla Letteratura
- L'uso combinato di prompt basati su ruoli (role-based), scomposizioni Chain-of-Thought e basse temperature (prossime a 0) incrementa l'accuratezza diagnostica e l'aderenza al protocollo (Adamkovič, 2025).
- L'impiego di temperature elevate favorisce la creatività nella formulazione di ipotesi ma incrementa significativamente il tasso di allucinazioni fattuali (Adamkovič, 2025).
- **Prompt di dominio nella supervisione:** in uno studio su ChatGPT-4, un prompt introduttivo sulla terapia della Gestalt e sulla supervisione ha prodotto feedback di supervisione giudicati dagli specializzandi migliori di quelli ottenuti senza contesto nella dimensione relazionale ed emotiva e nell'orientamento professionale, senza addestrare o modificare il modello. Il prompt era stato generato dallo stesso ChatGPT e corretto in modo iterativo da supervisori esperti (Cioffi et al., 2025). Vedi [[cioffi-et-al-2025]].

## Riferimenti Bibliografici
- Adamkovič, M. (2025). *Large Language Models in (Not Only) Psychology Training and Research: A Brief Introduction*. Centre of Social and Psychological Sciences, Slovak Academy of Sciences. https://doi.org/10.31577/2025.9788082980144
- Cioffi, V., Ragozzino, O., Mosca, L. L., Moretto, E., Tortora, E., Acocella, A., Montanari, C., Ferrara, A., Crispino, S., Gigante, E., Lommatzsch, A., Pizzimenti, M., Temporin, E., Barlacchi, V., Billi, C., Salonia, G., & Sperandeo, R. (2025). Can AI technologies support clinical supervision? Assessing the potential of ChatGPT. *Informatics*, *12*(1), 29. https://doi.org/10.3390/informatics12010029

## Relazioni
- Vedi anche: [[final-textbook-genaiinpsychologyresearchandtraining]], [[stepwise-cot]], [[ai-research-ethics]], [[cioffi-et-al-2025]]
