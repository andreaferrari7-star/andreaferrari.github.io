---
tags: [ocd, wearable-biosensors, machine-learning, adolescents, ecological-momentary-assessment]
source_papers: ["fpsyt-14-1231024.pdf"]
---

# Predicting Obsessive-Compulsive Disorder Episodes using Wearable Biosensors

## Definizione Operativa
- Studio di fattibilità ("Wrist Angel") sull'utilizzo di biosensori indossabili (Empatica E4) accoppiati a modelli di Machine Learning (Random Forest, MERF) per rilevare e prevedere automaticamente episodi di distress legato al Disturbo Ossessivo-Compulsivo (OCD) negli adolescenti nel loro ambiente di vita quotidiana (*in-the-wild*).
- **Utilità CBT / Applicativa:** Permette un monitoraggio continuo ed ecologico (EMA - Ecological Momentary Assessment) superando i limiti dei self-report intermittenti. Rilevare oggettivamente un episodio OCD tramite correlati autonomici (volume del polso ematico, attività elettrodermica) pone le basi per interventi *just-in-time* (JITAIs) durante la CBT, come l'invio di prompt per resistere alle compulsioni o la misurazione oggettiva dell'abituazione durante i compiti di esposizione (ERP).

## Evidenze dalla Letteratura
- **Efficacia:** Modelli basati su Random Forest (RF) e Mixed-Effect Random Forest (MERF) hanno dimostrato di poter classificare gli episodi OCD con un'accuratezza del 70% utilizzando segnali fisiologici (specialmente le variazioni e il contenuto in frequenza del Blood Volume Pulse - BVP). I modelli temporalmente generalizzati (addestrati su più pazienti) hanno superato quelli strettamente personalizzati su singolo paziente (Lønfeldt et al., 2023).
- **Limiti:** Alta variabilità inter-individuale e presenza di falsi positivi. Le sfide legate all'aderenza prolungata all'uso del biosensore da parte degli adolescenti, la difficoltà di isolare il distress OCD da stress fisici o altre emozioni, e la bassa sensibilità (recall) in alcuni pazienti rendono la tecnologia ancora non pronta per applicazioni cliniche autonome (Lønfeldt et al., 2023).

## Riferimenti Bibliografici
- Lønfeldt, N. N., Olesen, K. V., Das, S., Mora-Jensen, A. R. C., Pagsberg, A. K., & Clemmensen, L. K. H. (2023). Predicting obsessive-compulsive disorder episodes in adolescents using a wearable biosensor—A wrist angel feasibility study. *Frontiers in Psychiatry*, 14, 1231024. https://doi.org/10.3389/fpsyt.2023.1231024

## Relazioni
- Vedi anche: [[wearable-biosensors-ocd]]
