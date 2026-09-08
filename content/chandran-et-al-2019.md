---
tags: [nlp, ehr, ocs, schizophrenia, bipolar-disorder, gate]
source_papers: ["Chandran_D_et_al_NLP_for_OCS_in_SMI_Scientific_Reports_author_accepted_Sept_2019.pdf"]
---

# Use of Natural Language Processing to identify Obsessive Compulsive Symptoms in patients with severe mental illness

## Definizione Operativa
- Sviluppo e validazione di un algoritmo di Natural Language Processing (NLP) basato su regole (utilizzando il software GATE) per estrarre e identificare automaticamente la presenza di Sintomi Ossessivo-Compulsivi (OCS) o OCD dalle cartelle cliniche elettroniche (EHR) in testo libero di pazienti con disturbi mentali gravi (schizofrenia, disturbo schizoaffettivo o disturbo bipolare).
- **Utilità CBT / Applicativa:** Automatizza lo screening dei sintomi ossessivo-compulsivi in grandi database clinici (es. sistema CRIS), superando i limiti delle semplici ricerche per parole chiave. Permette di distinguere le reali ossessioni/compulsioni dalle descrizioni metaforiche o dai manierismi schizofrenici, facilitando l'individuazione di pazienti target per interventi mirati come la CBT.

## Evidenze dalla Letteratura
- **Efficacia:** L'approccio basato su regole si è dimostrato fattibile e valido per estrarre informazioni sintomatologiche complesse dai testi non strutturati. L'algoritmo ha raggiunto una *precision* di 0.77 e una *recall* di 0.67 nell'identificazione di qualsiasi OCS (con una precisione di 1.0 e recall di 0.85 specifica per la diagnosi di OCD) (Chandran et al., 2019).
- **Limiti:** L'approccio *rule-based* richiede molto tempo per lo sviluppo manuale delle regole e dei dizionari di inclusione/esclusione (es. gestione delle negazioni o di sintomi riportati dai familiari). La *recall* (0.67) risulta inferiore alla *precision*, implicando un rischio di sottostima (falsi negativi) dei casi di OCS per privilegiare l'assenza di falsi positivi (Chandran et al., 2019).

## Riferimenti Bibliografici
- Chandran, D., Ahn, D. Y., Chang, C.-K., Shetty, H., Sanyal, J., Downs, J. M., Fok, M., Ball, M., Jackson, R. G., Stewart, R., Cohen, H., Vermeulen, J. M., Schirmbeck, F., de Haan, L., & Hayes, R. (2019). Use of Natural Language Processing to identify Obsessive Compulsive Symptoms in patients with schizophrenia, schizoaffective disorder or bipolar disorder. *Scientific Reports*.

## Relazioni
- Vedi anche: [[nlp-ehr-ocs-detection]]
