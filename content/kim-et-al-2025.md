---
tags:
  - ocd
  - systematic-review
  - nlp
  - biomarker-discovery
  - erp-training
  - large-language-models
  - computer-vision
source_papers:
  - "AI_in_OCD.pdf"
  - "40501_2025_Article_359.pdf"
---

# Artificial Intelligence in Obsessive-Compulsive Disorder: A Systematic Review

## Definizione Operativa
- **Sintesi e Inquadramento:** Prima revisione sistematica della letteratura specificamente focalizzata sull'applicazione delle tecnologie di Intelligenza Artificiale (AI), Machine Learning (ML), Natural Language Processing (NLP) e Generative AI (GenAI) nel Disturbo Ossessivo-Compulsivo (OCD). Comprende 13 studi empirici (76,9% pubblicati tra il 2023 e il 2025) selezionati secondo linee guida PRISMA e valutati con metodologia GRADE (certezza dell'evidenza complessivamente "alta" per via degli ampi campioni esaminati).
- **Utilità CBT / Clinico-Applicativa:** L'OCD presenta tipicamente un ritardo diagnostico drammatico (in media 17 anni dall'esordio dei sintomi all'inizio di un trattamento basato sull'evidenza), con conseguente cronicizzazione e peggioramento della prognosi. L'integrazione di strumenti basati su intelligenza artificiale affronta nodi critici della Cognitive Behavioral Therapy (CBT) per l'OCD:
  1. *Early Detection e Screening:* Analisi automatizzata del linguaggio naturale su social media, cartelle cliniche elettroniche (EHR) e messaggistica dei pazienti per intercettare precocemente le manifestazioni ossessive.
  2. *Training Scalabile in ERP (Exposure and Response Prevention):* Superamento della grave carenza globale di clinici formati nel protocollo ERP attraverso simulatori di pazienti virtuali guidati da LLM (*TherapyTrainer*) e feedback supervisionato.
  3. *Supporto alla Pianificazione Clinica:* Generazione assistita da LLM di gerarchie espositive personalizzate (Bernstein et al., 2025) e supporto all'aderenza agli homework inter-seduta.
  4. *Biomarcatori Oggettivi e Sottotipizzazione:* Impiego della Computer Vision (CV) per quantificare oggettivamente i rituali comportamentali (evitando i bias dei self-report) e neuroimaging funzionale/strutturale per predire la risposta ai trattamenti (CBT e SSRI).

## Evidenze dalla Letteratura

### Efficacia
- **Screening e Riconoscimento Diagnostico Precoce:** L'analisi computazionale del linguaggio permette di estrarre marker linguistici distintivi dell'OCD. Studi su social media (Plank & Zlomuzica, 2024) hanno riscontrato una coerenza semantica significativamente ridotta nei post di individui con OCD rispetto ai controlli sani. Inoltre, nei test diagnostici su vignette cliniche fittizie (Kim et al., 2024), i Large Language Models (ChatGPT-4, Gemini 1.5, Llama 3) hanno superato in accuratezza diagnostica zero-shot i professionisti sanitari (psichiatri, medici, psicologi) e gli studenti di dottorato nell'identificare correttamente i quadri di OCD.
- **Generazione di Gerarchie di Esposizione (ERP):** Nello studio di Bernstein et al. (2025), ChatGPT-4 è stato impiegato per generare suggerimenti ed esercizi per gerarchie espositive in ERP: le gerarchie generate dall'LLM sono state valutate da esperti clinici come altamente appropriate, specifiche, variegate e utili per la strutturazione del percorso terapeutico.
- **Mappatura Semantica dei Cluster Ossessivi:** Feusner et al. (2021), analizzando 7.001 parole relative a sintomi ossessivi da un dataset internazionale di 25.369 utenti di un'app mobile tramite word embeddings (GloVe + Mittens), hanno evidenziato come i cluster ossessivi convergano centralmente sul tema del "danno a sé o agli altri" (*harm to self or others*), identificandolo come tema organizzatore latente comune a molteplici manifestazioni del disturbo.
- **Computer Vision e Marcatori Comportamentali Oggettivi:** L'integrazione di Computer Vision e ambienti di realtà virtuale consente la misurazione obiettiva dei comportamenti compulsivi (es. frequenza e durata delle azioni di controllo, latenza e movimenti ripetitivi nel lavaggio mani o nell'ordinamento di oggetti nei bambini, correlati positivamente ai punteggi della CY-BOCS).
- **Previsione della Risposta ai Trattamenti di Prima Linea:** Modelli di machine learning applicati a dati pre-trattamento di risonanza magnetica (fMRI resting-state e MRI strutturale) hanno identificato biomarcatori in grado di distinguere responder e non-responder a SSRI e CBT (Yun et al., 2015; Reggente et al., 2018).

### Limiti e Rischi Clinici
- **Predominanza di Analisi Secondarie e Carenza di Dati Prospettici:** L'84,6% degli studi inclusi ha utilizzato analisi secondarie di dati preesistenti (testi online, social network, archivi retrospettivi). Mancano quasi del tutto trial clinici prospettici controllati nel mondo reale con pazienti in carne ed ossa, limitando l'immediata trasferibilità clinica.
- **Rischio Iatrogeno di Rassicurazione Compulsiva (*Reassurance-Seeking*):** L'utilizzo diretto di chatbot generativi da parte dei pazienti con OCD comporta il rischio critico che il modello venga strumentalizzato come fonte inesauribile di rassicurazione (*reassurance seeking*), trasformando la conversazione con l'IA in un atto neutralizzante o compulsivo che alimenta il ciclo patologico anziché favorire l'abituazione e l'apprendimento inibitorio. La presenza del clinico supervisore (*human-in-the-loop*) rimane un requisito irrinunciabile.
- **Bias Algoritmici contro la Neurodivergenza:** Brandsen et al. (2024) hanno documentato che 11 modelli linguistici presentano bias impliciti e associazioni negative significative verso la neurodivergenza, collegando termini legati all'OCD a stereotipi di violenza, devianza, insulti o ossessività dispregiativa nei test WEAT e SERT.
- **Difficoltà di Generalizzazione del Neuroimaging:** Grandi consorzi multicentrici (ENIGMA-OCD) mostrano che i classificatori basati su neuroimaging strutturale o connettoma funzionale non riescono a generalizzare efficacemente a livello del singolo individuo tra centri differenti, complice la forte eterogeneità clinica e l'effetto confondente dei trattamenti psicofarmacologici pregressi.
- **Necessità di Framework Valutativi Multidimensionali:** È urgente l'adozione di framework specifici per la validazione clinica dell'IA in salute mentale (come FAITA-Mental Health a 6 domini e READI) per testare trasparenza, equità, gestione delle crisi e privacy differenziale.

## Riferimenti Bibliografici
- Bernstein, E. E., Jaroszewski, A. C., Jacoby, R. J., Bailen, N. H., Ragan, J., Usmani, A., & Wilhelm, S. (2025). Feasibility of using ChatGPT to generate exposure hierarchies for treating obsessive-compulsive disorder. *Behavior Therapy*. https://doi.org/10.1016/j.beth.2025.02.005
- Brandsen, S., Chandrasekhar, T., Franz, L., Grapel, J., Dawson, G., & Carlson, D. (2024). Prevalence of bias against neurodivergence-related terms in artificial intelligence language models. *Autism Research*, 17(2), 234–248. https://doi.org/10.1002/aur.3079
- Feusner, J. D., Mohideen, R., Smith, S., Patanam, I., Vaitla, A., Lam, C., Massi, M., & Leow, A. (2021). Semantic linkages of obsessions from an international obsessive-compulsive disorder mobile app data set: Big data analytics study. *Journal of Medical Internet Research*, 23(12), e25482. https://doi.org/10.2196/25482
- Golden, A., & Aboujaoude, E. (2024). Describing the framework for AI tool assessment in mental health and applying it to a generative AI obsessive-compulsive disorder platform: Tutorial. *JMIR Formative Research*, 8, e62963. https://doi.org/10.2196/62963
- Kim, J., Gonzalez Pacheco, J. P., Golden, A., Aboujaoude, E., van Roessel, P., Gandhi, A., Mukunda, P., Avanesyan, T., Xue, H., Adeli, E., Kim, J. P., Saggar, M., Wiltsey Stirman, S., Kuhn, E., Supekar, K., Pohl, K. M., & Rodriguez, C. I. (2025). Artificial Intelligence in Obsessive-Compulsive Disorder: A Systematic Review. *Current Treatment Options in Psychiatry*, 12, 23. https://doi.org/10.1007/s40501-025-00359-8
- Kim, J., Leonte, K. G., Chen, M. L., Torous, J. B., Linos, E., Pinto, A., & Rodriguez, C. I. (2024). Large language models outperform mental and medical health care professionals in identifying obsessive-compulsive disorder. *NPJ Digital Medicine*, 7(1), 193. https://doi.org/10.1038/s41746-024-01188-6
- Reggente, N., Moody, T. D., Morfini, F., Sheen, C., Rissman, J., O’Neill, J., & Feusner, J. D. (2018). Multivariate resting-state functional connectivity predicts response to cognitive behavioral therapy in obsessive-compulsive disorder. *Proceedings of the National Academy of Sciences*, 115(9), 2222–2227. https://doi.org/10.1073/pnas.1716686115

## Relazioni
- [automated-erp-training](concetti/automated-erp-training.md)
- [client101-simulazione-pazienti-virtuali](client101-simulazione-pazienti-virtuali.md)
- [exposure-interruption-mechanism](concetti/exposure-interruption-mechanism.md)
- [deliberate-practice-in-psicoterapia-ia](concetti/deliberate-practice-in-psicoterapia-ia.md)
- [diagnostic-accuracy-gap-llm-vs-physicians](concetti/concetti/concetti\diagnostic-accuracy-gap-llm-vs-physicians.md)
- [supervisione-clinica-ai](supervisione-clinica-ai.md)
- [ai-blended-therapy](ai-blended-therapy.md)
- [cbt](concetti/cbt.md)

