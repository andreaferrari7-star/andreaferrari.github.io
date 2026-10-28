---
tags: [diad, dati, analisi-predittiva, decisione-clinica, data-mining, sanita-digitale]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C2M1_JK_Dec17_2024_V1.0 (2).pdf", "BackgroundMaterials_AI-Health_C1M2_JK_Oct30_2024_V12.3 (1).pdf", "BackgroundMaterials_AI-Health_C2M2_JK_Dec17_2024_V1.0 (4).pdf"]
---

# Framework DIAD: dai dati alla decisione

## Definizione Operativa
- Il DIAD (*Data-Information-Analysis-Decision*) descrive il percorso con cui i dati grezzi diventano decisioni. I dati sono organizzati e contestualizzati in informazione; l'informazione viene analizzata per produrre previsioni (*intelligence*); l'intelligence, integrata con esperienza e competenza, sostiene la decisione (Khuntia, 2024e).
- **Utilità CBT / Applicativa:** davanti a uno strumento di IA permette di chiedersi su quale stadio interviene e che cosa resta al clinico. Un questionario somministrato via app produce dati; il punteggio con norme produce informazione; un modello che stima il rischio di drop-out produce intelligence; la scelta di cosa fare in seduta resta una decisione clinica.

## Evidenze dalla Letteratura

### Gli stadi
- **Dati:** cartelle cliniche elettroniche, dispositivi indossabili, sistemi amministrativi, registri di sanità pubblica, dati ambientali. Le criticità sono qualità, standardizzazione, integrazione e affidabilità dei dispositivi (Khuntia, 2024e).
- **Informazione:** dati organizzati e contestualizzati, che rispondono a «chi», «cosa», «dove». Il contesto dà valore al dato: una misura isolata è un dato, la stessa misura letta nella storia del paziente è informazione utile (Khuntia, 2024e).
- **Analisi:** produce *intelligence*, cioè previsioni che collegano ciò che è accaduto a ciò che potrebbe accadere. Le tecniche citate sono regressione, alberi decisionali, *clustering* e modelli predittivi (Khuntia, 2024e).
- **Decisione:** integra le fasi precedenti con esperienza e competenza. Il passaggio da uno stadio all'altro richiede impegno deliberato, strumenti e competenze, non avviene da solo (Khuntia, 2024e).

### Il DIAD e la storia della digitalizzazione
- Il framework risponde al limite della prima digitalizzazione sanitaria, che aveva prodotto grandi quantità di dati senza capacità di trarne conoscenza: quella che Khuntia (2024b) chiama *non-intelligence digitization*.

### Ruolo dell'IA e strumenti
- IA, ML e LLM automatizzano la trasformazione dei dati in conoscenza e la rendono disponibile in linguaggio naturale (Khuntia, 2024e).
- Il percorso si appoggia a processi ETL e pulizia dei dati, analisi statistiche e ML, strumenti di visualizzazione (cruscotti, mappe di calore) e cicli di retroazione tra decisori e analisti. Con i dati in tempo reale l'analisi passa da retrospettiva a proattiva (Khuntia, 2024e).

### Lo stadio dell'analisi
- Khuntia (2024f) descrive i modelli analitici che operano in questo stadio: dati in ingresso, variabili, algoritmo, addestramento, output con metriche e ciclo di retroazione. Avverte che il valore dell'analisi dipende da dati pronti, problema ben definito, collaborazione multidisciplinare e monitoraggio continuo. Vedi [[ai-health-c2m2-khuntia-2024]].

### Estensione: il Health AI Landscape
- Nel corso 3 lo stesso percorso è ampliato in una catena che aggiunge agli stadi del DIAD gli algoritmi, i modelli, gli agenti che portano l'output agli utenti e i processi organizzativi. Il tutto opera dentro vincoli legali, etici e di sicurezza (Khuntia, 2024k). Vedi [[health-ai-landscape]].

### Rischi e limiti
- Dati distorti o analisi non rigorose producono intelligence distorta e decisioni inique. Servono dataset diversificati, metodi robusti e processi decisionali trasparenti (Khuntia, 2024e). Vedi [[algorithmic-bias-and-digital-inequalities]].
- Il framework è presentato in materiali didattici senza bibliografia. La sua parentela con la gerarchia dati-informazione-conoscenza-saggezza (DIKW) della scienza dell'informazione non è dichiarata [da verificare]. Il vertice è chiamato ora «decisione», ora «conoscenza».

## Riferimenti Bibliografici
- Khuntia, J. (2024b). *Background materials for Course 1: Artificial intelligence (AI) for health systems: Foundation and potential. Module 2: Where health systems stand* [Materiale didattico, versione 12.3]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/foundation-and-potential-of-ai-in-healthcare
- Khuntia, J. (2024e). *Background materials for Course 2: The data to decision path for infusion of AI in healthcare. Module 1: The role of AI in the data-information-analysis-decision (DIAD) process in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/the-data-to-decision-path-for-infusion-of-ai-in-healthcare
- Khuntia, J. (2024f). *Background materials for Course 2: The data to decision path for infusion of AI in healthcare. Module 2: Emphasizing analytics in DIAD for healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/the-data-to-decision-path-for-infusion-of-ai-in-healthcare
- Khuntia, J. (2024k). *Background materials for Course 3: AI integration in healthcare. Module 3: The craft of modeling for AI in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare

## Relazioni
- Vedi anche: [[health-ai-landscape]], [[ai-health-c2m1-khuntia-2024]], [[ai-health-c2m2-khuntia-2024]], [[clinical-prediction-model-evaluation]], [[ai-health-c1m2-khuntia-2024]], [[ai-for-healthcare-systems-khuntia-2024]], [[ai-clinical-decision-support]], [[ia-machine-learning-deep-learning]], [[algorithmic-bias-and-digital-inequalities]]
