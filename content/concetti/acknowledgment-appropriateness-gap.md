---
title: Acknowledgment-Appropriateness Gap
tags: [IA, salute-mentale, psicoterapia, allineamento, ricerca-clinica]
---

# Acknowledgment-Appropriateness Gap & The Crisis Cliff

Fenomeno clinico-metodologico per cui i modelli linguistici mantengono livelli quasi perfetti di calore conversazionale ed empatia superficiale (*acknowledgment* $\approx 0.91 - 1.00$) anche quando la loro appropriatezza terapeutica e la fedeltà al protocollo collassano drasticamente ($0.22 - 0.33$), manifestando un crollo non lineare delle prestazioni nelle situazioni ad alto rischio clinico (*Crisis Cliff*).

## Definizione Operativa

L'**Acknowledgment-Appropriateness Gap** evidenzia una discrepanza fondamentale nella valutazione dell'intelligenza artificiale per la salute mentale:

1.  **Riconoscimento Superficiale (*Acknowledgment*)**: Capacità del modello di validare verbalmente il dolore dell'utente ("Capisco quanto sia difficile per te..."), misurato tradizionalmente tramite metriche di fluidità NLP e questionari di gradimento o empatia percepita.
2.  **Appropriatezza Terapeutica (*Therapeutic Appropriateness*)**: Capacità del modello di compiere atti linguistici conformi alla logica clinica, al protocollo di trattamento e alla tutela a lungo termine della salute del paziente.

Mentre le metriche di usabilità e le valutazioni superficiali suggeriscono che i modelli siano pronti per il deployment clinico, un'analisi strutturata rivela che la competenza clinica si disintegra proprio quando la gravità della situazione aumenta.

Il degrado prestazionale dei modelli linguistici non segue una curva lineare ma presenta un punto di rottura netto (*Crisis Cliff*):
*   **Livelli Routine e Distress**: I modelli rispondono in modo formalmente corretto.
*   **Livello Crisis-Adjacent**: Iniziano a emergere anomalie.
*   **Livello Imminent Risk (Rischio Imminente)**: Si verifica un **collasso sistemico**, dove la fedeltà al protocollo può azzerarsi.

## Evidenze dalla Letteratura

Lo studio di Suhas et al. (2026) dimostra la discrepanza tra le metriche di calore e la fedeltà clinica:

| Livello di Triage | Acknowledgment (Calore) | Appropriatezza Terapeutica | Fedeltà al Protocollo |
| :--- | :--- | :--- | :--- |
| **Routine** ($n=12$) | $1.00$ | $0.83$ | $0.61$ |
| **Distress** ($n=57$) | $0.99$ | $0.81$ | $0.54$ |
| **Crisis-Adjacent** ($n=175$) | $0.98$ | $0.65$ | $0.38$ |
| **Imminent Risk** ($n=6$) | **$0.86$** | **$0.40$** | **$0.04$** |

*Nota: Nei modelli non-frontier, l'appropriatezza terapeutica scende a $0.22 - 0.33$ e la fedeltà a $0.00$.*

### Modalità di Fallimento Clinico
1.  **Safety Preamble / Bookending**: Risolve il task ma inserisce scudi legali/disclaimer (es. Sonnet 4.6), segnalando al paziente ansia da responsabilità.
2.  **Task Abandonment e Silent Omission**: Evita i contenuti dolorosi o tronca le risposte (es. GPT-OSS-20B).

**Riferimenti Bibliografici:**

*   Suhas et al. (2026). *2604.23445v1.pdf*.

## Relazioni

*   [[suhas-et-al-2026]] — Lo studio empirico che formalizza l'Acknowledgment Gap e il Crisis Cliff.
*   [[exposure-interruption-mechanism]] — Le specifiche manifestazioni di rottura del protocollo clinico durante l'esposizione.
*   [[rlhf-safety-therapeutic-conflict]] — Le cause algoritmiche del conflitto tra allineamento e psicoterapia.
*   [[five-axis-mental-health-evaluation-framework]] — Il framework di valutazione pre-deployment.
*   [[rischio-suicidario-ai-limits]] — Limiti e rischi dei modelli di linguaggio nella gestione del rischio suicidario.
*   [[simulated-empathy-vs-authentic-presence]] — La differenza tra empatia sintetica e presenza terapeutica autentica.
