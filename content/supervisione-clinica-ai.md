# Supervisione Clinica e Intelligenza Artificiale

**Summary**: Inquadramento teorico ed evidenze empiriche sull'utilizzo dei Large Language Models e chatbot come strumenti a supporto della supervisione e dell'intervisione in psicoterapia. L'analisi include lo studio pionieristico di Cosentino et al. (2026) su allievi specializzandi e terapeuti esperti, focalizzandosi su timore della colpa, ansia sociale, rischi di de-skilling e sycophancy.
**Sources**: 06-10 Lezione_ RAG, LLM in Psicoterapia e Governance Etica.txt
**Last updated**: 2026-08-27
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

## Related pages
- [[06-10_Lezione_RAG_LLM]]
- [[modello-centauro-clinico]]
- [[uso-problematico-chatbot-ai]]
- [[augmented-psychotherapy]]
- [[digital-therapeutic-alliance]]
- [[human-in-the-reasoning]]
- [[ai-research-ethics]]
- [[ai-assisted-psychotherapy]]
- [[large-language-models]]
