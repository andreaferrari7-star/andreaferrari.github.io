---
tags: [intelligenza-artificiale, machine-learning, deep-learning, fondamenti, storia-ia, formazione]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_Module1_JK_Oct30_2024_V2.3 (2).pdf", "BackgroundMaterials_AI-Health_C1M4_JK_Nov14_2024_V1.2 (1).pdf", "BackgroundMaterials_AI-Health_C3M1_JK_Dec28_2024_V1.0 (1) (1).pdf"]
---

# Intelligenza Artificiale, Machine Learning e Deep Learning

## Definizione Operativa
- L'IA è la capacità di un sistema informatico di imitare processi dell'intelligenza umana. Il machine learning (ML) è il sottoinsieme dell'IA che apprende dai dati senza programmazione esplicita. Il deep learning (DL) è il sottoinsieme del ML basato su reti neurali a molti strati (Khuntia, 2024a).
- **Utilità CBT / Applicativa:** distinguere i tre livelli serve a capire che cosa fa davvero uno strumento presentato come «IA». Un sistema a regole, un modello di ML che stima un rischio e un LLM generativo hanno comportamenti, rischi e requisiti di validazione diversi. Vedi [[marketing-architecture-mismatch-in-mental-health-ai]].

## Evidenze dalla Letteratura

### La gerarchia IA ⊃ ML ⊃ DL
- **IA:** l'ambito più ampio, che comprende anche sistemi esperti, elaborazione del linguaggio naturale e visione artificiale. Si fonda su due concetti: costruire agenti intelligenti che svolgono compiti umani e simulare processi cognitivi come apprendere, ragionare e adattarsi (Khuntia, 2024a).
- **ML:** gli algoritmi vengono addestrati su grandi insiemi di dati per riconoscere pattern e fare predizioni, invece di ricevere istruzioni passo per passo. Esempi d'uso: sistemi di raccomandazione, filtri antispam, rilevazione delle frodi, stima del rischio di malattia da cartelle cliniche (Khuntia, 2024a).
- **DL:** l'apprendimento è gerarchico, con livelli di astrazione crescenti. In un'immagine i primi strati riconoscono bordi e forme, quelli profondi volti e oggetti. È il metodo che ha migliorato il riconoscimento di immagini e parlato e l'analisi delle immagini mediche (Khuntia, 2024a). Per le architetture (CNN, RNN, transformer) vedi [[reti-neurali-in-psicologia]].

### I paradigmi di apprendimento
- **Supervisionato:** impara da esempi etichettati, cioè con l'esito noto. Si divide in classificazione (categorie: diabete sì o no, rischio basso, medio o alto) e regressione (valori continui: pressione, giorni di degenza) (Khuntia, 2024i).
- **Non supervisionato:** cerca strutture in dati senza etichette, per esempio sottogruppi di pazienti. I gruppi trovati vanno poi validati sul piano clinico (Khuntia, 2024i).
- **Semi-supervisionato:** combina poche etichette con molti dati non etichettati, utile quando etichettare costa. Il rischio è che il bias delle etichette si propaghi (Khuntia, 2024i).
- **Per rinforzo:** impara una strategia di decisioni sequenziali dalla retroazione (ricompense). Pone problemi di sicurezza nei casi limite e richiede supervisione umana (Khuntia, 2024i).

### Sottoadattamento e sovradattamento
- Un modello troppo semplice sottoadatta (alto bias): sbaglia sia sui dati di addestramento sia su quelli nuovi. Un modello troppo complesso sovradatta (alta varianza): memorizza il rumore, va benissimo in addestramento e male sui dati nuovi. Il segnale tipico è un errore di validazione che cresce mentre quello di addestramento scende. I rimedi sono validazione incrociata, regolarizzazione, arresto anticipato e regolazione degli iperparametri (Khuntia, 2024i).
- Per un clinico la conseguenza pratica è che le prestazioni riportate su dati di addestramento o su un solo campione interno non bastano: contano quelle su dati indipendenti. Vedi [[clinical-prediction-model-evaluation]].

### Componenti e funzionamento
- Un sistema di IA ha tre componenti: dati, algoritmi e hardware. I dati sono la materia prima (cartelle, esami, immagini). Gli algoritmi sono regole che ordinano, filtrano, raggruppano e predicono. L'hardware fornisce la potenza di calcolo (Khuntia, 2024a).
- Il processo decisionale va dall'input dei dati all'analisi alla decisione, con tecniche come il raggruppamento (*clustering*), la ricerca di relazioni causa-effetto e la predizione di esiti (Khuntia, 2024a).

### L'analogia con l'apprendimento clinico
- Khuntia (2024d) paragona l'apprendimento da dati etichettati allo studio sui manuali. Paragona l'apprendimento da dati non etichettati all'esperienza clinica, che con gli anni insegna a riconoscere pattern sottili. Ne ricava una sinergia: l'IA elabora i dati su larga scala, il clinico li interpreta con giudizio ed empatia.
- L'analogia è utile come ponte didattico ma è imprecisa: trovare pattern in dati non etichettati non equivale a integrare contesto, valori del paziente e responsabilità. Vedi [[ai-health-c1m4-khuntia-2024]].

### Breve storia
- Tre periodi: gli inizi (anni '50-'60), con il test di Turing, la conferenza di Dartmouth (1956) ed ELIZA (1966); l'inverno dell'IA, con fondi ridotti e i limiti dei sistemi a regole; la rinascita trainata da dati, calcolo e deep learning, fino ad AlphaGo (2016) (Khuntia, 2024a).
- Su ELIZA la fonte concorda con quanto riferito alla Giornata Nazionale della Psicologia 2026: il sistema funzionava per *pattern matching* su parole chiave e la comprensione era solo apparente (cfr. [[10-10-giornata-nazionale-psicologia-ia-quo-vadis]]).
- La cronologia di Khuntia (2024a) è imprecisa in alcuni punti, come la datazione del Logic Theorist e del progetto giapponese Fifth Generation [da verificare]; i dettagli sono in [[ai-health-c1m1-khuntia-2024]].

### Limiti
- Le definizioni di Khuntia (2024a, 2024i) sono introduttive e non citano fonti. Alcune parti dei materiali sembrano generate con un'IA generativa e non revisionate. Vanno integrate con testi tecnici quando serve precisione.

## Riferimenti Bibliografici
- Khuntia, J. (2024a). *Background materials for Course 1: Artificial intelligence (AI) for health systems: Foundation and potential. Module 1: Preliminary meaning and evolution of AI in healthcare* [Materiale didattico, versione 2.3]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/foundation-and-potential-of-ai-in-healthcare
- Khuntia, J. (2024d). *Background materials for Course 1: Artificial intelligence (AI) for health systems: Foundation and potential. Module 4: The potential of AI for healthcare grand challenges* [Materiale didattico, versione 1.2]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/foundation-and-potential-of-ai-in-healthcare
- Khuntia, J. (2024i). *Background materials for Course 3: AI integration in healthcare. Module 1: Relevant ML algorithms in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare

## Relazioni
- Vedi anche: [[ai-health-c1m1-khuntia-2024]], [[ai-health-c1m4-khuntia-2024]], [[ai-health-c3m1-khuntia-2024]], [[algoritmi-ml-sanita]], [[clinical-prediction-model-evaluation]], [[ai-for-healthcare-systems-khuntia-2024]], [[reti-neurali-in-psicologia]], [[large-language-models]], [[marketing-architecture-mismatch-in-mental-health-ai]], [[mind-and-machine-beg-verma-2023]]
