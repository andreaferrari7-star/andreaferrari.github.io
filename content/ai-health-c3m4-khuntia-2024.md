---
tags: [ai-health-coursera, formazione, modelli-predittivi, modelli-prescrittivi, modelli-cognitivi, ciclo-di-vita-del-modello, implementazione]
tipo_fonte: scientifica
source_papers: ["BackgroundMaterials_AI-Health_C3M4_JK_Dec22_2024_V1.0 pgd (1).pdf"]
---

# AI for Healthcare Systems, C3M4: la modellazione per l'IA in sanità, parte 2 (Khuntia, 2024l)

## Definizione Operativa
- Materiale di approfondimento (52 pagine, versione 1.0 del 22 dicembre 2024) che chiude il corso 3 di [[ai-for-healthcare-systems-khuntia-2024|AI for Healthcare Systems]]; le intestazioni lo chiamano «Module 2». Completa la tipologia dei modelli con quelli predittivi, prescrittivi e cognitivi e li confronta. Descrive poi il processo di sviluppo in otto fasi e le dieci sfide di implementazione dell'IA in sanità, con le contromisure (Khuntia, 2024l).
- **Utilità CBT / Applicativa:** l'elenco delle sfide e delle contromisure è utilizzabile come griglia per valutare l'adozione di una piattaforma in un servizio. Comprende dati e interoperabilità, regolazione, spiegabilità, integrazione nei flussi di lavoro, bias, costi, privacy, monitoraggio, resistenze e generalizzabilità, e prevede l'avvio con un progetto pilota. Vedi [[health-ai-landscape]].

## Evidenze dalla Letteratura

### Modelli predittivi
- Il modulo indica tre usi e cinque tecniche (Khuntia, 2024l):
  - **punteggi di rischio e previsione di malattia:** riammissione nello scompenso, complicanze renali nel diabete (con un «70% a cinque anni» illustrativo), sepsi;
  - **ottimizzazione delle risorse:** accessi stagionali, turni, posti in terapia intensiva in pandemia, scorte;
  - **personalizzazione:** risposta alla chemioterapia, rischio di non aderenza per motivi economici o effetti collaterali, aggiustamenti in tempo reale da dispositivi indossabili, per esempio nell'asma;
  - **tecniche:** ML, regressione, serie temporali, *clustering* e classificazione, ensemble.

### Modelli prescrittivi
- Sono presentati come il livello più alto dell'analisi dei dati: oltre a prevedere, raccomandano un'azione (Khuntia, 2024l). Gli ambiti:
  - **decisioni ottimizzate:** regime chemioterapico, sequenza di trattamenti nel politrauma, piano per il diabete, antibiotici, liquidi e tempi nella sepsi;
  - **allocazione delle risorse:** personale, apparecchiature, approvvigionamento, ventilatori e dispositivi di protezione in pandemia;
  - **politiche sanitarie:** priorità vaccinali, simulazione dell'effetto di aperture serali degli ambulatori, unità vaccinali mobili.
- Le tecniche sono modelli di ottimizzazione, simulazione e ML. Gli esempi applicativi (Khuntia, 2024l):
  - inibitori di PARP nel tumore al seno con mutazione BRCA;
  - metformina e stile di vita nel prediabete;
  - prevenzione cardiovascolare e dell'osteoporosi;
  - gestione delle emergenze, con il confronto simulato tra lockdown precoce e test diffusi.

### Modelli cognitivi
- Imitano il ragionamento umano su dati non strutturati. Il modulo afferma che questi sono «oltre l'80%» dell'informazione sanitaria, senza fonte [da verificare]. Le tecniche sono NLP, deep learning e grafi di conoscenza (Khuntia, 2024l).
- Le applicazioni citate (Khuntia, 2024l):
  - errori di prescrizione e reazioni avverse dalle cartelle;
  - sorveglianza da social media e notizie;
  - trascrizione e analisi delle conversazioni tra clinico e paziente;
  - diagnosi differenziale, per esempio il sospetto di lupus;
  - combinazioni di farmaci nei casi resistenti;
  - Alzheimer precoce dall'analisi del linguaggio;
  - chatbot per sintomi, appuntamenti e promemoria, «programmati per dare risposte empatiche»;
  - accelerazione della ricerca.

### Il confronto tra i cinque modelli
- Il modulo li presenta come un continuum di complessità crescente (Khuntia, 2024l):
  - **descrittivi:** che cosa è successo. Limite: solo retrospettivi;
  - **diagnostici:** perché. Limite: reattivi;
  - **predittivi:** che cosa succederà. Limite: «forniscono solo probabilità, lasciando interpretazione e decisione ai professionisti»;
  - **prescrittivi:** che cosa fare. Limite: dipendono dalla qualità delle previsioni;
  - **cognitivi:** ragionare e interagire. Limite: richiedono molti dati e sono poco trasparenti.
- I cinque modelli condividono la dipendenza dai dati, lavorano in modo complementare e sono integrabili nelle cartelle elettroniche (Khuntia, 2024l). La tabella comparativa del PDF è impaginata male, e due delle quattro serie di illustrazioni sono quasi identiche.

### Il processo di sviluppo in otto fasi
- Il modulo descrive otto fasi, con esempi su diabete e malattia renale cronica (Khuntia, 2024l):
  1. raccolta e integrazione dei dati;
  2. preparazione e costruzione delle variabili, con attenzione a sovradattamento e sbilanciamento delle classi;
  3. analisi esplorativa, anche per individuare i bias di rappresentazione;
  4. scelta del modello, bilanciando complessità, accuratezza e interpretabilità, anche con AutoML;
  5. addestramento e validazione con divisione in training, validazione e test e con validazione incrociata *k-fold*;
  6. metriche: l'accuratezza è fuorviante con classi sbilanciate; precisione, *recall*, F1 e RMSE vanno scelte secondo il problema clinico, per esempio privilegiando la sensibilità nelle condizioni gravi;
  7. messa in produzione con monitoraggio della deriva dei dati (*data drift*);
  8. revisione iterativa.

### Le dieci sfide e le contromisure
- Le sfide e le relative contromisure (Khuntia, 2024l):
  1. **qualità e interoperabilità dei dati:** standard come FHIR, piattaforme di integrazione, accordi di condivisione;
  2. **regolazione e conformità:** HIPAA, GDPR, approvazioni lunghe soprattutto per i sistemi che continuano ad apprendere, rivalutazione in altre giurisdizioni. Contromisure: coinvolgere presto i regolatori e documentare dati, progetto e logica decisionale;
  3. **spiegabilità:** SHAP, LIME, visualizzazioni e formazione. Per le applicazioni ad alto rischio il modulo indica preferibili modelli più semplici e interpretabili, come gli alberi decisionali;
  4. **integrazione nei flussi di lavoro:** progettazione centrata sull'utente, architetture modulari, introduzione graduale a partire da progetti pilota;
  5. **bias ed equità:** dati diversificati, audit dei bias, vincoli di equità, coinvolgimento di associazioni di pazienti e comunità;
  6. **costi:** cloud, strumenti open source (TensorFlow, PyTorch), condivisione regionale, finanziamenti pubblici;
  7. **privacy e sicurezza:** privacy differenziale, apprendimento federato, anonimizzazione, cifratura, audit;
  8. **monitoraggio e manutenzione:** deriva dei dati, riaddestramento, monitoraggio automatico, opinioni degli utenti;
  9. **resistenza al cambiamento:** timore di essere sostituiti, sfiducia dei pazienti. Contromisure: comunicazione, coinvolgimento precoce, formazione;
  10. **scalabilità:** i modelli addestrati in ospedali urbani generalizzano male alle cliniche rurali. Contromisure: sistemi modulari, adattamento locale, formazione di team locali.

### Errori, limiti e divergenze con la wiki
- **Supervisione umana presentata come limite:** che i modelli predittivi lascino interpretazione e decisione al professionista viene elencato come un limite. Nel quadro normativo e deontologico raccolto nella wiki è invece un requisito: AI Act art. 14 e GDPR art. 22 (Regolamento [UE] 2024/1689; Regolamento [UE] 2016/679), e per la pratica psicologica le indicazioni dell'Ordine del Veneto (OPPV, 2026). Vedi [[human-in-the-loop]].
- **Prescrizioni ad alto rischio:** sequenze terapeutiche nel politrauma e regimi per la sepsi sono presentati come raccomandazioni che «aumentano la fiducia dei clinici», senza discutere il rischio di affidamento eccessivo. Vedi [[automation-bias-clinical-reasoning]].
- **Empatia programmata:** i chatbot «programmati per dare risposte empatiche» sono presentati senza discutere il divario tra empatia simulata e relazione autentica. Vedi [[genuineness-gap]].
- **Calibrazione:** la sezione sulle metriche corregge un errore dei moduli precedenti, perché dice che l'accuratezza è fuorviante con classi sbilanciate, ma non nomina ancora la calibrazione. Vedi [[clinical-prediction-model-evaluation]].
- **Struttura:** contenuti ripetuti, frasi introduttive in stile chatbot («Here are visual representations…») e nessun riferimento bibliografico. Gli esempi numerici sono illustrativi.

## Riferimenti Bibliografici
- Khuntia, J. (2024l). *Background materials for Course 3: AI integration in healthcare. Module 4: The craft of modeling for AI in healthcare* [Materiale didattico, versione 1.0]. AI for Healthcare Systems Specialization, University of Colorado System; Coursera. https://www.coursera.org/learn/ai-integration-in-healthcare
- Ordine delle Psicologhe e degli Psicologi del Veneto. (2026). *Guida operativa all'utilizzo dell'AI nella pratica professionale* (Versione 1, gennaio 2026). Gruppo di Lavoro Intelligenza Artificiale OPPV.
- Parlamento Europeo e Consiglio dell'Unione Europea. (2016). *Regolamento (UE) 2016/679 relativo alla protezione delle persone fisiche con riguardo al trattamento dei dati personali (GDPR)*. Gazzetta Ufficiale dell'Unione Europea, L 119/1.
- Regolamento (UE) 2024/1689 del Parlamento europeo e del Consiglio, del 13 giugno 2024, che stabilisce regole armonizzate sull'intelligenza artificiale (regolamento sull'intelligenza artificiale). (2024). *Gazzetta ufficiale dell'Unione europea*, L 2024/1689. http://data.europa.eu/eli/reg/2024/1689/oj

## Relazioni
- Serie: [[ai-for-healthcare-systems-khuntia-2024]]
- Vedi anche: [[health-ai-landscape]], [[human-in-the-loop]], [[automation-bias-clinical-reasoning]], [[genuineness-gap]], [[clinical-prediction-model-evaluation]], [[software-as-a-medical-device-salute-mentale]], [[ai-health-c3m3-khuntia-2024]]
