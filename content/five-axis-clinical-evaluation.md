---
tags: [five-axis-evaluation, clinical-safety, protocol-fidelity, hallucination-risk, multi-turn-consistency, crisis-safety, demographic-robustness, samd, eu-ai-act, readi-framework, synthetic-benchmarks]
source_papers: ["2604.23445v1.pdf"]
---

# Framework di Valutazione Clinica a Cinque Assi (Five-Axis Clinical Evaluation Framework)

## Definizione Operativa
Il **Framework di Valutazione Clinica a Cinque Assi** (*Five-Axis Evaluation Framework*) è un'architettura metodologica standardizzata per la validazione della sicurezza, efficacia e conformità regolatoria degli agenti di intelligenza artificiale impiegati nella salute mentale e nella psicoterapia computazionale (Suhas et al., 2026).

**Scopo e Origine:** Nasce per colmare il divario tra la facilità di calcolo delle metriche NLP generiche e la reale idoneità clinica dei modelli generativi. Il framework implementa operativamente le dimensioni del modello **READI** (*Readiness Evaluation for AI-Mental Health Deployment and Implementation*; Stade et al., 2025; Gaus et al., 2025), fornendo una procedura standardizzata per verificare che nessun sistema AI sia rilasciato a utenti clinici prima di aver superato un controllo multi-dimensionale rigoroso.

## Evidenze dalla Letteratura

### 1. Asse 1: Fedeltà al Protocollo Terapeutico (*Therapeutic Protocol Fidelity*)
- **Failure Mode Rilevato:** Generazione di risposte empatiche e fluenti ma che violano o saltano passaggi cardine del protocollo clinico manualizzato.
- **Metrica e Benchmark:** Classificazione automatizzata della fase clinica o aderenza alla scala CTRS.
- **Allineamento Regolatorio:** *FDA SaMD:* Clinical Performance Validation | *EU AI Act:* Accuracy and Robustness (Art. 15).

### 2. Asse 2: Rischio Allucinatorio nel Dialogo Clinico (*Hallucination Risk*)
- **Failure Mode Rilevato:** Fabbricazione di criteri diagnostici errati, attribuzione scorretta di sintomi o consigli controindicati.
- **Metrica e Benchmark:** Iniezione controllata di misstatements clinici (*seeded errors*) e valutazione della capacità di detection tramite confronto con testi di riferimento (DSM-5).
- **Allineamento Regolatorio:** *FDA SaMD:* Accuracy and Reliability | *EU AI Act:* Transparency and Correctness (Art. 13, 15).

### 3. Asse 3: Consistenza Comportamentale Multi-Turno (*Behavioral Consistency*)
- **Failure Mode Rilevato:** Slittamento della postura terapeutica (*stance drift*), contraddizione di valutazioni del rischio o perdita della persona clinica.
- **Metrica e Benchmark:** Valutazione della coerenza su sequenze standardizzate a 20 turni (*Thousand Voices of Trauma*).
- **Allineamento Regolatorio:** *FDA SaMD:* Performance Reproducibility | *EU AI Act:* Robustness and Reproducibility (Art. 15).

### 4. Asse 4: Sicurezza su Prompt Vulnerabili e di Crisi (*Crisis Safety*)
- **Failure Mode Rilevato:** Minimizzazione del rischio suicidario, false rassicurazioni o mancata fornitura di risorse di crisi.
- **Metrica e Benchmark:** Batteria standardizzata di 360 scenari di crisi valutata con rubrica VERA-MH.
- **Allineamento Regolatorio:** *FDA SaMD:* Risk Classification | *EU AI Act:* Risk Management System (Art. 9), Human Oversight (Art. 14).

### 5. Asse 5: Robustezza Demografica e Linguistica (*Demographic Robustness*)
- **Failure Mode Rilevato:** Degrado sistematico delle performance ed empatia in base a età, genere o lingua (vulnerabilità al *code-mixing*).
- **Metrica e Benchmark:** Valutazione disaggregata su 500 personas cliniche.
- **Allineamento Regolatorio:** *FDA SaMD:* Bias and Fairness | *EU AI Act:* Non-discrimination and Data Governance (Art. 10), Bias Testing (Art. 15).

**Riferimenti Bibliografici:**
- Suhas, B. N., et al. (2026). AI Safety Training Can be Clinically Harmful. *arXiv:2604.23445v1*.
- Bentley, K. H., et al. (2026). VERA-MH: Reliability and validity of an open-source AI safety evaluation in mental health. *arXiv:2601.xxxxx*.
- Gaus, R., et al. (2025). A scoping review of generative AI in mental health support. *PsyArXiv preprint*.
- Stade, E. C., et al. (2025). Readiness evaluation for artificial intelligence–mental health deployment and implementation (READI). *Technology, Mind, and Behavior*, 6(2).
- Suhas, B. N., et al. (2025a). Thousand voices of trauma: A large-scale synthetic dataset for modeling prolonged exposure therapy conversations. *NeurIPS Datasets & Benchmarks*.
- Young, J. E., & Beck, A. T. (1980). *Cognitive Therapy Rating Scale: Rating Manual*. University of Pennsylvania.

## Relazioni
- Vedi anche: [[2604-23445v1]], [[rlhf-safety-therapeutic-conflict]], [[clinical-fidelity-assessment]], [[software-as-a-medical-device-salute-mentale]], [[three-layer-governance-framework]], [[automated-clinical-ai-red-teaming]], [[audit-bias-llm-clinici]], [[validita-psicometrica-llm]], [[ai-assisted-psychotherapy]], [[000]]
