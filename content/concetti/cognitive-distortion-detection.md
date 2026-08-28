---
tags: [cbt, cognitive-distortions, nlp, machine-learning, llm, mentalbert, ernie, text-classification]
source_papers: ["2407.19422v1.pdf"]
title: "Cognitive Distortion Detection"
---

# Cognitive Distortion Detection (Rilevazione Computazionale delle Distorsioni Cognitive)

## Definizione Operativa
L'applicazione di modelli di Elaborazione del Linguaggio Naturale (NLP), Reti Neurali Profonde e Large Language Models (LLM) per identificare, estrarre e classificare automaticamente schemi di pensiero disfunzionali e irrazionali (*Cognitive Distortions* - CD) all'interno di testi, trascrizioni cliniche, post su social media o diari terapeutici (Jiang et al., 2024).

Secondo la teoria cognitiva standard di Beck e la tassonomia di Burns (Burns & Beck, 1999), le distorsioni cognitive comprendono tipicamente 10-15 categorie cliniche:
1. Pensiero tutto-o-nulla (*All-or-nothing thinking / Dichotomous reasoning*)
2. Ipergeneralizzazione (*Overgeneralization*)
3. Filtro mentale (*Mental filter*)
4. Squalificare il positivo (*Disqualifying the positive*)
5. Saltare alle conclusioni (*Jumping to conclusions: Mind reading / Fortune telling*)
6. Catastrofizzazione e minimizzazione (*Magnification & Minimization*)
7. Ragionamento emotivo (*Emotional reasoning*)
8. Doverizzazioni (*Should statements*)
9. Etichettamento (*Labeling and mislabeling*)
10. Personalizzazione e colpevolizzazione (*Personalization and blaming*)

---

## Architetture e Modelli Computazionali

```mermaid
graph TD
    A["Input Utente / Trascrizione Clinica"] --> B["Preprocessing & Topic Modeling (BERTopic, AraBERT)"]
    B --> C{Approccio di Modellazione}
    
    C -->|Classificazione Supervisionata / PTMs| D["Domain-Specific Transformers<br/>(MentalBERT, ERNIE 3.0, BERT, RoBERTa)"]
    C -->|Multimodalità (Multitask)| E["Framework Decode<br/>(Fusione Testo + Audio + Espressioni Facciali)"]
    C -->|LLM Prompting & Reasoning| F["Diagnosis of Thought - DoT<br/>(Generazione di razionali diagnostici)"]
    
    F -->|Rischio: Over-Diagnosis| G["Extraction-Reasoning-Debate - ERD<br/>(Multi-Agent LLM Debate)"]
    
    D --> H["Output: Categoria CD & Livello di Confidenza"]
    E --> H
    G --> H
```

---

## Metodologie Avanzate ed Evidenze

### 1. Pre-trained Language Models (PTMs) Specifici di Dominio
- **MentalBERT & AraBERT:** L'uso di modelli pre-addestrati su corpora di salute mentale ha mostrato una superiorità marcata rispetto a classificatori convenzionali nel gestire lo squilibrio delle classi (*data imbalance*) e testi brevi privi di contesto (Ding et al., 2022; Alhaj et al., 2022).
- **ERNIE 3.0:** Adottato per costruire classificatori gerarchici basati sul modello **ABCD** della CBT, consentendo di disambiguare contemporaneamente la credenza disfunzionale e l'emozione secondaria associata (Jiang et al., 2024).

### 2. Rilevazione Multimodale (Decode Framework)
- L'integrazione congiunta di canali testuali, segnali acustici vocali e micro-espressioni visive ha permesso di superare i limiti dell'analisi puramente lessicale, catturando l'incongruenza tra contenuto verbale e tono affettivo (Singh et al., 2023).

### 3. Dai Modelli di Prompting Semplici al Multi-Agent Debate
- **Diagnosis of Thought (DoT):** Framework che forza il LLM a generare una catena di ragionamento diagnostico prima di attribuire l'etichetta di distorsione (Chen et al., 2023). Limite principale: propensione alla *sovradiagnosi* (*over-diagnosis*), classificando anche enunciati benigni o fisiologiche espressioni di sconforto come distorsioni patologiche.
- **Extraction-Reasoning-Debate (ERD):** Architettura a più agenti LLM che svolgono separatamente i ruoli di estrazione, contestualizzazione e dibattito critico incrociato (Lim et al., 2024). Ha ridotto significativamente i falsi positivi del DoT, dimostrando prestazioni vicine a quelle dei clinici umani esperti.

---

## Mappatura dei Dataset di Benchmark

| Dataset | Autori & Anno | Dimensione Campionaria | Classi CD | Lingua & Modalità |
| :--- | :--- | :--- | :--- | :--- |
| **CrowdDist & MH** | Shickel et al. (2020) | 7.666 testi crowdsourced + dati TAO Connect | 15 distorsioni | Inglese, Testo |
| **C2D2** | Wang et al. (2023a) | 7.500 istanze verificate da esperti | 7 categorie principali | Cinese, Testo |
| **Elsharawi & El Bolock** | Elsharawi & El Bolock (2024) | 34.370 testi (Twitter, Facebook, Crowdsource) | 14 distorsioni | Inglese, Testo |
| **Therapist Q&A / CDD** | Shreevastava & Foltz (2021); Lim et al. (2024) | 2.530 – 3.000 campioni (Kaggle) | 10–11 classi | Inglese, Testo |
| **CBT-LLM Dataset** | Na (2024) | 22.327 campioni da forum clinici (PsyQA) | 10 classi | Cinese, Testo |

---

## Sfide Metodologiche e Utilità CBT
- **Soggettività di Annotazione (*Inter-rater Reliability*):** La definizione dei confini tra categorie di distorsione (es. *catastrofizzazione* vs *saltare alle conclusioni*) varia notevolmente tra gli annotatori.
- **Supporto all'Assessment e Co-Ragionamento:** In contesto clinico, il modulo di detection non formula diagnosi definitive ma offre al terapeuta (o all'utente in app di auto-aiuto) ipotesi di lavoro trasparenti da verificare mediante dialogo socratico.

---

## Relazioni
- [[automated-cognitive-restructuring]]: Fase successiva di ristrutturazione del pensiero individuato.
- [[ai-enhanced-cbt]]: Collocazione nell'assessment pre-trattamento e durante la terapia.
- [[cbt-dialogue-systems-and-tools]]: Integrazione nei motori conversazionali (es. TeaBot, Woebot).
- [[jiang-et-al-2024]]: Review sistematica di base.
