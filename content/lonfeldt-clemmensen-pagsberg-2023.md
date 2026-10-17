---
tags: [ocd, wearable-biosensors, machine-learning, adolescents, family-accommodation, erp, protocollo]
tipo_fonte: scientifica
source_papers: ["Predicting cognitive-behavioral therapy outcomes in obsessivecompulsive disorder from inhibitory control neural activity.pdf"]
---

# Wrist Angel: protocollo dello studio pilota su biosensore indossabile e IA nel DOC in età evolutiva (Lønfeldt, Clemmensen, & Pagsberg, 2023)

## Definizione Operativa
- Protocollo di uno studio pilota longitudinale, non randomizzato e caso-controllo, condotto in un centro pubblico di salute mentale dell'infanzia e dell'adolescenza a Copenaghen. Valuta se sia fattibile usare un biosensore da polso commerciale per monitorare i sintomi del disturbo ossessivo-compulsivo (DOC) in bambini e adolescenti, e se si possano sviluppare strumenti di IA che rilevino stati interni e processi familiari rilevanti per il DOC da segnali fisiologici, vocali e comportamentali (Lønfeldt, Clemmensen, & Pagsberg, 2023).
- **Utilità CBT / Applicativa:** descrive come raccogliere misure oggettive e continue del distress da usare nella CBT con esposizione e prevenzione della risposta (ERP): calibrare le esposizioni, seguire la risposta al trattamento tra una seduta e l'altra e aumentare la consapevolezza dei legami tra pensieri, emozioni, comportamenti e sensazioni corporee. I risultati dello studio sono in [[lonfeldt-et-al-2023]].

## Evidenze dalla Letteratura

### Disegno e partecipanti
- Obiettivo di 10 diadi paziente-genitore e 10 diadi controllo-genitore, con età dei ragazzi tra 8 e 17 anni. I pazienti hanno una diagnosi di DOC (ICD-10 F42) con punteggio CY-BOCS superiore a 7; i controlli non hanno diagnosi psichiatriche. Sono ammesse cure concomitanti, compresi psicoterapia, farmaci e lista d'attesa (Lønfeldt, Clemmensen, & Pagsberg, 2023).
- Ragazzi e genitori indossano per 8 settimane, da sveglia a sonno, il bracciale Empatica E4, che misura polso (fotopletismografia, da cui frequenza cardiaca e HRV), attività elettrodermica, temperatura cutanea e accelerazione. Pazienti e genitori premono un pulsante a ogni episodio di DOC; i controlli segnano gli episodi di paura (Lønfeldt, Clemmensen, & Pagsberg, 2023).
- All'inizio e dopo 8 settimane si svolgono esperimenti in laboratorio: riposo, poi un compito di esposizione fino a 15 minuti per i pazienti o attività fisica per i controlli, infine un compito di interazione genitore-figlio. Le sedute vengono filmate e codificate per affetto, sincronia, sensibilità del genitore, accomodamento e rassicurazione; i video sono analizzati anche con visione artificiale ed elaborazione del parlato. L'ossitocina salivare è misurata prima e dopo ogni condizione (Lønfeldt, Clemmensen, & Pagsberg, 2023).
- Questionari e interviste a 0, 4, 7 e 8 settimane: CY-BOCS, KIDSCREEN-52, accomodamento familiare (FAS-PR), stress genitoriale, DASS e Family Environment Scale. È in sviluppo anche un'app per valutazioni ecologiche momentanee (EMA) con esercizi di esposizione guidata (Lønfeldt, Clemmensen, & Pagsberg, 2023).

### Criteri di fattibilità
- Criteri fissati a priori: oltre il 30% delle famiglie invitate acconsente; ritenzione oltre l'80%; meno del 10% di malfunzionamenti irreparabili; atteggiamenti positivi verso il biosensore oltre l'85%; biosensore indossato in più del 30% dei giorni; più del 70% di eventi segnati correttamente; nessun danno o peggioramento dei sintomi; accuratezza superiore al 70% nel collegare i segnali agli esiti clinici (Lønfeldt, Clemmensen, & Pagsberg, 2023).
- Il protocollo misura la qualità dell'ERP secondo due teorie: la teoria dell'elaborazione emotiva, tramite l'abituazione (calo del distress senza evitamento né accomodamento), e la teoria dell'apprendimento inibitorio, tramite tre misure della violazione delle aspettative (Lønfeldt, Clemmensen, & Pagsberg, 2023). Vedi [[automated-erp-training]].
- Analisi: modelli a effetti misti per le associazioni tra ossitocina, segnali e condizioni; machine learning con doppia validazione incrociata, entro e tra soggetti, per classificare lo stress da DOC e prevedere gli episodi nella vita quotidiana (Lønfeldt, Clemmensen, & Pagsberg, 2023).

### Stato dello studio
- Il primo partecipante è stato arruolato il 3 dicembre 2021 e il reclutamento si è chiuso il 31 dicembre 2022: 9 diadi di pazienti e 9 di controllo, 16 delle quali hanno completato il follow-up (Lønfeldt, Clemmensen, & Pagsberg, 2023).
- Approvazione del comitato etico della Regione Capitale di Danimarca; registrazione NCT05064527; dati gestiti secondo il GDPR. Empatica è responsabile del trattamento per i segnali fisiologici, trasferiti in forma anonimizzata su un server sicuro (Lønfeldt, Clemmensen, & Pagsberg, 2023). Vedi [[gdpr-governance-mental-health-ai]].

### Limiti dichiarati
- Campione piccolo, che limita la generalizzabilità; rischio di falsi positivi e, con forte variabilità individuale, di falsi negativi (Lønfeldt, Clemmensen, & Pagsberg, 2023).
- Possibili ostacoli: aderenza a un dispositivo visibile, timore di stigma o di sorveglianza. Gli autori segnalano anche che chiedere a ragazzi con DOC di segnare gli eventi può interagire con il sintomo o diventarne parte (Lønfeldt, Clemmensen, & Pagsberg, 2023).

### Nota sul file sorgente
- Nel vault il protocollo è salvato con un nome di file che non corrisponde al contenuto: richiama il titolo del preprint ENIGMA-OCD (vedi [[dzinalija-et-al-2026]]).

## Riferimenti Bibliografici
- Lønfeldt, N. N., Clemmensen, L. K. H., & Pagsberg, A. K. (2023). A wearable artificial intelligence feedback tool (Wrist Angel) for treatment and research of obsessive compulsive disorder: Protocol for a nonrandomized pilot study. *JMIR Research Protocols*, *12*, Article e45123. https://doi.org/10.2196/45123

## Relazioni
- Vedi anche: [[lonfeldt-et-al-2023]], [[wearable-biosensors-ocd]], [[frank-et-al-2023]], [[automated-erp-training]], [[kim-et-al-2025]], [[gdpr-governance-mental-health-ai]]
