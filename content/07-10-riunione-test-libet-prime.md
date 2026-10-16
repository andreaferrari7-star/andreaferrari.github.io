---
tags: []
tipo_fonte: interna
data: 2026-07-10
source_papers: ["07-10 Riunione_ Test e Valutazione di “Libet Prime” (Tutor AI per Libet_CBT), Trainer Simulator e Piano Operativo.txt"]
---

# Riunione 07-10: Test e Valutazione di Libet Prime, Trainer Simulator e Piano Operativo

## Sintesi
Riunione operativa di presentazione e avvio del test pilota di "Libet Prime" (v1.2), introduzione dell'agente "Trainer Simulator" (v0.2), protocollo di sperimentazione strutturato su piattaforma Gemini per i responsabili di sede e didatti di Studi Cognitivi, e discussione pedagogico-etica sul co-ragionamento maieutico.

### Quadro Generale e Contesto Didattico
Il 10 luglio 2026 si è tenuta la riunione plenaria di presentazione e avvio della sperimentazione operativa dei primi agenti intelligenti sviluppati per la rete di scuole di psicoterapia *Studi Cognitivi* (SC Formazione), coordinata da Gabriele Caselli (co-autore del modello LIBET) con il gruppo di lavoro su IA e psicoterapia (Andrea Ferrari, Erika, Matilde Boattini).

Obiettivo dell'iniziativa è introdurre l'intelligenza artificiale nei percorsi di specializzazione in modo cauto, modulare e verificabile, partendo da prototipi controllati integrati nell'ecosistema istituzionale **Google for Education / Gemini** (Google Classroom e Gem condivisi), accessibili a docenti e allievi senza costi aggiuntivi di infrastruttura.

Il focus primario riguarda le competenze di base degli allievi dei primi due anni:
- Comprensione approfondita e discriminazione dei costrutti psicopatologici e teorici.
- Collegamento rigoroso tra formulazione del caso e razionale degli interventi.
- Sviluppo del ragionamento clinico prudente e ipotetico, evitando approssimazioni ed etichettature premature.

### 1. [[libet-prime]]: Tutor Clinico-Didattico (v1.2)

**Libet Prime** è un Gem di Gemini sviluppato come tutor didattico specializzato sul modello **LIBET** (*Life Themes and Plans in CBT*) e sulle terapie cognitivo-comportamentali.

#### Identità e Perimetro (Guardrails)
- **Cosa fa**: Chiarisce costrutti teorici, discrimina nomenclature sovrapposte o ambigue tra modelli cognitivisti, supporta l'analisi di vignette cliniche, corregge formulazioni e allena a costruire un razionale d'intervento.
- **Cosa NON è**: Non è un terapeuta, né un supervisore clinico, né un motore diagnostico, né un oracolo o un assistente generico (stile ChatGPT).
- **Tenuta dei confini (*Boundary Enforcement*)**: Rifiuto categorico di richieste cliniche dirette o fuori dominio (*out-of-domain*).

#### Postura Bimodale
1. **Sui contenuti teorici e costrutti**: Fornisce risposte scolastiche dirette, puntuali e rigorose, corredate da esempi clinici standard ed errori tipici di comprensione.
2. **Sul materiale clinico e vignette**: Assume una postura dialogica, socratica e maieutica. Non fornisce risposte chiuse né "verità" preconfezionate, ma stimola l'allievo attraverso domande di rilancio e contro-ipotesi, allungando il processo riflessivo anziché offrire scorciatoie cognitive.

#### Architettura e 5 Modalità Operative con Routing Dinamico
L'agente si basa su un macro-prompt strutturato che governa 5 modalità operative mediante un motore di routing:
1. *Spiegazione teorica* dei concetti del modello LIBET.
2. *Confronto e distinzione* tra costrutti psicopatologici e teorici.
3. *Ragionamento sulla formulazione* e analisi di vignette cliniche.
4. *Impostazione del razionale di trattamento* e ipotesi d'intervento.
5. *Interrogazione attiva* (l'agente interroga l'allievo per testarne la comprensione).

#### Knowledge Base e Versioning
- **Knowledge Base proprietaria**: Corpus strutturato di 33 capitoli e 230 pagine, ottimizzato per l'elaborazione degli LLM.
- **Prevenzione delle regressioni algoritmiche**: Superamento dei limiti riscontrati nelle versioni 1.0 e 1.1 (dove l'eccesso di vincoli sequenziali causava rigidità e collasso espressivo). Necessità di tracciare script standardizzati per testare le nuove iterazioni (v1.3).

### 2. [[trainer-simulator]]: Simulatore Esperienziale (v0.2)

Accanto a Libet Prime, è stato introdotto in anteprima il secondo agente in cantiere (**Trainer Simulator / Interview Trainer**), orientato all'allenamento esperienziale al colloquio clinico.

- **Perimetro di addestramento**: Dalla fase iniziale del colloquio alla formulazione condivisa (assessment, ABC, ABC Libet e restituzione).
- **Libreria di Pazienti Virtuali**: Pacchetto iniziale di 10 profili di pazienti simulati con quadri sintomatologici e dinamiche relazionali differenziate.
- **3 Livelli di Difficoltà**: Base, intermedio e avanzato (variazione progressiva di vaghezza nell'eloquio, difese e resistenze relazionali).
- **Comandi di Controllo Sessione**: Comandi interattivi per la gestione dell'esercitazione (`inizia`, `pausa`, `indizio`, `riformula`, `feedback`).
- **Valutazione e Feedback**: Generazione automatizzata di una rubrica di valutazione analitica delle competenze cliniche e comunicative mostrate dall'allievo.

### 3. [[testing-e-validazione-agenti-didattici|Protocollo di Test]] e Piano Operativo

La sperimentazione pilota coinvolge responsabili di sede, didatti storici e figure junior di Studi Cognitivi, selezionate per sensibilità tecnica o clinica, secondo un cronoprogramma definito:

```mermaid
graph TD
    A[Luglio - Agosto: Test Individuale Gemini] --> B[25 Luglio: Rilascio Survey & Upload Script]
    B --> C[25 Agosto: Chiusura Raccolta Dati]
    C --> D[Fine Agosto / Settembre: Focus Group di Sintesi]
    D --> E[Progettazione Libet Prime v1.3 & Estensione Didattica]
```

#### Protocollo di prova
- Test di almeno 3–5 turni di conversazione per ciascuna delle 5 modalità operative.
- Test di robustezza e di rifiuto delle richieste fuori dominio (*out-of-domain*).
- Tracciamento sistematico di prompt, output, allucinazioni, vaghezze, diagnosi indebite o anticipazioni inappropriate di tecniche.

#### Dimensioni di Valutazione del Test
1. **Accuratezza teorica e fedeltà lessicale**: Coerenza con il lessico LIBET e CBT.
2. **Qualità del ragionamento clinico**: Capacità di argomentare e stimolare riflessioni strutturate.
3. **Granularità**: Adeguatezza del livello di dettaglio rispetto alle informazioni fornite.
4. **Prudenza epistemica**: Uso del linguaggio ipotetico, assenza di conclusioni premature o diagnosi automatiche.
5. **Tenuta dei confini (*Guardrails*)**: Rifiuto puntuale dei compiti estranei al perimetro didattico.
6. **Rilevazione errori critici**: Confusione di dinamiche, allucinazioni, anticipazione indebita di interventi avanzati in fase sintomatica acuta.

### 4. [[ia-maieutica-e-co-ragionamento|Riflessioni Pedagogiche, Psicologiche ed Etiche]]

- **Dalla Scorciatoia al Prolungamento della Riflessione**: Contrastare l'uso dell'IA come generatore di risposte rapide, trasformandola in uno strumento che allunga e articola il processo metacognitivo (*[[human-in-the-reasoning]]*).
- **Gestione dei Bias Uomo-Macchina**:
  - *Over-confidence / Effetto Oracolo*: Rischio che gli studenti accettino acriticamente le indicazioni del modello.
  - *Rigidità di Conferma del Clinico Esperto*: Rischio che il didatta respinga spunti coerenti dell'IA solo perché disallineati rispetto alle proprie consuetudini interpretative.
- **Etica e Deontologia**: Salvaguardia della responsabilità decisionale umana come principio non delegabile.

## Decisioni
- Avvio della sperimentazione pilota di Libet Prime (v1.2) e Trainer Simulator (v0.2) secondo il cronoprogramma e il protocollo descritti nella sezione 3.

## Azioni aperte
- [ ] Test individuale su Gemini (luglio-agosto).
- [ ] Rilascio della survey con upload degli script di dialogo (25 luglio).
- [ ] Chiusura della raccolta dati (25 agosto).
- [ ] Focus group di sintesi (fine agosto / settembre).
- [ ] Progettazione di Libet Prime v1.3 ed estensione didattica.

## Relazioni
- Vedi anche: [[libet-prime]], [[trainer-simulator]], [[testing-e-validazione-agenti-didattici]], [[ia-maieutica-e-co-ragionamento]], [[human-in-the-reasoning]], [[simulazione-pazienti-ai]], [[clinical-ai-simulation]], [[ai-assisted-psychotherapy]], [[05-08-riunione-knowledge-base]], [[04-20-tavola-rotonda-integrazione-ia]], [[03-13-avvio-gruppo-lavoro-ia-psicoterapia]]
