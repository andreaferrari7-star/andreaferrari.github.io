# Simulazione Pazienti AI

**Summary**: Metodologia di impiego degli LLM per generare profili e dialoghi di pazienti virtuali a fini di addestramento psicoterapeutico, sperimentazione didattica e testing clinico.
**Sources**: 05-08 Riunione_ Sviluppo Knowledge Base AI, Etica e Applicazioni Cliniche.txt
**Last updated**: 2026-08-27
---

## Definizione Operativa
La **Simulazione Pazienti AI** consiste nella progettazione di agenti conversazionali basati su [[large-language-models]] configurati per simulare quadri psicopatologici, pattern di credenze disfunzionali e stili relazionali tipici del contesto psicoterapeutico.

## Principi di Prompt Design per la Simulazione Clinica
- **Esplicitazione dei Bias e Schemi Cognitivi**: Per evitare comportamenti meccanici o stereotipati (es. "paziente depresso da manuale"), il prompt di sistema deve definire esplicitamente i bias cognitivi attivi (es. pensiero dicotomico, catastrofizzazione, astrazione selettiva) e la specifica modalità di ragionamento disfunzionale.
- **Dinamiche di Alleanza e Compliance**: È necessario parametrizzare il livello di cooperazione del paziente virtuale, la diffidenza relazionale e le possibili rotture dell'alleanza di lavoro, offrendo un banco di prova realistico per gli allievi terapeuti.
- **Prevenzione dell'Irrigidimento dell'Agente**: Vincoli eccessivi e regole rigide sovrapposte possono provocare un collasso della naturalezza espressiva del modello; è raccomandato l'uso di prompt mirati e il versioning pulito dell'agente.

## Utilità Didattica e Formativa in CBT
- **Palestra Clinica a Basso Rischio**: Consente agli studenti di specializzazione dei primi anni di esercitarsi su colloqui simulati, formulazione del caso, accertamento delle credenze di base e tecniche di ristrutturazione cognitiva in un ambiente sicuro e a costo contenuto.
- **Standardizzazione degli Scenari**: Permette di testare l'efficacia di interventi specifici o protocolli standardizzati (come la gestione dei pazienti *Not-On-Track*) su profili clinici calibrati e riproducibili.

## Limiti e Cautele Etiche
- **Bias Algoritmici di Genere e Categoria**: Rischio che i modelli interpretino con gravità asimmetrica scenari clinici equivalenti in base a variabili demografiche (es. sovrastima della severità diagnostica in vignette cliniche femminili).
- **Trasparenza e Tutela dei Dati**: Necessità assoluta di non utilizzare trascrizioni o dati clinici reali non anonimizzati per la generazione o l'alimentazione dei profili di simulazione.

## Related pages
- [[05-08_Riunione_Knowledge_Base]]
- [[human-in-the-reasoning]]
- [[prompting-in-psychology]]
- [[machine-psychology]]
- [[ai-research-ethics]]
- [[large-language-models]]
