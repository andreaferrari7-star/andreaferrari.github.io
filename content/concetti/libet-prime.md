---
title: Libet Prime
created: 2026-08-27
last_updated: 2026-08-27
tags: [ai, libet, cbt, didattica, supervisione]
---

# Libet Prime

**Libet Prime** è un tutor clinico-didattico basato su LLM (Gemini Gem) specializzato sul modello LIBET (Life Themes and Plans in CBT), progettato per guidare gli allievi di psicoterapia nell'apprendimento teorico e nel ragionamento clinico attraverso un'architettura bimodale e maieutica.

## Definizione Operativa

Libet Prime è un agente conversazionale (*Gem* su piattaforma Google Workspace / Gemini) sviluppato per le scuole di psicoterapia cognitivo-comportamentale di SC Formazione (Studi Cognitivi).

L'obiettivo primario è fungere da tutor didattico-clinico per allenare le capacità di concettualizzazione e ragionamento dell'allievo.

### Funzioni principali
- **Chiarimento teorico**: Discrimina i costrutti del modello LIBET e delle psicoterapie cognitivo-comportamentali.
- **Analisi critica**: Aiuta a distinguere costrutti teoricamente o lessicalmente vicini.
- **Supporto alla formazione**: Guida lo studente nell'analisi di vignette cliniche, nella formulazione del caso e nella definizione di un razionale d'intervento.
- **Interrogazione maieutica**: Verifica la padronanza concettuale attraverso domande stimolo.

### Guardrails (Perimetro di utilizzo)
- **Non è un terapeuta**: Non interagisce con pazienti reali.
- **Non è un supervisore clinico**: Non valida decisioni su casi reali.
- **Non è uno strumento diagnostico**: Rifiuta l'emissione di diagnosi definitive.
- **Non è un oracolo generico**: Rigetta richieste fuori dominio.

## Evidenze dalla Letteratura

L'architettura del sistema si basa su una Knowledge Base dedicata di 33 capitoli e oltre 230 pagine, redatta dagli autori del modello. Il design implementa un comportamento bimodale:
1. **Ambito Teorico**: Risposte scolastiche ed esaustive.
2. **Ambito Clinico**: Postura maieutica (*Human-in-the-reasoning*), che incoraggia l'allievo a formulare autonomamente ipotesi cliniche anziché ricevere soluzioni preconfezionate.

L'agente utilizza un routing dinamico tra 5 modalità funzionali per gestire efficacemente i quesiti:
1. Spiegazione Teorica
2. Confronto e Distinzione di Costrutti
3. Ragionamento sulla Formulazione del Caso
4. Razionale e Ipotesi di Intervento
5. Interrogazione e Stimolo Riflessivo

**Riferimenti Bibliografici:**
- 07-10 Riunione_ Test e Valutazione di “Libet Prime” (Tutor AI per Libet_CBT), Trainer Simulator e Piano Operativo.
- 05-08 Riunione_ Sviluppo Knowledge Base AI, Etica e Applicazioni Cliniche.

## Relazioni

- [[07-10_Riunione_Test_Valutazione_Libet_Prime]]
- [[trainer-simulator]]
- [[testing-e-validazione-agenti-didattici]]
- [[ia-maieutica-e-co-ragionamento]]
- [[human-in-the-reasoning]]
- [[simulazione-pazienti-ai]]
- [[05-08_Riunione_Knowledge_Base]]
