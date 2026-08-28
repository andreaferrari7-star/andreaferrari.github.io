# Dynamic Boundary Mediation Framework

**Summary**: Framework concettuale e socio-tecnico formulato da Quan et al. (2025) che definisce il ruolo dei sistemi LLM come mediatori relazionali adattivi in psicoterapia, articolando tre meta-ruoli di mediazione (Epistemica, Relazionale, Contestuale) distribuiti lungo 5 stadi del percorso terapeutico per supportare popolazioni vulnerabili e marginalizzate.
**Sources**: Quan et al. (2025) - `2512.22462v1.pdf`
**Last updated**: 2026-08-27
---

## Definizione e Razionale

Il **Dynamic Boundary Mediation Framework** (Quan et al., 2025) ridefinisce l'integrazione dei Large Language Models (LLM) nella salute mentale. Superando sia la visione dell'IA come mero strumento documentale per il clinico sia quella dell'agente autonomo di auto-aiuto disconnesso dalla relazione, il framework concettualizza l'IA come un **mediatore relazionale dinamico** (*relational mediator*) capace di rimodulare le proprie funzioni in base alla fase terapeutica e ai bisogni di soggetti vulnerabili (es. comunità LGBTQ+, fasce a basso reddito, pazienti cronici).

```mermaid
flowchart TD
    subgraph MetaRoles ["Tre Meta-Ruoli di Mediazione"]
        EM["Mediazione Epistemica<br>Traduzione di conoscenze & riduzione asimmetrie"]
        RM["Mediazione Relazionale<br>Ribilanciamento del potere & sicurezza affettiva"]
        CM["Mediazione Contestuale<br>Ponte setting clinico - vita quotidiana"]
    end

    subgraph Stages ["5 Stadi del Percorso Terapeutico"]
        S1["1. Matching & Contatto Iniziale"]
        S2["2. Costruzione Fiducia & Autosvelamento"]
        S3["3. Espressione Clinica & Alleviamento Educator Burden"]
        S4["4. Continuità Tra le Sedute"]
        S5["5. Chiusura & Integrazione nel Mondo Reale"]
    end

    EM -.->|Primaria in| S1 & S3
    RM -.->|Primaria in| S1 & S2 & S3 & S4 & S5
    CM -.->|Primaria in| S4 & S5
```

---

## I Tre Meta-Ruoli di Mediazione

### 1. Mediazione Epistemica (*Epistemic Mediation*)
- **Obiettivo**: Ridurre le asimmetrie informative e colmare il divario epistemico tra la conoscenza clinico-istituzionale del terapeuta e la conoscenza situata/vissuta del paziente.
- **Funzioni chiave**:
  - *Traduzione dell'esperienza soggettiva*: Formalizzazione del disagio psicologico in costrutti clinici interpretabili senza snaturare l'autenticità del vissuto.
  - *Abbattimento dell'[[educator-burden-marginalized-clients|Educator Burden]]*: Fornitura proattiva al terapeuta di nozioni identitarie e contesti subculturali, evitando che il paziente debba impiegare tempo ed energie a "istruire" il professionista.

### 2. Mediazione Relazionale (*Relational Mediation*)
- **Obiettivo**: Ribilanciare le asimmetrie di potere, promuovere la sicurezza psicologica e offrire uno spazio intermedio a basso rischio per regolare il ritmo dell'autosvelamento.
- **Funzioni chiave**:
  - *Gestione Negoziabile dei Confini*: [[negotiable-data-visibility-privacy|Architettura di privacy multilivello]] (condivisione istantanea, parziale o totale riserbo).
  - *Buffer Relazionale Non-Giudicante*: Spazio dialogico che riduce la paura del rifiuto e permette di testare la propria vulnerabilità prima della seduta formale.

### 3. Mediazione Contestuale (*Contextual Mediation*)
- **Obiettivo**: Risolvere la discontinuità tra il setting protetto della terapia e la complessità spesso ostile o non supportiva della vita quotidiana (*lack of contextual portability*).
- **Funzioni chiave**:
  - *[[between-session-continuity-ai|Continuità Asincrona]]*: Presenza di supporto 24/7 tra le sedute, consolidamento degli esercizi e diario emotivo.
  - *Supporto alla Chiusura e Crisi*: Strumenti di riflessione longitudinale e canali di emergenza attivi dopo il termine del trattamento.

---

## Dinamica Evolutiva attraverso i 5 Stadi

```mermaid
sequenceDiagram
    autonumber
    actor P as Paziente Marginalizzato
    participant AI as Sistema LLM (Boundary Object)
    actor T as Psicoterapeuta

    Note over P,T: Stadio 1: Matching & Contatto Iniziale
    P->>AI: Esplorazione bisogni identitari e preferenze
    AI-->>T: Profilo pre-screening strutturato (consenso P)
    
    Note over P,T: Stadio 2: Costruzione Fiducia & Autosvelamento
    P->>AI: Diario riflessivo a privacy graduata
    AI->>P: Rispecchiamento empatico non giudicante
    
    Note over P,T: Stadio 3: Espressione Clinica (Seduta)
    AI-->>T: Pre-caricamento glossario identitario / vissuti
    P->>T: Dialogo clinico mirato (senza educator burden)
    
    Note over P,T: Stadio 4: Continuità Tra Sedute
    P->>AI: Check-in emotivo e compiti tra le sedute
    AI-->>P: Regolazione affettiva e continuità narrativa
    
    Note over P,T: Stadio 5: Chiusura & Integrazione
    P->>AI: Pratica autonoma di abilità relazionali e piano crisi
```

---

## Rilevanza Clinica e per l'HCI

1. **Superamento del Modello Strumento-Puro**: Il sistema non è un mero esecutore algoritmico, ma un attore sociotecnico che modula le relazioni umane senza sostituirsi all'etica del curante.
2. **Accountability Relazionale**: L'efficacia dell'IA viene valutata non solo su metriche computazionali (accuratezza, engagement), ma sulla sua capacità di proteggere l'alleanza terapeutica e redistribuire il carico emotivo.

---
## Concetti Correlati
- [[boundary-objects-in-psychotherapy]]
- [[educator-burden-marginalized-clients]]
- [[negotiable-data-visibility-privacy]]
- [[contextualized-relational-memory]]
- [[between-session-continuity-ai]]
- [[interazione-triadica-terapeuta-paziente-ia]]
- [[ai-mental-health-vulnerable-populations]]
