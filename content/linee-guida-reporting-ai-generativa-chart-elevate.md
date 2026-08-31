---
tags: [reporting-guidelines, generative-ai, medical-ai, health-economics, heor, chart-statement, elevate-genai, evidence-based-medicine, living-guidelines, ai-ethics, clinical-transparency, hallucination-prevention, equator-network, ispor]
source_papers: ["Linee Guida per il Reporting dell'Intelligenza Artificiale Generativa in Medicina e Ricerca Economico-Sanitaria_ Analisi dei Quadri CHART ed ELEVATE-GenAI.pdf"]
---

# Linee Guida per il Reporting dell'Intelligenza Artificiale Generativa in Medicina e Ricerca Economico-Sanitaria: Analisi dei Quadri CHART ed ELEVATE-GenAI

## Definizione Operativa
Il documento costituisce un briefing metodologico comparativo dedicato all'analisi sinottica dei due principali quadri di riferimento internazionali per la rendicontazione scientifica dell'Intelligenza Artificiale Generativa ([[large-language-models|LLM]] e modelli di fondazione) nelle scienze mediche, cliniche ed economico-sanitarie:

1. **Lo Statement [[chart-reporting-guideline|CHART]] (*Chatbot Assessment Reporting Tool*):** standard registrato presso la rete [[chart-reporting-guideline|EQUATOR Network]] per gli studi che valutano le prestazioni dei chatbot nell'erogazione di consigli sanitari e nella sintesi di evidenze cliniche (*Chatbot Health Advice - CHA studies*).
2. **Il Framework [[elevate-genai-framework|ELEVATE-GenAI]] (*Evidence, Transparency, and Efficiency for Generative AI*):** standard sviluppato dal gruppo di lavoro ISPOR per l'impiego dei Large Language Models nell'Economia Sanitaria e nella Ricerca sugli Esiti (*Health Economics and Outcomes Research* - [[heor-generative-ai-validation|HEOR]]).

**Scopo e Rationale Metodologico:** Rispondere alla crisi di riproducibilità, all'opacità dei protocolli di prompt engineering e al rischio clinico derivante da [[accuratezza-vs-fattualita-in-genai|allucinazioni e bias]] negli studi biomedici, fornendo a clinici, revisori paritari, comitati etici, agenzie di [[comparative-ai-health-governance|Health Technology Assessment (HTA)]] e autorità regolatorie una base strutturata per valutare la trasparenza e la sicurezza delle applicazioni di GenAI in sanità.

## Evidenze dalla Letteratura

### 1. Inquadramento del Problema: La Necessità di Standard Rigorosi
L'esplosione dell'intelligenza artificiale generativa e dei modelli linguistici di grandi dimensioni nella pratica clinica e nella ricerca sui risultati sanitari ha generato un'urgente necessità di standard di rendicontazione trasparenti e condivisibili:
- **Eterogeneità e Mancanza di Trasparenza:** Una revisione sistematica preliminare su 137 studi eleggibili su chatbot sanitari ha documentato che meno del **40%** degli articoli riportava elementi metodologici essenziali, quali la data esatta di esecuzione delle query, la collocazione geografica dei test o il numero di sessioni di chat indipendenti utilizzate.
- **Rischi per i Pazienti e per le Politiche Sanitarie:** L'omissione dei prompt grezzi, la mancata specificazione della versione del modello (checkpoint esatto, parametri stocastici come temperatura e top-p) e l'assenza di protocolli rigorosi di verifica della fattualità aumentano il rischio di propagazione di errori diagnostici, allucinazioni farmacologiche e bias nosografici, compromettendo la fiducia tra clinici, decisori politici e pazienti.

### 2. Lo Statement CHART (Chatbot Assessment Reporting Tool)
Lo Statement CHART, annunciato alla fine del 2023 e pubblicato integralmente nel 2025, è stato sviluppato seguendo rigorosamente le linee guida metodologiche della rete EQUATOR Network.

**Struttura e Contenuti Chiave (12 Item Principali e 39 Sub-item):**
- **Identificatori del Modello:** Denominazione esatta, numero di versione/checkpoint, data di rilascio o di ultimo aggiornamento.
- **Dettagli del Modello:** Esplicitazione chiara dell'architettura e della natura del modello.
- **Prompt Engineering:** Descrizione dettagliata dell'evoluzione e della cronologia dei prompt.
- **Strategia di Query:** Percorso di accesso (API vs interfaccia web), date e luoghi delle interrogazioni.
- **Valutazione Performance:** Definizione operativa esplicita della *ground truth*.
- **Open Science & Etica:** Disponibilità pubblica dei dati grezzi, repository del codice e iperparametri.

### 3. Il Framework ELEVATE-GenAI per l'HEOR
Sviluppato dall'ISPOR Working Group on Generative AI, ELEVATE-GenAI introduce uno standard specifico per l'uso dei Large Language Models nell'HEOR, focalizzandosi su:
1. **Revisioni Sistematiche della Letteratura (SLR):** Screening automatizzato, estrazione tabellare, valutazione rischio di bias.
2. **Modellazione Economica Sanitaria (HEM):** Generazione e validazione di script computazionali.
3. **Generazione di Evidenze dal Mondo Reale (RWE):** Estrazione, pulizia e strutturazione di dati non strutturati.

**I 10 Domini di Reporting:**
1. Caratteristiche del Modello
2. Valutazione Accuratezza
3. Completezza (*Comprehensiveness*)
4. Verifica Fattualità
5. Riproducibilità e Generalizzabilità
6. Contesto di Deployment
7. Robustezza
8. Equità e Bias (*Fairness*)
9. Calibrazione e Incertezza
10. Sicurezza e Privacy

### 4. Temi Trasversali
- **Accuratezza vs. Fattualità:** Necessità di distinguere tra coerenza stilistica e veridicità empirica.
- **Sicurezza e Privacy:** Protezione dei dati sensibili (PHI) e conformità normativa.
- **Bias Algoritmico:** Monitoraggio delle disparità nei dataset.
- **Living Guidelines:** Natura dinamica dei framework per adattarsi all'evoluzione dei modelli.

**Riferimenti Bibliografici:**
- Riferimenti completi inclusi nel documento originale citato nei metadati (`source_papers`).

## Relazioni
- [[chart2025-1|CHART Statement 2025]]
- [[elevate-genai2025-1|ELEVATE-GenAI 2025]]
- [[heor-generative-ai-validation|Validazione della GenAI nell'Economia Sanitaria (HEOR)]]
- [[accuratezza-vs-fattualita-in-genai|Accuratezza vs. Fattualità]]
- [[living-guidelines-in-health-ai|Living Guidelines nell'Intelligenza Artificiale Sanitaria]]
- [[comparative-ai-health-governance|Governance Comparativa dell'IA in Sanità]]
