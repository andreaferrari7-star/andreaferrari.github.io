---
tags: [pseudoreplicazione, dipendenza-dati, statistica, modelli-multilivello]
source_papers: ["2507.04491v2.pdf"]
---

# Pseudoreplication

## Definizione Operativa
- Errore inferenziale derivante dal trattare risposte multiple interdipendenti generate dallo stesso LLM o contesto come se fossero osservazioni indipendenti da campioni separati.
- **Utilità CBT:** Previene l'illusione di robustezza clinica quando si valutano risposte ripetute generate da un modello o registrazioni multiple di uno stesso paziente in sessioni ravvicinate.

## Evidenze dalla Letteratura
- L'alta correlazione intraclasse delle risposte dei modelli linguistici riduce la reale varianza dei dati, gonfiando artificialmente il tasso di errori di Tipo I (falsi positivi) (Lin, 2026).
- L'adozione di modelli multilivello e di equazioni di stima generalizzate (GEE) è indispensabile per correggere la struttura nidificata delle osservazioni (Lin, 2026).

**Riferimenti Bibliografici:**
- Lin, Z. (2026). A validity-guided workflow for robust large language model research in psychology. *Behavior Research Methods*, 58, Article 216. https://doi.org/10.3758/s13428-026-03073-2

## Relazioni
- Vedi anche: [[lin-2026]], [[dual-validity-framework]], [[measurement-phantoms]]
