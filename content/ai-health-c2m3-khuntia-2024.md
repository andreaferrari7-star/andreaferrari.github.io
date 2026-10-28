---
tags: [ai-health-coursera, formazione, algoritmi, regressione-lineare, regressione-logistica, modelli-predittivi, validazione]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C2M3_JK_Dec18_2024_V1.0 (1).pdf"]
---

# AI for Healthcare Systems, C2M3: algoritmi di IA e ML nei modelli sanitari (Khuntia, 2024g)

## Definizione Operativa
- Materiale di approfondimento (22 pagine, versione 1.0 del 18 dicembre 2024) del terzo modulo del corso 2 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]]. Fa una panoramica delle famiglie di algoritmi usate in sanità e tratta in dettaglio regressione lineare e logistica, con due guide operative passo-passo (Khuntia, 2024g).
- **Utilità CBT / Applicativa:** la regressione logistica è il modello di base di molti strumenti di screening e stima del rischio, anche in salute mentale. Il modulo cita la stima della probabilità di depressione da età, genere, condizione socioeconomica, sonno e umore riferito. Saperla leggere (probabilità, odds ratio, matrice di confusione) aiuta a valutare uno strumento predittivo. Le guide del modulo hanno però errori di metodo, indicati sotto. Vedi [[algoritmi-ml-sanita]].

## Evidenze dalla Letteratura

### Panoramica degli algoritmi
- Il modulo elenca queste famiglie (Khuntia, 2024g):
  - **metodi statistici classici:** regressione logistica per il rischio di malattia, regressione lineare per esiti continui come la durata della degenza;
  - **sistemi a regole:** alberi decisionali e sistemi esperti, per esempio per scegliere tra imaging ed esami di laboratorio nel dolore toracico o per scegliere l'antibiotico;
  - **ML supervisionato:** random forest, SVM;
  - **ML non supervisionato:** *clustering*, per esempio di pazienti oncologici per profilo genetico;
  - **apprendimento per rinforzo:** dosaggio automatico dell'insulina;
  - **deep learning:** CNN per l'imaging, RNN per serie temporali da dispositivi indossabili;
  - **altri:** NLP basato su transformer per note cliniche e letteratura, algoritmi su grafi, reti bayesiane, algoritmi di ottimizzazione, sistemi di raccomandazione.
- Il ciclo comune è ingresso, elaborazione, uscita e raffinamento iterativo. Esempi applicativi:
  - la predizione del danno renale acuto con 48 ore di anticipo di DeepMind;
  - l'analisi genomica per terapie oncologiche di IBM Watson Health;
  - la gestione delle code;
  - il monitoraggio remoto dello scompenso (Khuntia, 2024g).
- Sfide citate:
  - opacità dei modelli complessi e IA spiegabile (XAI);
  - bias da dati non rappresentativi, con ricampionamento e *adversarial debiasing* come rimedi;
  - apprendimento federato per la privacy.
- Prospettive: calcolo quantistico, dati multi-omici, robotica (Khuntia, 2024g).
- Benefici attribuiti agli algoritmi:
  - risoluzione efficiente dei problemi;
  - decisioni basate sui dati attraverso il [[diad-framework|DIAD]];
  - medicina personalizzata;
  - predizione e passaggio a cure proattive;
  - efficienza operativa;
  - automazione di compiti ripetitivi: screening delle radiografie, documentazione con NLP, pratiche assicurative (Khuntia, 2024g).

### Regressione lineare
- Modella la relazione tra un esito continuo e i predittori. È apprezzata per l'interpretabilità: i coefficienti mostrano quanto pesa ogni fattore (Khuntia, 2024g). Esempi:
  - il peso della glicemia sui tempi di recupero post-operatorio;
  - la previsione degli accessi in pronto soccorso, con un aumento atteso del 30% nella stagione influenzale;
  - la durata della degenza nella polmonite;
  - il costo di una protesi d'anca;
  - la soddisfazione dei pazienti in funzione delle attese;
  - l'incidenza del diabete per reddito e accesso alle cure;
  - la valutazione pre-post di un nuovo protocollo.
- La guida in 10 passi (Khuntia, 2024g):
  - definire il problema e preparare i dati (pulizia, *feature engineering*, standardizzazione);
  - visualizzare le relazioni e controllare la multicollinearità;
  - dividere i dati 80/20 tra addestramento e test;
  - stimare il modello e valutarlo con R², residui, MSE e MAE;
  - interpretare i coefficienti con p-value e intervalli di confidenza;
  - testare, rifinire, mettere in produzione con monitoraggio e comunicare i risultati.

### Regressione logistica
- Stima la probabilità di un esito binario, tra 0 e 1, poi tradotta in classi. Esempi:
  - rischio cardiovascolare;
  - complicanze chirurgiche;
  - screening della depressione;
  - infezioni ospedaliere;
  - riammissione entro 30 giorni dopo scompenso;
  - rischio di focolai influenzali.
- Il modulo ne sottolinea l'interpretabilità: una probabilità del 78% di sviluppare diabete è facile da comunicare al paziente. Indica anche l'uso come base di sistemi di ML più complessi (Khuntia, 2024g).
- La guida in 11 passi (Khuntia, 2024g):
  - definire l'esito binario;
  - preparare i dati: pulizia, codifica *one-hot*, bilanciamento delle classi con sovra- o sottocampionamento o SMOTE;
  - esplorazione e correlazioni;
  - divisione 80/20 stratificata;
  - stima del modello;
  - valutazione con accuratezza, matrice di confusione, curva ROC e AUC, precisione e *recall*;
  - interpretazione con odds ratio e significatività;
  - ottimizzazione con selezione delle variabili, regolarizzazione L1/L2 e iperparametri in validazione incrociata;
  - test su dati mai visti, messa in produzione con monitoraggio, comunicazione.

### Errori e limiti della fonte
- **Regressione lineare per un esito binario:** il modulo propone la regressione lineare per stimare la probabilità di riammissione entro 30 giorni, che è un esito binario. Due pagine dopo indica correttamente la logistica per lo stesso problema.
- **Ordine dei passaggi e *data leakage*:** nella guida alla logistica il bilanciamento delle classi (passo 2) precede la divisione tra addestramento e test (passo 4). Jacobs et al. (2026) prescrivono di applicare SMOTE e le altre trasformazioni solo dentro il training set, per evitare che informazioni del test set entrino nell'addestramento. Vedi [[mccv-and-statistical-validation-clinical-ml]].
- **Divisione singola e accuratezza:** la guida usa un'unica divisione 80/20 e mette l'accuratezza come prima metrica. Su campioni piccoli e sbilanciati una singola divisione dà stime instabili e l'accuratezza è fuorviante. Jacobs et al. (2026) raccomandano validazione ripetuta e *balanced accuracy*.
- **Calibrazione:** per un modello che restituisce probabilità la valutazione non comprende la calibrazione, che TRIPOD+AI considera indispensabile (Collins et al., 2024). Vedi [[clinical-prediction-model-evaluation]].
- **Affermazioni senza fonte:** il monitoraggio della sepsi in terapia intensiva ridurrebbe «significativamente» la mortalità. IBM Watson Health è presentato come attivo, ma risulta ceduto da IBM nel 2022 [da verificare].
- **Refuso:** «ospedali ben forniti e sovraforniti» invece di «non sovraforniti».

## Riferimenti Bibliografici
- Collins, G. S., Moons, K. G. M., Dhiman, P., Riley, R. D., Beam, A. L., Van Calster, B., Ghassemi, M., Liu, X., Reitsma, J. B., van Smeden, M., Boulesteix, A.-L., Camaradou, J. C., Celi, L. A., Denaxas, S., Denniston, A. K., Glocker, B., Golub, R. M., Harvey, H., Heinze, G., . . . Logullo, P. (2024). TRIPOD+AI statement: Updated guidance for reporting clinical prediction models that use regression or machine learning methods. *BMJ*, *385*, Article e078378. https://doi.org/10.1136/bmj-2023-078378
- Jacobs, N., Voelkle, M. C., Kathmann, N., & Hilbert, K. (2026). Can we Improve Prediction of Psychotherapy Outcomes Through Pretraining With Simulated Data? *arXiv preprint arXiv:2601.06159v1 [stat.ML]*.
- Khuntia, J. (2024g). *Background materials for Course 2: The data to decision path for infusion of AI in healthcare. Module 3: AI and ML relevant algorithms in healthcare models* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/the-data-to-decision-path-for-infusion-of-ai-in-healthcare

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[algoritmi-ml-sanita]], [[mccv-and-statistical-validation-clinical-ml]], [[clinical-prediction-model-evaluation]], [[diad-framework]], [[ia-machine-learning-deep-learning]], [[ai-health-c2m2-khuntia-2024]]
