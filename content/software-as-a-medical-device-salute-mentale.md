# Software as a Medical Device (SaMD) in Salute Mentale

**Summary**: Framework regolatorio, metodologico e clinico per l'integrazione di sistemi di intelligenza artificiale certificati come dispositivi medici (SaMD) nei servizi sanitari pubblici, con focus sulla gestione dei pazienti Not-On-Track e la validazione tramite RCT in cieco.
**Sources**: 05-11 Discussione del Gruppo di Ricerca su AI e Psicoterapia.txt
**Last updated**: 2026-08-27
---

## Definizione e Contesto di Applicazione

La classificazione di algoritmi e piattaforme di intelligenza artificiale come **Software as a Medical Device (SaMD)** rappresenta il massimo livello di integrazione formale e regolatoria dell'IA nella salute mentale:
- Differisce dai comuni software di benessere o chatbot generalisti in quanto è destinato a compiti di diagnosi, supporto alle decisioni cliniche, monitoraggio degli esiti e guida dell'intervento psicoterapeutico.
- Richiede l'approvazione rigorosa da parte di enti regolatori internazionali (come FDA negli Stati Uniti e conformità Medical Device Regulation / MDR in Europa).

---

## Il Modello NHS / NIHR e il Progetto di Ricerca (Prof. Delgadillo)

Un esempio applicativo di rilievo internazionale discusso dal gruppo è il bando di ricerca NIHR (National Institute for Health and Care Research) per il Servizio Sanitario Nazionale britannico (NHS - *Talking Therapies* / ex IAPT):
- **Obiettivi Primari**:
  1. Incrementare l'efficacia dei trattamenti per disturbi d'ansia e depressione del **10%**.
  2. Ridurre drasticamente i tassi di abbandono precoce della terapia (*dropout*).
- **Integrazione *End-to-End* lungo l'intero Percorso Clinico**:
  - *Fase di pre-screening e triage automatizzato*.
  - *Assessment multidimensionale* (inclusa analisi del tono di voce ed elaborazione emotiva).
  - *Monitoraggio continuo del processo terapeutico*.

---

## Digitalizzazione del Protocollo *Not-On-Track* (CTS)

L'elemento innovativo cardine del sistema consiste nell'automazione del protocollo clinico per pazienti **Not-On-Track** (soggetti che non mostrano il trend di miglioramento clinico atteso o mostrano segnali precoci di deterioramento):
- **Tracciamento Predittivo delle Traiettorie**: Riconoscimento tempestivo delle discrepanze tra la curva di risposta del paziente e le traiettorie normative evidence-based.
- **Supporto Decisionale Algoritmico alla Diade Clinica**: Il sistema attiva indicazioni procedurali guidate per il terapeuta e feedback strutturati per il paziente, facilitando l'applicazione di protocolli di correzione e recupero della rottura dell'alleanza terapeutica (CTS) altrimenti troppo complessi per essere gestiti manualmente nella routine clinica.

---

## Standard di Validazione Clinica e Barriere Regolatorie

Ottenere la certificazione SaMD impone requisiti di evidenza empirica eccezionalmente elevati:
- **Pipeline Triennale**: Fase di prototipizzazione e co-design clinico (Anno 1) seguita da due anni di Trial Controllati Randomizzati (RCT) condotti all'interno delle strutture ospedaliere/territoriali del servizio sanitario.
- **Test in Cieco su Campioni Rappresentativi**: I requisiti FDA/MDR prevedono una verifica formale a cieco (*one-shot evaluation*) su popolazioni controllate non note a priori allo sviluppatore; l'incapacità dell'algoritmo di replicare performance omogenee su tutta la coorte comporta il rigetto della certificazione.
- **Sicurezza dei Dati e Prevenzione Data Breach**: Necessità di un'architettura software e crittografica rigorosa per prevenire violazioni e garantire la conformità al GDPR e agli standard sanitari internazionali.

---

## Related pages
- [[05-11_Discussione_Gruppo_Ricerca]]
- [[libet-prime-agenti-didattici]]
- [[human-in-the-reasoning]]
- [[digital-therapeutic-alliance]]
- [[ai-research-ethics]]
- [[large-language-models]]
