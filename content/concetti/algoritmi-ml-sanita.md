---
tags: [algoritmi, machine-learning, regressione, modelli-predittivi, sanita, formazione]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C2M3_JK_Dec18_2024_V1.0 (1).pdf", "BackgroundMaterials_AI-Health_C2M4_JK_Dec18_2024_V1.0 (1).pdf", "BackgroundMaterials_AI-Health_C3M1_JK_Dec28_2024_V1.0 (1) (1).pdf", "BackgroundMaterials_AI-Health_C3M2_JK_Dec28_2024_V1.0 pdf  (1).pdf", "BackgroundMaterials_AI-Health_C3M4_JK_Dec22_2024_V1.0 pgd (1).pdf"]
---

# Algoritmi di machine learning in sanità

## Definizione Operativa
- È la mappa delle famiglie di algoritmi usate per l'analisi dei dati sanitari, con il tipo di problema a cui ciascuna risponde: esiti continui, esiti binari, gruppi senza etichette, decisioni sequenziali, immagini, testi (Khuntia, 2024g).
- **Utilità CBT / Applicativa:** riconoscere la famiglia di un modello aiuta a porre le domande giuste. Che esito stima? È interpretabile? Come è stato validato? È calibrato? Molti strumenti di screening e di stima del rischio in salute mentale sono regressioni logistiche o modelli ad albero, non «IA» opaca.

## Evidenze dalla Letteratura

### Le famiglie
- **Metodi statistici classici:** la regressione lineare stima esiti continui (durata della degenza, costi); la regressione logistica stima la probabilità di esiti binari (malattia sì/no, riammissione). Sono interpretabili, con coefficienti e odds ratio leggibili, e spesso fanno da modello di riferimento per sistemi più complessi (Khuntia, 2024g). Altre varianti utili sono la regressione lasso, che seleziona le variabili azzerando i coefficienti poco utili (adatta a dati con molte variabili, come quelli genomici), e quella polinomiale per relazioni non lineari come la curva dose-effetto (Khuntia, 2024i).
- **Sistemi a regole:** alberi decisionali costruiti a mano e sistemi esperti, che traducono conoscenza clinica in percorsi decisionali (Khuntia, 2024g).
- **ML supervisionato:** impara da dati etichettati. Esempi: random forest e SVM per il rischio di complicanze (Khuntia, 2024g).
- **ML non supervisionato:** raggruppa i casi senza etichette (*clustering*), per esempio pazienti con profili simili (Khuntia, 2024g).
- **Apprendimento per rinforzo:** ottimizza decisioni sequenziali con la retroazione, per esempio l'aggiustamento dell'insulina (Khuntia, 2024g).
- **Deep learning:** le CNN servono per le immagini, le RNN per le serie temporali (Khuntia, 2024g). Vedi [[reti-neurali-in-psicologia]].

### Tecniche non supervisionate, k-NN, semi-supervisionate e per rinforzo
- **Non supervisionate:** *clustering* con K-means o DBSCAN (gruppi di forma qualsiasi, rumore isolato); riduzione di dimensionalità con PCA e ICA (per esempio per separare il segnale cerebrale dal rumore nell'EEG); regole di associazione con Apriori e FP-Growth; rilevazione di anomalie con z-score e Isolation Forest (Khuntia, 2024j).
- **Attenzione alle associazioni:** che due elementi compaiano spesso insieme (un farmaco e un miglioramento clinico) non dimostra che uno causi l'altro. I materiali didattici trascurano questa distinzione e presentano le regole di associazione come base per prescrivere (Khuntia, 2024j).
- **k-NN:** predice dai k casi più simili. È semplice ma lento su grandi dataset e sensibile alla scala delle variabili, al rumore, all'alta dimensionalità e allo sbilanciamento (Khuntia, 2024j).
- **Semi-supervisionate:** *self-training* con soglie di confidenza, *co-training* su viste indipendenti, propagazione delle etichette su grafo, dati sintetici con VAE e GAN (Khuntia, 2024j).
- **Per rinforzo:** un agente impara una strategia da stati, azioni e ricompense. È *model-free* (ottimizzazione della policy, Q-learning) o *model-based* (con un modello dell'ambiente appreso o dato). Nelle applicazioni ad alto rischio, come insulina, ventilazione o sepsi, trasparenza, equità e responsabilità sono questioni aperte (Khuntia, 2024j).

### Alberi, ensemble e reti neurali
- **Alberi decisionali:** sequenze di condizioni leggibili come un protocollo, adatte a triage e classificazione del rischio. Perdono chiarezza quando le variabili aumentano. Va distinto l'albero appreso dai dati da quello scritto a mano con soglie cliniche, che è una regola esperta (Khuntia, 2024h).
- **Random forest:** aggregano centinaia di alberi addestrati su sottoinsiemi casuali. Riducono il sovradattamento a scapito dell'interpretabilità, che si recupera in parte con l'importanza delle variabili (Khuntia, 2024h).
- **Gradient boosting:** costruisce gli alberi in sequenza, ognuno a correzione degli errori del precedente. Le varianti diffuse sono XGBoost, LightGBM e CatBoost. La loro superiorità sulle random forest, affermata nei materiali didattici, dipende dai dati e va verificata caso per caso (Khuntia, 2024h).
- **Reti neurali:** le CNN servono per le immagini, le RNN e le loro varianti (LSTM, GRU) per le sequenze, i transformer per testi e dati multimodali. Ci sono poi i GAN per i dati sintetici, gli autoencoder per le anomalie, le reti su grafi per le relazioni e le *neural ODE* per i dati continui. Il prezzo è l'opacità: per spiegare le predizioni si usano strumenti come SHAP e LIME (Khuntia, 2024h).
- **Il compromesso di fondo:** più un modello è flessibile, meno è leggibile. In clinica la scelta va motivata: un modello semplice e calibrato può essere preferibile a uno più accurato ma opaco, se la differenza di prestazione è piccola. Anche i materiali didattici indicano preferibili, nelle applicazioni ad alto rischio, modelli più interpretabili come gli alberi decisionali (Khuntia, 2024l).
- **Altri:** NLP basato su transformer per note cliniche e letteratura, algoritmi su grafi, reti bayesiane che integrano conoscenza a priori ed evidenza nuova, algoritmi di ottimizzazione, sistemi di raccomandazione (Khuntia, 2024g).

### Il ciclo di lavoro
- Le guide didattiche descrivono una sequenza: definire il problema, preparare i dati, esplorarli, dividerli tra addestramento e test, stimare il modello, valutarlo, interpretarlo, ottimizzarlo, metterlo in produzione con monitoraggio, comunicare i risultati (Khuntia, 2024g).
- Tre correzioni di metodo vanno tenute presenti:
  - **ordine dei passaggi:** imputazione, standardizzazione, selezione delle variabili e bilanciamento delle classi (per esempio SMOTE) vanno fatti solo dentro il training set, dopo la divisione, per evitare il *data leakage*. La guida di Khuntia (2024g) li colloca prima della divisione (Jacobs et al., 2026). Vedi [[mccv-and-statistical-validation-clinical-ml]];
  - **validazione:** su campioni clinici piccoli e sbilanciati una singola divisione 80/20 dà stime instabili; è preferibile una validazione ripetuta con *balanced accuracy* (Jacobs et al., 2026);
  - **metriche:** per i modelli che stimano probabilità servono discriminazione, calibrazione e utilità clinica, non solo accuratezza e AUC (Collins et al., 2024). Vedi [[clinical-prediction-model-evaluation]].

### Limiti
- Gli esempi applicativi nei materiali didattici sono riportati senza fonti e alcuni prodotti citati non sono più attivi [da verificare]. Vedi [[ai-health-c2m3-khuntia-2024]].
- Gli esempi numerici delle guide (probabilità di esito, importanza delle variabili) sono illustrativi, non risultati di studi (Khuntia, 2024h).

## Riferimenti Bibliografici
- Collins, G. S., Moons, K. G. M., Dhiman, P., Riley, R. D., Beam, A. L., Van Calster, B., Ghassemi, M., Liu, X., Reitsma, J. B., van Smeden, M., Boulesteix, A.-L., Camaradou, J. C., Celi, L. A., Denaxas, S., Denniston, A. K., Glocker, B., Golub, R. M., Harvey, H., Heinze, G., . . . Logullo, P. (2024). TRIPOD+AI statement: Updated guidance for reporting clinical prediction models that use regression or machine learning methods. *BMJ*, *385*, Article e078378. https://doi.org/10.1136/bmj-2023-078378
- Jacobs, N., Voelkle, M. C., Kathmann, N., & Hilbert, K. (2026). Can we Improve Prediction of Psychotherapy Outcomes Through Pretraining With Simulated Data? *arXiv preprint arXiv:2601.06159v1 [stat.ML]*.
- Khuntia, J. (2024g). *Background materials for Course 2: The data to decision path for infusion of AI in healthcare. Module 3: AI and ML relevant algorithms in healthcare models* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/the-data-to-decision-path-for-infusion-of-ai-in-healthcare
- Khuntia, J. (2024h). *Background materials for Course 2: The data to decision path for infusion of AI in healthcare. Module 4: AI relevant complex algorithms in healthcare models* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/the-data-to-decision-path-for-infusion-of-ai-in-healthcare
- Khuntia, J. (2024i). *Background materials for Course 3: AI integration in healthcare. Module 1: Relevant ML algorithms in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare
- Khuntia, J. (2024j). *Background materials for Course 3: AI integration in healthcare. Module 2: Relevant ML algorithms in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare
- Khuntia, J. (2024l). *Background materials for Course 3: AI integration in healthcare. Module 4: The craft of modeling for AI in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare

## Relazioni
- Vedi anche: [[ia-machine-learning-deep-learning]], [[ai-health-c2m3-khuntia-2024]], [[ai-health-c2m4-khuntia-2024]], [[ai-health-c3m1-khuntia-2024]], [[ai-health-c3m2-khuntia-2024]], [[mccv-and-statistical-validation-clinical-ml]], [[clinical-prediction-model-evaluation]], [[reti-neurali-in-psicologia]], [[diad-framework]]
