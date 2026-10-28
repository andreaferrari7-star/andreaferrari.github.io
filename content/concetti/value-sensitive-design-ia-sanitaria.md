---
tags: [value-sensitive-design, etica, progettazione-partecipata, equita, spiegabilita, privacy, governance]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C4M2_JK_Dec29_2024_V1.0 (1).pdf"]
---

# Value-Sensitive Design nell'IA sanitaria

## Definizione Operativa
- Il *Value-Sensitive Design* (VSD) è un approccio che integra i valori etici nell'intero ciclo di vita di un sistema di IA, dalla definizione degli obiettivi al monitoraggio dopo l'introduzione. Non li tratta come controlli finali. Nei materiali didattici sull'IA sanitaria si articola in sette componenti (Khuntia, 2024n):
  - coinvolgimento dei portatori di interesse;
  - test iterativi;
  - modelli equi e trasparenti;
  - spiegabilità;
  - protezione della privacy;
  - equità;
  - supervisione etica.
- **Utilità CBT / Applicativa:** fornisce una griglia per progettare o scegliere uno strumento digitale per la salute mentale. Chi ha coinvolto pazienti e clinici? Su quali gruppi è stato testato? L'uso previsto è dichiarato, per esempio screening e non diagnosi? Le uscite sono spiegabili? Come sono trattati consenso e dati? Chi vigila nel tempo?

## Evidenze dalla Letteratura

### Le componenti
- **Coinvolgere i portatori di interesse:** pazienti, clinici, decisori, tecnici e comunità vanno coinvolti fin dall'inizio, perché fanno emergere barriere (connettività, sfiducia) e preoccupazioni etiche: i pazienti chiedono trasparenza sui dati, i clinici spiegabilità. L'esempio è uno strumento per la retinopatia diabetica co-progettato con operatori e comunità locali (Khuntia, 2024n).
- **Test iterativi:** prototipi, opinioni degli utenti e revisione per scoprire bias ed effetti indesiderati. Gli esempi sono i pulsossimetri meno accurati sulla pelle scura e un sistema di priorità per la terapia intensiva che penalizza i pazienti cronici (Khuntia, 2024n).
- **Modelli equi e trasparenti:** audit delle prestazioni per età, etnia e genere, ripetuti nel tempo e non una tantum (Khuntia, 2024n).
- **Spiegabilità:** evidenziare le aree dell'immagine che contribuiscono alla predizione, usare modelli surrogati interpretabili, spiegare al paziente in parole semplici. Le spiegazioni servono anche alla responsabilità professionale (Khuntia, 2024n).
- **Protezione della privacy:** apprendimento federato, cifratura, anonimizzazione, consenso informato su usi e accessi, meccanismi di responsabilità. L'esempio è un comitato etico che verifica le pratiche sui dati di un sistema di supporto alla salute mentale (Khuntia, 2024n).
- **Equità:** strumenti leggeri per contesti con poche risorse, monitoraggio per gruppi demografici, formazione dei clinici delle aree svantaggiate (Khuntia, 2024n).
- **Supervisione etica:** comitati di revisione, audit periodici, aggiornamento alle nuove norme e responsabilità condivisa tra sviluppatori, clinici e decisori (Khuntia, 2024n).

### Rapporto con altri approcci nella wiki
- Il VSD è affine all'etica incorporata nello sviluppo (*embedded ethics*), che inserisce eticisti e portatori di interesse nei cicli di sviluppo. Vedi [[embedded-ethics-interface]].
- La componente di supervisione si collega ai requisiti di supervisione umana di AI Act e GDPR. Vedi [[human-in-the-loop]].
- La componente di equità riprende i rischi di amplificazione delle disuguaglianze. Vedi [[algorithmic-bias-and-digital-inequalities]].

### Limiti
- La fonte presenta il VSD senza citare la letteratura che lo ha formulato [da verificare]. Gli esempi di casi riusciti non sono documentati. Vedi [[ai-health-c4m2-khuntia-2024]].

## Riferimenti Bibliografici
- Khuntia, J. (2024n). *Background materials for Course 4: AI integration in healthcare. Module 2: Health AI relevant design and ethics issues* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-agents-in-healthcare-and-capstone

## Relazioni
- Vedi anche: [[ai-health-c4m2-khuntia-2024]], [[embedded-ethics-interface]], [[human-in-the-loop]], [[algorithmic-bias-and-digital-inequalities]], [[health-ai-landscape]], [[ai-for-healthcare-systems-khuntia-2024]]
