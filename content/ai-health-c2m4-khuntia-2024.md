---
tags: [ai-health-coursera, formazione, alberi-decisionali, random-forest, gradient-boosting, reti-neurali, cnn, rnn, xai]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C2M4_JK_Dec18_2024_V1.0 (1).pdf"]
---

# AI for Healthcare Systems, C2M4: algoritmi complessi nei modelli sanitari (Khuntia, 2024h)

## Definizione Operativa
- Materiale di approfondimento (63 pagine, versione 1.0 del 18 dicembre 2024) che chiude il corso 2 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]]. Le intestazioni di pagina lo chiamano per errore «Module 3». Tratta gli algoritmi che superano i limiti delle regressioni con relazioni non lineari e dati non strutturati: alberi decisionali, random forest, gradient boosting e reti neurali. Per ciascuno offre guide operative ed esempi clinici simulati (Khuntia, 2024h).
- **Utilità CBT / Applicativa:** chiarisce il compromesso tra interpretabilità e potenza che attraversa tutta l'IA clinica. Un albero decisionale si legge come un protocollo; una foresta o una rete neurale richiedono strumenti di spiegazione (importanza delle variabili, SHAP, LIME). Gli esempi numerici del modulo sono illustrativi e non vanno presi come evidenze. Vedi [[algoritmi-ml-sanita]].

## Evidenze dalla Letteratura

### Perché algoritmi complessi
- Regressione lineare e logistica non colgono bene relazioni non lineari, interazioni tra molti predittori e dati non strutturati come immagini o testi. Gli algoritmi complessi colmano questi limiti e affiancano i modelli semplici senza sostituirli (Khuntia, 2024h).

### Alberi decisionali
- Struttura a diagramma di flusso: ogni ramo è una condizione, ogni foglia un esito. Il pregio principale è la trasparenza, che li rende adatti a triage, classificazione del rischio e predizione dell'aderenza. Un esempio è il «rischio alto di non aderenza» per effetti collaterali gravi e basso reddito. Il limite è che, aggiungendo variabili, perdono chiarezza (Khuntia, 2024h).
- La guida in 11 passi comprende scelta del criterio di divisione (Gini, guadagno di informazione), limite di profondità, potatura, valutazione (matrice di confusione, ROC/AUC, validazione incrociata), esportazione in JSON o PMML, integrazione in un sistema di supporto alla decisione, test con dati anonimizzati, monitoraggio e formazione degli utenti (Khuntia, 2024h).
- Due esempi:
  - un albero per il rischio di diabete: glicemia a digiuno sopra 126 mg/dL = rischio alto, altrimenti IMC sopra 30 = rischio moderato;
  - un albero a dieci nodi per le complicanze dopo chirurgia addominale maggiore, basato su età, pressione, comorbilità, emoglobina, durata dell'intervento, parametri post-operatori, PCR e mobilizzazione (Khuntia, 2024h).

### Random forest
- Combina centinaia di alberi addestrati su sottoinsiemi casuali dei dati e ne aggrega le risposte. Rispetto al singolo albero riduce il sovradattamento e regge dati ad alta dimensionalità. Gli usi citati: mortalità in terapia intensiva, sepsi precoce, riammissioni, risposta a terapie oncologiche, aritmie da dispositivi indossabili, aderenza. Il costo è una minore interpretabilità, in parte compensata dall'importanza delle variabili (Khuntia, 2024h).
- Gli esempi guidati riguardano complicanze, tempi di recupero e degenza in terapia intensiva dopo chirurgia cardiovascolare, e l'efficacia di terapie oncologiche personalizzate. Solo in quest'ultimo il modulo chiede di verificare la **calibrazione** delle probabilità (Khuntia, 2024h).

### Gradient boosting e varianti
- Costruisce gli alberi in sequenza: ogni albero corregge gli errori del precedente e si concentra sui casi difficili, come pazienti atipici o malattie rare. Gli usi citati: insorgenza di scompenso, bisogno di ventilazione in terapia intensiva, riammissioni, terapie oncologiche, trapianti, focolai a livello di popolazione (Khuntia, 2024h).
- La guida in 11 passi copre la scelta del framework (XGBoost, LightGBM, CatBoost), gli iperparametri, l'arresto anticipato, la spiegabilità con SHAP e LIME, gli audit dei bias tra gruppi demografici e la conformità a HIPAA e GDPR. Un capitolo è dedicato alla regolazione degli iperparametri: *learning rate*, numero e profondità degli alberi, *min child weight*, sottocampionamento di righe e colonne, regolarizzazione L1/L2, *gamma*; ricerca a griglia, casuale o bayesiana (Optuna, Hyperopt) (Khuntia, 2024h).
- Varianti descritte:
  - AdaBoost: semplice ma sensibile al rumore;
  - XGBoost: regolarizzazione e gestione dei dati mancanti;
  - LightGBM: istogrammi e crescita per foglie, veloce;
  - CatBoost: variabili categoriali native e *ordered boosting* contro il leakage;
  - boosting stocastico.
  La tabella comparativa del PDF è impaginata male e non si può leggere in modo affidabile (Khuntia, 2024h).

### Reti neurali
- Strati di nodi interconnessi che apprendono rappresentazioni da dati non strutturati: immagini, segnali, testi (Khuntia, 2024h). Le architetture descritte:
  - **CNN:** strati convolutivi, pooling, strati completamente connessi, ReLU, dropout e output softmax o sigmoide. Imparano da sole le caratteristiche rilevanti. Si usano per mammografie, noduli polmonari, retinopatia diabetica (citato DeepMind), istopatologia, ECG, pianificazione chirurgica, dermatologia. I limiti sono il bisogno di molti dati etichettati, l'opacità, la scarsa generalizzazione a popolazioni o macchinari diversi e il costo computazionale;
  - **RNN:** stato nascosto come memoria, pesi condivisi nel tempo, addestramento con *backpropagation through time*. Le varianti sono LSTM, GRU, bidirezionali e con attenzione. Si usano per parametri vitali in terapia intensiva, traiettorie dalle cartelle cliniche, genomica, risposta ai trattamenti, e per la diagnosi dal parlato nel Parkinson e nell'Alzheimer. I limiti sono gradiente che svanisce, costo, sovradattamento e opacità;
  - **ibridi CNN-RNN:** per serie di risonanze, video endoscopici, ECG e rischio di ictus;
  - **altre architetture:** transformer (NLP clinico, LLM, genomica), GAN (dati sintetici, miglioramento delle immagini, molecole), *capsule networks*, autoencoder (anomalie, riduzione del rumore), reti a impulsi per dispositivi a basso consumo, reti su grafi, *neural ODE* per dati continui come la glicemia.

### Errori e limiti della fonte
- **Soglia diagnostica scambiata per rischio:** nell'albero sul diabete una glicemia a digiuno sopra 126 mg/dL classifica il paziente a «rischio alto». Ma 126 mg/dL è la soglia diagnostica del diabete secondo i criteri internazionali correnti [da verificare]: l'albero etichetta come «a rischio» persone che probabilmente hanno già la malattia.
- **Alberi scritti a mano:** gli alberi dei due esempi hanno soglie fissate a priori. Sono regole cliniche esperte, non alberi appresi dai dati, e il modulo non distingue i due casi.
- **Ordine dei passaggi:** nella guida agli alberi il bilanciamento con SMOTE precede di nuovo la divisione tra training e test, con rischio di *data leakage*. Vedi [[mccv-and-statistical-validation-clinical-ml]].
- **Risultati inventati:** le probabilità (85% di complicanze, 87% di successo terapeutico, 85% di mortalità) e le importanze delle variabili sono valori illustrativi. Lo è anche l'affermazione che positività a HER2 e mutazione di BRCA1 «aumentano significativamente» la probabilità di risposta, presentata senza fonte.
- **Errore concettuale:** la probabilità di successo di una terapia viene definita un compito di «regressione».
- **Affermazioni senza prove:** la «superiorità» del gradient boosting sulle random forest e il fatto che le CNN superino «spesso» i radiologi.
- **Automatismo terapeutico:** nell'esempio sulla terapia intensiva l'allerta del modello porta direttamente a liquidi, antibiotici e regolazione del ventilatore, senza menzionare il giudizio clinico. Vedi [[automation-bias-clinical-reasoning]].
- **Aspetti positivi rispetto ai moduli precedenti:** compaiono la calibrazione, gli audit dei bias tra gruppi e gli strumenti di spiegabilità.

## Riferimenti Bibliografici
- Khuntia, J. (2024h). *Background materials for Course 2: The data to decision path for infusion of AI in healthcare. Module 4: AI relevant complex algorithms in healthcare models* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/the-data-to-decision-path-for-infusion-of-ai-in-healthcare

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[algoritmi-ml-sanita]], [[reti-neurali-in-psicologia]], [[mccv-and-statistical-validation-clinical-ml]], [[clinical-prediction-model-evaluation]], [[automation-bias-clinical-reasoning]], [[explainable-mental-health-diagnosis]], [[ai-health-c2m3-khuntia-2024]]
