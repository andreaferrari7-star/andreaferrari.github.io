---
tags: [dropout, cbt-online, early-dropout, late-dropout, pid-5, ampd, machine-learning, latent-class-analysis, clinical-decision-support, greta, therapeutic-alliance]
source_papers: ["Bollettino_IPERlab_inTherapy_N01 (1).pdf"]
---

# Differenziazione tra Dropout Precoce e Tardivo nella CBT Online (Early vs. Late Dropout)

## Definizione Operativa
La **differenziazione tra Dropout Precoce e Tardivo** (*Early vs. Late Dropout Distinction*) è un paradigma clinico e metodologico che dimostra come l'interruzione non programmata della psicoterapia cognitivo-comportamentale non costituisca un fenomeno omogeneo, ma si articoli in due processi qualitativamente e prognosticanente distinti guidati da fattori di rischio dissociati (Grazioli et al., 2026; Caselli et al., 2026):

1. **Dropout Precoce (*Early Dropout*, $\le$ 5ª seduta):** Interruzione prematura che avviene prima che i meccanismi specifici della CBT abbiano iniziato a produrre benefici clinici; è primariamente predetto da un basso livello di fattori protettivi biopsicosociali all'intake e da elevati tratti di **Disinibizione (PID-5)** (impulsività, intolleranza alla frustrazione e insofferenza verso la strutturazione iniziale del setting).
2. **Dropout Tardivo (*Late Dropout*, > 5ª seduta):** Interruzione che subentra nelle fasi avanzate del trattamento durante l'esposizione o la ristrutturazione attiva degli schemi di funzionamento; è primariamente predetto da elevati tratti di **Antagonismo (PID-5)** (diffidenza relazionale, rottura dell'alleanza terapeutica) e, nei pazienti con disturbo di personalità comorbido, si associa a un marcato deterioramento funzionale.
3. **Superiorità Dimensionale:** La modellazione statistica dimostra che le categorie diagnostiche DSM-5 e il mero numero di disturbi in comorbilità perdono potere predittivo una volta inserite le classi anamnestiche latenti (*Latent Class Analysis* - LCA) e i domini dimensionali del **PID-5 / AMPD**.

```mermaid
flowchart TD
    subgraph Intake ["Assessment Iniziale (ROM su GRETA)"]
        Anamnesi["Anamnesi Biopsicosociale<br/>(LCA: 3 Classi di Fattori Protettivi)"]
        PID5["Profilo Dimensionale PID-5<br/>(Disinibizione, Antagonismo, Distacco...)"]
    end

    subgraph Phase1 ["Prime 5 Sedute (Early Stage)"]
        RiskEarly{"Fattori di Rischio Precoce:<br/>• Bassi Fattori Protettivi (+52% Rischio)<br/>• Alta Disinibizione"}
        EarlyDrop["EARLY DROPOUT (≤ 5ª seduta)<br/>Meccanismo: Intolleranza alla strutturazione del setting & Impulsività"]
        StayEarly["Proseguimento del Percorso"]
    end

    subgraph Phase2 ["Dalla 6ª Seduta in Poi (Late Stage)"]
        RiskLate{"Fattori di Rischio Tardivo:<br/>• Alto Antagonismo<br/>• Comorbidità Disturbo Personalità"}
        LateDrop["LATE DROPOUT (> 5ª seduta)<br/>Meccanismo: Rottura Alleanza Terapeutica & Attrito Relazionale"]
        LateDropImpair["Severo Danno Funzionale Residuo (WSAS) nei Pazienti PD"]
        Completion["Completamento del Percorso (Completers)<br/>RCSI 71% (Dose: 17 sedute no-PD, 22 sedute PD)"]
    end

    Intake --> Phase1
    Anamnesi & PID5 --> RiskEarly & RiskLate
    RiskEarly -->|Insuccesso Setting| EarlyDrop
    RiskEarly -->|Tenuta Setting| StayEarly
    StayEarly --> Phase2
    RiskLate -->|Crisi Alleanza| LateDrop
    LateDrop --> LateDropImpair
    RiskLate -->|Manutenzione Alleanza| Completion
```

## Evidenze dalla Letteratura
### 1. Epidemiologia e Distribuzione Temporale dell'Abbandono
- **Tassi Globali:** Nella CBT online naturalistica, il tasso di dropout globale si attesta attorno al **30–35%** (Grazioli et al., 2025; Grazioli et al., 2026).
- **Concentrazione Iniziale:** La distribuzione temporale delle interruzioni è asimmetrica:
    - Il **50% dei dropout complessivi si consuma entro la 4ª seduta**.
    - Il **75% dei dropout complessivi si consuma entro la 10ª seduta**.

### 2. Dissociazione dei Predittori Biopsicosociali e di Personalità

| Dimensione Predittiva | Dropout Precoce ($\le$ 5ª seduta) | Dropout Tardivo (> 5ª seduta) | Meccanismo Clinico Sottostante |
| :--- | :---: | :---: | :--- |
| **Fattori Protettivi Anamnestici (LCA)** | **Forte predittore protettivo** (Alti fattori: **-52% rischio**) | Effetto attenuato / non significativo | Il supporto sociale e la stabilità abitativa proteggono l'ingaggio iniziale |
| **Disinibizione (PID-5)** | **Predittore specifico significativo** | Non predittivo | Bassa regolazione degli impulsi e insofferenza alle regole del setting |
| **Antagonismo (PID-5)** | Non predittivo | **Predittore specifico significativo** | Tendenza alla rivalità, diffidenza, rotture non riparate dell'alleanza |
| **Diagnosi Categoriale di PD** | Non predittiva (dopo controllo PID-5) | Non predittiva (dopo controllo PID-5) | Il formato categoriale maschera la variabilità dimensionale predittiva |
| **Esito Funzionale (WSAS post-dropout)** | Compromissione moderata | **Decadimento funzionale severo (specie in PD)** | L'interruzione durante l'attivazione emotiva avanzata lascia il paziente scompensato |

### 3. Implicazioni per il Clinical Decision Support (CDSS)
I modelli di Machine Learning (es. Random Forest, XGBoost) integrano *feature* dimensionali continue (tratti PID-5 e profili latenti LCA), superando le categorizzazioni nosografiche binarie. Il sistema di alert calcola una probabilità di interruzione dipendente dalla fase temporale del percorso:
- *Prime sedute:* Alert guidato da punteggi di Disinibizione e bassi supporti anamnestici $\rightarrow$ raccomandazione di consolidare il contratto terapeutico e chiarire le aspettative.
- *Sedute intermedie/avanzate:* Alert guidato da punteggi di Antagonismo $\rightarrow$ raccomandazione di esplorare attivamente attriti, sentimenti di incomprensione e rotture dell'alleanza.

**Riferimenti Bibliografici:**
- Grazioli, S., Canessa, N., Villa, G., De Francesco, S., Ocera, A., Galletti, E., Sassaroli, S., & Caselli, G. (2026). Distinguishing early from late dropout in online Cognitive Behavioral Therapy: the role of biopsychosocial anamnestic profiles and maladaptive personality traits. *Manoscritto in fase di pubblicazione*.
- Grazioli, S., Ocera, A., Notaristefano, I., Piron, R., Fanfoni, M., Terrazzan, L., Ruggiero, G. M., Sassaroli, S., & Caselli, G. (2025). Advancing Cognitive Behavioural Therapy Progress Tracking: A Study on the Design and Implementation of the Online Platform GRETA. *Psychological Reports*, DOI: 10.1177/00332941251409157.
- Caselli, G., Grazioli, S., Piron, R., Fanfoni, M., Giuri, S., Scaini, S., Ruggiero, G. M., & Sassaroli, S. (2026). Effectiveness of Cognitive Behavioral Therapy on anxiety and depression symptoms in naturalistic settings for patients with and without personality disorders. *British Journal of Clinical Psychology* (In revisione).

## Relazioni
- Vedi anche: [[bollettino-iperlab-intherapy-n01-1]], [[treatment-outcome-and-relapse-prediction]], [[clinical-fidelity-assessment]], [[process-based-therapy]], [[software-as-a-medical-device-salute-mentale]], [[000]]