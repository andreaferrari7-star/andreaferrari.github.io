---
tags:
  - digital-phenotyping
  - computational-psychiatry
  - multimodal-sensing
  - passive-sensing
  - psychiatric-biomarkers
  - wearable-devices
  - speech-analysis
  - nlp
  - machine-learning
  - affective-computing
---

# Fenotipizzazione Computazionale (Digital Phenotyping)

## Definizione Operativa

- La **fenotipizzazione computazionale** (*digital phenotyping* o *computational phenotyping*) è la quantificazione continua, oggettiva e non invasiva del comportamento umano, delle dinamiche affettive e dell'attività fisiologica tramite flussi di dati generati spontaneamente dall'individuo nel suo ambiente ecologico naturale (Oudin et al., 2023; Močnik et al., 2025).
- **Utilità Clinica/Applicativa:** Supera la natura episodica e retrospettiva della psicodiagnosi classica (interviste strutturate, questionari autosomministrati come PHQ-9 e GAD-7) sostituendola con una misurazione ecologica, longitudinale e multimodale. Consente rilevazione precoce di ricadute, personalizzazione del trattamento e interventi adattativi in tempo reale (*Just-In-Time Adaptive Interventions*, JITAI).

---

## I Sei Canali Sensoriali

La fenotipizzazione computazionale integra sei flussi informativi obiettivi (Močnik et al., 2025):

| # | Canale | Indicatori principali |
|---|--------|-----------------------|
| 1 | **Linguaggio naturale / NLP** | Pronomi personali (1ª vs 3ª persona), valenza semantica, bias della negatività, complessità sintattica, espressioni assolutistiche |
| 2 | **Acustica vocale e paralinguistica** | Frequenza fondamentale F0, jitter, shimmer, formanti F1-F4, latenza di risposta, durata delle pause |
| 3 | **Computer vision / espressioni facciali** | Action Units FACS, attivazione muscolo zigomatico vs corrugatore, direzione dello sguardo, sorriso paradossale |
| 4 | **Fisiologia autonomica (wearable)** | HRV (RMSSD, HF-HRV), aritmia sinusale respiratoria (RSA), conduttanza cutanea (EDA/SCL), intervallo QTc |
| 5 | **Telemetria passiva da smartphone** | Raggio di mobilità GPS, entropia spaziale, log chiamate/messaggi, sblocchi notturni dello schermo |
| 6 | **Self-report ecologico (EMA)** | Ecological Momentary Assessment contestualizzato, campionato nel momento e nel contesto naturale |

---

## Evidenze dalla Letteratura

### Firme Transdiagnostiche Condivise
Alcuni segnali si riscontrano trasversalmente in piu disturbi (Mocnik et al., 2025):
- Riduzione dell'HRV e dell'aritmia sinusale respiratoria (RSA): indica il fallimento del "freno vagale" parasimpatico.
- Appiattimento prosodico (bassa deviazione standard di F0): tipico della depressione e del PTSD (Low et al., 2020).
- Disregolazione del ritmo circadiano sonno-veglia.
- Ritiro sociale misurabile via telemetria passiva.

### Firme Disturbo-Specifiche
- **Depressione:** Sovra-rappresentazione di pronomi di prima persona singolare (io, me, mio) come indicatore di ruminazione egocentrata (Khoo et al., 2024; Zierer et al., 2024); drastica riduzione del raggio di mobilita GPS e diminuzione dell'entropia spaziale (Rohani et al., 2018); ipoattivazione del muscolo zigomatico e iperattivazione del corrugatore (Mocnik et al., 2025).
- **Disturbo Bipolare (Mania):** Incremento della mobilita geospaziale, aumento di F0 e velocita articolatoria, innalzamento delle formanti F1, F2, F4 (Saccaro et al., 2021).
- **Ansia / PTSD:** Iperarousal simpatico cronico (EDA/SCL elevata), parole a valenza di minaccia e vigilanza visiva, evitamento di luoghi pubblici nel GPS (Mocnik et al., 2025).
- **Disturbo Borderline di Personalita (BPD):** Sorriso paradossale (co-occorrenza di espressioni di rabbia e sorriso sociale), prevalenza di pronomi di terza persona, prolungamento dell'intervallo QTc a riposo (Mocnik et al., 2024).

### Architetture di Machine Learning
- Il **Framework Trimodale** (Wang et al., 2025) combina EMA periodico, biosensori da polso e Speech Emotion Recognition (SER) per catturare la dinamica emotiva longitudinale.
- Il **Science-Guided Machine Learning (SGML)** incorpora vincoli fisiologici nelle funzioni di perdita per prevenire overfitting e correlazioni spurie (Koppe et al., 2021).
- Il **few-shot learning** e il **transfer learning** affrontano lo small-data problem tipico dei dati clinici longitudinali (Koppe et al., 2021).

### Limiti Tecnici e Rischi
- **Small-data problem:** I dati clinici per singolo paziente sono scarsi e ad alta dimensionalita, rendendo necessari approcci di transfer learning o SGML [da verificare su specifici disturbi rari].
- **Privacy e governance:** L'acquisizione di biosegnali e dati comportamentali passivi richiede crittografia, elaborazione on-device (Edge AI) e consenso informato granulare conforme al GDPR e alle normative SaMD (Welzel et al., 2025).
- **Opacita algoritmica:** Le architetture puramente deep learning rischiano di essere "black-box"; l'ancoraggio a feature osservabili favorisce la trasparenza (XAI) (Mocnik et al., 2025).
- **Bias di campionamento:** I dataset di addestramento riflettono prevalentemente popolazioni WEIRD (Western, Educated, Industrialized, Rich, Democratic), limitando la generalizzabilita transculturale [da verificare].

---

## Applicazioni Cliniche

1. **Early Warning Systems:** Rilevazione passiva di deviazioni subcliniche dal baseline individuale (es. alterazione del ritmo sonno-veglia, calo delle interazioni vocali) prima che si manifesti un episodio depressivo maggiore o una crisi suicidaria.
2. **JITAI (Just-In-Time Adaptive Interventions):** Micro-interventi psicologici (es. esercizi di respirazione, ristrutturazione cognitiva) erogati nel momento in cui i biosensori segnalano un picco di iperattivazione simpatica.
3. **Dashboard clinica XAI:** Trasmissione trasparente delle feature di rischio al terapeuta, che mantiene la funzione ermeneutica e decisionale ([[modello-centauro-clinico|Modello Centauro]]).

---

## Riferimenti Bibliografici

- Mocnik, G., Rehberger, A., Smogavc, Z., Mlakar, I., Smrke, U., & Mocnik, S. (2025). Multimodal observable cues in mood, anxiety, and borderline personality disorders: a review of reviews to inform explainable AI in mental health. *Frontiers in Artificial Intelligence*, 8:1696448. https://doi.org/10.3389/frai.2025.1696448
- Mocnik, S., Smrke, U., Mlakar, I., Mocnik, G., Gregoric Kumperschak, H., & Plohl, N. (2024). Beyond clinical observations: a scoping review of AI-detectable observable cues in borderline personality disorder. *Frontiers in Psychiatry*, 15:1345916. https://doi.org/10.3389/fpsyt.2024.1345916
- Oudin, A., Maatoug, R., Bourla, A., Ferreri, F., Bonnot, O., Millet, B., et al. (2023). Digital phenotyping: data-driven psychiatry to redefine mental health. *Journal of Medical Internet Research*, 25:e44502. https://doi.org/10.2196/44502
- Wang, P., Liu, A., & Sun, X. (2025). Integrating emotion dynamics in mental health: a trimodal framework combining ecological momentary assessment, physiological measurements, and speech emotion recognition. *Interdisciplinary Medicine*, 3:e20240095. https://doi.org/10.1002/INMD.20240095
- Koppe, G., Meyer-Lindenberg, A., & Durstewitz, D. (2021). Deep learning for small and big data in psychiatry. *Neuropsychopharmacology*, 46(1), 176-190. https://doi.org/10.1038/s41386-020-0767-z
- Low, D. M., Bentley, K. H., & Ghosh, S. S. (2020). Automated assessment of psychiatric disorders using speech: a systematic review. *Laryngoscope Investigative Otolaryngology*, 5(1), 96-116. https://doi.org/10.1002/lio2.354
- Rohani, D. A., Faurholt-Jepsen, M., Kessing, L. V., & Bardram, J. E. (2018). Correlations between objective behavioral features collected from mobile and wearable devices and depressive mood symptoms in patients with affective disorders: systematic review. *JMIR Mhealth Uhealth*, 6(8):e165. https://doi.org/10.2196/mhealth.9691
- Saccaro, L. F., Amatori, G., Cappelli, A., Mazziotti, R., Dell'Osso, L., & Rutigliano, G. (2021). Portable technologies for digital phenotyping of bipolar disorder: a systematic review. *Journal of Affective Disorders*, 295, 323-338. https://doi.org/10.1016/j.jad.2021.08.052

---

## Relazioni

- Vedi anche: [[multimodal-observable-cues-in-psychiatry]], [[social-media-phenotyping-anxiety]], [[wearable-sensor-fusion-adherence]], [[modello-centauro-clinico]], [[explainable-mental-health-diagnosis]], [[algorithmic-tractability-in-psychotherapy]]
