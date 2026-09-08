---
tags: [nlp, ehr, ocs, rule-based-extraction, gate]
source_papers: ["Chandran_D_et_al_NLP_for_OCS_in_SMI_Scientific_Reports_author_accepted_Sept_2019.pdf"]
---

# NLP per la Rilevazione OCS nelle EHR (NLP-EHR OCS Detection)

## Definizione Operativa
- Metodologia di Natural Language Processing applicata alle Electronic Health Records (EHR) in testo libero per individuare e classificare i sintomi ossessivo-compulsivi (OCS). A differenza del Machine Learning puramente statistico, l'approccio classico (es. tramite GATE - Generalized Architecture for Text Engineering) utilizza set complessi di regole linguistiche, dizionari di inclusione/esclusione, filtri per le negazioni e identificazione del soggetto dell'esperienza.
- **Utilità CBT / Applicativa:** Risolve il problema dell'oscurità dei dati clinici testuali ("dark data"). Nell'ambito dell'OCD e della psicosi, permette di mappare retrospettivamente grandi coorti di pazienti, estraendo descrizioni sintomatologiche (es. "compulsioni di lavaggio" o "pensieri intrusivi") per indirizzare tempestivamente protocolli CBT specifici, distinguendo i sintomi reali da usi metaforici delle parole "ossessione" o "compulsione".

## Evidenze dalla Letteratura
- **Vantaggi:** Garantisce elevata precisione ("Positive Predictive Value") poiché le regole sono modellate sull'effettivo ragionamento clinico. Ad esempio, è possibile escludere i manierismi schizofrenici o la ricerca di rischio ("gambling compulsion") non correlati all'OCD.
- **Sfide:** Lo sviluppo manuale delle regole è computazionalmente e temporalmente dispendioso (rispetto ai moderni LLM zero-shot) ed è incline a falsi negativi (bassa sensibilità o "recall") se i clinici descrivono i sintomi in modi non previsti dal set di regole codificato (Chandran et al., 2019).

## Riferimenti Bibliografici
- Chandran, D., Ahn, D. Y., Chang, C.-K., Shetty, H., Sanyal, J., Downs, J. M., Fok, M., Ball, M., Jackson, R. G., Stewart, R., Cohen, H., Vermeulen, J. M., Schirmbeck, F., de Haan, L., & Hayes, R. (2019). Use of Natural Language Processing to identify Obsessive Compulsive Symptoms in patients with schizophrenia, schizoaffective disorder or bipolar disorder. *Scientific Reports*.

## Relazioni
- Vedi anche: [[chandran-et-al-2019]]
