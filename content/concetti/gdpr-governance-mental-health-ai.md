---
title: GDPR Governance e Protezione Dati nell'IA per la Salute Mentale
last_updated: 2026-10-16
tags: [GDPR, AI Act, Salute Mentale, Privacy, Governance]
tipo_fonte: scientifica
source_papers: ["ai-v5-e84305.pdf"]
---

# GDPR Governance e Protezione Dati nell'IA per la Salute Mentale

## Definizione Operativa

Il framework di governance per l'Intelligenza Artificiale (IA) applicata alla salute mentale rappresenta l'insieme di norme, procedure tecniche e strategie di conformità progettate per conciliare le necessità di analisi dei dati (tipiche del Machine Learning e Deep Learning) con le stringenti tutele richieste per le categorie particolari di dati personali.

L'implementazione richiede una rigorosa aderenza ai principi del **Regolamento Generale sulla Protezione dei Dati (GDPR - Regolamento UE 2016/679)**, in particolare gli articoli 5 (principi del trattamento) e 9 (categorie particolari di dati), integrati con i requisiti dell'**AI Act (Regolamento UE 2024/1689)** per i sistemi ad alto rischio. La finalità è prevenire violazioni come il *purpose creep*, la re-identificazione non autorizzata e l'uso improprio di dati psicologici per finalità commerciali o discriminatorie.

## Evidenze dalla Letteratura

La ricerca evidenzia una tensione strutturale tra la raccolta massiva di dati, necessaria per addestrare i modelli, e la vulnerabilità delle popolazioni cliniche (Kandeel et al., 2026).

*   **Articolo 9 GDPR (categorie particolari di dati):** i dati sulla salute mentale, biometrici e genetici possono essere trattati solo in presenza di una base giuridica esplicita, come il consenso esplicito. Kandeel et al. (2026) segnalano che molti sistemi di IA non prevedono meccanismi di consenso adeguati e che la sorveglianza passiva dei social media rischia di sfruttare persone vulnerabili, come gli adolescenti, senza consenso informato.
*   **Articolo 5 GDPR (limitazione della finalità e minimizzazione):** i dati devono restare entro le finalità dichiarate al momento della raccolta, e i modelli di IA sollevano problemi di minimizzazione quando raccolgono più dati del necessario (Kandeel et al., 2026). Nel *digital phenotyping* i rischi per la privacy sono particolarmente rilevanti per gli adolescenti e richiedono salvaguardie normative (D'Alfonso et al., 2025).
*   **Rischi di re-identificazione:** una quota significativa di dati sanitari anonimizzati può essere re-identificata combinandola con dati ausiliari come i codici postali (Rocher et al., 2019). Nei sistemi NLP che analizzano post su Reddit per stimare il rischio depressivo, conservare metadati come orari di pubblicazione e stile di scrittura aumenta il rischio di re-identificazione (Guntuku et al., 2017). Entrambi gli studi sono citati da Kandeel et al. (2026), che indicano tra le contromisure l'apprendimento federato (cfr. [[federated-learning-and-differential-privacy-mental-health]]).
*   **Il caso BetterHelp:** i dati degli utenti sono stati riutilizzati a fini di marketing e ceduti a inserzionisti. Il caso mostra come una gestione dei dati non conforme porti a violazioni della privacy, che secondo gli autori possono derivare anche da lacune normative e non solo da condotte scorrette (Kandeel et al., 2026; Martinez-Martin & Kreitmair, 2018). Resta poco studiato quanto i sistemi di IA in salute mentale rispettino davvero il vincolo di finalità del GDPR (Kandeel et al., 2026).
*   **AI Act:** il Regolamento UE 2024/1689 classifica come ad alto rischio i sistemi di IA che rientrano nella disciplina dei dispositivi medici e richiedono una valutazione di conformità da parte di terzi (art. 6), con obblighi di governance dei dati, documentazione tecnica, trasparenza e sorveglianza umana (art. 14). Non tutte le applicazioni per la salute mentale rientrano in questa categoria: la distinzione tra app di benessere e dispositivi medici è trattata in [[demarcazione-wellness-vs-samd-salute-mentale]] e il quadro normativo italiano in [[normativa-llm-psicologia-in-italia]].

## Riferimenti Bibliografici

*   D'Alfonso, S., Coghlan, S., Schmidt, S., & Mangelsdorf, S. (2025). Ethical dimensions of digital phenotyping within the context of mental healthcare. *Journal of Technology in Behavioral Science*, *10*(1), 132–147. https://doi.org/10.1007/s41347-024-00423-9
*   Guntuku, S. C., Yaden, D. B., Kern, M. L., Ungar, L. H., & Eichstaedt, J. C. (2017). Detecting depression and mental illness on social media: An integrative review. *Current Opinion in Behavioral Sciences*, *18*, 43–49. https://doi.org/10.1016/j.cobeha.2017.07.005
*   Kandeel, M. E., Abo Hamza, E. G., Abouahmed, A., AbdelAziz, G. M., Hashish, A., Abo El Wafa, T., Khalil, A., & Eldakak, A. (2026). AI applications integrating legal and regulatory perspectives in mental health: Systematic review. *JMIR AI*, *5*, e84305. https://doi.org/10.2196/84305
*   Martinez-Martin, N., & Kreitmair, K. (2018). Ethical issues for direct-to-consumer digital psychotherapy apps: Addressing accountability, data protection, and consent. *JMIR Mental Health*, *5*(2), e32. https://doi.org/10.2196/mental.9423
*   Regolamento (UE) 2016/679 del Parlamento europeo e del Consiglio del 27 aprile 2016 relativo alla protezione delle persone fisiche con riguardo al trattamento dei dati personali (Regolamento generale sulla protezione dei dati). (2016). *Gazzetta ufficiale dell'Unione europea*, L 119, 1–88.
*   Regolamento (UE) 2024/1689 del Parlamento europeo e del Consiglio del 13 giugno 2024 che stabilisce regole armonizzate sull'intelligenza artificiale (AI Act). (2024). *Gazzetta ufficiale dell'Unione europea*, L 2024/1689.
*   Rocher, L., Hendrickx, J. M., & de Montjoye, Y.-A. (2019). Estimating the success of re-identifications in incomplete datasets using generative models. *Nature Communications*, *10*(1), 3069. https://doi.org/10.1038/s41467-019-10933-3

## Relazioni

*   [[kandeel-et-al-2026]]
*   [[federated-learning-and-differential-privacy-mental-health]]
*   [[software-as-a-medical-device-salute-mentale]]
*   [[demarcazione-wellness-vs-samd-salute-mentale]]
*   [[normativa-llm-psicologia-in-italia]]
*   [[three-layer-governance-framework]]
*   [[etica-privacy-bias-ia-clinica]]
*   [[algorithmic-paternalism-in-ai-mental-health]]
*   [[cross-cultural-bias-and-fairness-audits-ai]]
