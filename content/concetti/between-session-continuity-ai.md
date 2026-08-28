# Continuità Tra le Sedute e Mediazione dei Confini Temporali

**Summary**: Funzione di mediazione contestuale e relazionale (Stadio 4, Quan et al., 2025) in cui l'IA agisce come ponte asincrono tra una seduta di psicoterapia e la successiva, rispondendo al bisogno di presenza continuativa dei pazienti vulnerabili senza violare i confini professionali e il carico di lavoro del terapeuta.
**Sources**: Quan et al. (2025) - `2512.22462v1.pdf`, Oewel et al. (2024)
**Last updated**: 2026-08-27
---

## Il Conflitto dei Confini Temporali nell'Intervallo tra Sedute

Nell'intervallo tra le sedute di psicoterapia tradizionale (tipicamente a cadenza settimanale o quindicinale), emerge una tensione relazionale e strutturale tra due bisogni contrastanti:

1. **Il Bisogno di Contenimento del Paziente Vulnerabile**:
   - I pazienti appartenenti a minoranze o con elevata sofferenza vivono spesso momenti di acuta vulnerabilità nella vita quotidiana e desiderano un senso di "presenza continuativa" e ascolto (Quan et al., 2025: C1).
2. **I Confini Professionali ed Emotivi del Clinico**:
   - I terapeuti devono tutelare il proprio tempo libero, prevenire il burnout e mantenere rigorosi confini di setting (P2: *"I clienti possono inviarci messaggi, ma noi non possiamo e non dobbiamo rispondere fuori dall'orario clinico"*).

```mermaid
flowchart LR
    subgraph Tension ["Tensione Strutturale tra le Sedute"]
        P["Paziente Vulnerabile<br>(Bisogno di Presenza & Contenimento 24/7)"]
        VS["⚡ Conflitto di Aspettative"]
        T["Terapeuta<br>(Necessità di Confini Temporali & Setting Rigido)"]
        P --- VS --- T
    end

    subgraph Solution ["Mediazione Contestuale tramite LLM (Boundary Object)"]
        AI["Sistema LLM (Compagno Asincrono & Ponte Relazionale)"]
        P <-->|"Interazione Quotidiana, Diari, Esercizi"| AI
        AI -->>|"Sintesi Settimanale Distillata (Consenso P)"| T
    end

    Tension -->|Risolto da| Solution
```

---

## Funzioni Operative dell'IA nella Continuità tra Sedute

L'IA opera come un **mediatore di confine contestuale e relazionale**, assumendo tre funzioni principali:

### 1. Compagnia Asincrona e Decompressione (*24/7 Asynchronous Support*)
- Offre uno spazio di sfogo e ascolto in tempo reale nei momenti di disregolazione affettiva o solitudine notturna.
- Attenua l'ansia da disconnessione senza caricare il terapeuta di chiamate o messaggi fuori orario.

### 2. Sostegno all'Esecuzione dei Compiti a Casa (*Between-Session Activities*)
- Guida attiva nella compilazione di schede CBT, diari di monitoraggio dell'umore o pratiche di mindfulness.
- Adattamento degli esercizi alle contingenze reali del paziente (es. strategie discrete per gestire un attacco di panico sul posto di lavoro o in famiglia).

### 3. Triage e Rete di Sicurezza per la Crisi (*Crisis Safety Net*)
- Monitoraggio passivo di segnali di rischio acuto (autolesionismo, ideazione suicidaria) con reindirizzamento immediato a linee telefoniche di emergenza o protocolli concordati, allertando il clinico secondo le soglie prestabilite.

---

## Vantaggi Clinici del Modello

- **Riduzione del Tasso di Dropout**: Il paziente non si sente abbandonato tra una seduta e l'altra, mantenendo viva l'alleanza di lavoro.
- **Ottimizzazione del Tempo in Seduta**: Il clinico riceve un quadro pre-sintetizzato dell'andamento emotivo settimanale, potendo focalizzare i 50 minuti di colloquio sui nodi trasformativi più rilevanti.

---
## Concetti Correlati
- [[dynamic-boundary-mediation-framework]]
- [[boundary-objects-in-psychotherapy]]
- [[negotiable-data-visibility-privacy]]
- [[contextualized-relational-memory]]
- [[blended-care-ai-framework]]
- [[acute-crisis-action-plans-ai]]
