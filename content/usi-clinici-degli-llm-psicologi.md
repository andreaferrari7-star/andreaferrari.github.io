---
tags: [llm, psicologia-clinica, sintesi-query, supporto-clinico, documentazione-clinica, diagnosi]
tipo_fonte: [scientifica, interna, evento]
source_papers: ["Using_Large_Language_Models_in_Psychological_Resea.pdf", "final_textbook_genAIinpsychologyresearchandtraining.pdf", "2508.11398v2.pdf", "07-17 Riunione_ Corso di Formazione sull'IA in Psicologia e Utilizzo Clinico.txt", "[Italian (auto-generated)] Giornata Nazionale della Psicologia 2026 - IA – Intelligenza Artificiale Quo Vadis [DownSub.com].txt"]
---

# Usi Clinici degli LLM da parte degli Psicologi

## Definizione Operativa
- Sintesi guidata da quesito: come gli psicologi clinici impiegano i [[large-language-models]] nella pratica, nella documentazione e nella ricerca diagnostica.
- **Utilità CBT / Applicativa:** Orienta la scelta del tipo di impiego (supporto al colloquio, documentazione d'équipe, screening) in base a vantaggi e limiti documentati.

## Evidenze dalla Letteratura

### 1. Supporto al lavoro clinico quotidiano
- Trascrizione e sintesi dei colloqui, codifica di trascrizioni cliniche e sintesi della letteratura (Adeyemi, 2024; Adamkovič, 2025).
- Generazione di metafore per la ristrutturazione cognitiva e simulazione a scopo didattico (Adamkovič, 2025).
- Limiti: allucinazioni fattuali, forte sensibilità al prompt, assenza di autentica comprensione semantica o intenzionalità clinica (Adeyemi, 2024; Adamkovič, 2025).

### 2. Documentazione clinica "bottom-up" (prassi di gruppo)
- Nel progetto *inTherapy* gli LLM (es. Claude) elaborano le trascrizioni delle riunioni d'équipe ed estraggono caso indice, temi trasversali e snodi decisionali, producendo checklist e addendum operativi (cfr. [[07-17-riunione-corso-formazione]]).
- Il risultato è un *Living Clinical Document*, aggiornato per aree tematiche e con versioning: vedi [[bottom-up-clinical-documentation]].
- Si tratta di una pratica del gruppo, non di un dato empirico.

### 3. Screening diagnostico e simulazione
- Il framework multi-agente DSM5AgentFlow somministra il DSM-5 Level-1 con agenti terapeuta, paziente simulato e diagnosta con RAG sul DSM-5, producendo diagnosi provvisorie con razionali tracciabili (Ozgun et al., 2025). Vedi [[dsm5agentflow]] e [[ozgun-et-al-2025]].
- Il modello di ragionamento Qwen-QWQ-32b raggiunge F1 = 77% sulla diagnosi; i modelli conversazionali eccellono in realismo ed empatia del dialogo (Ozgun et al., 2025).
- Errori sistematici sui quadri sovrapposti: disturbo dell'adattamento confuso con depressione, bipolare con depressione (Ozgun et al., 2025).
- Strumento di ricerca su dialoghi sintetici, non dispositivo medico: serve validazione con clinici prima dell'uso pratico (Ozgun et al., 2025).

### 4. Diffusione tra gli psicologi italiani (survey CNOP)
- Una survey del CNOP su circa 6.000 psicologi, condotta tra dicembre 2025 e gennaio 2026, è stata presentata alla Giornata Nazionale della Psicologia 2026 (cfr. [[10-10-giornata-nazionale-psicologia-ia-quo-vadis]]). I risultati principali:
  - il 58% usa l'IA;
  - il 55% riferisce che i propri utenti la usano, anche tra una seduta e l'altra;
  - gli usi prevalenti sono ricerca e lavoro amministrativo;
  - la preoccupazione principale è l'impatto sulla relazione terapeutica, seguita da privacy, riservatezza e trasparenza;
  - la richiesta principale al CNOP è la formazione.
- I dati sono riferiti dalla coordinatrice del gruppo di lavoro CNOP; il documento con i risultati non è in `raw/` [da verificare].

## Lacune
- Nella wiki non esisteva una pagina di panoramica sul tema: questa sintesi si basa su tre pagine lette integralmente.
- Non sono state lette le pagine su sicurezza, bias e allineamento: [da verificare] se integrano o correggono il quadro.
- La pagina [[large-language-models]] cita Lin (2026) senza riferimento completo: omesso qui.

## Riferimenti Bibliografici
- Adamkovič, M. (2025). *Large Language Models in (Not Only) Psychology Training and Research: A Brief Introduction*. Centre of Social and Psychological Sciences, Slovak Academy of Sciences. https://doi.org/10.31577/2025.9788082980144
- Adeyemi, V. (2024). Using Large Language Models in Psychological Research: A New Frontier for Hypothesis Generation. *Premier Journal of Psychology*, 1–4.
- Ozgun, M. C., Pei, J., Hindriks, K., Donatelli, L., Liu, Q., & Wang, J. (2025). Trustworthy AI Psychotherapy: Multi-Agent LLM Workflow for Counseling and Explainable Mental Disorder Diagnosis. In *Proceedings of the 34th ACM International Conference on Information and Knowledge Management (CIKM '25)*. ACM. https://doi.org/10.1145/3746252.3761164

## Relazioni
- Vedi anche: [[large-language-models]], [[10-10-giornata-nazionale-psicologia-ia-quo-vadis]], [[bottom-up-clinical-documentation]], [[dsm5agentflow]], [[ozgun-et-al-2025]], [[ai-assisted-psychotherapy]], [[augmented-psychotherapy]], [[human-in-the-reasoning]]
