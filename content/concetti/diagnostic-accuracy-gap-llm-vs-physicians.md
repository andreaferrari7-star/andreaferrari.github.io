---
tags: [diagnostic-accuracy, clinical-decision-support, large-language-models, physician-vs-ai, meta-analysis, primary-diagnosis, differential-diagnosis, emergency-triage, medical-reasoning, tacit-knowledge]
source_papers: ["medinform-v13-e64963.pdf"]
---

# Diagnostic Accuracy Gap: Large Language Models vs Clinical Professionals

## Definizione Operativa
Il **Diagnostic Accuracy Gap** (Divario di Accuratezza Diagnostica) definisce la discrepanza quantitativa e qualitativa di prestazione riscontrata tra i modelli linguistici di grandi dimensioni ([[large-language-models|LLM]]) e i professionisti sanitari qualificati nella formulazione di diagnosi cliniche accurate, stratificazione del rischio e diagnosi differenziale.

- **Evidenza Meta-Analitica Globale (Shan et al., 2025):** Sintetizzando 30 studi clinici primari ($N = 4.762$ casi) e conducendo una meta-analisi su 18 studi mirati sulla diagnosi primaria ($N = 1.472$ casi), la ricerca ha stabilito che i medici superano in modo statisticamente significativo gli LLM:
  $$\text{Pooled Odds Ratio: } \text{OR} = 0.71 \quad (95\%\text{ CI } [0.60, 0.84], Z = 4.06, P < .0001)$$
  con una percentuale di successo globale del **$71.8\%$ per i clinici umani** contro il **$65.1\%$ per i modelli LLM ottimali**.
- **La Tripartizione Funzionale delle Competenze:** Il divario di accuratezza non è omogeneo ma si distribuisce su tre livelli gerarchici di complessità cognitiva:
  1. **Triage e Urgenza (Parità/Vantaggio IA):** Accuratezza $66.5\% - 98.0\%$;
  2. **Diagnosi Differenziale Top-N (Parità/Recall Elevato):** Inclusione del target patologico nel $70\% - 98.3\%$ dei casi;
  3. **Diagnosi Primaria Singola (Netto Vantaggio Umano):** Accuratezza $25.0\% - 97.8\%$, con superiorità umana nel $66.7\%$ degli studi comparativi.

## Evidenze dalla Letteratura

### Meccanismi Epistemologici e Cognitivi
1. **Conoscenza Tacita (*Polanyi's Paradox*):** La pratica medica esperta si fonda su conoscenza tacita e *clinical gestalt*, integrando indizi non strutturati che gli LLM, operando su base simbolico-testuale, faticano a cogliere.
2. **Correlazione vs Ragionamento:** Mentre gli LLM sono predittori probabilistici basati sulla frequenza lessicale, i medici applicano modelli causali-fisiopatologici.
3. **Gestione dell'Incertezza:** La [[single-correct-answer-fallacy-in-clinical-ai|Fallacia della Risposta Corretta Singola]] penalizza gli LLM, che faticano a gestire l'iteratività del processo diagnostico clinico.
4. **Bias Demografici:** Gli LLM mostrano bias sistematici in base a variabili anagrafiche (etnia, genere) presenti nei dati di pretraining.

### Analisi per Setting (Shan et al., 2025)
- **Triage (ED):** Parità o vantaggio IA (protocolli strutturati).
- **Medicina Interna/Rare/Autoimmuni:** Marcato vantaggio umano (complessità polisindromica).
- **Seniority dell'Umano:** Gli LLM superano specializzandi in domini complessi, ma sono surclassati da specialisti senior.

**Riferimenti Bibliografici:**
- Shan, et al. (2025). "Diagnostic Accuracy Gap: Large Language Models vs Clinical Professionals". *Journal of Medical Informatics*. (medinform-v13-e64963).
- Ito, et al. (2023). "Bias in LLM Diagnostic Proposals".
- Pillai, et al. (2023). "Performance of LLMs in Rare Diseases".
- Gunes, et al. (2024); Nakaura, et al.; Hirosawa, et al.; Kaya, et al.

## Relazioni
- [[medinform-v13-e64963]]: Sintesi sistematica e meta-analisi PRISMA-DTA.
- [[multimodal-diagnostic-paradox-in-llms]]: Degrado diagnostico nei modelli visione-linguaggio.
- [[single-correct-answer-fallacy-in-clinical-ai]]: Limiti epistemologici nella valutazione.
- [[modello-centauro-clinico]]: Framework di simbiosi diagnostica.
- [[human-in-the-reasoning]]: Preservazione del giudizio critico.
- [[cognitive-offloading-e-diagnostic-deskilling]]: Rischi di atrofia delle competenze.
- [[traffic-light-quality-appraisal-clinical-ai]]: Metodologia di valutazione.
