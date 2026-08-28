# Libet Prime e Agenti Didattici CBT

**Summary**: Framework per la progettazione, sviluppo e versioning di agenti conversazionali intelligenti applicati alla didattica della psicoterapia cognitiva (modello LIBET), basato su prompt multi-modali, knowledge base strutturate e tutoraggio maieutico-socratico.
**Sources**: 05-11 Discussione del Gruppo di Ricerca su AI e Psicoterapia.txt
**Last updated**: 2026-08-27
---

## Architettura del Sistema Libet Prime

*Libet Prime* rappresenta un modello applicativo di intelligenza artificiale didattica per le scuole di specializzazione in psicoterapia cognitiva (Studi Cognitivi):
- **Distribuzione Controllata e Sostenibile**: Implementato come Gem su Google Workspace Education integrato con Google Classroom, consentendo una gestione privatizzata e selettiva per classi di allievi senza costi a consumo per singola chiamata API.
- **Architettura a 5 Modalità di Risposta**: Il master prompt governa cinque sotto-modalità specializzate:
  1. *Spiegazione teorica*: Esposizione strutturata dei costrutti e della metateoria LIBET.
  2. *Confronto e distinzione*: Differenziazione nosografica e concettuale tra quadri clinici.
  3. *Vignetta clinica e formulazione*: Analisi di trascritti e concettualizzazione del caso su base LIBET.
  4. *Intervento razionale*: Guida alla scelta di strategie e tecniche di intervento evidence-based.
  5. *Interrogazione / Autovalutazione*: Modalità di testing per l'autoapprendimento dello studente.

---

## Knowledge Base Dedicata (26 Capitoli)

A differenza dell'approccio generico basato sull'iniezione di PDF grezzi, la Knowledge Base di Libet Prime è stata ingegnerizzata ad hoc:
- **Redazione e Validazione Ibrida**: Co-costruita tramite iterazioni strutturate tra clinico esperto e [[large-language-models]] avanzati (ChatGPT, Claude) per sintetizzare e gerarchizzare 26 moduli concettuali.
- **Regole Epistemologiche Incorporate**:
  - Precedenza rigorosa dei dati fattuali sulle inferenze interpretative.
  - Avvio della formulazione sempre a partire dai cicli sintomatici.
  - Rispetto della dialettica dei bisogni (evitando di mirare alla mera eliminazione della sensibilità emotiva).
  - Esplicitazione sistematica dei limiti di inferenza del modello.
  - Interconnessione e mappatura dinamica tra moduli e capitoli correlati.

---

## Il Paradigma Socratico vs Correzione Passiva

Un'evoluzione fondamentale del modello è la transizione da un agente puramente nozionistico/correttivo a un **agente socratico**:
- Invece di limitarsi a identificare gli errori o fornire formulazioni pre-confezionate, l'agente pone domande guida (*guiding questions*), richiede chiarimenti e invita lo studente a riformulare le ipotesi diagnostiche, stimolando la riflessione metacognitiva e il ragionamento clinico autonomo.

---

## Gestione del *Prompt Regression* e Best Practice di Versioning

Durante il ciclo di sviluppo (passaggio da Libet Prime 1.0 a 1.1), è emerso il fenomeno del **Prompt Regression** da *over-constraining*:
- **Collo di Bottiglia Istruzionale**: L'aggiunta progressiva di vincoli, condizioni e istruzioni rigide su un prompt esistente induce una regressione qualitativa del modello, portandolo ad appiattirsi su scalette meccaniche e stereotipate.
- **Priorità Gerarchica dei Token**: Gli LLM tendono ad attribuire priorità sproporzionata alle istruzioni aggiunte in coda, alterando l'equilibrio complessivo del reasoning.
- **Soluzione Metodologica**: Per iterare e migliorare un agente clinico è preferibile sviluppare un'istanza pulita (*clean agent*) da zero ed eseguire test comparativi (A/B testing) su casi standardizzati, isolando le versioni precedenti.

---

## Related pages
- [[05-11_Discussione_Gruppo_Ricerca]]
- [[human-in-the-reasoning]]
- [[simulazione-pazienti-ai]]
- [[software-as-a-medical-device-salute-mentale]]
- [[prompting-in-psychology]]
- [[large-language-models]]
- [[ai-research-ethics]]
