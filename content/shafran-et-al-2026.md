---
tags: [supervisione, formazione-clinica, cbt, pazienti-virtuali, clinical-fidelity, governance, salute-mentale-globale]
tipo_fonte: scientifica
source_papers: ["1-s2.0-S0005796725002736-main.pdf"]
---

# Dall'innovazione all'implementazione: l'IA nella formazione e supervisione in CBT (Shafran et al., 2026)

## Definizione Operativa
- Articolo di posizione di un gruppo internazionale di 20 autori, coordinato da Roz Shafran (UCL), su *Behaviour Research and Therapy*. Descrive usi, benefici, sfide e rischi dell'IA nella formazione e nella supervisione dei clinici in [[cbt|CBT]] e chiude con linee guida per sviluppo, ricerca e implementazione. Non presenta dati originali (Shafran et al., 2026).
- **Utilità CBT / Applicativa:** offre una mappa degli usi possibili (pazienti virtuali, rating automatico della fedeltà, supervisione con agenti, consulente IA) e una lista di requisiti (Tabella 1) utile per valutare uno strumento di training prima di adottarlo o di proporlo in un corso.

## Evidenze dalla Letteratura

### Perché la CBT
- Gli autori scelgono la CBT per tre motivi: è la terapia evidence-based più studiata; pochi studi hanno esaminato l'IA nella sua formazione e supervisione; esistono protocolli diversi con la stessa etichetta (per esempio per l'ansia sociale), e un sistema di IA deve preservarne le distinzioni teoriche. In alternativa, l'IA potrebbe essere addestrata sui principi attivi del cambiamento anziché sui protocolli (Shafran et al., 2026).

### Aderenza e competenza
- L'obiettivo della formazione è che il terapeuta faccia «le cose giuste, bene». Verificare l'**aderenza** (fare ciò che prevede il protocollo, senza elementi estranei) è possibile con checklist ed è adatto all'automazione. Valutare la **competenza** (farlo bene) è più difficile, per l'IA come per gli umani, perché richiede un'applicazione flessibile e la concettualizzazione del caso (Shafran et al., 2026).
- Con un paziente a rischio suicidario la scelta competente può essere *non* usare certe tecniche di cambiamento o privilegiare la collaborazione; un sistema basato solo sulla CTS-R la registrerebbe come carenza. Gli autori ipotizzano di valutare gli esiti anziché la competenza, pur ricordando che il legame tra competenza ed esiti è incoerente e modesto (Power et al., 2022, citati in Shafran et al., 2026). Vedi [[ctrs-automated-evaluation]].
- Esistono già sistemi in cui il terapeuta interagisce con un paziente virtuale e riceve un giudizio automatico sulla propria prestazione: TherapyTrainer per la Written Exposure Therapy, Virtual Insomnia Patients per la CBT-I, lo strumento di Lyssn per la CBT per la psicosi. Gli algoritmi raggiungono un'affidabilità equivalente a quella dei codificatori umani, i clinici giudicano questi strumenti accettabili e fattibili, ed è in corso un trial ibrido di implementazione ed efficacia in un grande sistema pubblico di salute mentale (Shafran et al., 2026).
- Gli autori chiedono che le valutazioni del training assistito da IA adottino gli indicatori osservabili di competenza dell'iniziativa WHO-UNICEF EQUIP e siano verificate in contesti clinici e culturali diversi (Shafran et al., 2026).

### Pazienti virtuali standardizzati (AI-VSP)
- Vantaggi: nessun paziente reale a rischio; pratica immediata, senza attendere le fasi del trattamento; più autoefficacia; meno costi e variabilità; esposizione a casi rari, ad alto rischio e diversi; adattamento dinamico di emozioni, sintomi e complessità della conversazione (Shafran et al., 2026). Vedi [[simulazione-clinica-pazienti-virtuali]].
- Tre benefici specifici (Shafran et al., 2026):
  - micro-coaching con feedback immediato e role-play, clinicamente più valido se sviluppato con supervisori esperti;
  - segnali non verbali (postura, tono, espressioni) tramite realtà virtuale e sistemi multimodali;
  - competenza multiculturale, perché la simulazione non dipende dalla composizione della popolazione locale; utile anche in contesti con poche risorse.
- Limiti: l'uso in CBT è in fase iniziale e le prove rigorose sono poche. Alcuni studi riguardano abilità di base come l'empatia, ma l'addestramento a tecniche cognitivo-comportamentali complesse resta in gran parte non testato. Rischio pedagogico: privilegiare la risposta immediata a scapito della riflessione e del pensiero strategico (Shafran et al., 2026).
- L'IA può servire anche a formare i supervisori, analizzando le sedute di supervisione con strumenti standardizzati di valutazione (Shafran et al., 2026).

### Strumenti per la supervisione nella pratica reale
- Trascrizione e analisi delle sedute, bozze di note cliniche, individuazione dei momenti chiave (opportunità mancate, deviazioni dal protocollo, interazioni critiche) e dati per una supervisione basata sulle misure (Shafran et al., 2026). Vedi [[supervisione-clinica-ai]].
- LLM per competenze specifiche, come Socrates 2.0 per il dialogo socratico (Shafran et al., 2026).
- **Concettualizzazione del caso assistita:** promettente, ma richiede memoria tra sessioni e la capacità di inferire stati mentali. L'affidabilità delle formulazioni dei terapeuti è a sua volta problematica (Kuyken et al., 2005, citati in Shafran et al., 2026); resta aperto se gli LLM possano produrre formulazioni che migliorano l'efficacia clinica. Vedi [[barriere-astrazione-concettualizzazione-caso]].
- **Architettura multi-agente:** un agente fa da consulente conversazionale; un secondo agente, nascosto, guida il «terapeuta» sulla concettualizzazione del caso, riassume le decisioni precedenti e suggerisce miglioramenti, sul modello della supervisione *bug-in-ear* (Shafran et al., 2026).

### Dati e algoritmi
- I modelli generalisti come ChatGPT non sono stati addestrati su trascrizioni di terapia, che non sono pubbliche, e senza ulteriore addestramento possono non rappresentare una terapia di qualità. Therabot è stato addestrato su dialoghi terapeuta-paziente fittizi, scritti in oltre 100.000 ore di lavoro di esperti. Nella pratica il prompting *few-shot* è diventato il metodo più comune, e spesso il più efficace, per adattare il comportamento del modello (Shafran et al., 2026).
- I requisiti dei dati cambiano con l'uso. Un sistema di rating della fedeltà richiede dataset etichettati con valutazioni accurate; un paziente virtuale o un sistema di feedback narrativo ne ha meno bisogno. Per scegliere i dataset serve competenza disciplinare sui modelli CBT e sui loro elementi attivi (Shafran et al., 2026).
- Privacy e consenso: non è chiaro chi «possieda» i dati né se i consensi generali usati in sanità coprano il successivo uso per prodotti di IA; c'è anche il rischio di addestrare su materiali protetti da diritto d'autore (Shafran et al., 2026).
- Rumore e bias dei dati vanno misurati, per esempio con una Fairness Metrics Ontology. Nessuna decisione clinica o formativa va basata ciecamente sull'output del modello, che deve spiegare perché ha raggiunto una conclusione (Shafran et al., 2026).

### Contesti globali e a basse risorse
- I dati dei paesi ad alto reddito sono sovrarappresentati nell'IA clinica: il feedback può risultare culturalmente inappropriato o poco pertinente. Servono dati culturalmente e linguisticamente diversi e il contributo di clinici, comunità e pazienti locali (Shafran et al., 2026). Vedi [[cross-cultural-bias-and-fairness-audits-ai]].
- Barriere: infrastruttura digitale, costi iniziali e un possibile «effetto di esclusione» legato alle licenze. Gli autori raccomandano modelli open-access o a basso costo, integrati nelle piattaforme sanitarie già esistenti (Shafran et al., 2026).
- Nei modelli di *task-sharing* i fornitori non specialisti potrebbero ricevere feedback in tempo reale, alleviando la carenza di supervisori; ma devono essere formati a interpretare il feedback, per evitare usi impropri o un affidamento eccessivo (Shafran et al., 2026).
- L'addestramento e l'uso dei grandi modelli consumano energia e acqua; i paesi a basso e medio reddito sono i più esposti al riscaldamento globale. Lo sviluppo responsabile deve considerare anche l'impronta di carbonio (Shafran et al., 2026).
- Governance dei dati: standard globali (gli autori indicano il [[readi-framework|framework READI]]), privacy by design con de-identificazione automatica, controllo locale dei dati da parte di clinici e istituzioni, formazione all'etica digitale (Shafran et al., 2026).

### Stato della ricerca
- Mancano studi sperimentali che confrontino modelli di formazione e supervisione. In una revisione sistematica solo 9 studi su 76 (12%) erano RCT (Frank et al., 2020, citati in Shafran et al., 2026); in un'altra solo 6 studi di training su 28 avevano un basso rischio di bias e meno della metà usava una misura oggettiva della fedeltà (Valenstein-Mah et al., 2020, citati in Shafran et al., 2026).
- La ricerca sugli AI-VSP consiste soprattutto in studi pilota di fattibilità e accettabilità, molti precedenti agli LLM avanzati (Shafran et al., 2026).
- Criterio proposto: l'IA deve dimostrare superiorità sugli esiti a livello di terapeuta (velocità, accuratezza, qualità del feedback) rispetto al gold standard in presenza, oppure non inferiorità sugli esiti clinici insieme a superiorità su costi, accessibilità e scalabilità. Servono una linea guida analoga a CONSORT per questo campo e dichiarazioni obbligatorie di conflitto di interessi (Shafran et al., 2026).

### Linee guida (Tabella 1)
- **Sviluppo:** bilanciare fedeltà al protocollo e flessibilità; integrare dati del paziente, preferenze, sensibilità culturale e giudizio clinico; includere nel feedback indicazioni su engagement e drop-out; ricavare i benchmark di fedeltà da campioni rappresentativi; verificare nel tempo bias e accuratezza; adottare politiche «anti-sicofanzia», per cui il sistema valida l'emozione dell'utente ma non le credenze improbabili o dannose (Carlbring & Andersson, 2025, citati in Shafran et al., 2026). Vedi [[sycophantic-mirroring]].
- **Ricerca:** RCT, revisioni sistematiche e meta-analisi; specificare i disturbi per cui il clinico viene formato; dataset CBT diversi, con misure oggettive della qualità del trattamento; consenso informato di allievi e pazienti all'uso dei loro dati (Shafran et al., 2026).
- **Implementazione:** trasparenza su come l'IA genera valutazioni e su quanto è accurata rispetto al giudizio umano; possibilità di rifiutare l'uso dei propri dati; personalizzazione sullo stile di apprendimento; l'IA affianca e non sostituisce la supervisione umana; integrazione nei flussi di lavoro esistenti (Shafran et al., 2026).
- Gli autori citano anche il framework TEQUILA (Trust, Evidence, Quality, Usability, Interest, Liability, Accreditation) di Löchner et al. (2025) per lo sviluppo responsabile di questi strumenti (citati in Shafran et al., 2026).

### Rischi
- Un'analisi di chatbot per la salute mentale molto usati ha rilevato consigli clinicamente non sicuri in situazioni ad alto rischio ed espressioni di stigma verso chi rivela condizioni gravi (Moore et al., 2025, citati in Shafran et al., 2026).
- **[[algorithmic-paternalism-in-ai-mental-health|Paternalismo algoritmico]]:** se un sistema molto autonomo viene trattato come se «sapesse meglio», le decisioni sul progresso dell'allievo possono essere prese senza il suo coinvolgimento. Formatori e supervisori che si rimettono alla tecnologia rischiano di perdere gradualmente le proprie competenze, e conclusioni prodotte da algoritmi complessi sono difficili da contestare (Shafran et al., 2026).
- Conflitti di interesse dichiarati: un autore ha un ruolo di consulenza retribuita con Lyssn.io, uno degli strumenti citati; un altro ha ricevuto compensi da aziende tra cui OpenAI (Shafran et al., 2026).

## Riferimenti Bibliografici
- Shafran, R., Bond, L., Carlbring, P., Cohen, Z. D., Creed, T. A., Davey, E., Egan, S. J., Freeman, D., Hollon, S. D., Jacobson, N. C., Johnson, C., Kaysen, D., McGuinness, D. L., Patel, V., Pozuelo, J. R., Santos, H., Singla, D. R., Wiltsey Stirman, S., Taylor, D. J., & Wade, T. D. (2026). From innovation to implementation: Artificial intelligence in cognitive behaviour therapy training and supervision. *Behaviour Research and Therapy*, *197*, Article 104945. https://doi.org/10.1016/j.brat.2025.104945

## Relazioni
- Vedi anche: [[supervisione-clinica-ai]], [[cioffi-et-al-2025]], [[simulazione-clinica-pazienti-virtuali]], [[ctrs-automated-evaluation]], [[deliberate-practice-in-psicoterapia-ia]], [[readi-framework]], [[algorithmic-paternalism-in-ai-mental-health]], [[cbt]], [[human-in-the-loop]]
