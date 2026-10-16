---
tags: []
tipo_fonte: scientifica
source_papers: ["2602.19948v2.pdf"]
---

# Modello Cognitivo-Affettivo Dinamico (Dynamic Cognitive-Affective Model for Simulated Patients)

**Summary**: Architettura computazionale a 5 stadi (Appraisal, State Update, Belief Formation, Emotion Regulation, Response Formulation) integrata in agenti LLM tramite Chain-of-Thought prompting per simulare con realismo psicologico l'evoluzione degli stati interni, delle credenze e delle reazioni emotive dei pazienti durante la psicoterapia.
**Fonti**: Steenstra et al. (2026); Steenstra, Nouraei & Bickmore (2025), cfr. [[simpatient-evaluation-testbed]].
**Last updated**: 2026-08-27
---

## Definizione e Fondamenti Teorici

Il **Modello Cognitivo-Affettivo Dinamico** trasforma gli LLM impiegati come pazienti virtuali da semplici "generatori di testo black-box" a veri e propri **motori cognitivi strutturati**. 

Il modello si fonda su solide teorie psicologiche:
- **Cognitive Appraisal Theory** (Lazarus & Folkman, 1984; Ellsworth, 1991): Le emozioni scaturiscono dalla valutazione soggettiva degli eventi ambientali (gli enunciati del terapeuta) rispetto agli scopi e al benessere dell'individuo.
- **Belief-Desire-Intention (BDI) Model** (Georgeff et al., 1998): Modellazione dell'agente basata sulle sue credenze centrali, bisogni motivazionali e piani d'azione.
- **Emotion Regulation Theory** (Gross, 2013): Selezione di strategie di coping consone agli obiettivi emotivi.
- **Perception-Action Cycle** (Neisser, 2014): Chiusura circolare tra percezione, elaborazione interna e azione linguistica.

```mermaid
flowchart LR
    Msg["Messaggio del Terapeuta IA"] --> S1["1. Appraisal"]
    S1 --> S2["2. State Update"]
    S2 --> S3["3. Belief Formation"]
    S3 --> S4["4. Emotion Regulation"]
    S4 --> S5["5. Response Formulation"]
    S5 --> Out["Risposta Esterna del Paziente"]
```

---

## La Pipeline di Elaborazione a 5 Stadi

A ogni turno di dialogo, l'agente paziente (alimentato da Gemini 2.5 Pro) esegue una sequenza esplicita di passaggi cognitivi guidata da Chain-of-Thought prompting:

### 1. Appraisal (Valutazione Cognitiva)
L'agente analizza l'enunciato del terapeuta rapportandolo alle proprie credenze nucleari (*core beliefs*), desideri, stadio motivazionale e cronologia della seduta.
*Esempio*: Un paziente con la credenza di essere "irrecuperabile" interpreta un invito all'astinenza totale come una richiesta insormontabile, confermando il proprio senso di fallimento.

### 2. State Update (Aggiornamento degli Stati Interni)
Sulla base dell'appraisal, l'agente modifica i punteggi (su scala Likert 1–5) di **10 costrutti psicologici chiave**:
1. *Hopelessness Intensity* (Disperazione)
2. *Negative Core Belief Intensity* (Forza degli schemi disfunzionali)
3. *Cognitive Preoccupation with Use* (Pensieri ossessivi su sostanze)
4. *Self-Efficacy Intensity* (Autoefficacia percepita)
5. *Distress Tolerance Intensity* (Tolleranza della sofferenza)
6. *Substance Craving Intensity* (Craving viscerale)
7. *Motivational Intensity* (Spinta al cambiamento)
8. *Ambivalence about Change* (Conflitto motivazionale)
9. *Perceived Burdensomeness* (Percezione di essere un peso)
10. *Thwarted Belongingness* (Disconnessione e isolamento)

### 3. Belief Formation (Formazione di Credenze e Attribuzioni Causali)
L'agente produce una motivazione causale esplicita per spiegare la variazione dei propri stati interni (es. *"Il terapeuta ha ignorato la mia fatica, aumentando la mia disperazione e facendomi dubitare delle mie capacità"*). Questo garantisce tracciabilità e coerenza longitudinale.

### 4. Emotion Regulation (Regolazione Emotiva e Coping)
L'agente definisce un obiettivo regolatorio (es. mantenere il controllo, ridurre l'ansia, evitare la vulnerabilità) e sceglie una specifica strategia di coping:
- *Modifica della situazione* (cambiare argomento, porre limiti, contestare l'approccio).
- *Dispiegamento dell'attenzione* (distrazione, evitamento, ruminazione).
- *Cambiamento cognitivo* (distanziamento/intellettualizzazione, reframing).
- *Modulazione della risposta* (soppressione espressiva, sfogo/ventilazione).

### 5. Response Formulation (Formulazione dell'Enunciato)
L'agente sintetizza tutti i passaggi interni per generare la risposta verbale esterna, assicurando perfetta coerenza tra vissuto psicologico interno e comportamento dialogico esteriore.

---

## Valore per la Valutazione della Sicurezza dell'IA

1. **Trasparenza del Rischio Latente**: Rende quantificabile ciò che normalmente è invisibile: i micro-slittamenti di disperazione o craving che precedono gli esiti avversi (ricaduta, tentato suicidio, dropout).
2. **Generazione di Spiegazioni Cliniche Interpretabili**: I log turno per turno permettono a clinici e sviluppatori di eseguire *root-cause analysis* dettagliate sugli errori dei terapeuti IA.
3. **Resistenza e Realismo Clinico**: Evita che i pazienti virtuali siano passivi o condiscendenti, permettendo l'emergere spontaneo di reazioni difensive autentiche (*help-rejecting*, ostilità, ambivalenza).

---

## Relazioni
- [[automated-clinical-ai-red-teaming]] — Metodologia di red teaming clinico basata su questo modello
- [[ai-psychosis]] — Fenomeno di deterioramento psicologico tracciabile tramite la pipeline
- [[four-stage-simulation-cycle]] — Il ciclo di simulazione multi-sessione in cui il modello è inserito
- [[simpatient-evaluation-testbed]] — Sistema SimPatient per l'addestramento e la valutazione clinica
- [[risk-ontology-ai-psychotherapy]] — Ontologia dei costrutti e dei segnali di allarme

## Riferimenti Bibliografici
- Ellsworth, P. C. (1991). Some implications of cognitive appraisal theories of emotion.
- Georgeff, M., Pell, B., Pollack, M., Tambe, M., & Wooldridge, M. (1998). The belief-desire-intention model of agency. In *International workshop on agent theories, architectures, and languages. Springer* (pp. 1–10).
- Gross, J. J. (2013). Handbook of emotion regulation. Guilford publications.
- Lazarus, R. S., & Folkman, S. (1984). Stress, appraisal, and coping. Springer publishing company.
- Neisser, U. (2014). Cognitive psychology: Classic edition. Psychology press.
- Steenstra, I., Nouraei, F., & Bickmore, T. (2025). Scaffolding empathy: Training counselors with simulated patients and utterance-level performance visualizations. In *Proceedings of the 2025 CHI Conference on Human Factors in Computing Systems (CHI '25)*. Association for Computing Machinery.
- Steenstra, I., Pedrelli, P., Shi, W., Marsella, S., & Bickmore, T. W. (2026). Assessing Risks of Large Language Models in Mental Health Support: A Framework for Automated Clinical AI Red Teaming. *arXiv preprint arXiv:2602.19948v2 [cs.CL]*, 1–32.
