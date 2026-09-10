---
tags: 
  - diagnosis-of-thought-framework
  - dot-framework
  - prompt-engineering
  - clinical-reasoning
  - coast-framework
  - disaccoppiamento-fatti-interpretazioni
  - cot-avalanche-effect
  - ehr-noise
  - premature-closure
  - cbt-case-formulation
source_papers: 
  - "Clinical_AI_Cognitive_Assessment.pdf"
---

# Framework Diagnosis of Thought (DoT) e Disaccoppiamento Fatti-Interpretazioni

## Definizione Operativa
Il **Framework Diagnosis of Thought (DoT)** è una metodologia strutturata di prompt engineering clinico e guida inferenziale per modelli linguistici generativi (LLM) applicati alla psicoterapia, alla psichiatria e alla medicina.

**Principio Cardine:** Impone la **separazione procedurale rigorosa e sequenziale** tra:
1. L'estrazione oggettiva e descrittiva degli eventi narrati e dei comportamenti manifesti (*Fatti Oggettivi Osservati / Raw Observed Facts*);
2. La generazione delle ipotesi cliniche, la concettualizzazione del caso e l'inferenza di schemi cognitivi disfunzionali (*Ipotesi e Interpretazioni Diagnostiche*).

**Finalità Metodologica:** Disinnescare il *Paradosso dei Testi Clinici* e l'**Effetto Valanga del Chain-of-Thought (CoT)**, impedendo che micro-allucinazioni o fraintendimenti lessicali iniziali su cartelle cliniche reali ed eterogenee (EHR) si propaghino a cascata, causando il crollo dell'accuratezza diagnostica (-86.3%).

## Evidenze dalla Letteratura
Il framework è nato per superare il *Paradosso dei Testi Clinici Reali*:
- Nei benchmark logico-matematici tradizionali, l'approccio *Chain-of-Thought* incrementa le prestazioni.
- In ambito clinico su EHR e trascrizioni di colloqui reali, il materiale è intrinsecamente non standardizzato, ricco di abbreviazioni, ambiguità e dettagli contingenti privi di rilevanza nosografica.
- Il CoT libero causa un'amplificazione esponenziale degli errori lungo la catena deduttiva, portando a una degradazione dell'accuratezza clinica pari all'86.3% e a gravi falsi positivi diagnostici.
- Il DoT, attraverso il controllo biforcato (Filtro Fatti Oggettivi -> Ipotesi Differenziali Multiple -> Sintesi Clinica Rigorosa), neutralizza l'**Automation Bias** e previene la **Chiusura Prematura (*Premature Closure*)**.
- Ancorando le inferenze a un insieme verificato di fatti estratti nella fase iniziale, si inibisce la tendenza all'iper-compiacenza e si neutralizza l'allucinazione di tipo Korsakoff.

**Riferimenti Bibliografici:**
- "Clinical_AI_Cognitive_Assessment.pdf"
- Documentazione interna sul COAST Framework.

## Relazioni
- [COAST Framework](concetti/concetti\coast-framework-clinical-prompting.md) - Il DoT agisce come il motore logico interno per la componente *Actions* del framework COAST.
- [Allucinazioni LLM](korsakoff-confabulazione-llm.md) - Il DoT mitiga la dissociazione tra accuratezza formale e fattualità empirica.
- [CBT Case Formulation](cbt-case-formulation.md) - Applicazione specifica del DoT alla concettualizzazione cognitiva (Modello ABC).
- [LLM](large-language-models.md) - Base tecnologica su cui viene applicato il framework.
- [Modello Centauro Clinico](concetti/concetti\modello-centauro-clinico.md) - La metodologia DoT facilita la cooperazione clinica uomo-macchina con supervisione umana attiva.
- [Explainable Mental Health Diagnosis](explainable-mental-health-diagnosis.md) - Tecniche di interpretabilità nosografica correlate al DoT.

## Riferimenti Bibliografici
- [Da integrare]
