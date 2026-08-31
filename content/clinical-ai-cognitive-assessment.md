---
tags: [clinical-ai-cognitive-assessment, large-language-models, assessment-cognitivo-ai, korsakoff-confabulazione-llm, accuratezza-vs-fattualita, concept-grounding, automation-bias, mind-safe, llm4cbt, rag-esame-libro-aperto, guardrails-clinici, cot-avalanche-effect, coast-framework, diagnosis-of-thought-framework, few-shot-prompting, exploratory-thinking, tripod-llm, chart-reporting-guideline, human-in-the-loop]
source_papers: ["Clinical_AI_Cognitive_Assessment.pdf"]
---

# L'Assessment Cognitivo dell'AI: Oltre l'Illusione Relazionale

## Definizione Operativa
L'Assessment Cognitivo dell'AI è un'architettura pedagogica e metodologica per guidare professionisti della salute mentale nell'analisi critica e nell'ingegnerizzazione sicura dei modelli linguistici generativi (LLM) nella pratica clinica. Supera l'illusione relazionale (effetto ELIZA) chiarendo che l'AI opera tramite calcolo stocastico, non intuito clinico. I pilastri includono: comprensione dei limiti matematici, mitigazione del rischio iatrogeno (Automation Bias), ingegneria di sistema protetta (MIND-SAFE) e governance metodologica (COAST, DoT).

## Evidenze dalla Letteratura
- **Confabulazione (Korsakoff Computazionale):** Gli LLM colmano vuoti informativi con narrazioni fluide ma prive di fattualità, presentando una dissociazione tra accuratezza formale (sintattica) e fattualità empirica (biomedica).
- **Degradazione CoT:** L'applicazione di tecniche di *Chain-of-Thought* (CoT) su dati clinici reali rumorosi (EHR) ha mostrato una degradazione dell'accuratezza dell'86.3% a causa dell'effetto valanga delle micro-allucinazioni.
- **Bias e De-Biasing:** Documentata una tendenza al default androcentrico (94%) e asimmetrie diagnostiche di genere. Mitigazione tramite *Exploratory Thinking* (swap demografico) e architetture multi-agente (Avvocato del Diavolo).
- **Standard di Rendicontazione:** Adozione dei framework TRIPOD-LLM e CHART per garantire trasparenza e riproducibilità scientifica nell'uso dell'AI clinica.

**Riferimenti Bibliografici:**
- *Clinical AI Cognitive Assessment* (Documento tecnico di riferimento).
- Linee guida CHART per la rendicontazione dell'AI in sanità.
- TRIPOD-LLM (2025) per la validazione di modelli clinici.
- Framework MIND-SAFE per l'ingegneria dei sistemi clinici.

## Relazioni
- [[korsakoff-confabulazione-llm]]: Approfondisce la natura delle allucinazioni.
- [[diagnosis-of-thought-framework]]: Metodologia per isolare fatti da interpretazioni.
- [[coast-framework-clinical-prompting]]: Framework per prompt engineering strutturato.
- [[mind-safe-framework]]: Sicurezza e triage in ambito salute mentale.
- [[cbt-dialogue-systems-and-tools]]: Strumenti per la regolazione del pacing terapeutico.
- [[large-language-models]]: Fondamenti architetturali.
- [[human-in-the-loop]]: Principio inderogabile della responsabilità clinica finale.
