---
tags: []
---

# Etica, Privacy e Bias nell'IA Clinica

**Summary**: Analisi delle sfide deontologiche, della tutela dei dati ipersensibili e dei bias sistematici di genere/diagnostici nell'utilizzo dei modelli linguistici in psicoterapia, con definizione delle buone pratiche di alfabetizzazione clinica.
**Sources**: `05-11 Discussione del Gruppo di Ricerca su AI e Psicoterapia.txt`, `04-17 Convegno_ Integrazione ed etica dell'Intelligenza Artificiale in Psicoterapia.txt`, `05-08 Riunione_ Sviluppo Knowledge Base AI, Etica e Applicazioni Cliniche.txt`
**Last updated**: 2026-08-27
---

## Deontologia e Tutela della Privacy Sanitaria

L'integrazione informale degli LLM nella pratica clinica espone i professionisti a gravi rischi etici e normativi legati alla gestione dei dati dei pazienti:
- **Trattamento Inadeguato del Materiale Clinico**: Pratiche scorrette quali il caricamento diretto su chatbot commerciali di fotografie di schede ABC, trascrizioni di sedute o appunti anamnestici senza consenso informato e senza preventiva de-identificazione.
- **Dati Ipersensibili**: Necessità di riconoscere che elementi come l'orientamento sessuale, il credo religioso, la storia traumatica e i pattern relazionali costituiscono dati a massimo vincolo di riservatezza, che richiedono canali criptati e conformità rigorosa al GDPR e agli standard HIPAA.

---

## Bias Impliciti e Disparità nei Modelli Linguistici

I modelli generativi incorporano bias cognitivi e socio-culturali derivanti dai dataset di pre-training:
- **Bias di Genere nella Valutazione Diagnostica**: Studi sperimentali evidenziano che, a parità di criteri clinici e vignette descrittive, i modelli tendono ad attribuire una gravità significativamente superiore e una peggiore prognosi a pazienti di genere femminile con tratti borderline rispetto a controparti maschili.
- **Trasparenza Apparente della "Scatola Nera"**: Le recenti implementazioni in cui i modelli mostrano la "catena di ragionamento" (*thinking process*) rappresentano spesso simulazioni a posteriori e non garantiscono la reale interpretabilità dei pesi neurali probabilistici sottostanti.
- **Strumenti di Filtraggio e Mitigazione**: Prospettiva di sviluppo di filtri algoritmici standardizzati di de-biasing da integrare preventivamente nei modelli sanitari dedicati.

---

## Oltre l'Allarmismo Politico-Difensivo

La reazione iniziale della comunità professionale e degli ordini professionali si è spesso polarizzata su posizioni di allarmismo difensivo (analogamente a quanto accaduto per le prime regolamentazioni della terapia online durante l'emergenza COVID):
- **Necessità di Buone Pratiche Proattive**: Il divieto o la delega passiva devono essere sostituiti da linee guida operative concrete che consentano l'uso sicuro, etico ed efficace delle tecnologie.

---

## Il Modello Formativo a Tre Pilastri per Psicoterapeuti

Per garantire un utilizzo clinicamente ed eticamente fondato dell'IA, il gruppo di ricerca propone un percorso formativo strutturato su tre aree:
1. **Comprendere l'Architettura**: Conoscere il funzionamento probabilistico degli LLM, la tokenizzazione, i limiti inferenziali e i bias sistematici.
2. **Saper Costruire gli Agenti**: Progettare knowledge base strutturate, definire prompt modulari ed esplicitare i pattern cognitivi nei casi clinici.
3. **Saper Interrogare e Governare l'Interazione**: Applicare tecniche di prompt engineering socratico, preservando l'autonomia clinica e la riservatezza deontologica.

---

## Related pages
- [05-11_Discussione_Gruppo_Ricerca_AI_Psicoterapia](../sintesi/05-11_Discussione_Gruppo_Ricerca_AI_Psicoterapia.md)
- [human-in-the-reasoning](human-in-the-reasoning.md)
- [simulazione-pazienti-ai](simulazione-pazienti-ai.md)
- [software-as-a-medical-device-salute-mentale](software-as-a-medical-device-salute-mentale.md)
- [ai-research-ethics](../ai-research-ethics.md)
- [large-language-models](../large-language-models.md)
- [prompting-in-psychology](../prompting-in-psychology.md)

## Riferimenti Bibliografici
- [Da integrare]
