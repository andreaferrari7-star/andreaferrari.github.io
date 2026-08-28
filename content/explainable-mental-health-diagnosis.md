---
tags: [explainable-ai, xai-salute-mentale, diagnostica-esplicabile, evidence-tagging, audit-clinico, llm-reasoning, psicoterapia-ai]
source_papers: ["2508.11398v2.pdf"]
---

# Explainable Mental Health Diagnosis

## Definizione Operativa
- Paradigma e metodologia di Intelligenza Artificiale Spiegabile (**Explainable AI, XAI**) applicata alla salute mentale e alla psicodiagnostica computazionale, volta a superare il problema della "scatola nera" (*black-box*) nei Large Language Models (LLM) attraverso l'esplicitazione intrinseca della catena di inferenza clinica, l'ancoraggio a criteri nosografici standardizzati (es. DSM-5, ICD-11) e l'indicizzazione semantica delle evidenze verbali fornite dal paziente.
- **Utilità CBT / Clinica:** Trasforma la predizione diagnostica opaca in un referto clinico verificabile e verificato (*auditable diagnostic rationale*). Consente ai clinici, ai supervisori e alle équipe multidisciplinari di ispezionare turno per turno quali verbalizzazioni del paziente supportano o contraddicono specifici criteri nosografici, garantendo trasparenza decisionale, riduzione del rischio di allucinazioni diagnostiche e maggiore aderenza all'alleanza terapeutica.

## Evidenze dalla Letteratura
- **Opacità Diagnostica e Rischio di Rigetto Clinico:** Nei contesti di screening psicologico e psichiatrico, l'output di modelli di IA che forniscono unicamente punteggi sintetici o etichette categoriali senza giustificazione argomentativa genera sfiducia (*medical mistrust*) sia nei pazienti (che non comprendono l'origine della valutazione) sia nei clinici (che non possono validare il processo logico) (Cirasola et al., 2024; Ozgun et al., 2025).
- **Trasparenza Intrinseca vs Spiegazioni Post-Hoc:** Rispetto ai metodi classici di interpretabilità post-hoc (come mappe di calore dell'attenzione o calcolo di attribuzioni di feature che spesso mancano di fedeltà clinica, Barkan et al., 2024), l'approccio integrato a livello di workflow genera spiegazioni intrinseche e contestuali durante la sintesi diagnostica (Ozgun et al., 2025).
- **Tre Segnali Chiave di Explainability (Ozgun et al., 2025):**
  1. *Evidence Tagging (Marcatura Semantica delle Evidenze):* Inserimento sistematico di marcatori semantici all'interno del referto per distinguere e isolare entità cliniche:
     - `<sym>` per i sintomi identificati (es. `<sym>allucinazioni uditive per 3 settimane</sym>`);
     - `<quote>` per le citazioni testuali verbatim del paziente (es. `<quote>“so che queste voci non sono reali”</quote>`);
     - `<med>` per le condizioni mediche, diagnosi differenziali o farmaci (es. `<med>Schizophreniform Disorder</med>`).
  2. *Criterion Anchoring (Ancoraggio ai Criteri Nosografici):* Riferimento esplicito e puntuale alle singole clausole dei manuali diagnostici (es. Criterio A1, Criterio D per la durata degli episodi, Criterio E per l'esclusione di sostanze organiche).
  3. *Step-by-Step Logic (Ragionamento Sequenziale Strutturato):* Articolazione dell'argomentazione clinica in una catena deduttiva numerata che mappa: Evidenza Verbale $\rightarrow$ Criterio Nosografico $\rightarrow$ Diagnosi Differenziale / Esclusione $\rightarrow$ Giudizio Clinico Finale.
- **Trade-off tra Fluenza Conversazionale e Rigore di Ragionamento:** La sperimentazione comparativa di Ozgun et al. (2025) evidenzia una divergenza critica tra modelli linguistici:
  - Modelli orientati al dialogo (*dialogue-focused LLM*, es. Llama-4, Mistral-Saba) producono testi empatici e scorrevoli ma generano referti opachi o tautologici ("i sintomi appaiono coerenti con i criteri DSM-5"), senza citare clausole o evidenze dirette.
  - Modelli specializzati nel ragionamento logico (*reasoning-focused LLM*, es. Qwen-QwQ-32b) sacrificano parzialmente la fluidità del parlato ma producono catene diagnostiche complete, rigorose e perfettamente tracciabili, garantendo la massima fedeltà nosografica.
- **Implicazioni Medico-Legali e Sicurezza Clinica:** La spiegabilità diagnostica è un prerequisito fondamentale per la conformità normativa (es. Software as a Medical Device - SaMD, AI Act) e per la governance etica della salute mentale digitale, consentendo la *root-cause analysis* in caso di errore diagnostico e facilitando la supervisione umana (*Human-in-the-Loop*) (Ozgun et al., 2025).

**Riferimenti Bibliografici:**
- Ozgun, M. C., Pei, J., Hindriks, K., Donatelli, L., Liu, Q., & Wang, J. (2025). Trustworthy AI Psychotherapy: Multi-Agent LLM Workflow for Counseling and Explainable Mental Disorder Diagnosis. In *Proceedings of the 34th ACM International Conference on Information and Knowledge Management (CIKM ’25)*, November 10–14, 2025, Seoul, Republic of Korea. ACM, New York, NY, USA, 10 pages. https://doi.org/10.1145/3746252.3761164 / arXiv:2508.11398v2 [cs.HC]
- Barkan, O., Toib, Y., Elisha, Y., & Koenigstein, N. (2024). A learning-based approach for explaining language models. In *Proceedings of CIKM ’24* (pp. 98–108). ACM.
- Cirasola, A., Szegedi, D., Fonagy, P., & Midgley, N. (2024). “You can't really have a relationship with them because they just ask you questions”: Understanding adolescent dropout. *Frontiers in Psychology*, 15, 1381901.

## Relazioni
- Vedi anche: [[2508.11398v2]], [[dsm5agentflow]], [[audit-bias-llm-clinici]], [[clinical-ai-simulation]], [[risk-ontology-ai-psychotherapy]], [[supervisione-clinica-ai]], [[modello-centauro-clinico]], [[software-as-a-medical-device-salute-mentale]]
