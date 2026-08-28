---
tags: [oppv, ordine-psicologi-veneto, guida-operativa, deontologia-ia, gdpr-sanita, ai-act, legge-132-2025, ehds, consenso-informato-ia, human-in-the-loop, privacy-clinica, sicurezza-dati, llm-psicologia, zoom-ai-companion, copilot-m365, gemini-meet, turboscribe, plaud-note, notebooklm]
source_papers: ["Guida-Pratica-AI-OPPV.pdf"]
---

# Guida Operativa all'Utilizzo dell'AI nella Pratica Professionale (OPPV, 2026)

**Summary**: Linee guida ufficiali e operative emanate dal Gruppo di Lavoro Intelligenza Artificiale dell'Ordine delle Psicologhe e degli Psicologi del Veneto (OPPV, Gennaio 2026). Il documento fornisce il quadro giuridico-deontologico integrato (GDPR, AI Act, L. 132/2025, EHDS, Codice Deontologico), stabilisce le quattro condizioni inderogabili di liceità per l'uso dell'IA nella pratica psicologica, fornisce i template personalizzabili di Informativa Privacy e Consenso Informato modulare, e definisce le schede tecniche di configurazione di sicurezza per i principali strumenti commerciali di IA (ChatGPT, Claude, Gemini, Grok, Copilot, Perplexity, Zoom, Teams, Meet, TurboScribe, Plaud Note, NotebookLM, Canva).
**Sources**: `Guida-Pratica-AI-OPPV.pdf` (Versione 1 e 1.1 – Gennaio 2026, a cura del GdL Intelligenza Artificiale OPPV)
**Last updated**: 2026-08-27
---

## Definizione Operativa e Inquadramento Istituzionale

La **Guida Operativa all'Utilizzo dell'AI nella Pratica Professionale** rappresenta il primo documento organico emanato da un Ordine regionale degli psicologi in Italia volto a normare, guidare e disciplinare l'adozione dell'[[large-language-models|Intelligenza Artificiale Generativa]] e degli strumenti digitali avanzati nella professione psicologica e clinica.

Il documento nasce dalla constatazione che l'ingresso dell'IA nella quotidianità professionale avviene spesso in modo informale, frammentario e inconsapevole: molti professionisti considerano i chatbot, i software di trascrizione vocale e i sistemi di sintesi come meri ausili tecnici analoghi a correttori ortografici, motori di ricerca o elaboratori di testo. La Guida OPPV chiarisce che tale percezione è gravemente fuorviante, poiché i sistemi di IA generativa:
1. Elaborano dati personali e particolari (sensibili) su server remoti di terze parti, spesso collocati al di fuori dello Spazio Economico Europeo (extra-SEE);
2. Operano secondo algoritmi complessi e logiche opache (*black box*);
3. Riutilizzano potenzialmente i dati inseriti (prompt, testi, registrazioni vocali) per il riaddestramento continuo dei modelli (*retraining*);
4. Pongono criticità inedite rispetto al segreto professionale, al consenso informato, alla trasparenza relazionale e all'autonomia valutativa del clinico.

L'uso dell'IA generativa in psicologia **non è vietato di per sé**, purché sia impiegato esclusivamente come **strumento assistivo di supporto** e mai come sostituto del ragionamento e dell'atto professionale.

```mermaid
flowchart TD
    subgraph NormativeLayer ["1. Quadro Giuridico-Normativo a Quattro Livelli"]
        N1["Deontologia: Codice Deontologico (Artt. 5, 11-17, 24)"]
        N2["Privacy: GDPR (Reg. UE 2016/679) & D.Lgs. 101/2018"]
        N3["Salute & Consenso: Costituzione Art. 32 & Legge 219/2017"]
        N4["Sicurezza & AI: EU AI Act (Reg. UE 2024/1689), L. 132/2025, EHDS (Reg. UE 2025/327)"]
    end

    subgraph FourPillars ["2. [[quattro-condizioni-liceita-ia-psicologia|Le Quattro Condizioni di Liceità]]"]
        P1["A) Tutela Dati Sensibili: Art. 9 GDPR & Identificabilità Contestuale"]
        P2["B) Segretezza & Riservatezza: Divieto Retraining & Server SEE"]
        P3["C) Trasparenza & Consenso Informato Modulare (Patto Fiduciario)"]
        P4["D) Responsabilità Esclusiva & Human-in-the-Loop Inderogabile"]
    end

    subgraph ToolGovernance ["3. [[configurazione-sicurezza-piattaforme-ia-clinica|Protocolli di Configurazione Piattaforme]]"]
        T1["Videoconferenze Cliniche: Zoom, Teams, Meet (AI & Rec SPENTI)"]
        T2["LLM & Assistenti: ChatGPT, Claude, Gemini, Grok, Copilot (No Training, No Memoria)"]
        T3["Trascrizione & Hardware: TurboScribe, Plaud (No Dati Pazienti, Solo Studio/Formazione)"]
        T4["Ricerca & RAG: NotebookLM, Perplexity (Fonti Ancorate, No Allegati Clinici)"]
    end

    NormativeLayer --> FourPillars
    FourPillars --> ToolGovernance
```

---

## 1. Il Quadro Normativo di Riferimento a Quattro Livelli

L'attività dello psicologo che adotta tecnologie di intelligenza artificiale si colloca all'incrocio vincolante di quattro livelli normativi:

| Livello Normativo | Fonti Giuridiche | Obblighi e Presidi Chiave per lo Psicologo |
| :--- | :--- | :--- |
| **1. Deontologia Professionale** | **Codice Deontologico degli Psicologi Italiani** | - **Artt. 11–17:** Segreto professionale e stretta riservatezza dei dati clinici.<br/>- **Art. 24:** Obbligo di acquisizione del consenso informato preliminare.<br/>- **Art. 5:** Dovere di competenza, formazione continua e alfabetizzazione digitale adeguata agli strumenti adottati. |
| **2. Protezione dei Dati Personali** | **GDPR (Reg. UE 2016/679)** & **D.Lgs. 101/2018** | - **Art. 9:** Divieto generale di trattamento dati sanitari salvo consenso esplicito e finalità di cura.<br/>- **Art. 5:** Principi di liceità, correttezza, trasparenza, limitazione della finalità (*purpose limitation*), minimizzazione dei dati ed esattezza.<br/>- **Art. 22:** Diritto a non essere sottoposti a decisioni basate unicamente su trattamenti automatizzati (profilazione).<br/>- **Art. 35:** Valutazione d'Impatto sulla Protezione dei Dati (**DPIA**) in caso di trattamenti sistematici di dati sanitari con tecnologie complesse. |
| **3. Diritto alla Salute e Consenso** | **Costituzione Italiana (Art. 32)** & **Legge 219/2017** | - Centralità inderogabile del consenso informato libero, consapevole e documentato.<br/>- Nessun trattamento sanitario (diretto o indiretto) può avere inizio senza preventiva informazione completa. |
| **4. Sicurezza dell'IA e Dati Sanitari Europei** | **EU AI Act (Reg. UE 2024/1689)**, **Legge 23 settembre 2025 n. 132**, **EHDS (Reg. UE 2025/327)** | - **AI Act:** Obbligo di supervisione umana effettiva (*Human-in-the-Loop*), trasparenza algoritmica e divieto di delega decisionale autonoma in sanità.<br/>- **Legge n. 132/2025:** Disciplina nazionale italiana sull'impiego dell'IA a supporto delle professioni intellettuali con riserva di titolarità decisionale al professionista.<br/>- **EHDS:** Regolamentazione dello Spazio Europeo dei Dati Sanitari tra *usi primari* (cura e assistenza diretta) e *usi secondari* (ricerca, sanità pubblica, training algoritmico), con diritto del paziente di opporsi agli usi secondari. |

---

## 2. Le Quattro Condizioni Fondamentali di Liceità Deontologica

Per garantire la tutela del paziente e la legittimità giuridica, l'uso dell'IA deve rispettare **simultaneamente** quattro condizioni (la violazione anche di una sola determina illecito disciplinare e normativo):

```mermaid
graph LR
    C1["1. Tutela Dati Sensibili<br/>(Superamento mito de-identificazione parziale)"]
    C2["2. Segretezza & Sovranità<br/>(No Retraining, No Data-leakage Extra-SEE)"]
    C3["3. Trasparenza & Consenso<br/>(Estensione modulare patto fiduciario)"]
    C4["4. Responsabilità Esclusiva<br/>(Human-in-the-Loop & Divieto delega)"]

    C1 & C2 & C3 & C4 --> Conformita["Pratica Professionale Conforme (OPPV 2026)"]
```

### A) Tutela dei Dati Personali e Sensibili (Art. 9 GDPR)
- I dati sulla salute psicologica e mentale godono di protezione rafforzata a prescindere dal formato (appunti, sintesi, audio) e dalle buone intenzioni del clinico.
- **La fallacia della "pseudonimizzazione parziale":** Rimuovere semplicemente il nome e il cognome (*"Tolgo il nome, quindi è anonimo"*) **non rende il dato anonimo**. Nei casi clinici, la ricchezza di dettagli contestuali (professione specifica, dinamiche familiari insolite, micro-localizzazione geografica, eventi temporali precisi) rende la persona pienamente **identificabile per contesto**. Inserire narrazioni cliniche dettagliate in un LLM non conforme costituisce violazione del GDPR.

### B) Segretezza, Riservatezza e Controllo dell'Infrastruttura
- Lo psicologo ha l'obbligo di sapere e poter dimostrare **dove, come e per quanto tempo** i dati vengono trattati.
- **Il rischio del retraining:** L'inserimento di frammenti di anamnesi o sedute in modelli che attuano il riaddestramento automatico può incorporare tali dati nella struttura parametrica del modello, con il rischio teorico che emergano in risposte fornite ad altri utenti.
- **Server extra-SEE:** Il trasferimento di dati sanitari su server statunitensi o extra-europei richiede idonee garanzie giuridiche (es. *Data Privacy Framework UE-USA*, Clausole Contrattuali Standard - SCC). L'affidamento di dati clinici a chatbot gratuiti consumer equivale alla cessione a terzi non vincolati dal segreto professionale.

### C) Trasparenza e Consenso Informato Modulare
- L'utilizzo dell'IA costituisce un trattamento di dati personali che **non può mai essere sottinteso o taciuto**.
- Il paziente ha il diritto inviolabile di conoscere: se e quali strumenti di IA vengono utilizzati, per quali scopi specifici, con quali garanzie tecniche e con quali modalità di opposizione o revoca. La trasparenza è concepita come **estensione del patto fiduciario**.

### D) Responsabilità Professionale Esclusiva e Human-in-the-Loop (HITL)
- L'IA non possiede capacità di giudizio, deontologia né personalità giuridica: è strutturalmente soggetta ad **allucinazioni** (generazione di informazioni errate ma plausibili).
- **Divieto di delega:** L'IA non può in alcuna circostanza formulare diagnosi, stabilire indicazioni terapeutiche o sostituire il ragionamento clinico.
- Qualsiasi output prodotto dalla macchina deve essere criticamente valutato, contestualizzato e validato dal professionista, il quale ne risponde integralmente in sede civile, penale e disciplinare.

---

## 3. Template Documentali Ufficiali (OPPV)

La Guida OPPV include i modelli contrattuali ufficiali precompilati che ogni psicologo deve personalizzare e integrare nella propria modulistica:

### 3.1. Template di Informativa sul Trattamento dei Dati Personali
Il modello recepisce congiuntamente il GDPR (Artt. 13-14), il D.Lgs. 196/2003, l'AI Act (Reg. UE 2024/1689), la Legge n. 132/2025 e l'EHDS (Reg. UE 2025/327):
- **Categorie di dati trattati:** Dati identificativi, particolari sanitari (Art. 9 GDPR), dati biometrici vocali/video (solo previo consenso) e dati elaborati tramite IA (esclusivamente note/bozze preventivamente pseudonimizzate).
- **Finalità d'uso dell'IA:** Supporto strumentale redazionale e organizzativo (revisione linguistica, sintesi di appunti anonimi, traduzioni).
- **Garanzie contrattuali esplicite:**
  1. Principio *Human-in-the-loop*: nessun processo decisionale automatizzato;
  2. Divieto di profilazione automatizzata (Art. 22 GDPR);
  3. Pseudonimizzazione e minimizzazione preventiva;
  4. Esclusione contrattuale del training sui dati immessi e limitazione della persistenza temporale sui server;
  5. Diritto di opposizione agli usi secondari dei dati sanitari ex Reg. EHDS.

### 3.2. Template di Modulo di Consenso Informato Modulare
Strutturato in sezioni autonome per consentire decisioni granulari da parte del paziente:

```mermaid
graph TD
    Modulo["Modulo di Consenso Informato Unificato"]
    Modulo --> SezA["Sezione A: Prestazioni Sanitarie Psicologiche<br/>(Obbligatorio per la cura, include setting online)"]
    Modulo --> SezB["Sezione B: Trattamento Dati Personali GDPR<br/>(Presa d'atto informativa privacy)"]
    Modulo --> SezC["Sezione C: Consenso Specifico IA Generativa<br/>- Supporto strumentale<br/>- Garanzia No-Training & De-identificazione<br/>- Human-in-the-Loop<br/>- Revocabile liberamente senza pregiudizio"]
    Modulo --> SezD["Sezione D: Registrazioni Audio/Video & Trascrizione<br/>- Finalità esclusiva di supervisione/studio<br/>- Cifratura file & cancellazione dopo trascrizione<br/>- Divieto diffusione a terzi"]
```

> [!IMPORTANT]
> **Autonomia della Sezione C e D:** Il mancato rilascio del consenso per l'impiego dell'IA generativa (Sezione C) o per le registrazioni/trascrizioni audio-video (Sezione D) **non impedisce l'erogazione della prestazione psicologica ordinaria**, la quale prosegue con le metodologie cliniche tradizionali.

---

## 4. Vademecum Operativo e Checklist per il Professionista

L'agire concreto dello psicologo richiede l'integrazione di cautele strutturali nella routine professionale:

```mermaid
flowchart TD
    Step1["1. Minimizzazione Radicale"] -->|"Rimozione identificatori diretti e contestuali"| Step2["2. Selezione Strumento Idoneo"]
    Step2 -->|"Account Professional/Enterprise, Opt-out Training, Server SEE"| Step3["3. Trasparenza Contrattuale"]
    Step3 -->|"Informativa & Consenso Sezione C/D"| Step4["4. Documentazione & DPIA"]
    Step4 -->|"Registro Trattamenti & Valutazione Art. 35 GDPR"| Step5["5. Controllo Clinico Diretto"]
    Step5 -->|"Supervisione Human-in-the-Loop su ogni output"| Step6["6. Formazione Continua (Art. 5 C.D.)"]
```

### Regole Operative Cardine:
1. **Minimizzazione rigorosa:** Eliminare nomi, recapiti, codici, luoghi specifici, date insolite, mestieri rari o combinazioni narrative che rendano riconoscibile il paziente.
2. **Selezione degli strumenti e abbonamenti a pagamento:** Nelle versioni consumer gratuite *"i dati degli utenti sono il prezzo da pagare"*; per l'attività professionale occorre adottare licenze *Professional, Business o Enterprise* che garantiscano contrattualmente l'esclusione del training e tempi certi di cancellazione.
3. **Preferenza per i Reasoning Models:** Nei compiti di riflessione teorica, prediligere modelli capaci di esplicitare la catena di pensiero (*reasoning models* come ChatGPT Thinking o Gemini 3) per consentire una valutazione critica passo-passo della logica algoritmica.
4. **Accountability e DPIA:** Aggiornare il *Registro dei Trattamenti* e valutare la redazione di una *Valutazione d'Impatto sulla Protezione dei Dati (DPIA)* ex art. 35 GDPR in caso di impiego continuativo di strumenti cloud complessi.

---

## 5. Schede Tecnico-Operative delle Piattaforme di Mercato

La Guida OPPV fornisce indicazioni puntuali e percorsi di configurazione per i principali applicativi digitali:

```mermaid
mindmap
  root((Governance Piattaforme))
    Piattaforme Videoconferenza
      Zoom / Zoom AI Companion
      Microsoft Teams / Copilot
      Google Meet / Gemini
    LLM e Chatbot Generalisti
      ChatGPT (OpenAI)
      Claude (Anthropic)
      Gemini (Google)
      Grok (xAI)
      Copilot M365 (Microsoft)
    Trascrizione e Hardware
      TurboScribe
      Plaud Note
    Ricerca e Document RAG
      NotebookLM (Google)
      Perplexity AI
    Grafica e Psicoeducazione
      Canva
```

### 5.1. Piattaforme di Videoconferenza Clinica (Zoom, Teams, Google Meet)
*Regola aurea per tutte le piattaforme di telepsicologia:* **La seduta clinica online deve essere una videochiamata in tempo reale pura, senza registrazione, senza trascrizione e senza assistenti IA attivi.**

| Piattaforma | Funzionalità ad Alto Rischio | Regole per Sedute Cliniche | Impostazioni di Hardening Raccomandate |
| :--- | :--- | :--- | :--- |
| **Zoom** | Zoom AI Companion, Meeting Summary, Smart Recording, salvataggio chat | - **AI Companion rigorosamente SPENTO**.<br/>- Nessuna registrazione (né locale né cloud).<br/>- Sottotitoli ammessi solo per accessibilità senza salvataggio. | - Disattivare registrazione automatica.<br/>- Impostare *Data Residency* su server SEE (Impostazioni > Avanzate > Dati e privacy > Imposta SEE). |
| **Microsoft Teams** | Copilot in Teams, Intelligent Recap, Meeting Recap, bot terzi (AI note-takers) | - **Nessuna registrazione né trascrizione live**.<br/>- Nessun prompt a Copilot sul contenuto della seduta.<br/>- Divieto assoluto di ammettere bot/estensioni di terze parti nella riunione. | - Disattivare registrazione e trascrizione automatica nei criteri di riunione.<br/>- Mantenere le licenze Intelligent Recap disattivate per gli account clinici.<br/>- Consentito con recap solo per riunioni organizzative/formative prive di dati sensibili. |
| **Google Meet** | Gemini in Meet (*Take notes for me*, *Ask Gemini in Meet*), trascrizione Drive | - **Funzioni Gemini e "Take notes for me" rigorosamente SPENTE**.<br/>- Disattivare trascrizione automatica della riunione (evita generazione di file su Google Drive e link su Calendar). | - Configurare Google Calendar escludendo la registrazione automatica.<br/>- Se si usano sottotitoli live per accessibilità, informare il paziente ed evitare il salvataggio degli artefatti. |

---

### 5.2. Assistenti LLM e Chatbot Generalisti

| Strumento | Usi Consentiti | Usi Vietati | Configurazione di Privacy e Gestione Cronologia |
| :--- | :--- | :--- | :--- |
| **ChatGPT** *(OpenAI)* | - Spiegazione concetti e procedure.<br/>- Revisione stilistica di testi già anonimizzati.<br/>- Supporto teorico e psicoeducazione generica. | - Inserimento di dati anagrafici o contesti clinici identificabili.<br/>- Caricamento di referti, test o note di seduta. | - **Disattivare Training:** `Settings > General > Data Controls > Improve the model for everyone -> OFF`.<br/>- **Disattivare Memoria:** `Settings > Personalizzazione > Memoria -> OFF` (per "Memorie salvate" e "Cronologia chat").<br/>- Utilizzare *Temporary Chat* (icona fumetto tratteggiato) per sessioni delicate.<br/>- Cancellazione account: eliminazione permanente in 30 giorni.<br/>- *Nota su ChatGPT for Health (Gennaio 2026):* iniziativa OpenAI non ancora accessibile né conformata al GDPR in Italia. |
| **Claude** *(Anthropic)* | - Riflessione teorico-clinica su modelli psicoterapeutici.<br/>- Redazione di bozze di informative e consensi generici.<br/>- Riformulazione strutturale di testi de-identificati. | - Descrizione di casi clinici reali.<br/>- Caricamento di trascrizioni o documentazione sanitaria.<br/>- Utilizzo come diario clinico. | - **Disattivare Training:** `Settings > Privacy > Help improve Claude -> OFF` (su Desktop e App mobile).<br/>- **Gestione Memoria:** `Settings > Capabilities > Pause / Reset Memory`.<br/>- Utilizzare le **Incognito Chats** (icona fantasma).<br/>- **Divieto Feedback:** Evitare pollici su/giù su contenuti sensibili (Anthropic trattiene i dati con feedback fino a 5 anni). Cancellazione chat: rimozione entro 30 giorni. |
| **Gemini** *(Google)* | - Elaborazione di materiali psicoeducativi generici.<br/>- Supporto alla strutturazione teorica di interventi.<br/>- Semplificazione testi teorici per pazienti. | - Inserimento di casi clinici o anamnesi reali.<br/>- Repository di note o archivio sanitario. | - **Disattivare Training:** Account Google > Dati e privacy > `Gemini Apps Activity -> OFF` (le chat non salvate restano fino a 72h solo per sicurezza).<br/>- Disattivare la spunta *"Migliora i servizi Google"*. Impostare auto-cancellazione a 3 mesi.<br/>- Usare *Chat Temporanea*.<br/>- **Divieto Feedback:** Non inviare pollici su/giù su chat professionali (Google conserva i dati dei feedback fino a 3 anni con possibile revisione umana). |
| **Microsoft Copilot** *(M365)* | - Bozza email, riassunti di testi organizzativi, slide formative.<br/>- Elaborazione su testi teorici o relazioni preventivamente anonimizzate in locale. | - Caricamento diretto di cartelle cliniche, test psicodiagnostici o registrazioni audio con dati sensibili. | - **Account Enterprise:** Lavorare esclusivamente con account aziendale/Enterprise M365 verificando la presenza dello **scudetto verde (Enterprise Data Protection)**, dove i dati non vengono usati per il training.<br/>- Se si usa account personale: disattivare training testo/voce in `Impostazioni Profilo > Privacy`. |
| **Grok** *(xAI)* | - Brainstorming su temi teorici e ricerca di trend/notizie in tempo reale sulla piattaforma X. | - Trattamento di casi clinici o informazioni sanitarie. | - **Disattivare Training su X:** `Settings & Privacy > Privacy & Safety > Data sharing and personalization > Grok & Third-party Collaborators > Data Sharing -> OFF`.<br/>- **Disattivare Training su grok.com:** `Impostazioni > Controllo dati > Migliora il modello -> OFF`.<br/>- *Attenzione:* Grok su X e su grok.com possiedono cronologie e impostazioni distinte (occorre disattivarle entrambe). |

---

### 5.3. Software di Trascrizione, Dispositivi Hardware e Strumenti RAG

| Piattaforma / Tool | Natura dello Strumento | Usi Consentiti | Usi Vietati e Criticità Giuridiche | Buone Pratiche Operative |
| :--- | :--- | :--- | :--- | :--- |
| **TurboScribe** | Piattaforma AI cloud di trascrizione audio/video in testo. | Trascrizione di lezioni, webinar, convegni, interviste simulate e appunti vocali personali teorici. | - **Vietata la trascrizione di sedute cliniche reali** senza tutele contrattuali avanzate.<br/>- Nelle versioni standard non offre piene garanzie formali ex art. 28 GDPR per dati sanitari. | - Utilizzare account dedicati separati da quelli personali.<br/>- Eliminare file audio e trascrizioni testuali dalla piattaforma subito dopo il download.<br/>- Lavorare solo su simulazioni o audio de-identificati. |
| **PLAUD (Plaud Note)** | Dispositivo hardware con registrazione e trascrizione AI cloud online. | Registrazione di riunioni di équipe non cliniche, corsi di formazione, conferenze, memo vocali personali di studio. | - **Vietata la registrazione di sedute cliniche e dati sensibili**.<br/>- Server extra-SEE (USA) privi di accordo formale ex art. 28 GDPR per categorie particolari di dati sanitari. | - In caso di registrazione di riunioni formative, informare sempre i partecipanti.<br/>- Non archiviare registrazioni con contenuti sanitari sulla memoria del device o sul cloud associato. |
| **NotebookLM** *(Google)* | Ambiente assistivo RAG (*Retrieval-Augmented Generation*) per studio su fonti caricate dall'utente. | - Analisi e sintesi di linee guida, paper scientifici, manuali diagnostici, appunti teorici.<br/>- Generazione di FAQ, mappe concettuali, sintesi audio/video psicoeducative. | - **Vietato il caricamento di cartelle cliniche reali, referti o trascrizioni di seduta**.<br/>- Rischio condivisione accidentale pubblica del Notebook. | - Utilizzare account Google Workspace istituzionali (dove Google non addestra sui dati caricati).<br/>- Mantenere la condivisione ristretta (accesso privato esclusivo).<br/>- Non inviare feedback con pollice su/giù su documenti confidenziali. |
| **Canva** | Piattaforma di progettazione grafica con moduli generativi (Magic Write/Media). | Creazione di infografiche psicoeducative, schede riassuntive per pazienti, slide per corsi di formazione. | - Inserimento di foto di pazienti, storie cliniche dettagliate o screenshot di comunicazioni terapeutiche. | - Considerare ogni input di Magic Write/Media come prompt soggetto a memorizzazione.<br/>- Usare account professionali/team con nomi di file e cartelle neutri. |

---

## 6. Esemplificazioni Clinico-Operative (Prompting Sicuro vs Rischioso)

La Guida OPPV illustra concretamente la differenza tra formulazioni vietate ad alto rischio di re-identificazione e varianti conformi:

```mermaid
graph TD
    subgraph Errato ["Approccio Scorretto (Violazione Deontologica e Privacy)"]
        E1["'Ho in terapia Mario Rossi, 37 anni, psicologo scolastico nella scuola X di Treviso...'"]
        E2["'Ti incollo il referto diagnostico della mia paziente, scrivimi la relazione clinica...'"]
        E3["'Carico la registrazione audio della seduta su TurboScribe/Plaud per farmi dare i punti chiave...'"]
    end

    subgraph Corretto ["Approccio Conforme (Tutela del Setting e del Dato)"]
        C1["'In termini generali e teorici, come si concettualizza lo stress lavorativo in ambito scolastico secondo il modello CBT?'"]
        C2["'Ti fornisco un testo già anonimizzato e generalizzato privo di contesti univoci: aiutami a migliorarne chiarezza espositiva e sintassi.'"]
        C3["'Trascrivo un role-play didattico o una simulazione clinica costruita ad hoc per la formazione specialistica.'"]
    end
```

---

## Concetti Correlati e Navigazione nella Knowledge Base

- [[quattro-condizioni-liceita-ia-psicologia|Le Quattro Condizioni di Liceità e Correttezza Deontologica per l'IA in Psicologia]]: Approfondimento dottrinale e giuridico del framework OPPV.
- [[configurazione-sicurezza-piattaforme-ia-clinica|Configurazione di Sicurezza e Mitigazione del Rischio per Piattaforme di IA in Ambito Clinico]]: Protocollo pratico di hardening per gli applicativi digitali.
- [[informed-consent-for-clinical-ai|Consenso Informato per l'IA nella Pratica Clinica]]: Modello etico APA e confronto con il framework europeo/italiano.
- [[gdpr-governance-mental-health-ai|GDPR Governance e Protezione Dati nell'IA per la Salute Mentale]]: Inquadramento regolatorio e rischi di ri-identificazione.
- [[human-oversight-and-liability-in-clinical-ai|Supervisione Umana e Responsabilità Giuridica nell'IA Clinica]]: Principi di non delegabilità e colpa professionale.
- [[modello-centauro-clinico|Modello Centauro Clinico]]: Integrazione post-seduta tra psicoterapeuta e co-pilota computazionale.
- [[augmented-psychotherapy|Psicoterapia Aumentata]]: Applicazioni dell'NLP e della scrittura clinica assistita.
