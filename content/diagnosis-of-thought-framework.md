---
tags: [diagnosis-of-thought-framework, dot-framework, prompt-engineering, clinical-reasoning, coast-framework, disaccoppiamento-fatti-interpretazioni, cot-avalanche-effect, ehr-noise, premature-closure, cbt-case-formulation]
source_papers: ["Clinical_AI_Cognitive_Assessment.pdf"]
---

# Framework Diagnosis of Thought (DoT) e Disaccoppiamento Fatti-Interpretazioni

## Definizione Operativa
Il **Framework Diagnosis of Thought (DoT)** è una metodologia strutturata di prompt engineering clinico e guida inferenziale per modelli linguistici generativi ([[large-language-models]]) applicati alla psicoterapia, alla psichiatria e alla medicina.

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
- Ancorando le inferenze a un insieme verificato di fatti estratti nella fase iniziale, si inibisce la tendenza all'iper-compiacenza e si neutralizza l'[[korsakoff-confabulazione-llm|Allucinazione di tipo Korsakoff]].

**Riferimenti Bibliografici:**
- "Clinical_AI_Cognitive_Assessment.pdf"
- Documentazione interna sul [[coast-framework-clinical-prompting]]

## Relazioni
- [[coast-framework-clinical-prompting]] - Il DoT agisce come il motore logico interno per la componente *Actions* del framework COAST.
- [[korsakoff-confabulazione-llm]] - Il DoT mitiga la dissociazione tra accuratezza formale e fattualità empirica.
- [[cbt-case-formulation]] - Applicazione specifica del DoT alla concettualizzazione cognitiva (Modello ABC).
- [[large-language-models]] - Base tecnologica su cui viene applicato il framework.
- [[modello-centauro-clinico]] - La metodologia DoT facilita la cooperazione clinica uomo-macchina con supervisione umana attiva.
- [[explainable-mental-health-diagnosis]] - Tecniche di interpretabilità nosografica correlate al DoT.
