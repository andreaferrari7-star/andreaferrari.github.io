---
tags: [mi-claim-gen, reporting-guidelines, clinical-ai-evaluation, research-transparency, reproducibility, generative-ai, model-cards, joanna-briggs-institute, mental-health-ai]
source_papers: ["mental_v12i1e70610.pdf"]
---

# MI-CLAIM-GEN Checklist

## Definizione Operativa
- La **MI-CLAIM-GEN Checklist** (*Minimum Information about Clinical Artificial Intelligence for Generative Modeling Research*) è lo standard metodologico internazionale di rendicontazione elaborato da Miao et al. (2025; *Nature Medicine*, doi: [10.1038/s41591-024-03470-0](https://doi.org/10.1038/s41591-024-03470-0)) specificamente concepito per valutare la qualità, la trasparenza e la riproducibilità degli studi clinici basati su Intelligenza Artificiale Generativa (GenAI) e Large Language Models (LLM) in sanità e salute mentale.
- **Architettura a 5 Domini Metodologici:** Struttura la valutazione della trasparenza scientifica su cinque aree chiave: (1) *Study Design*, (2) *Resources and Optimization*, (3) *Model Performance and Evaluation*, (4) *Model Examination and Safety*, e (5) *Reproducibility and Open Science*.
- **Utilità Clinica e Psicoterapia CBT:** Costituisce uno strumento fondamentale di *critical appraisal* per clinici e ricercatori per discernere tra modelli con eccellenza teorica/aneddotica e sistemi realmente validati per la pratica clinica, smascherando studi affetti da opacità dei dati di training, assenza di audit sui danni iatrogeni (*harm assessment*) e totale irriproducibilità dei prompt.

```mermaid
flowchart TD
    subgraph MICLAIM_Ecosystem ["Ecosistema delle Linee Guida di Reporting Clinico per l'IA"]
        R1["<b>MI-CLAIM (2020)</b><br/>Machine Learning tradizionale & Visione artificiale in medicina"]
        R2["<b>TRIPOD+AI / CONSORT-AI</b><br/>Modelli predittivi clinici & Trial randomizzati controllati"]
        R3["<b>ELEVATE-GenAI / CHART / GAMER</b><br/>Linee guida per HEOR, Chatbot sanitari e Revisioni"]
        R4["<b>MI-CLAIM-GEN (2025)</b><br/>Modelli Generativi (LLM, VLM) in compiti clinici e salute mentale"]
        R1 --> R4
    end

    subgraph FiveDomains ["I 5 Domini Fondazionali di MI-CLAIM-GEN"]
        D1["<b>1. Study Design (Items 1.1-1.5)</b><br/>Contesto, quesito clinico, popolazione, rappresentatività dati"]
        D2["<b>2. Resources & Optimization (Items 2.1-2.4)</b><br/>Architettura, compute budget, fine-tuning, efficienza"]
        D3["<b>3. Model Performance (Items 3.1-3.4)</b><br/>Metriche cliniche, framework multi-skill, output, baseline"]
        D4["<b>4. Model Examination (Items 4.1-4.5)</b><br/>Analisi errori, bias sociodemografico, audit danni, real-world"]
        D5["<b>5. Reproducibility (Items 5.1-5.3)</b><br/>Tier-1 (prompt/seed/temp), Model Cards, pesi/codice aperti"]
    end

    MICLAIM_Ecosystem --> FiveDomains
```

---

## Evidenze dalla Letteratura

### 1. I 5 Domini Metodologici di MI-CLAIM-GEN

| Dominio | Sotto-Componenti e Requisiti di Trasparenza | Stato di Conformità nella Salute Mentale (Wang et al., 2025) |
| :--- | :--- | :---: |
| **1. Study Design** | • **1.1 Contesto Clinico:** Razionale e setting di cura.<br/>• **1.2 Quesito di Ricerca:** Formulazione clinica esplicita.<br/>• **1.3 Task Definition:** Input/output previsti.<br/>• **1.4 Popolazione:** Caratteristiche demografiche.<br/>• **1.5 Rappresentatività Dati:** Documentazione del dataset di training originario. | **73.9% conformità complessiva**<br/>(Item 1.1 al 97%, Item 1.2 al 100%, ma Item 1.5 **solo all'11%**) |
| **2. Resources & Optimization** | • **2.1 Architettura & Pesi:** Modello, versione, checkpoint esatto.<br/>• **2.2 Compute Infrastructure:** Hardware (GPU/TPU) e consumi.<br/>• **2.3 Hyperparameters:** Parametri di tuning, LoRA, temperature, top-p.<br/>• **2.4 Efficienza Computazionale:** Latenza e throughput. | **25.3% conformità complessiva**<br/>(Grave sotto-rendicontazione delle risorse e dei parametri di inferenza) |
| **3. Model Performance & Evaluation** | • **3.1 Metriche Cliniche & NLP:** Accuratezza, sensibilità, F1, BLEU, ROUGE.<br/>• **3.2 Framework Olistico:** Valutazione multi-skill contestuale.<br/>• **3.3 Descrizione Output:** Trascrizioni qualitative delle risposte.<br/>• **3.4 Baseline Comparison:** Confronto con modelli preesistenti o umani. | **56.0% conformità complessiva**<br/>(Item 3c all'89%, ma framework di valutazione completo **solo al 20%**) |
| **4. Model Examination & Safety** | • **4.1 Error Analysis:** Tipologia e frequenza di allucinazioni.<br/>• **4.2 Demographic Fairness:** Audit di disparità (sesso, etnia, età).<br/>• **4.3 Robustness:** Stress testing e stabilità del prompt.<br/>• **4.4 Real-World Setting:** Valutazione in condizioni d'uso ecologiche.<br/>• **4.5 Harm Assessment:** Valutazione post-deployment dei danni potenziali. | **54.1% conformità complessiva**<br/>(Valutazione in setting reali e audit dei danni quasi completamente assenti) |
| **5. Reproducibility & Open Science** | • **5.1 Tier-1 Reproducibility:** Rilascio di prompt esatti, seed, script di pipeline.<br/>• **5.2 Model Card / System Card:** Documentazione standardizzata di scopo e limiti.<br/>• **5.3 Open Artifacts:** Repository pubblici di codice e pesi (GitHub/Zenodo). | **5.5% conformità complessiva**<br/>(**0% di Model Cards formali**, solo il 14% raggiunge la conformità Tier-1) |

---

### 2. Risultati dell'Audit Empirico sulla GenAI in Salute Mentale (Wang et al., 2025)

Nell'applicazione sistematica della checklist MI-CLAIM-GEN su un corpus di 79 studi peer-reviewed (periodo 2019–2024), Wang, Zhou e Zhou (2025) hanno riscontrato un punteggio medio di conformità pari al **45.39%** (753/1659 item valutati positivamente secondo il protocollo Joanna Briggs Institute; Santos et al., 2018):

```mermaid
pie title Disparità di Rendicontazione negli Studi di GenAI per la Salute Mentale
    "Study Design (Forte: 73.9%)" : 73.9
    "Model Performance (Medio: 56.0%)" : 56.0
    "Model Examination (Medio: 54.1%)" : 54.1
    "Resources & Optimization (Critico: 25.3%)" : 25.3
    "Reproducibility & Open Science (Allarmante: 5.5%)" : 5.5
```

#### Snodi Critici Emersi dall'Audit:
1. **La "Scatola Nera" dei Dati di Addestramento (Item 1.5):** Solo l'**11%** degli studi descrive la composizione sociodemografica o la rappresentatività dei dati di pretraining/fine-tuning. Tale omissione impedisce di stimare il rischio di bias culturale (WEIRD bias) o di mancata decodifica di manifestazioni somatiche del disagio psicologico (Ryder et al., 2008).
2. **Deficit dei Framework di Valutazione Olistica (Item 3b):** Solo il **20%** degli studi adotta un framework di valutazione multidimensionale che esamini congiuntamente accuratezza teorica, sicurezza, aderenza alle linee guida, tenuta relazionale ed empatia percepita. Il restante 80% ricade nella *single-task zero-shot trap* (Wang et al., 2025).
3. **Assenza di Validazione in Setting Reali e Audit dei Danni (Items 4d, 4e):** La quasi totalità delle pubblicazioni valuta i modelli su vignette cliniche sintetiche o benchmark chiusi, trascurando l'impatto clinico effettivo su pazienti reali (*in-the-wild evaluations*).
4. **Crisi della Riproducibilità Scientifica (Dominio 5):** **Nessuno studio (0%) ha fornito una Model Card formale** e solo il **14%** ha soddisfatto i criteri di riproducibilità *Tier-1* (pubblicazione del prompt integrale con relative istruzioni di sistema, temperature, top-p e seed numerico).

---

## Integrazione con altri Standard di Reporting Clinico

```mermaid
graph TD
    A["Linee Guida di Trasparenza per l'IA in Sanità"] --> B["<b>MI-CLAIM-GEN (Miao et al., 2025)</b><br/>Focus: Valutazione architetturale, training data, model cards, harm audit per GenAI"]
    A --> C["<b>ELEVATE-GenAI (Fleurence et al., 2025)</b><br/>Focus: Trasparenza, efficienza, living reviews ed evidenze HEOR"]
    A --> D["<b>CHART Statement (2025)</b><br/>Focus: Chatbot sanitari erogatori di consigli medici/psicologici"]
    A --> E["<b>GAMER Guidelines (2025)</b><br/>Focus: Reporting dell'uso di GenAI nella stesura di manoscritti e sintesi"]

    B -.->|Fornisce standard di audit per| C
    B -.->|Complementare a| D
```

---

## Raccomandazioni per la Ricerca e l'Uso Clinico

1. **Adozione Obbligatoria delle Model Cards nei Trial di Salute Mentale:**
   - Ogni modello o pipeline proposta deve essere corredata da una *Model Card* standardizzata che specifichi esplicitamente i casi d'uso previsti (*intended use*), i contesti d'uso controindicati (*out-of-scope uses*), le popolazioni testate e le limitazioni note (Miao et al., 2025; Wang et al., 2025).
2. **Rilascio Integrale dei Parametri Tier-1:**
   - Pubblicare sistematicamente la formulazione esatta dei prompt di sistema (*system prompt*), le catene di ragionamento (*few-shot exemplars*, catene CoT), le temperature di campionamento e le versioni di runtime per garantire la verificabilità empirica indipendente.
3. **Audit dei Danni Post-Deployment (*Harm Assessment*):**
   - Integrare protocolli longitudinali per il monitoraggio continuativo di effetti iatrogeni, dipendenza emotiva, allucinazioni diagnostiche e interruzioni traumatiche del dialogo terapeutico.

---

**Riferimenti Bibliografici:**
- Miao, B. Y., Chen, I. Y., Williams, C. Y., Davidson, J., Garcia-Agundez, A., Sun, S., et al. (2025). The MI-CLAIM-GEN checklist for generative artificial intelligence in health. *Nature Medicine*, 31(5), 1394–1398. https://doi.org/10.1038/s41591-024-03470-0
- Wang, X., Zhou, Y., & Zhou, G. (2025). The Application and Ethical Implication of Generative AI in Mental Health: Systematic Review. *JMIR Mental Health*, 12, e70610. https://doi.org/10.2196/70610
- Fleurence, R. L., et al. (2025). ELEVATE-GenAI: Reporting Guidelines for Generative AI in Health Economics and Outcomes Research. *Value in Health*, 28(6), 701–712. https://doi.org/10.1016/j.jval.2025.06.018
- Ryder, A. G., Yang, J., Zhu, X., et al. (2008). The cultural shaping of depression: somatic symptoms in China, psychological symptoms in North America? *Journal of Abnormal Psychology*, 117(2), 300–313. https://doi.org/10.1038/0021-843X.117.2.300
- Santos, W. M., Secoli, S. R., & Püschel, V. A. (2018). The Joanna Briggs Institute approach for systematic reviews. *Revista Latino-Americana de Enfermagem*, 26, e3074. https://doi.org/10.1590/1518-8345.2885.3074

---

## Relazioni
- Vedi anche: [[mental-v12i1e70610]], [[genai4mh-framework]], [[elevate-genai-framework]], [[chart-reporting-guideline]], [[gamer-reporting-guideline]], [[single-task-zero-shot-evaluation-trap]], [[clinician-user-evaluation-discrepancy]], [[five-domain-chatbot-validation-framework]], [[traffic-light-quality-appraisal-clinical-ai]], [[gai-research-integrity-and-verification]]
