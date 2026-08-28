# Riunione 07-10: Test e Valutazione di Libet Prime, Trainer Simulator e Piano Operativo

**Summary**: Sintesi della riunione operativa di presentazione e avvio del test pilota di "Libet Prime" (v1.2), introduzione dell'agente "Trainer Simulator" (v0.2), protocollo di sperimentazione strutturato su piattaforma Gemini per i responsabili di sede/didatti di Studi Cognitivi e considerazioni pedagogico-etiche sul co-ragionamento maieutico.
**Sources**: `07-10 Riunione_ Test e Valutazione di “Libet Prime” (Tutor AI per Libet_CBT), Trainer Simulator e Piano Operativo.txt`
**Last updated**: 2026-08-27
---

## Sintesi dei Contenuti

### 1. Visione Generale e Sperimentazione Didattica
- **Integrazione prudente dell'IA**: L'iniziativa condotta in SC Formazione (Studi Cognitivi) si propone di esplorare l'adozione dell'intelligenza artificiale generica e specializzata all'interno dell'iter formativo degli specializzandi in psicoterapia cognitivo-comportamentale, procedendo in modo cauto, modulare e verificabile.
- **Infrastruttura Google for Education e Gemini**: Utilizzo dell'ecosistema istituzionale (Google Classroom / Gemini Gems) per fornire accesso sicuro, standardizzato e scalabile a docenti e allievi senza costi aggiuntivi di infrastruttura.
- **Target formativo prioritario**: Focus iniziale sulle competenze di base degli allievi dei primi due anni (comprensione e discriminazione dei costrutti psicopatologici, formulazione del caso, razionale di intervento e prudenza diagnostico-esplicativa).

---

### 2. [[libet-prime|Libet Prime]]: Architettura e Funzionamento (v1.2)
- **Definizione e natura dell'agente**: Gem di Gemini ideato come *tutor clinico-didattico* sul modello LIBET (*Life Themes and Plans in CBT*).
- **Cosa NON è**: Non è un terapeuta, né un supervisore, né un oracolo infallibile, né uno strumento per fare diagnosi automatiche o un'assistenza diretta alla psicoterapia reale.
- **Comportamento differenziato (Bimodale)**:
  - *Sui contenuti teorici e concettuali*: Fornisce risposte scolastiche, accurate, nette e puntuali, discriminando costrutti affini o nomenclature sovrapposte.
  - *Sul materiale clinico e vignette*: Assume una postura dialogica, maieutica e prudente. Non rilascia risposte chiuse o direttive; pone domande di riflessione, suggerisce ipotesi alternative e stimola l'allievo ad argomentare il razionale clinico.
- **Architettura a Macro-Prompt e 5 Modalità con Routing**:
  1. *Spiegazione teorica* dei concetti del modello LIBET.
  2. *Confronto e distinzione* tra costrutti psicopatologici e clinici.
  3. *Formulazione del caso* e ragionamento guidato su vignette cliniche.
  4. *Impostazione del razionale di intervento* e ipotesi tattiche di trattamento.
  5. *Interrogazione maieutica* attiva (l'agente interroga l'allievo e valuta le risposte).
- **Knowledge Base di riferimento**: Corpus strutturato di 33 capitoli e 230 pagine, redatto e ottimizzato specificamente per massimizzare la fedeltà teorica del modello di linguaggio.

---

### 3. [[trainer-simulator|Trainer Simulator]]: Simulatore di Pazienti Virtuali (v0.2)
- **Scopo e posizionamento**: Secondo agente in fase di sviluppo (Interview Trainer) finalizzato alla pratica esperienziale e alla simulazione del colloquio clinico.
- **Perimetro di addestramento**: Dalla fase iniziale di assessment alla formulazione del caso condivisa (ABC, ABC Libet e restituzione).
- **Caratteristiche funzionali**:
  - *Libreria clinica*: Pacchetto iniziale di 10 pazienti simulati con quadri sintomatologici e profili differenti.
  - *3 Livelli di difficoltà*: Base, intermedio, avanzato (con variazione di vaghezza dell'eloquio, resistenze e difese).
  - *Comandi operativi*: Gestione interattiva tramite comandi dedicati (`inizia`, `pausa`, `indizio`, `riformula`, `feedback`).
  - *Valutazione e Feedback*: Rubric finale automatizzata per l'analisi delle competenze cliniche mostrate dal terapeuta in formazione.

---

### 4. [[testing-e-validazione-agenti-didattici|Protocollo Operativo di Test]] e Roadmap
- **Campione di tester**: Responsabili di sede, didatti storici della scuola e figure junior selezionate per sensibilità tecnica o clinica.
- **Cronoprogramma**:
  - *Luglio - Agosto*: Fase di sperimentazione individuale su Gemini.
  - *25 Luglio*: Rilascio della survey strutturata con upload degli script di dialogo.
  - *25 Agosto*: Chiusura della raccolta dati.
  - *Fine Agosto / Settembre*: Focus group di restituzione qualitativa e progettazione della versione 1.3.
- **Protocollo di prova**:
  - Test di almeno 3–5 turni di conversazione per ciascuna delle 5 modalità operative.
  - Test di robustezza e rifiuto delle richieste fuori dominio (*out-of-domain*).
  - Tracciamento sistematico di prompt, output, allucinazioni, vaghezze, diagnosi indebite o anticipazioni inappropriate di tecniche.
- **Prevenzione delle regressioni algoritmiche**: Riutilizzo di script standardizzati per garantire che i perfezionamenti del prompt non degradino le capacità di ragionamento precedentemente acquisite.

---

### 5. [[ia-maieutica-e-co-ragionamento|Implicazioni Pedagogiche, Psicologiche ed Etiche]]
- **Dal paradigma della scorciatoia al prolungamento della riflessione**: Contrastare la tendenza a usare l'IA come generatore passivo di risposte rapide; strutturare l'interazione affinché imponga uno sforzo metacognitivo e allunghi il tempo di ragionamento dell'allievo.
- **Gestione dei Bias e dell'Over-Confidence**:
  - *Over-confidence / Effetto Oracolo*: Rischio che l'allievo accetti acriticamente le risposte dell'IA.
  - *Rigidità / Bias di conferma del clinico esperto*: Rischio che il didatta respinga indicazioni valide dell'IA solo perché disallineate dalle proprie abitudini interpretative.
- **Etica e Deontologia**: Preservazione integrale della responsabilità clinica del terapeuta, coerenza con i principi di trasparenza epistemica e co-ragionamento (*Human-in-the-reasoning*).

---

## Related pages
- [[libet-prime]]
- [[trainer-simulator]]
- [[testing-e-validazione-agenti-didattici]]
- [[ia-maieutica-e-co-ragionamento]]
- [[human-in-the-reasoning]]
- [[simulazione-pazienti-ai]]
- [[05-08_Riunione_Knowledge_Base]]
- [[04-20_Tavola_rotonda_Integrazione_IA]]
