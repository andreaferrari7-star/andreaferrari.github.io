---
tags: [supervisione, large-language-models, psychotherapy, anxiety]
tipo_fonte: [evento, scientifica]
source_papers: ["06-10 Lezione_ RAG, LLM in Psicoterapia e Governance Etica.txt", "1-s2.0-S0005796725002736-main.pdf", "informatics-12-00029.pdf"]
---

# Supervisione Clinica e Intelligenza Artificiale

**Summary**: Inquadramento teorico ed evidenze empiriche sull'utilizzo dei Large Language Models e chatbot come strumenti a supporto della supervisione e dell'intervisione in psicoterapia. L'analisi include lo studio pionieristico di Cosentino et al. (2026) su allievi specializzandi e terapeuti esperti, focalizzandosi su timore della colpa, ansia sociale, rischi di de-skilling e sycophancy, la rassegna di Shafran et al. (2026) sugli strumenti di IA per la supervisione in CBT e lo studio di Cioffi et al. (2025) sul feedback di supervisione generato da ChatGPT-4.
**Fonti**: [[06-10-lezione-rag-llm|Lezione e Seminario: RAG, LLM in Psicoterapia, Supervisione e Governance Etica (10 Giugno 2026)]]; [[shafran-et-al-2026|Shafran et al. (2026)]]; [[cioffi-et-al-2025|Cioffi et al. (2025)]]
**Last updated**: 2026-10-17

---

## Definizione e Razionale

L'applicazione dell'[[large-language-models|Intelligenza Artificiale]] nell'ambito della **supervisione clinica** e dell'intervisione tra pari rappresenta una delle frontiere più discusse della psicoterapia contemporanea. La supervisione costituisce storicamente lo spazio privilegiato per la riflessione metacognitiva, l'elaborazione dei vissuti relazionali, la gestione dell'alleanza terapeutica e la calibrazione del ragionamento clinico.

L'introduzione di assistenti conversazionali intelligenti (LLM generalisti o agenti potenziati da RAG) apre opportunità di supporto preliminare, ma solleva interrogativi cruciali sulla tenuta del giudizio autonomo del clinico, sull'assenza di saggezza clinica incarnata e sul rischio di de-responsabilizzazione formativa.

---

## Stato dell'Arte e Ricerca Empirica (Studio Cosentino et al., 2026)

Lo studio empirico condotto dalla Dott.ssa Teresa Cosentino (APC/SPC, *Cognitivismo Clinico*) ha indagato la diffusione, gli atteggiamenti e le determinanti psicologiche individuali nell'uso dell'IA a supporto della supervisione su un campione nazionale di $N = 93$ professionisti:

- **Campione**: 48 allievi specializzandi in psicoterapia e 45 psicoterapeuti già specializzati (età media 38 anni).
- **Misure somministrate**: 
  - Questionario ad hoc a 25 item (scala Likert 1–5 articolata su 4 dimensioni: uso clinico, fiducia nello strumento, IA come sostituto umano, IA per ridurre il disagio interpersonale).
  - *Fear of Guilt Scale (FGS)*: misura della tendenza al timore della colpa e della sensibilità al danno morale.
  - *Liebowitz Social Anxiety Scale (LSAS)*: misura dell'ansia e dell'evitamento sociale.

```mermaid
graph TD
    subgraph Benefici & Usi Percepiti
        B1["Disponibilità continua H24 & Bassi costi"]
        B2["Preparazione note e brainstorming preliminare"]
        B3["Identificazione di bias e schemi ciechi prima della supervisione umana"]
    end

    subgraph Rischi & Limiti Critici
        R1["Compiacenza algoritmica (Sycophancy)"]
        R2["Timore di De-skilling (Erosione del giudizio clinico autonomo)"]
        R3["Incapacità strutturale di riconoscere e gestire il rischio suicidario"]
        R4["Assenza totale di empatia autentica, saggezza e contenimento emotivo"]
    end

    Clinico["Terapeuta / Specializzando"] --> Benefici & Usi Percepiti
    Clinico --> Rischi & Limiti Critici
```

---

## Principali Risultanze Empiriche

### 1. Cautela Diffusa e Rifiuto della Sostituzione
- Il campione rifiuta compattamente l'idea che l'IA possa costituire un valido sostituto della supervisione umana (accordo estremamente basso).
- Gli intervistati evidenziano che l'IA non possiede saggezza clinica, non è in grado di cogliere la complessità delle dinamiche relazionali né di offrire un autentico supporto emotivo nei momenti di difficoltà del terapeuta.

### 2. Consapevolezza del Limite sul Rischio Suicidario e Quadri Complessi
- Si registra un accordo quasi plebiscitario sulla pericolosità dell'IA nei quadri psicopatologici gravi (psicosi, disturbi severi di personalità) e sull'incapacità dell'algoritmo di identificare l'ideazione e il rischio suicidario.

### 3. Timore di De-skilling e Differenze di Status Professionale
- Il timore che l'uso continuativo dell'IA possa **indebolire il pensiero e il giudizio clinico autonomo (*de-skilling*)** è ampiamente presente in entrambi i gruppi, ma risulta marcatamente più accentuato negli **allievi specializzandi** rispetto ai clinici esperti.
- Gli psicoterapeuti formati, forti della loro consolidata esperienza, utilizzano lo strumento con maggiore postura critica; gli specializzandi temono maggiormente di vedere compromessa la propria auto-efficacia in costruzione.

### 4. Determinanti Psicologiche Individuali: Colpa e Ansia Sociale
- **Timore della Colpa (sottoscala Punishment)**: La vulnerabilità morale al timore di arrecare danno mostra un'associazione positiva con la preoccupazione che delegare valutazioni all'IA possa compromettere la qualità dell'atto terapeutico.
- **Ansia Sociale (LSAS)**: L'evitamento sociale correla positivamente con l'attrattiva dell'IA come mezzo per attenuare l'ansia del giudizio del supervisore umano. Inoltre, l'ansia sociale spiega statisticamente il **10,3% della varianza** nel timore di de-skilling clinico.

---

## Limiti Epistemologici e Clinici dei Modelli Linguistici

| Limite Funzionale | Meccanismo Algoritmico | Impatto nella Supervisione |
| :--- | :--- | :--- |
| **Compiacenza (*Sycophancy*)** | Ottimizzazione RLHF volta a soddisfare le premesse dell'utente. | L'IA tende a confermare le ipotesi del clinico invece di svolgere il necessario ruolo di contraddittorio critico. |
| **Empatia Fittizia** | Simulazione lessicale priva di substrato affettivo e somatico. | Incapacità di offrire risonanza emotiva, validazione profonda e funzione di contenimento (*holding*). |
| **Allucinazione Diagnostica** | Generazione probabilistica su pattern statistici superficiali. | Rischio di proporre concettualizzazioni clinicamente fallaci o etichette nosografiche fuorvianti. |
| **Vulnerabilità Deontologica** | Elaborazione di informazioni sensibili su server di terze parti. | Violazione del segreto professionale e del GDPR in assenza di rigorosa anonimizzazione preventiva. |

---

## Raccomandazioni Operative e Governance

1. **Strumento Complementare, Mai Sostitutivo**: L'IA può essere utilmente impiegata come *sparring partner preliminare* (per riassumere sedute, identificare nomenclature teoriche o schematizzare note), mantenendo la supervisione con il clinico umano come fulcro irrinunciabile della formazione.
2. **Promozione dell'AI Literacy Critica**: Inserimento nei percorsi di specializzazione in psicoterapia di moduli formativi dedicati ai bias, alle allucinazioni e ai limiti epistemologici degli LLM.
3. **Consenso e Trasparenza**: Garanzia di consenso informato da parte del paziente e conformità alle normative sulla protezione dei dati (anonimizzazione radicale e server europei protetti).

---

## Evidenze dalla Letteratura: strumenti di IA per la supervisione in CBT

- Shafran et al. (2026) distinguono quattro usi dell'IA nella formazione e nella supervisione, con requisiti di dati diversi: paziente virtuale standardizzato, rating automatico della fedeltà, supervisione o feedback narrativo tramite agenti, consulente IA che risponde alle domande del supervisore.
- Nella pratica reale questi strumenti possono trascrivere e analizzare le sedute, preparare bozze di note e segnalare i momenti da rivedere in supervisione: opportunità mancate, deviazioni dal protocollo, interazioni critiche (Shafran et al., 2026). Per il rating della fedeltà vedi [[ctrs-automated-evaluation]].
- Architettura proposta: un agente fa da consulente conversazionale; un secondo agente, nascosto, guida il «terapeuta» sulla concettualizzazione del caso e riassume le decisioni delle consultazioni precedenti, sul modello della supervisione *bug-in-ear* (Shafran et al., 2026).
- L'IA potrebbe servire anche a formare i supervisori, analizzando le sedute di supervisione con strumenti standardizzati di valutazione delle competenze supervisive (Shafran et al., 2026).
- Rischi: [[algorithmic-paternalism-in-ai-mental-health|paternalismo algoritmico]] se le decisioni sul percorso dell'allievo vengono prese senza coinvolgerlo; perdita graduale di competenze in formatori e supervisori che si rimettono al giudizio della macchina; valutazioni opache e difficili da contestare. Per gli autori l'IA va usata insieme al giudizio umano e deve spiegare le proprie conclusioni (Shafran et al., 2026).
- **Feedback di supervisione generato da ChatGPT-4 (Cioffi et al., 2025).** Specializzandi in psicoterapia della Gestalt hanno valutato alla cieca tre feedback sullo stesso caso clinico: ChatGPT-4 senza contesto, ChatGPT-4 orientato da un prompt sulla supervisione gestaltica, un supervisore esperto. Il feedback orientato dal prompt è stato giudicato migliore di quello senza contesto nella dimensione relazionale ed emotiva, dove non differisce dal supervisore umano, e migliore anche del supervisore nell'orientamento professionale. Il supervisore umano è stato giudicato migliore nell'evidenziare le aree di miglioramento; su chiarezza, completezza e analisi delle tecniche non ci sono differenze. Lo studio usa un solo caso e un solo supervisore e misura la soddisfazione degli specializzandi, non gli effetti sulle competenze: vedi [[cioffi-et-al-2025]].
- Gli autori propongono una supervisione *blended* a due livelli, con un primo feedback dell'IA rivisto poi dal supervisore esperto, e l'uso dell'IA tra un incontro di supervisione e l'altro (Cioffi et al., 2025).
- La rassegna converge con quanto emerso nella lezione del 10 giugno (cfr. [[06-10-lezione-rag-llm]]): l'IA è un complemento, non un sostituto, della supervisione umana, e il rischio di de-skilling è centrale. Shafran et al. (2026) aggiungono che le prove sperimentali sui modelli di formazione e supervisione, con o senza IA, sono ancora scarse.

---

## Riferimenti Bibliografici
- Cioffi, V., Ragozzino, O., Mosca, L. L., Moretto, E., Tortora, E., Acocella, A., Montanari, C., Ferrara, A., Crispino, S., Gigante, E., Lommatzsch, A., Pizzimenti, M., Temporin, E., Barlacchi, V., Billi, C., Salonia, G., & Sperandeo, R. (2025). Can AI technologies support clinical supervision? Assessing the potential of ChatGPT. *Informatics*, *12*(1), 29. https://doi.org/10.3390/informatics12010029
- Shafran, R., Bond, L., Carlbring, P., Cohen, Z. D., Creed, T. A., Davey, E., Egan, S. J., Freeman, D., Hollon, S. D., Jacobson, N. C., Johnson, C., Kaysen, D., McGuinness, D. L., Patel, V., Pozuelo, J. R., Santos, H., Singla, D. R., Wiltsey Stirman, S., Taylor, D. J., & Wade, T. D. (2026). From innovation to implementation: Artificial intelligence in cognitive behaviour therapy training and supervision. *Behaviour Research and Therapy*, *197*, Article 104945. https://doi.org/10.1016/j.brat.2025.104945

---

## Relazioni
- [[shafran-et-al-2026]]
- [[cioffi-et-al-2025]]
- [[06-10-lezione-rag-llm]]
- [[modello-centauro-clinico]]
- [[uso-problematico-chatbot-ai]]
- [[augmented-psychotherapy]]
- [[digital-therapeutic-alliance]]
- [[human-in-the-reasoning]]
- [[ai-research-ethics]]
- [[ai-assisted-psychotherapy]]
- [[large-language-models]]
