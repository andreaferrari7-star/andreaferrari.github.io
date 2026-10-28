---
tags: [ai-health-coursera, formazione, sistemi-multi-agente, ia-agentica, progettazione, etica, value-sensitive-design, equita]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C4M2_JK_Dec29_2024_V1.0 (1).pdf"]
---

# AI for Healthcare Systems, C4M2: progettazione ed etica dell'IA sanitaria (Khuntia, 2024n)

## Definizione Operativa
- Materiale di approfondimento (27 pagine, versione 1.0 del 29 dicembre 2024) che chiude il corso 4 e l'intera serie [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]]; le intestazioni lo chiamano «Course 3, Module 3». Tratta quattro temi (Khuntia, 2024n):
  - i sistemi multi-agente;
  - le «tre ondate» dell'IA in sanità (modelli, IA generativa, IA agentica);
  - otto questioni di progettazione;
  - il *Value-Sensitive Design* (VSD) come quadro per un'IA sanitaria etica.
- **Utilità CBT / Applicativa:** è il modulo più utile della serie per chi valuta o progetta uno strumento per la salute mentale, perché offre una lista di principi di progettazione:
  - coinvolgere gli utenti;
  - dichiarare l'uso previsto e i limiti;
  - testare l'equità tra gruppi;
  - spiegare le uscite;
  - proteggere i dati con consenso informato;
  - prevedere un comitato etico che vigili sul sistema.
  Vedi [[value-sensitive-design-ia-sanitaria]].

## Evidenze dalla Letteratura

### Sistemi multi-agente
- Un sistema multi-agente è un insieme di agenti autonomi che collaborano, ciascuno con un compito, per problemi che coinvolgono più attori e interdipendenze. Le caratteristiche sono autonomia, collaborazione, adattabilità e scalabilità. Il flusso tipico è raccolta dei dati, assegnazione dei compiti, ottimizzazione con algoritmi distribuiti, monitoraggio e retroazione (Khuntia, 2024n).
- Il modulo elenca quindici applicazioni (Khuntia, 2024n). Alcuni esempi:
  - agende ambulatoriali e chirurgiche, con un algoritmo di ottimizzazione distribuita sotto vincoli chiamato «DCDCOP» [da verificare];
  - diabete, cardiopatie, malattia renale cronica;
  - pronto soccorso, aderenza, oncologia, terapia intensiva;
  - **salute mentale:** chatbot come «terapeuti virtuali» che danno supporto immediato e passano i casi ai clinici, e un «agente di prevenzione del suicidio» che avvisa chi assiste il paziente se compaiono segnali d'allarme nella conversazione.
- Le sfide sono la complessità di integrazione e la fiducia: i medici esitano ad affidarsi ad agenti autonomi senza studi di validazione. Per la scalabilità pesano il sovraccarico di dati e le infrastrutture carenti nelle aree svantaggiate (Khuntia, 2024n).

### Le tre ondate dell'IA in sanità
- Il modulo descrive tre ondate successive (Khuntia, 2024n):
  - **prima ondata, i modelli:** dal descrittivo al predittivo, per esempio il rischio di riammissione o di complicanze diabetiche;
  - **seconda ondata, l'IA generativa:** crea contenuti, come materiali educativi personalizzati in linguaggio semplice o video, e riduce il carico di documentazione strutturando le note e riassumendo le storie cliniche;
  - **terza ondata, l'IA agentica:** agenti autonomi che svolgono compiti complessi «con un intervento umano minimo» e agiscono come «decisori». Esempi: agende, raccomandazioni sull'insulina, triage nelle maxi-emergenze.
- Le tre ondate si integrano: il modello prevede, l'IA generativa traduce in contenuti, l'agente esegue. Nell'esempio oncologico l'IA generativa «crea piani di trattamento personalizzati» e l'agente programma la chemioterapia e regola i farmaci (Khuntia, 2024n).

### Otto questioni di progettazione
- Le otto questioni (Khuntia, 2024n):
  1. **qualità dei dati e bias:** modelli dermatologici meno accurati sulla pelle scura, diagnosi cardiovascolari mancate nelle donne, modelli urbani che non generalizzano alle aree rurali. Contromisure: audit, ripesatura, inclusione dei gruppi sottorappresentati;
  2. **spiegabilità e fiducia:** importanza delle variabili, mappe di calore sulle immagini, spiegazioni in linguaggio naturale. Il modulo cita il «diritto alla spiegazione» del GDPR;
  3. **progettazione centrata sull'utente:** interviste, focus group, test di usabilità; output dentro la cartella elettronica; interfacce semplici e adattabili a contesti con poche risorse;
  4. **etica ed equità:** validazione su popolazioni diverse e dichiarazione dell'uso previsto. Uno strumento di screening non va presentato come diagnostico;
  5. **privacy e sicurezza:** cifratura, autenticazione, minimizzazione, limitazione delle finalità, consenso esplicito, controllo del paziente sui propri dati;
  6. **integrazione e scalabilità:** FHIR e cloud; esempi della Cleveland Clinic e dell'app indiana Aarogya Setu;
  7. **collaborazione uomo-IA:** l'IA evidenzia, il clinico decide. Il modulo afferma che diagnosi finale e piano di trattamento restano responsabilità del clinico e che servono formazione e consapevolezza dei limiti;
  8. **miglioramento continuo:** validazione nel mondo reale e uso dei casi in cui i clinici scavalcano il sistema come segnale di debolezza del modello. Viene citato il programma di precertificazione FDA per il software sanitario.

### Il Value-Sensitive Design
- Il VSD è presentato come filosofia che integra i valori etici nell'intero ciclo di vita del sistema, in sette componenti (Khuntia, 2024n):
  - **coinvolgere i portatori di interesse:** per esempio uno strumento per la retinopatia diabetica co-progettato con operatori e comunità locali;
  - **test iterativi:** per esempio i pulsossimetri meno accurati sulla pelle scura, o i modelli per la sepsi con gruppi poco rappresentati;
  - **modelli equi e trasparenti:** audit periodici, non una tantum;
  - **IA spiegabile:** anche con modelli surrogati interpretabili e spiegazioni semplici al paziente;
  - **protezione della privacy:** apprendimento federato, cifratura, consenso informato, un comitato etico che verifica le pratiche sui dati di un sistema di supporto alla salute mentale;
  - **equità:** strumenti mobili per le aree rurali, monitoraggio per gruppi demografici, formazione del personale;
  - **supervisione etica:** comitati, audit, responsabilità condivise tra sviluppatori, clinici e decisori.

### Errori, limiti e divergenze con la wiki
- **Incoerenza sull'autonomia:** la sezione sulle tre ondate presenta l'IA agentica come «decisore» che agisce «con un intervento umano minimo». Quella sulla collaborazione uomo-IA dice che la diagnosi finale resta al clinico. Il secondo principio è coerente con AI Act e GDPR. Vedi [[human-in-the-loop]] e [[tiered-autonomy-in-clinical-ai]].
- **IA generativa che «crea piani di trattamento»:** l'esempio oncologico affida all'IA generativa la stesura del piano terapeutico, senza discutere allucinazioni e validazione. Vedi [[ai-clinical-decision-support]].
- **Salute mentale:** i chatbot come «terapeuti virtuali» e l'agente che avvisa i familiari in caso di segnali suicidari sono presentati senza discutere sicurezza clinica, consenso, falsi allarmi e riservatezza. Vedi [[rischio-suicidario-ai-limits]].
- **Affermazioni da verificare:**
  - il «diritto alla spiegazione» nel GDPR è un'interpretazione discussa: il testo del regolamento prevede all'art. 22 il diritto a non essere sottoposti a decisioni solo automatizzate [da verificare];
  - l'adozione della blockchain per le cartelle alla Mayo Clinic [da verificare];
  - Aarogya Setu è presentata come sistema di IA, mentre era un'app di tracciamento dei contatti [da verificare];
  - il programma di precertificazione FDA è presentato come attivo [da verificare];
  - i pulsossimetri sono descritti come problema risolto con test iterativi [da verificare].
- **Fonti teoriche:** il VSD è un quadro con una propria letteratura, che il modulo non cita [da verificare]. Babylon Health compare di nuovo come esempio positivo.

## Riferimenti Bibliografici
- Khuntia, J. (2024n). *Background materials for Course 4: AI integration in healthcare. Module 2: Health AI relevant design and ethics issues* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-agents-in-healthcare-and-capstone

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[value-sensitive-design-ia-sanitaria]], [[agenti-ia-sanita]], [[embedded-ethics-interface]], [[compound-opacity-in-multi-agent-systems]], [[human-in-the-loop]], [[algorithmic-bias-and-digital-inequalities]], [[rischio-suicidario-ai-limits]], [[ai-health-c4m1-khuntia-2024]]
