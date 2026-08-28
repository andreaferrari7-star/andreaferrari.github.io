# Clinical Fidelity Assessment
**Summary**: Metodologia automatizzata per la valutazione dell'aderenza e della competenza nell'erogazione di psicoterapie evidence-based (EBT) mediante NLP e [[large-language-models]]. Consente supervisione clinica scalabile, feedback in tempo reale e contrasto all'erosione delle abilità terapeutiche post-training.
**Sources**: 000.txt
**Last updated**: 2026-08-27
---

## Definizione Operativa
La **Clinical Fidelity Assessment** (valutazione della fedeltà clinica o integrità del trattamento) rappresenta il processo metodologico volto a verificare che un intervento psicologico manualizzato ed evidence-based (es. CBT, CPT, Written Exposure Therapy - WET) venga erogato conformemente ai parametri di efficacia stabiliti dalla ricerca scientifica.

La fedeltà clinica si articola in due componenti distinte:
1. **Aderenza (*Adherence*)**: Parametro quantitativo che misura se il terapeuta include tutti gli elementi obbligatori previsti dal protocollo di trattamento nella sequenza corretta, evitando l'introduzione di tecniche proscritte o controindicate.
2. **Competenza (*Competence*)**: Parametro qualitativo che valuta il livello di maestria, accuratezza, responsività relazionale e giudizio clinico con cui le singole tecniche vengono implementate.

---

## Limiti della Supervisione Tradizionale e Innovazione Computazionale
- **Collo di Bottiglia Tradizionale**: Nella pratica standard, la valutazione della fedeltà richiede la registrazione delle sedute, l'ascolto manuale integrale da parte di supervisori esperti e la codifica tramite griglie psicometriche. Questo processo è costoso, ad alta intensità di tempo e non scalabile nei sistemi sanitari pubblici o nella pratica privata.
- **Erosione della Fedeltà (*Fidelity Erosion*)**: Gli studi di implementation science mostrano che, terminata la fase di training iniziale intensivo, l'aderenza e la qualità degli interventi decadono rapidamente nel tempo senza una supervisione continua.
- **Automazione con AI e NLP**: L'uso di sistemi di elaborazione del linguaggio naturale e [[large-language-models]] consente di automatizzare la trascrizione, estrarre indicatori linguistici e generare checklist di fedeltà e report di valutazione in modo quasi istantaneo.

---

## Approcci Computazionali: NLP Rule-Based vs Modelli LLM
La ricerca del centro CREATE e della letteratura computazionale evidenzia un'interazione tra differenti tecnologie:
- **Approcci NLP Linguistico-Statistici On-Premise**: Algoritmi di elaborazione del testo specializzati (es. pattern matching avanzato, analisi lessicale) che operano in locale senza trasmettere dati sensibili al cloud. Risultano spesso superiori e più affidabili nella codifica dell'aderenza stretta al protocollo (*adherence*), garantendo elevati standard di privacy e conformità HIPAA.
- **Large Language Models (LLM)**: Modelli generativi capaci di cogliere sfumature semantiche complesse, utili per valutazioni di contesto e per la formulazione di feedback qualitativi personalizzati, sebbene richiedano ancoraggio rigoroso a scale psicometriche validate per evitare valutazioni impressionistiche arbitrarie.

---

## Applicazioni Formative e Cliniche
L'integrazione della valutazione automatizzata della fedeltà abilita scenari applicativi innovativi:

1. **Training con Pazienti Simulati (*Therapy Trainer*)**:
   - Piattaforme che simulano pazienti virtuali affetti da disturbi specifici (es. PTSD) permettendo al clinico in formazione di esercitarsi su snodi critici (gestione del trauma, rischio suicidario).
   - Il sistema calcola in tempo reale il punteggio di fedeltà sulle risposte del terapeuta, consentendo di ripetere i passaggi fino al raggiungimento della soglia di competenza.
2. **Supervisione On-Demand (*Coach AI*)**:
   - Sistemi di supporto a disposizione del terapeuta subito dopo la conclusione di un colloquio reale.
   - Analisi strutturata dei punti di forza della seduta e indicazioni mirate sugli elementi del protocollo da rinforzare nella seduta successiva.
3. **Nudging Clinico e Supporto Ambientale**:
   - Durante le sedute in telepsicologia o tramite *ambient listening*, il sistema può fornire discreti promemoria visivi al terapeuta per assicurare la copertura di tutti i componenti obbligatori del protocollo.

---

## Requisiti di Validazione e Quadro READY
Per essere adottati responsabilmente nelle organizzazioni sanitarie, gli strumenti di valutazione della fedeltà devono soddisfare i criteri del **Framework READY**:
- **Validità Psicometrica**: Ancoraggio a misure di fedeltà empiricamente validate (es. scale di aderenza CPT/WET) anziché a giudizi intuitivi non verificati del modello linguistico.
- **Sicurezza e Protezione Dati**: Gestione conforme dei dati sensibili dei pazienti e contratti BAA dedicati.
- **Accettabilità e Usabilità**: Interfacce intuitive che favoriscano la riflessione e l'autovalutazione del terapeuta, riducendo l'ansia da valutazione automatizzata.

## Related pages
- [[000]]
- [[ai-assisted-psychotherapy]]
- [[large-language-models]]
- [[adamkovic-2025]]
- [[ai-research-ethics]]
- [[prompting-in-psychology]]
