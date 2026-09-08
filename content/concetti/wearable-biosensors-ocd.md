---
tags: [wearables, biomarkers, ocd, machine-learning, digital-health]
source_papers: ["fpsyt-14-1231024.pdf"]
---

# Biosensori Indossabili per il Monitoraggio dell'OCD

## Definizione Operativa
- Utilizzo di dispositivi wearable (es. smartwatch, fasce toraciche) equipaggiati con sensori fisiologici per la rilevazione continua di parametri del sistema nervoso autonomo associati allo stress ossessivo-compulsivo. I parametri tipicamente acquisiti includono la frequenza cardiaca (HR), la variabilità della frequenza cardiaca (HRV), l'attività elettrodermica (EDA), la temperatura cutanea (TEMP) e la fotopletismografia (BVP - Blood Volume Pulse). L'analisi di tali dati storicamente delegata alla statistica lineare viene oggi processata tramite modelli di intelligenza artificiale.
- **Utilità CBT / Applicativa:** Fornisce insight obiettivi sulle fluttuazioni del distress OCD "in-the-wild" (nella vita reale). Nella pratica della Terapia Cognitivo-Comportamentale (CBT) ed ERP, i biosensori offrono l'opportunità di misurare i livelli base di reattività autonomica, mappare le situazioni di esposizione non pianificate, oggettivare la curva di abituazione ansiosa e implementare avvisi predittivi di "ricaduta" (relapse prevention) o innescare interventi digitali "just-in-time" (JITAI).

## Evidenze dalla Letteratura
- **Vantaggi e Fattibilità:** L'integrazione di segnali complessi (es. morfologia dell'onda BVP) in architetture Machine Learning (come i Mixed-Effect Random Forest) riesce a discriminare gli episodi acuti di OCD dallo stato di riposo con circa il 70% di accuratezza, indicando che la "firma" autonomica del distress ossessivo-compulsivo è parzialmente isolabile (Lønfeldt et al., 2023).
- **Sfide:** Il distress dell'OCD produce risposte simpatiche che possono sovrapporsi a stressori non clinici (attività fisica, forti emozioni generiche), generando falsi positivi. Inoltre, l'addestramento richiede enormi moli di dati etichettati dagli utenti (spesso gravati da scarsa compliance prolungata) e una complessa generalizzazione temporale a causa dei bias individuali (Lønfeldt et al., 2023).

## Riferimenti Bibliografici
- Lønfeldt, N. N., Olesen, K. V., Das, S., Mora-Jensen, A. R. C., Pagsberg, A. K., & Clemmensen, L. K. H. (2023). Predicting obsessive-compulsive disorder episodes in adolescents using a wearable biosensor—A wrist angel feasibility study. *Frontiers in Psychiatry*, 14, 1231024. https://doi.org/10.3389/fpsyt.2023.1231024

## Relazioni
- Vedi anche: [[lonfeldt-et-al-2023]]
