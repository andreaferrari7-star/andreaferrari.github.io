---
tags:
  - cbt
  - ocd
  - machine-learning
  - neuroimaging
  - rs-fmri
  - treatment-outcome-prediction
  - remission-prediction
  - y-bocs
  - random-forest
  - support-vector-machine
  - enigma-ocd
source_papers:
  - 1-s2.0-S0165032725011711-main.pdf
---

# Development and Validation of a Machine Learning Model to Predict Cognitive Behavioral Therapy Outcome in Obsessive-Compulsive Disorder Using Clinical and Neuroimaging Data

## Definizione Operativa

*   **Framework Metodologico:** Studio prognostico multicentrico di coorte condotto all'interno del consorzio internazionale **ENIGMA-OCD**, mirato a sviluppare e validare modelli di Machine Learning supervisionato (Random Forest e Support Vector Machine) per la predizione pre-trattamento dell'esito della Terapia Cognitivo-Comportamentale (CBT) con Esposizione e Prevenzione della Risposta (ERP) in pazienti adulti con Disturbo Ossessivo-Compulsivo (OCD, DSM-IV/5; $N = 159$).
*   **Pipeline Computazionale e Validazione Multicentrica:**
    *   *Sorgenti di Dati:* Confronto sistematico tra tre configurazioni di input: (1) soli parametri clinico-anamnestici e demografici di routine, (2) soli parametri di risonanza magnetica funzionale a riposo (rs-fMRI: *fractional amplitude of low frequency fluctuations* [fALFF], *regional homogeneity* [ReHo] su atlante Schaefer 400, e matrici di connettività funzionale inter-regionale $330 \times 330$), (3) modello multimodale combinato.
    *   *Strategia di Cross-Validation:* Implementazione di un framework nested *Leave-One-Site-Out* (LOSO) su 4 centri clinici indipendenti (Amsterdam, Bellvitge/Barcellona, Bergen, UCLA) per valutare la reale generalizzabilità a nuovi contesti ospedalieri, integrata da una nested $3 \times 5$ cross-validation con armonizzazione ComBat per gli effetti centro/scanner.
    *   *Categorizzazione degli Esiti:* Disaccoppiamento tra **Risposta Clinica** (*response*, riduzione $\ge 35\%$ del punteggio Yale-Brown Obsessive Compulsive Scale [Y-BOCS]) e **Remissione Clinica** (*remission*, punteggio Y-BOCS post-trattamento $\le 12$), oltre alla regressione continua sul punteggio Y-BOCS post-terapia (SVR e RF Regressor).
*   **Utilità CBT:** Consente al clinico e all'équipe psichiatrica di identificare tempestivamente, prima dell'inizio del ciclo di esposizione, i pazienti ad alto rischio di mancata remissione con i protocolli standard, consentendo una stratificazione basata sull'evidenza (es. incremento dell'intensità terapeutica, erogazione di protocolli intensivi tipo Bergen 4-day, o combinazione precoce con farmacoterapia SSRI).

## Evidenze dalla Letteratura

### Efficacia Predittiva dei Modelli Clinici
*   **Discriminazione della Remissione:** L'impiego esclusivo delle variabili cliniche di routine ha mostrato una capacità predittiva statisticamente significativa e moderata per la remissione clinica, raggiungendo un'**AUC di 0.69** ($95\%\text{ CI } [0.58, 0.73]$, $p = 0.001$) mediante classificatore Random Forest in validazione *leave-one-site-out* (Sensibilità: $0.70 \pm 0.21$; Specificità: $0.68 \pm 0.26$; PPV: $0.67 \pm 0.20$; NPV: $0.75 \pm 0.20$; con SVM: $\text{AUC} = 0.63 \pm 0.07$).
*   **Fattori Clinici Determinanti (SHAP Values):** L'analisi dei valori Shapley (SHAP) ha evidenziato che la probabilità di raggiungere la remissione post-CBT è massimizzata dalla presenza di:
    1.  *Minore gravità sintomatica al baseline:* Punteggi Y-BOCS basali inferiori;
    2.  *Età più giovane:* Pazienti in fasce di età più precoci;
    3.  *Assenza di ossessioni di contaminazione e lavaggio:* I pazienti con ossessioni di pulizia/contaminazione (*cleaning/contamination*) hanno mostrato tassi di remissione significativamente inferiori rispetto ad altri sottotipi (aggressivi, simmetria, religiosi);
    4.  *Stato non medicato (Drug-Free Status):* L'assenza di terapia farmacologica concomitante (SSRI/antipsicotici) prima e durante il trattamento predice una maggiore probabilità di remissione psicoterapeutica;
    5.  *Maggiore livello di istruzione:* Anni superiori di scolarizzazione formale.
*   **Superiorità del Modello Multivariato sulla Y-BOCS Singola:** L'analisi ROC univariata della sola gravità Y-BOCS basale ha evidenziato un'AUC nominale di 0.72 (cut-off ottimale a 23.5 con balanced accuracy 0.67), ma caratterizzata da una marcata asimmetria tra sensibilità (0.87) e specificità (0.46). Il modello multivariato Random Forest supera tale limite, offrendo un profilo bilanciato che riduce drasticamente i falsi positivi di non-remissione.

### Limiti e Fallimento del Neuroimaging Multicentrico
*   **Incapacità Predittiva della rs-fMRI:** I modelli basati esclusivamente sui biomarcatori di risonanza magnetica funzionale a riposo non hanno superato il livello del caso nella predizione della risposta clinica:
    *   *fALFF:* $\text{AUC} = 0.52 \pm 0.04$ (SVM), $\text{AUC} = 0.56 \pm 0.06$ (RF);
    *   *ReHo:* $\text{AUC} = 0.44 \pm 0.05$ (SVM), $\text{AUC} = 0.50 \pm 0.08$ (RF);
    *   *Connettività Funzionale inter-regionale:* $\text{AUC} = 0.44 \pm 0.10$ (SVM), $\text{AUC} = 0.44 \pm 0.04$ (RF).
*   **Modesto Riscontro su ReHo per la Remissione:** Nella predizione della remissione, solo l'omogeneità regionale (ReHo) ha ottenuto un'accuratezza marginale superiore al caso ($\text{AUC} = 0.59 \pm 0.08$ con RF; $\text{AUC} = 0.57 \pm 0.09$ con SVM), mentre connettività funzionale ($\text{AUC} = 0.45 - 0.50$) e fALFF ($\text{AUC} = 0.49 - 0.50$) sono rimaste interamente casuali.
*   **Assenza di Valore Incrementale Multimodale:** L'integrazione congiunta di dati clinici e rs-fMRI non ha migliorato le performance rispetto ai soli dati clinici: la combinazione migliore (Dati Clinici + ReHo) ha raggiunto un'AUC di appena 0.61-0.63 con RF e SVM, risultando inferiore all'AUC di 0.69 ottenuta con i soli dati clinici anamnestici.
*   **Invarianza Biologica Univariata:** L'analisi univariata voxel-wise su tutto l'encefalo (SPM12, correzione *Family-Wise Error* [FWE] a $p < 0.05$) e l'analisi di rete basata su connettività (*Network-Based Statistics*, NBS) non hanno evidenziato alcuna differenza statisticamente significativa nei parametri basali di connettività o ampiezza neurale tra futuri remitter e non-remitter.
*   **Fallimento della Regressione Continua:** Il tentativo di prevedere il punteggio continuo Y-BOCS post-intervento tramite SVR e RF Regressor ha prodotto errori elevati ($\text{RMSE} = 6.05$ per i dati clinici) e un coefficiente $R^2$ nullo o negativo per i dati fMRI.
*   **Eterogeneità dei Protocolli e Inefficacia di ComBat:** La correzione per gli effetti sito/scanner mediante ComBat non ha incrementato le performance di validazione incrociata. La variabilità multicentrica nei protocolli terapeutici (es. formato intensivo Bergen di 4 giorni vs. sedute settimanali standard individuali o di gruppo, con durata compresa tra 4 e 24 settimane) e le differenze nell'acquisizione delle immagini rappresentano forti limiti ecologici.
*   **Sbilanciamento di Classe nella Risposta vs Remissione:** Mentre la maggioranza del campione ($69\%$) ha risposto alla CBT rendendo difficile la classificazione anche con *random under-sampling*, la remissione ha presentato una distribuzione più equilibrata ($42\%$), confermandosi l'outcome prognosticamente e clinicamente più rilevante.

## Riferimenti Bibliografici

*   Bruin, W. B., Taylor, L., Thomas, R. M., van Rooij, D., Vriend, C., van de Mortel, L. A., ... & van Wingen, G. A. (2023). The functional connectome in obsessive-compulsive disorder: resting-state mega-analysis and machine learning classification for the ENIGMA-OCD consortium. *Molecular Psychiatry*, 28(10), 4307–4319. https://doi.org/10.1038/s41380-023-02157-w
*   Elsner, B., Kathmann, N., Schmidt, H. P., & Riesel, A. (2020). Long-term stability of benefits of cognitive behavioral therapy for obsessive compulsive disorder depends on symptom remission during treatment. *Clinical Psychology in Europe*, 2(1), Article e2785. https://doi.org/10.32872/cpe.v2i1.2785
*   Hansen, B., Kvale, G., Hagen, K., Havnen, A., & Öst, L. G. (2018). The Bergen 4-day OCD treatment delivered in a group setting: 12-month follow-up. *Behaviour Research and Therapy*, 107, 10–16. https://doi.org/10.1016/j.brat.2018.05.006
*   Simpson, H. B., Huppert, J. D., Petkova, E., Foa, E. B., & Liebowitz, M. R. (2006). Response versus remission in obsessive-compulsive disorder. *The Journal of Clinical Psychiatry*, 67(2), 269–276. https://doi.org/10.4088/jcp.v67n0214
*   Van de Mortel, L. A., Bruin, W. B., Alonso, P., Bertolín, S., Feusner, J. D., Guo, J., Hagen, K., Hansen, B., Thorsen, A. L., Martínez-Zalacaín, I., Menchón, J. M., Nurmi, E. L., O'Neill, J., Piacentini, J. C., Real, E., Segalàs, C., Soriano-Mas, C., Thomopoulos, S. I., Stein, D. J., Thompson, P. M., van den Heuvel, O. A., & van Wingen, G. A. (2025). Development and validation of a machine learning model to predict cognitive behavioral therapy outcome in obsessive-compulsive disorder using clinical and neuroimaging data. *Journal of Affective Disorders*, 389, 119729. https://doi.org/10.1016/j.jad.2025.119729

## Relazioni

*   [[cbt-outcome-prediction-in-ocd]]
*   [[treatment-outcome-and-relapse-prediction]]
*   [[clinical-prediction-model-evaluation]]
*   [[automated-erp-training]]
*   [[cbt]]
*   [[tripod-ai2024]]
