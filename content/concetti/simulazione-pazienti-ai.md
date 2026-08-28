# Simulazione Pazienti con Intelligenza Artificiale

**Summary**: Metodologie avanzate di prompt engineering e modellizzazione computazionale per la simulazione di pazienti virtuali mediante LLM, finalizzate al training clinico e alla ricerca psicoterapeutica, con enfasi sull'esplicitazione dei bias cognitivi e delle dinamiche relazionali.
**Sources**: `05-11 Discussione del Gruppo di Ricerca su AI e Psicoterapia.txt`, `05-08 Riunione_ Sviluppo Knowledge Base AI, Etica e Applicazioni Cliniche.txt`
**Last updated**: 2026-08-27
---

## Obiettivi della Simulazione Clinica

L'uso di modelli linguistici ([[large-language-models]]) per simulare pazienti virtuali rappresenta una frontiera centrale nella formazione psicoterapeutica (CBT) e nella ricerca clinica:
- **Addestramento Protetto**: Permette agli allievi e ai terapeuti in formazione di esercitarsi su colloqui clinici, assessment, concettualizzazione del caso e gestione di situazioni critiche in un ambiente sicuro e controllato.
- **Sperimentazione Pilota a Basso Costo**: Possibilità di testare scenari di interazione complessi su piattaforme scalabili e accessibili (es. Google Workspace / Gemini) senza costi proibitivi di infrastruttura.

---

## Modellizzazione dei Bias Cognitivi vs Stereotipizzazione Meccanica

Uno dei problemi principali riscontrati nei modelli generativi non specificamente configurati è la tendenza a produrre risposte stereotipate, piatte o rigidamente descrittive (es. una simulazione meccanica di un "depresso standard" basata su checklist sintomatiche del DSM):
- **Esplicitazione delle Euristiche e Distorsioni Cognitive**: Per ottenere una simulazione psicologicamente valida e clinicamente realistica, il prompt deve specificare la struttura interna di pensiero del paziente, inclusi:
  - *Bias cognitivi prevalenti*: Pensiero dicotomico (tutto-o-nulla), catastrofizzazione, astrazione selettiva, personalizzazione.
  - *Processi di mantenimento*: Rimuginio ossessivo, evitamento esperienziale, ruminazione depressiva.
  - *Dinamiche interpersonali e di alleanza*: Atteggiamento verso la terapia (compliance passiva, diffidenza, sfida, richiesta di rassicurazione continua).
- **Livelli di Astrazione e Trasparenza**: Aderenza a linee guida metodologiche (adattamento di framework come TRIPOD) che definiscono chiaramente il livello di astrazione richiesto al modello, distinguendo tra espressione verbale spontanea del paziente simulato e stati interni non verbalizzati.

---

## Linee Guida di Progettazione dei Prompt

1. **Definizione della Persona Clinica**: Specificare contesto socio-demografico, anamnesi remota, eventi scatenanti e tema di vita prevalente.
2. **Definizione dello Stile Linguistico**: Calibrare il registro comunicativo, la latenza di risposta, la reticenza o la prolissità verbale.
3. **Evitamento del collasso della simulazione**: Impedire che l'agente esca dal personaggio (*character breaking*) o che fornisca meta-spiegazioni psicologiche non plausibili per il livello di consapevolezza del paziente.

---

## Related pages
- [[05-11_Discussione_Gruppo_Ricerca_AI_Psicoterapia]]
- [[human-in-the-reasoning]]
- [[libet-prime-agenti-didattici]]
- [[prompting-in-psychology]]
- [[large-language-models]]
- [[etica-privacy-bias-ia-clinica]]
