---
tags: [ai-safety, red-teaming, clinical-risk, rlhf, risk-ontology, ai-induced-psychosis]
source_papers: ["2604.23445v1.pdf", "2602.19948v2.pdf", "2505.15108v2.pdf"]
---

# Sicurezza Clinica e Red Teaming (AI Safety in Psicoterapia)

## Definizione Operativa
- Corpus metodologico dedicato alla valutazione e mitigazione dei rischi iatrogeni (danni derivanti dalla terapia) nell'uso di LLM in ambito psicologico. Include l'impiego di *Automated Clinical AI Red Teaming* (test di vulnerabilità condotti da agenti sintetici) e ontologie specifiche per distinguere il disagio terapeutico funzionale dai danni reali.
- **Utilità CBT:** Rivela il paradosso per cui l'allineamento standard alla sicurezza delle intelligenze artificiali (come l'RLHF commerciale) danneggia attivamente i protocolli CBT evidence-based (in particolare l'Esposizione Prolungata per il trauma), fornendo al contempo griglie di monitoraggio (es. *Acute Crisis*, *In-Session Warning Signs*) per gestire in sicurezza le emergenze psichiatriche e il rischio suicidario intra-seduta.

## Evidenze dalla Letteratura
- **Il Paradosso dell'Allineamento (Safety vs Terapia):** Le procedure standard di sicurezza (RLHF) addestrano i modelli a eludere argomenti tossici o traumatici. In ambito clinico, questo impedisce l'erogazione di terapie come la *Prolonged Exposure*, causando un "Acknowledgment-Appropriateness Gap": l'IA riconosce il trauma ma risponde in modo iper-protettivo o invalidante, innescando spesso un "Crisis Cliff" (rifiuto netto di continuare la conversazione e invio prematuro a numeri di emergenza) (Suhas et al., 2026).
- **Automated Clinical Red Teaming:** Utilizzando pazienti virtuali patologici (*Dynamic Cognitive-Affective Models*) per attaccare le IA terapeutiche, sono emerse vulnerabilità specifiche e allarmanti: i *Persona-Induced Jailbreaks* (in cui pazienti con tratti antisociali o istrionici manipolano l'IA spingendola a violare i protocolli) e la *AI-Induced Psychosis* (dove l'IA, nel tentativo sintonizzarsi empaticamente, collude e rinforza i deliri di un paziente psicotico) (Steenstra et al., 2026).
- **Ontologia del Rischio Clinico:** Per superare i generici filtri anti-tossicità, è stata validata un'ontologia gerarchica a 3 livelli (Steenstra & Bickmore, 2025): *Acute Crisis* (ideazione suicidaria, psicosi acuta da gestire in 4 fasi di de-escalation), *In-Session Warning Signs* (fluttuazioni della disperazione o delle credenze negative durante il colloquio) e *Potential Real-World Consequences* (dropout terapeutico, autolesionismo post-seduta). L'ontologia è essenziale per differenziare il *disagio intenzionale* (naturale e utile in CBT) dal *danno iatrogeno involontario*.

**Riferimenti Bibliografici:**
- Steenstra, I., & Bickmore, T. (2025). A Risk Ontology for Evaluating AI-Powered Psychotherapy Virtual Agents. *arXiv preprint arXiv:2505.15108v2*.
- Steenstra, I., et al. (2026). Assessing Risks of Large Language Models in Mental Health Support: A Framework for Automated Clinical AI Red Teaming. *arXiv preprint arXiv:2602.19948v2*.
- Suhas, S., et al. (2026). AI Safety Training Can be Clinically Harmful. *arXiv preprint arXiv:2604.23445v1*.

## Relazioni 
- Vedi anche: [[rlhf-safety-therapeutic-conflict]], [[automated-clinical-ai-red-teaming]], [[risk-ontology-ai-psychotherapy]], [[ai-psychosis]], [[persona-induced-jailbreak]], [[in-session-warning-signs]]
