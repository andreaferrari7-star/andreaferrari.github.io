---
tags: [ai-health-coursera, formazione, apprendimento-supervisionato, classificazione, regressione, overfitting, paradigmi-di-apprendimento]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C3M1_JK_Dec28_2024_V1.0 (1) (1).pdf"]
---

# AI for Healthcare Systems, C3M1: algoritmi di ML rilevanti in sanità, parte 1 (Khuntia, 2024i)

## Definizione Operativa
- Materiale di approfondimento (26 pagine, versione 1.0 del 28 dicembre 2024) del primo modulo del corso 3 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]], *AI Integration in Healthcare*. Presenta i quattro paradigmi di apprendimento automatico (supervisionato, non supervisionato, semi-supervisionato, per rinforzo), approfondisce classificazione e regressione e spiega sottoadattamento e sovradattamento (Khuntia, 2024i).
- **Utilità CBT / Applicativa:** distinguere classificazione e regressione, e capire il sovradattamento, permette di valutare con senso critico uno studio che «predice» esiti terapeutici. Un modello che va benissimo sui dati di addestramento e male su quelli nuovi ha imparato il rumore, non la regola. Vedi [[ia-machine-learning-deep-learning]].

## Evidenze dalla Letteratura

### Dai sistemi a regole ai sistemi che apprendono
- Il modulo contrappone i sistemi a regole statiche, che falliscono con casi rari o dati ambigui, ai sistemi che apprendono dai dati e migliorano con l'esperienza. Restano però insostituibili gli elementi umani: empatia, giudizio, fiducia del paziente (Khuntia, 2024i).
- Ostacoli all'adozione (Khuntia, 2024i):
  - qualità e disponibilità dei dati, con poca rappresentatività delle popolazioni svantaggiate e conseguente bias;
  - opacità del deep learning;
  - difficoltà di integrazione con sistemi informatici datati;
  - scetticismo dei professionisti per accuratezza, perdita di controllo e posti di lavoro;
  - costi;
  - questioni di responsabilità, consenso ed equità, con una regolazione in ritardo;
  - deriva di accuratezza ed equità nel tempo;
  - fiducia del pubblico.
- Scegliere l'algoritmo adatto ai dati e al compito aiuta ad affrontare alcuni di questi ostacoli: modelli con vincoli di equità o strumenti di spiegazione riducono bias e opacità (Khuntia, 2024i).

### I quattro paradigmi
- I quattro paradigmi, ciascuno con i suoi esempi e le domande critiche che il modulo pone (Khuntia, 2024i):
  - **supervisionato:** dati etichettati, per esempio per predire l'aderenza alle terapie croniche. Domande: come standardizzare l'etichettatura tra istituzioni? Che ruolo può avere l'apprendimento federato?
  - **non supervisionato:** pattern in dati non etichettati, come sottogruppi oncologici per profilo genomico o flussi di pazienti. Domanda: come verificare che i pattern trovati corrispondano alla realtà clinica?
  - **semi-supervisionato:** pochi casi etichettati e molti non etichettati, per esempio per anticipare le infezioni ospedaliere. Domanda: come evitare che il bias delle poche etichette si propaghi?
  - **per rinforzo:** decisioni sequenziali con retroazione, come l'allocazione delle risorse in terapia intensiva o la chirurgia robotica. Domanda: come garantire la sicurezza nei casi limite rari e bilanciare autonomia dell'algoritmo e supervisione umana?
- Secondo il modulo i quattro paradigmi lavorano meglio insieme, come un'orchestra. Nell'esempio di una pandemia: diagnosi (supervisionato), mappa dei contagi (non supervisionato), dati incompleti (semi-supervisionato), logistica (rinforzo) (Khuntia, 2024i).

### Classificazione e regressione
- **Classificazione:** assegna una categoria (benigno o maligno, diabete sì o no, rischio basso, medio o alto). Gli algoritmi tipici sono regressione logistica, alberi, Naive Bayes e SVM; le metriche sono accuratezza, precisione, *recall* e F1. Esempi: triage dell'ictus in pronto soccorso, mammografia, riammissione a 30 giorni. Il modulo chiede come ridurre i falsi negativi nella diagnosi oncologica (Khuntia, 2024i).
- **Regressione:** stima un valore continuo (pressione, glicemia, degenza, posti letto in pandemia); le metriche sono R² e RMSE (Khuntia, 2024i). Varianti descritte:
  - lineare, per relazioni semplici e interpretabili;
  - logistica, per esiti binari;
  - lasso, che azzera i coefficienti poco utili e seleziona le variabili, utile in genomica;
  - «multivariata», con più predittori;
  - polinomiale, per relazioni non lineari come la crescita tumorale o la curva dose-effetto.
- Le due famiglie hanno in comune dati etichettati, preelaborazione, selezione delle variabili e ottimizzazione. Differiscono nell'output e nei problemi tipici: lo sbilanciamento delle classi nella classificazione, la multicollinearità nella regressione. Spesso si usano insieme, per esempio per il rischio di complicanze (sì/no) e la gravità (continua) nel diabete (Khuntia, 2024i).

### Sottoadattamento e sovradattamento
- **Sottoadattamento:** il modello è troppo semplice (alto bias), con errori alti sia in addestramento sia in validazione.
- **Adattamento ottimale:** errori bassi e simili sui due insiemi.
- **Sovradattamento:** il modello memorizza rumore e casi anomali (alta varianza), con errore di addestramento quasi nullo ed errore di validazione che cresce.
- Il modulo lo illustra con confini di decisione (logistica sottoadattata, SVM con kernel RBF ottimale, albero di profondità 10 sovradattato) e curve di perdita. I rimedi indicati sono validazione incrociata, regolarizzazione (dropout, L1/L2), arresto anticipato e regolazione degli iperparametri (Khuntia, 2024i).

### Errori e limiti della fonte
- **Traccia di generazione automatica:** a pagina 19 il testo contiene una frase rivolta all'utente di un assistente conversazionale: «Let me know if you'd like detailed diagrams for specific examples!». Parti della dispensa sembrano quindi generate con un'IA generativa e non revisionate. È un motivo in più per verificare ogni affermazione su fonti primarie.
- **Terminologia:** la «regressione multivariata» è descritta come modello con più predittori, cosa che di solito si chiama regressione multipla; il termine multivariata indica più esiti [da verificare]. Tra gli esempi torna la predizione della riammissione, un esito binario, con un modello di regressione.
- **Semplificazioni:** la classificazione è associata alla diagnosi e la regressione alla prognosi, ma molti modelli prognostici sono classificatori binari. L'apprendimento per rinforzo è detto capace di decisioni «interpretabili» senza spiegazioni. La relazione lineare tra tassi di vaccinazione e ricoveri è affermata senza dati.
- **Bilanciamento delle classi:** il modulo afferma che nella classificazione è «cruciale» una rappresentazione uguale delle classi. La letteratura raccolta nella wiki tratta lo sbilanciamento con metriche adatte (*balanced accuracy*) e con il ricampionamento confinato al training set, non imponendo classi uguali (Jacobs et al., 2026). Vedi [[mccv-and-statistical-validation-clinical-ml]].

## Riferimenti Bibliografici
- Jacobs, N., Voelkle, M. C., Kathmann, N., & Hilbert, K. (2026). Can we Improve Prediction of Psychotherapy Outcomes Through Pretraining With Simulated Data? *arXiv preprint arXiv:2601.06159v1 [stat.ML]*.
- Khuntia, J. (2024i). *Background materials for Course 3: AI integration in healthcare. Module 1: Relevant ML algorithms in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[ia-machine-learning-deep-learning]], [[algoritmi-ml-sanita]], [[mccv-and-statistical-validation-clinical-ml]], [[ai-health-c2m3-khuntia-2024]], [[ai-health-c2m4-khuntia-2024]]
