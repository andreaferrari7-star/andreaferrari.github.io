# Riunione 05-11: Discussione del Gruppo di Ricerca su AI e Psicoterapia

**Summary**: Sintesi dell'incontro del gruppo di ricerca incentrato su architettura e versioning di agenti didattici CBT (Libet Prime), transizione verso il co-ragionamento Human-in-the-Reasoning, simulazione clinica dei bias nei pazienti virtuali, sfide etico-deontologiche e progetti di digitalizzazione clinica su larga scala (SaMD e protocollo Not-On-Track nel NHS).
**Sources**: 05-11 Discussione del Gruppo di Ricerca su AI e Psicoterapia.txt
**Last updated**: 2026-08-27
---

## 1. Aggiornamenti ed Esperienze di Ricerca
- **Premio di Ricerca su AI (Sapienza / Cattolica / Digital)**: Discussione sull'esperienza e presentazione di un lavoro di ricerca basato sull'analisi qualitativa di testi clinici processati con modelli generativi ([[large-language-models]]).
- **Necessità di Dialogo Interdisciplinare**: Evidenziata l'importanza dell'integrazione tra la prospettiva clinico-umanistica e il mondo ingegneristico per evitare sia l'allarmismo difensivo/politico, sia derive tecnocratiche prive di fondamento psicologico.

---

## 2. Architettura di Agenti Didattici CBT: [[libet-prime-agenti-didattici|Libet Prime]]
- **Infrastruttura e Accessibilità Didattica**: Progettazione di un Gem su Google Workspace Education integrato con Google Classroom per gli allievi di Studi Cognitivi, consentendo un accesso selettivo per classi a costo zero (senza tariffazione API a consumo per singolo studente).
- **Prompt Master a 5 Modalità Operative**:
  1. *Spiegazione teorica*: Approfondimento concettuale e teorico del modello clinico LIBET.
  2. *Confronto e distinzione*: Differenziazione nosografica e concettuale tra quadri clinici e meccanismi di mantenimento.
  3. *Vignetta clinica e formulazione*: Lettura di trascritti e concettualizzazione del caso.
  4. *Intervento razionale*: Suggerimenti operativi e razionale delle tecniche di intervento.
  5. *Interrogazione / Autovalutazione*: Modalità di testing interattivo per lo studente.
- **Knowledge Base Modulare (26 Capitoli)**:
  - Strutturazione ad hoc di una Knowledge Base dedicata, redatta e raffinata iterativamente tramite modelli LLM (ChatGPT e Claude) con supervisione clinica diretta.
  - Principi epistemologici incorporati: precedenza dei dati osservativi sulle ipotesi inferenziali, analisi clinica a partire dai cicli sintomatici, centralità della dialettica dei bisogni, esplicitazione dei limiti inferenziali del modello.
- **Evoluzione verso un Agente Socratico**:
  - Superamento della correzione passiva e nozionistica.
  - Transizione verso un modello maieutico che pone domande guida allo studente, sollecitando il pensiero critico e la riflessione metacognitiva sul caso.

---

## 3. Fenomenologia del *Prompt Regression* e Best Practice di Versioning
- **Rischio di *Over-constraining***: Nel passaggio da *Libet Prime 1.0* a *1.1*, l'accumulo sequenziale di vincoli, gerarchie e regole ha causato un collo di bottiglia (*bottleneck*), appiattendo l'agente su schemi di risposta rigidi e meccanici.
- **Dinamica Attentiva e Pesi Gerarchici**: Gli LLM non apprendono per semplice accumulo cumulativo, ma ridefiniscono le priorità contestuali assegnando un peso gerarchico sproporzionato alle clausole introdotte in coda.
- **Isolamento delle Versioni**: Per perfezionare un agente clinico è preferibile sviluppare un'istanza pulita da zero (*clean agent*) e condurre test comparativi controllati (A/B testing) piuttosto che sovrascrivere iterativamente prompt complessi.

---

## 4. Prompting Avanzato e [[simulazione-pazienti-ai]]
- **Standard di Trasparenza**: Utilizzo di linee guida e standard metodologici (es. framework TRIPOD) per definire chiaramente il contesto e i vincoli operativi dei prompt clinici.
- **Calibrazione dei Livelli di Astrazione**: Necessità di esplicitare nei prompt se l'agente deve limitarsi a descrivere dati fattuali, interpretare fenomeni o condurre inferenze causali.
- **Modellizzazione dei Bias Cognitivi**: Nella simulazione di pazienti virtuali per il training degli specializzandi, è fondamentale esplicitare le euristiche disfunzionali (es. pensiero dicotomico, catastrofizzazione, pattern di compliance/resistenza nell'alleanza) per evitare simulazioni stereotipate o meramente sintomatiche.

---

## 5. Transizione verso lo [[human-in-the-reasoning]]
- **Superamento dello Human-in-the-Loop**: La validazione passiva a posteriori (*Human-in-the-Loop*) espone a rischi di deregolamentazione etica (*moral crumple zone*) e acquiescenza acritica (*automation bias*).
- **Competenza Metacognitiva**: Il terapeuta deve apprendere come "ragiona" l'algoritmo, decodificando la natura probabilistica della black-box e guidando congiuntamente l'albero logico-inferenziale.

---

## 6. Deontologia, Privacy e Bias nei Modelli Linguistici
- **Tutela della Privacy e Dati Ipersensibili**: Rischi legati all'immissione non protetta di dati clinici (es. foto di schede ABC o note anamnestiche); necessità di protocolli rigorosi di anonimizzazione, soprattutto per dati ipersensibili (orientamento sessuale, dinamiche relazionali).
- **Bias Sistematici negli LLM**: Presenza di bias impliciti nella valutazione clinica (es. tendenza dei modelli ad attribuire gravità maggiore a vignette cliniche borderline associate a soggetti femminili rispetto a profili maschili).
- **Governance e Buone Pratiche**: Superamento delle posizioni meramente allarmistiche attraverso la formazione all'interazione etica e consapevole.

---

## 7. Ricerca Clinica su Larga Scala e [[software-as-a-medical-device-salute-mentale|SaMD]]
- **Progetto NHS / NIHR (Prof. Delgadillo - Mindlive)**:
  - Analisi del bando di ricerca britannico (oltre 2 milioni di sterline) per integrare sistemi di IA nei servizi Talking Therapies (ex IAPT) dell'NHS.
  - Obiettivi clinici: incremento dell'efficacia terapeutica del 10% per ansia e depressione e abbattimento dei tassi di abbandono (*dropout*).
- **Digitalizzazione del Protocollo *Not-On-Track* (CTS)**:
  - Monitoraggio continuo lungo l'intero iter terapeutico (pre-screening, assessment multimodale, processo).
  - Identificazione precoce dei pazienti che deviano dalle traiettorie positive attese e supporto guidato a terapeuta e paziente nell'applicazione di protocolli di riparazione clinica.
- **Complessità Regolatoria SaMD**:
  - Requisiti stringenti per la certificazione FDA / Medical Device Regulation (MDR).
  - Necessità di Trial Controllati Randomizzati (RCT) e valutazioni in cieco su popolazioni rappresentative.

---

## 8. Linee Guida per la Formazione dei Terapeuti
Proposta di strutturazione di un microcorso formativo (FAD) focalizzato su tre direttrici:
1. *Come funzionano gli LLM*: Architettura, euristiche e limiti del ragionamento computazionale.
2. *Come si costruiscono*: Ingegnerizzazione dei prompt, strutturazione modulare della knowledge base e validazione clinica.
3. *Come si interrogano e si utilizzano*: Prompting socratico, gestione dei bias e conformità etico-deontologica.

---

## Related pages
- [[libet-prime-agenti-didattici]]
- [[software-as-a-medical-device-salute-mentale]]
- [[human-in-the-reasoning]]
- [[simulazione-pazienti-ai]]
- [[large-language-models]]
- [[prompting-in-psychology]]
- [[ai-research-ethics]]
- [[05-08_Riunione_Knowledge_Base]]
