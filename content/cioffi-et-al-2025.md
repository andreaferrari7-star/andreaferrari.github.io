---
tags: [supervisione, formazione-clinica, chatgpt, prompt-engineering, gestalt, blended-supervision]
tipo_fonte: scientifica
source_papers: ["informatics-12-00029.pdf"]
---

# Può l'IA supportare la supervisione clinica? Il potenziale di ChatGPT (Cioffi et al., 2025)

## Definizione Operativa
- Studio italiano, condotto da 12 scuole di psicoterapia della Gestalt e coordinato dalla SiPGI, che valuta la fattibilità di ChatGPT-4 come strumento di supervisione nella formazione in psicoterapia. Specializzandi in Gestalt valutano alla cieca tre feedback di supervisione sullo stesso caso clinico: ChatGPT-4 senza istruzioni, ChatGPT-4 orientato da un prompt sulla supervisione gestaltica, un supervisore esperto (Cioffi et al., 2025).
- **Utilità applicativa:** mostra che un prompt di dominio cambia la qualità percepita del feedback dell'IA e propone una supervisione *blended* a due livelli: un primo feedback generato dall'IA, poi una supervisione del supervisore esperto che parte da quel feedback (Cioffi et al., 2025). Vedi [[supervisione-clinica-ai]].

## Evidenze dalla Letteratura

### Disegno dello studio
- **Caso clinico:** un caso reale anonimizzato (il «caso Leonard») con anamnesi, analisi della domanda, assessment psicodiagnostico, descrizione del funzionamento di personalità e resoconto delle prime tre sedute dal punto di vista del terapeuta, con attenzione al suo vissuto in seduta (Cioffi et al., 2025).
- **I tre feedback** (Cioffi et al., 2025):
  - **Fb1**: ChatGPT-4 in una finestra di conversazione nuova, senza contesto; il feedback evidenzia punti di forza e aree di miglioramento e valuta le strategie usate;
  - **Fb2**: ChatGPT-4 preceduto da un prompt introduttivo sulla terapia della Gestalt e sulla supervisione, sviluppato in uno studio precedente degli stessi autori; il feedback si concentra sull'uso del sé del terapeuta e sulla gestione di transfert e controtransfert;
  - **Fb3**: un supervisore esperto; il feedback si concentra sulla relazione terapeutica, sulle dinamiche controtransferali e sull'uso delle metafore.
- **Il prompt:** è stato generato da ChatGPT stesso, sintetizzando le informazioni fornite in conversazioni precedenti, ed è stato verificato e corretto in modo iterativo da terapeuti e supervisori della Gestalt. Gli autori chiamano «pretraining» questo orientamento tramite prompt, ma il modello non viene addestrato né modificato (Cioffi et al., 2025). Vedi [[prompting-in-psychology]].
- **Valutazione:** specializzandi in psicoterapia della Gestalt integrata, tra 25 e 40 anni, senza sapere chi avesse scritto ciascun feedback. Il questionario di soddisfazione, costruito ad hoc, ha 16 item su scala Likert a 4 punti ed è ispirato al modello di supervisione di Clarkson; l'alfa di Cronbach complessiva è 0,92. Le valutazioni raccolte sono 25 per Fb1, 24 per Fb2 e 22 per Fb3, 71 in totale, analizzate con analisi delle componenti principali e ANOVA a una via (Cioffi et al., 2025).

### Risultati
- L'analisi delle componenti principali individua quattro componenti, che spiegano il 68,2% della varianza (KMO = 0,86) (Cioffi et al., 2025):
  - **C1, relazionale ed emotiva:** approccio empatico, aiuto all'autoriflessione, aiuto alla fiducia, impatto emotivo;
  - **C2, qualità didattica e tecnica:** chiarezza, pertinenza, completezza, analisi delle tecniche;
  - **C3, supporto al trattamento e sviluppo:** aiuto al trattamento, suggerimenti pratici, evidenziazione delle aree di miglioramento, comunicazione tra pari;
  - **C4, orientamento professionale e adattabilità:** orientamento deontologico, aiuto alla definizione del contratto, adeguatezza al livello professionale, utilità per lo sviluppo professionale.
- **C1:** differenza significativa tra i tre feedback (F = 5,73; p = 0,005), con medie di 10,40 per Fb1, 13,01 per Fb2 e 11,98 per Fb3. Secondo il testo e l'abstract, Fb1 è valutato meno degli altri due e non c'è differenza significativa tra Fb2 e il supervisore umano (Cioffi et al., 2025).
- **C4:** differenza significativa (F = 3,39; p = 0,04), con medie di 10,42 per Fb1, 11,91 per Fb2 e 10,44 per Fb3. Fb2 ottiene punteggi più alti anche del supervisore umano (Cioffi et al., 2025).
- **C2 e C3:** nessuna differenza significativa. Chiarezza, pertinenza, completezza, analisi delle tecniche e suggerimenti pratici sono giudicati simili per i tre feedback (Cioffi et al., 2025).
- **Singoli item:** Fb2 supera Fb1 per approccio empatico, aiuto al contratto, adeguatezza al livello professionale e aiuto alla fiducia. Il supervisore umano supera Fb2 nell'evidenziare le aree di miglioramento (Cioffi et al., 2025).
- Per l'impatto emotivo gli autori riportano che Fb2 supera sia Fb1 sia il supervisore umano. Nella Tabella 4, però, le medie di Fb2 e del supervisore sono molto vicine (2,96 e 2,86), mentre il distacco netto è da Fb1 (1,88): la superiorità sul supervisore va controllata [da verificare].

### Proposte degli autori
- Una supervisione *blended* in cui l'IA fornisce un primo feedback e il supervisore esperto lavora a partire da esso, unendo «creatività umana e sistematicità dell'IA» (Cioffi et al., 2025).
- Un uso dell'IA tra un incontro di supervisione e l'altro, per sostenere il benessere del terapeuta e prevenire il burnout (Cioffi et al., 2025).
- In prospettiva, con la memoria a lungo termine di ChatGPT, usare i resoconti delle sedute di supervisione come materiale per l'IA e i feedback dell'IA come oggetto della supervisione reale (Cioffi et al., 2025). L'articolo non analizza la protezione dei dati di questi resoconti; vedi [[gdpr-governance-mental-health-ai]].
- Studi futuri dovrebbero confrontare più piattaforme di IA e più supervisori umani, e valutare segnali fisiologici come frequenza cardiaca, respiro e tono muscolare per rendere gli output più empatici (Cioffi et al., 2025).

### Limiti
- **Dichiarati dagli autori:** caso singolo; un solo supervisore umano di confronto; campione piccolo e omogeneo, composto solo da specializzandi; background socioculturale dei valutatori non rilevato, mentre la percezione dell'empatia varia tra culture; capacità limitata dell'IA di cogliere la complessità emotiva. All'epoca dello studio ChatGPT-4 non aveva memoria a lungo termine. Gli autori non hanno richiesto il parere di un comitato etico, ritenendolo non necessario (Cioffi et al., 2025).
- **Dal disegno:** l'esito misurato è la soddisfazione degli specializzandi verso il testo del feedback, non l'effetto sulle loro competenze o sugli esiti dei pazienti. L'articolo non chiarisce se gli stessi valutatori abbiano giudicato tutti e tre i feedback, mentre l'ANOVA li tratta come gruppi indipendenti [da verificare].
- **Incoerenze interne:** la nota della Tabella 3 indica Fb2 come diverso da entrambi gli altri feedback in C1, mentre il testo esclude la differenza con il supervisore; nella metodologia si parla di «4 feedback» invece di tre.
- Rispetto ai criteri proposti da [[shafran-et-al-2026|Shafran et al. (2026)]] per valutare l'IA nella supervisione, cioè superiorità sugli esiti a livello di terapeuta o non inferiorità sugli esiti clinici, lo studio fornisce un primo dato di qualità percepita, non ancora di efficacia. Shafran et al. lo citano con l'anno 2024 e il titolo «Can AI technologies support automating clinical supervision?»; l'articolo è stato pubblicato nel marzo 2025 con il titolo riportato sotto.

## Riferimenti Bibliografici
- Cioffi, V., Ragozzino, O., Mosca, L. L., Moretto, E., Tortora, E., Acocella, A., Montanari, C., Ferrara, A., Crispino, S., Gigante, E., Lommatzsch, A., Pizzimenti, M., Temporin, E., Barlacchi, V., Billi, C., Salonia, G., & Sperandeo, R. (2025). Can AI technologies support clinical supervision? Assessing the potential of ChatGPT. *Informatics*, *12*(1), 29. https://doi.org/10.3390/informatics12010029
- Shafran, R., Bond, L., Carlbring, P., Cohen, Z. D., Creed, T. A., Davey, E., Egan, S. J., Freeman, D., Hollon, S. D., Jacobson, N. C., Johnson, C., Kaysen, D., McGuinness, D. L., Patel, V., Pozuelo, J. R., Santos, H., Singla, D. R., Wiltsey Stirman, S., Taylor, D. J., & Wade, T. D. (2026). From innovation to implementation: Artificial intelligence in cognitive behaviour therapy training and supervision. *Behaviour Research and Therapy*, *197*, Article 104945. https://doi.org/10.1016/j.brat.2025.104945

## Relazioni
- Vedi anche: [[supervisione-clinica-ai]], [[shafran-et-al-2026]], [[prompting-in-psychology]], [[simulated-empathy-vs-authentic-presence]], [[11920-2026-article-1690]], [[human-in-the-loop]], [[gdpr-governance-mental-health-ai]]
