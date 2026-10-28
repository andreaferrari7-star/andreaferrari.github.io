---
tags: [ai-health-coursera, formazione, apprendimento-non-supervisionato, clustering, knn, semi-supervisionato, reinforcement-learning, anomaly-detection]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C3M2_JK_Dec28_2024_V1.0 pdf  (1).pdf"]
---

# AI for Healthcare Systems, C3M2: algoritmi di ML rilevanti in sanità, parte 2 (Khuntia, 2024j)

## Definizione Operativa
- Materiale di approfondimento (37 pagine, versione 1.0 del 28 dicembre 2024) del secondo modulo del corso 3 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]]; le intestazioni lo chiamano per errore «Module 1». Completa la rassegna dei paradigmi di apprendimento con le tecniche non supervisionate, il k-NN, i metodi semi-supervisionati e l'apprendimento per rinforzo, ciascuno con scenari sanitari e diagrammi illustrativi (Khuntia, 2024j).
- **Utilità CBT / Applicativa:** il *clustering* dei pazienti per gravità e risposta al trattamento e la riduzione di dimensionalità (PCA, ICA per l'EEG) sono tecniche usate anche nella ricerca in psicoterapia. Il modulo serve anche come esempio da evitare: presenta le associazioni trovate nei dati come se indicassero quali trattamenti prescrivere. Vedi [[algoritmi-ml-sanita]].

## Evidenze dalla Letteratura

### Apprendimento non supervisionato
- Il modulo descrive quattro famiglie di tecniche (Khuntia, 2024j):
  - ***clustering*:** raggruppa pazienti con andamento o risposta simili. Il K-means trova gruppi attorno a centri; il DBSCAN trova gruppi di forma qualsiasi e isola il rumore, con l'esempio dei focolai di COVID-19 e dei lockdown locali;
  - **riduzione di dimensionalità:** la PCA riassume molte variabili in poche componenti che spiegano la varianza, per esempio nell'espressione genica; l'ICA separa sorgenti indipendenti, per esempio l'attività cerebrale dal rumore nell'EEG dell'epilessia;
  - **regole di associazione:** Apriori e FP-Growth trovano elementi che compaiono spesso insieme, come farmaci co-prescritti per gestire la politerapia o combinazioni di sintomi nelle malattie rare;
  - **rilevazione di anomalie:** lo z-score individua valori di glicemia anomali, l'Isolation Forest le richieste di rimborso fraudolente, e ci sono i picchi nei parametri vitali. Serve un equilibrio tra sensibilità e specificità per non sommergere i clinici di falsi allarmi.
- Le sfide indicate sono l'interpretabilità, perché i gruppi trovati vanno validati da esperti del dominio, la privacy e il bias (Khuntia, 2024j).

### k-Nearest Neighbors (k-NN)
- Il k-NN predice per vicinanza: classifica un nuovo caso con il voto dei k casi più simili, o ne stima il valore come media dei vicini, eventualmente pesata per distanza. Non costruisce un modello esplicito. Un k piccolo rischia il sovradattamento, uno grande appiattisce le stime (Khuntia, 2024j).
- Esempi: rischio di diabete, tempi di recupero post-operatori, glicemia in un'app personale, imaging, risposta ai farmaci, categorie di rischio in terapia intensiva, attività da dispositivi indossabili, focolai di dengue o COVID-19 (Khuntia, 2024j).
- Limiti: costo di calcolo su grandi dataset, «maledizione della dimensionalità», sensibilità alla scala delle variabili, al rumore e allo sbilanciamento delle classi, consumo di memoria (Khuntia, 2024j).

### Apprendimento semi-supervisionato
- Il modulo descrive quattro tecniche (Khuntia, 2024j):
  - **self-training:** il modello etichetta i dati non etichettati e usa le proprie predizioni più sicure per migliorarsi, per esempio sulle radiografie del torace. Il rischio è che gli errori iniziali si propaghino; il rimedio sono soglie di confidenza;
  - **co-training:** due modelli addestrati su viste diverse dei dati si etichettano a vicenda, per esempio esami di laboratorio e immagini. Funziona se le viste sono abbastanza indipendenti;
  - **metodi su grafo:** le etichette si propagano lungo le relazioni tra casi, per esempio nelle interazioni farmaco-proteina;
  - **modelli generativi:** VAE e GAN producono dati sintetici, come immagini di risonanza, per malattie rare o fasi precoci. La loro utilità dipende dal realismo dei dati generati.

### Apprendimento per rinforzo
- Un agente osserva uno stato, sceglie un'azione, riceve una ricompensa e aggiorna la propria strategia (*policy*). Nell'esempio guida osserva la glicemia, sceglie la dose di insulina e riceve come ricompensa la stabilità glicemica (Khuntia, 2024j).
- **Senza modello (*model-free*):** ottimizzazione della policy, applicata a chirurgia robotica e angoli dei fasci in radioterapia, e Q-learning, applicato ad agende ambulatoriali e dimissioni dalla terapia intensiva.
- **Con modello (*model-based*):** il modello dell'ambiente può essere appreso (risposta tumorale alla radioterapia, progressione del Parkinson) o dato in partenza (dosaggio antibiotico nella sepsi, risorse del pronto soccorso). Gli scenari illustrati sono l'insulina, la ventilazione meccanica e la radioterapia (Khuntia, 2024j).
- Le sfide etiche indicate sono trasparenza delle decisioni, equità rispetto ai gruppi poco rappresentati nei dati e responsabilità in caso di errore. Diventano critiche quando l'agente regola un ventilatore o suggerisce terapie per la sepsi (Khuntia, 2024j).

### Errori e limiti della fonte
- **Associazione scambiata per causalità:** le regole di associazione che legano «Farmaco A» a «miglioramento della glicemia» o «minor rischio di ictus» sono presentate come guida per raccomandare combinazioni di farmaci. Una co-occorrenza nei dati osservazionali non prova l'efficacia: può riflettere indicazioni, selezione dei pazienti o fattori confondenti. Lo stesso vale per l'associazione tra esercizio e salute cardiaca usata per suggerire piani di trattamento.
- **Applicazioni senza fonti:** l'apprendimento per rinforzo è presentato come già applicato in chirurgia robotica, radioterapia, sepsi e ventilazione, senza citare studi né distinguere tra simulazioni, ricerca e uso clinico [da verificare]. L'esempio della radioterapia per l'artrite è inusuale e non è accompagnato da spiegazioni.
- **Soglie arbitrarie:** nell'esempio del monitoraggio cardiaco il range «normale» è fissato a 55-85 battiti al minuto, più stretto dei riferimenti abituali per la frequenza a riposo [da verificare].
- **Incoerenza:** il k-NN è definito prima «interpretabile», poi poco interpretabile per la dipendenza dall'intero dataset.
- Il modulo non ha riferimenti bibliografici e gli scenari sono simulati.

## Riferimenti Bibliografici
- Khuntia, J. (2024j). *Background materials for Course 3: AI integration in healthcare. Module 2: Relevant ML algorithms in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[algoritmi-ml-sanita]], [[ia-machine-learning-deep-learning]], [[llm-assisted-clustering]], [[context-aware-adaptive-nudging]], [[synthetic-clinical-dialogues]], [[ai-health-c3m1-khuntia-2024]]
