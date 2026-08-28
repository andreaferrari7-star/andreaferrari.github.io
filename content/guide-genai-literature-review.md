# Guide: GenAI per la Revisione della Letteratura

**Summary**: Una guida operativa passo-passo per ricercatori su come utilizzare in modo responsabile e strutturato l'IA generativa nelle revisioni sistematiche della letteratura (SLR).

**Sources**: JML_1001.pdf, s44163-025-00495-3.pdf, 2605.24351v1.pdf, Using_Large_Language_Models_in_Psychological_Resea.pdf

**Last updated**: 2026-08-27

---

L'utilizzo dell'IA generativa per la revisione della letteratura non deve consistere nel delegare al modello la stesura libera del testo, poiché questo espone al rischio di citazioni fittizie e allucinazioni. L'approccio corretto si basa sui [[hybrid-ai-research-workflows]], in cui l'LLM funge da co-pilota all'interno di un processo rigorosamente guidato dall'umano.

Di seguito la guida operativa in 4 fasi per un'integrazione responsabile:

### Fase 1: Progettazione e Ricerca (Human-Led)
L'LLM **non** è un motore di ricerca accademico affidabile per lo scouting primario.
1. **Definizione dei Criteri**: Stabilisci rigorosi criteri di inclusione ed esclusione tipici delle [[structured-literature-reviews]].
2. **Raccolta Dati**: Utilizza database accademici tradizionali (es. Scopus, Web of Science, PubMed) per trovare e scaricare i paper.
3. **Tutela della Privacy**: Assicurati che i dati o i PDF che intendi caricare nel modello non violino policy istituzionali o diritti d'autore (vedi [[ai-research-ethics]]).

### Fase 2: Analisi e Organizzazione (Strutturazione Algoritmica)
Per evitare che il modello inventi collegamenti metodologici, è necessario fornirgli un'"impalcatura" solida.
1. **Clustering Bibliometrico**: Raggruppa gli articoli per tematiche, metodologie o co-citazioni tramite software di [[bibliometric-analysis]] o raggruppamento manuale.
2. **Preparazione dei Prompt**: Applica tecniche di [[prompting-in-psychology]] avanzate (es. *role-prompting*, *few-shot*), fornendo al modello blocchi di testo limitati e contestualizzati, accompagnati da istruzioni chiare e vincolate ai testi allegati.

### Fase 3: Sintesi Assistita (LLM-Assisted Synthesis)
Una volta forniti i cluster strutturati, l'LLM entra in gioco come sintetizzatore avanzato.
1. **Estrazione delle Evidenze**: Richiedi all'IA di estrarre sistematicamente per ogni paper: metodologia, dimensione del campione, risultati chiave e limiti dichiarati.
2. **Sintesi Narrativa**: Fai generare all'IA una [[llm-assisted-synthesis]] per descrivere l'evoluzione del cluster tematico, vincolando le affermazioni ai soli paper inseriti nel prompt.
3. **Verifica Critica (Human-in-the-Loop)**: Controlla manualmente ogni citazione generata. L'uomo rimane l'arbitro finale della correttezza concettuale, prevenendo bias metodologici e [[measurement-phantoms]].

### Fase 4: Identificazione dei Gap e Conclusioni
La revisione sistematica funge da base per la ricerca futura.
1. **Ragionamento a Passaggi (Stepwise CoT)**: Chiedi al modello di applicare il [[stepwise-cot]] per identificare attivamente contraddizioni o lacune (gap) nella letteratura sintetizzata e di supportarti nella [[hypothesis-generation]] per studi futuri.
2. **Reporting Etico**: Nella stesura finale dell'articolo, dichiara apertamente in che fasi, per quali task e con quali modelli hai utilizzato l'IA, nel pieno rispetto dell'etica della ricerca accademica.

## Related pages
- [[hybrid-ai-research-workflows]]
- [[structured-literature-reviews]]
- [[llm-assisted-synthesis]]
- [[stepwise-cot]]
- [[ai-research-ethics]]
