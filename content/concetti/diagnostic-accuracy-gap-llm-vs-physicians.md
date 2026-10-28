---
tags: [diagnostic-accuracy, clinical-decision-support, large-language-models, physician-vs-ai, meta-analysis, primary-diagnosis, differential-diagnosis, emergency-triage, medical-reasoning, tacit-knowledge]
tipo_fonte: scientifica
source_papers: ["medinform-v13-e64963.pdf", "BackgroundMaterials_AI-Health_C4M1_JK_Dec29_2024_V1.0 (1).pdf"]
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

### Una divergenza nei materiali didattici
- Il corso *AI for Healthcare Systems* afferma che gli LLM hanno dimostrato capacità diagnostiche «eccezionali», «spesso superiori ai medici in studi controllati» (Khuntia, 2024m). Il quadro meta-analitico di Shan et al. (2025) contraddice questa affermazione per la diagnosi principale; regge solo per il triage e per il confronto con gli specializzandi in alcuni domini. Generalizzare quei risultati favorevoli porta a sovrastimare l'affidabilità diagnostica degli LLM.

## Riferimenti Bibliografici
- Shan, G., Chen, X., Wang, C., Liu, L., Gu, Y., Jiang, H., & Shi, T. (2025). Comparing diagnostic accuracy of clinical professionals and large language models: Systematic review and meta-analysis. *JMIR Medical Informatics*, *13*, e64963. https://doi.org/10.2196/64963
- Ito, N., Kadomatsu, S., Fujisawa, M., et al. (2023). The accuracy and potential racial and ethnic biases of GPT-4 in the diagnosis and triage of health conditions: Evaluation study. *JMIR Medical Education*, *9*, e47532. https://doi.org/10.2196/47532
- Pillai, J., & Pillai, K. (2023). Accuracy of generative artificial intelligence models in differential diagnoses of familial Mediterranean fever and deficiency of interleukin-1 receptor antagonist. *Journal of Translational Autoimmunity*, *7*, 100213. https://doi.org/10.1016/j.jtauto.2023.100213
- Gunes, Y. C., & Cesur, T. (2024). The diagnostic performance of large language models and general radiologists in thoracic radiology cases: A comparative study. *Journal of Thoracic Imaging*. Advance online publication. https://doi.org/10.1097/RTI.0000000000000805
- Hirosawa, T., Kawamura, R., Harada, Y., et al. (2023a). ChatGPT-generated differential diagnosis lists for complex case-derived clinical vignettes: Diagnostic accuracy evaluation. *JMIR Medical Informatics*, *11*, e48808. https://doi.org/10.2196/48808
- Hirosawa, T., Mizuta, K., Harada, Y., & Shimizu, T. (2023b). Comparative evaluation of diagnostic accuracy between Google Bard and physicians. *The American Journal of Medicine*, *136*(11), 1119–1123. https://doi.org/10.1016/j.amjmed.2023.08.003
- Kaya, K., Gietzen, C., Hahnfeldt, R., et al. (2024). Generative pre-trained transformer 4 analysis of cardiovascular magnetic resonance reports in suspected myocarditis: A multicenter study. *Journal of Cardiovascular Magnetic Resonance*, *26*(2), 101068. https://doi.org/10.1016/j.jocmr.2024.101068
- Khuntia, J. (2024m). *Background materials for Course 4: AI integration in healthcare. Module 1: Models to agents in health AI* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-agents-in-healthcare-and-capstone
- Nakaura, T., Yoshida, N., Kobayashi, N., et al. (2024). Preliminary assessment of automated radiology report generation with generative pre-trained transformers: Comparing results to radiologist-generated reports. *Japanese Journal of Radiology*, *42*(2), 190–200. https://doi.org/10.1007/s11604-023-01487-y

## Relazioni
- [[medinform-v13-e64963]]: Sintesi sistematica e meta-analisi PRISMA-DTA.
- [[multimodal-diagnostic-paradox-in-llms]]: Degrado diagnostico nei modelli visione-linguaggio.
- [[single-correct-answer-fallacy-in-clinical-ai]]: Limiti epistemologici nella valutazione.
- [[modello-centauro-clinico]]: Framework di simbiosi diagnostica.
- [[human-in-the-reasoning]]: Preservazione del giudizio critico.
- [[cognitive-offloading-e-diagnostic-deskilling]]: Rischi di atrofia delle competenze.
- [[traffic-light-quality-appraisal-clinical-ai]]: Metodologia di valutazione.
- [[ai-health-c4m1-khuntia-2024]]: Materiale didattico che sovrastima le capacità diagnostiche degli LLM.
