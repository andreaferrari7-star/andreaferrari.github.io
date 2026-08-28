# Sintesi Riunione: Discussione del Gruppo di Ricerca su AI e Psicoterapia (05-11)

**Summary**: Sintesi approfondita della discussione del gruppo di ricerca su intelligenza artificiale e psicoterapia, incentrata sullo sviluppo e versioning di agenti didattici (Libet Prime), transizione verso lo Human-in-the-Reasoning, tecniche di prompt engineering per la simulazione clinica di pazienti, sfide etiche/deontologiche (bias e privacy) e progetti di ricerca su larga scala per la digitalizzazione clinica (SaMD e protocollo Not-On-Track nel NHS).
**Sources**: `05-11 Discussione del Gruppo di Ricerca su AI e Psicoterapia.txt`
**Last updated**: 2026-08-27
---

## 1. Aggiornamenti ed Esperienze di Ricerca
- **Premio di Ricerca su AI (Sapienza / Cattolica / Digital)**: Presentazione del lavoro di ricerca basato sull'analisi qualitativa di testi clinici generati/analizzati con ChatGPT.
- Riconoscimento dell'importanza del dialogo interdisciplinare tra mondo clinico/umanistico e ingegneristico, evidenziando la necessità di integrare competenze psicologiche nella progettazione degli strumenti computazionali.

---

## 2. Architettura di Agenti Didattici CBT: Il Progetto *Libet Prime*
- **Infrastruttura e Accessibilità**: Sviluppo di un Gem su Google Workspace Education integrato con Google Classroom per gli allievi della scuola di specializzazione (Studi Cognitivi), consentendo una distribuzione selettiva e controllata senza costi aggiuntivi di consumo API per singolo studente.
- **Struttura del Prompt e Modalità di Risposta**: Il master prompt è progettato per orchestrare cinque modalità operative specifiche in base alla richiesta dell'utente:
  1. *Spiegazione teorica*: Approfondimento dei costrutti concettuali del modello LIBET.
  2. *Confronto e distinzione*: Differenziazione tra concetti clinici e quadri psicopatologici.
  3. *Vignetta clinica e formulazione*: Guida alla lettura e concettualizzazione del caso.
  4. *Intervento razionale*: Suggerimenti procedurali e operativi per la pianificazione terapeutica.
  5. *Interrogazione / Correzione risposta*: Modalità di testing e autovalutazione dello studente.
- **Knowledge Base Modulare (26 Capitoli)**:
  - Strutturazione di una Knowledge Base dedicata, redatta e raffinata iterativamente tramite modelli LLM (ChatGPT e Claude) e supervisione clinica diretta.
  - Regole e principi epistemologici integrati: precedenza dei dati fattuali sulle inferenze, analisi a partire dai cicli sintomatici, centralità della dialettica dei bisogni, esplicitazione dei limiti inferenziali dell'agente.
  - Mappatura trasversale e interconnessione modulare tra capitoli.
- **Evoluzione verso un Agente Socratico**:
  - Necessità di superare la mera erogazione passiva di risposte o correzioni dirette.
  - Implementazione di logiche maieutiche che pongono domande guida allo studente, stimolando il ragionamento clinico e il pensiero critico.

---

## 3. Fenomenologia del *Prompt Regression* e Best Practice di Versioning
- **Problematica dell'*Over-constraining***: Nel passaggio dalla versione 1.0 alla 1.1 di Libet Prime, l'aggiunta cumulativa di regole, vincoli e gerarchie di istruzioni ha prodotto un collo di bottiglia (*bottleneck*), rendendo l'agente iper-rigido, meccanico e appiattito su scalette predeterminate.
- **Logica Gerarchica e Attenzione degli LLM**: Gli LLM non processano le istruzioni per semplice accumulo, ma riordinano le priorità attentive assegnando un peso sproporzionato alle nuove clausole aggiunte in coda.
- **Strategia di Sviluppo**: Risulta più efficace e sicuro creare una nuova istanza pulita da zero (*clean agent*) e confrontare le versioni (A/B testing) piuttosto che sovrascrivere o appesantire progressivamente un prompt esistente.

---

## 4. Prompt Engineering e [[simulazione-pazienti-ai]]
- **Standard Scientifici e Trasparenza**: Riferimento a framework metodologici e linee guida di trasparenza (es. standard TRIPOD adattati ai modelli generativi) per contestualizzare l'interazione clinica.
- **Calibrazione del Livello di Astrazione**: Necessità di specificare esplicitamente nel prompt il livello cognitivo richiesto al modello (descrizione fattuale, interpretazione clinica, inferenza causale).
- **Modellizzazione dei Bias Cognitivi nei Pazienti Virtuali**:
  - Per evitare simulazioni cliniche stereotipate, superficiali o puramente sintomatiche, è essenziale definire nel prompt gli specifici pattern di ragionamento disfunzionale del paziente (es. pensiero dicotomico, catastrofizzazione, dinamiche di compliance/resistenza nell'alleanza terapeutica).

---

## 5. [[human-in-the-reasoning]]: Dal Controllo Passivo alla Co-Costruzione
- **Oltre lo Human-in-the-Loop**: La classica supervisione operativa a posteriori (*Human-in-the-Loop*) è insufficiente e rischia di generare deresponsabilizzazione (*moral crumple zone*) o accettazione acritica (*automation bias*).
- **Comprensione Metacognitiva del Modello**: Il clinico deve acquisire la capacità di comprendere come "ragiona" il modello, i suoi pesi inferenziali, le sue allucinazioni e i suoi limiti strutturali (natura di scatola nera probabilistica e simulazione del ragionamento step-by-step).

---

## 6. Etica, Privacy e Deontologia nell'Uso Clinico
- **Protezione dei Dati e Anonimizzazione**: Rischi associati al caricamento non autorizzato di materiale clinico (trascrizioni, foto di schede ABC, dettagli anamnestici). Necessità di una rigorosa de-identificazione, con particolare attenzione ai dati ipersensibili (es. orientamento sessuale).
- **Bias di Genere e Diagnostici negli LLM**: Evidenze di bias impliciti nei modelli (es. tendenza ad attribuire un grado di gravità clinica significativamente maggiore a vignette descrittive di disturbo borderline associate a pazienti donne rispetto a pazienti uomini).
- **Superamento dell'Allarmismo Difensivo**: Superamento delle posizioni meramente difensive/allarmistiche attraverso la definizione di linee guida operative e buone pratiche contestuali.

---

## 7. Ricerca Clinica su Larga Scala e Regolamentazione SaMD
- **Progetto NHS / NIHR (Prof. Delgadillo - Mindlight)**:
  - Revisione di un progetto da oltre 2 milioni di sterline per integrare l'IA nei servizi sanitari inglesi (Talking Therapies / NHS).
  - Obiettivo clinico: incrementare del 10% l'efficacia dei trattamenti per ansia e depressione e ridurre significativamente i tassi di abbandono (*dropout*).
- **Digitalizzazione del Protocollo *Not-On-Track* (CTS)**:
  - Rilevazione algoritmica precoce dei pazienti che deviano dalla traiettoria di miglioramento clinico attesa.
  - Guida semi-automatizzata per terapeuta e paziente nell'applicazione di protocolli clinici complessi di recupero.
- **Requisiti Software as a Medical Device (SaMD)**:
  - Complessità delle validazioni cliniche e trial controllati randomizzati (RCT) in cieco su popolazioni rappresentative per ottenere le certificazioni regolatorie (FDA / normative europee).

---

## 8. Piano Formativo per Terapeuti
Definizione di un percorso formativo/microcorso articolato su tre pilastri:
1. **Come funzionano e sono architettati gli LLM**: Caratteristiche del ragionamento computazionale, limiti e bias.
2. **Come si costruiscono**: Architettura modulare dei prompt, knowledge base dedicate e modellizzazione clinica.
3. **Come si interrogano e si utilizzano**: Prompting avanzato, approccio socratico, deontologia e tutela della privacy.

---

## Related pages
- [[human-in-the-reasoning]]
- [[simulazione-pazienti-ai]]
- [[libet-prime-agenti-didattici]]
- [[software-as-a-medical-device-salute-mentale]]
- [[etica-privacy-bias-ia-clinica]]
- [[large-language-models]]
- [[prompting-in-psychology]]
- [[ai-research-ethics]]
