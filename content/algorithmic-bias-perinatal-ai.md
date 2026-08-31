---
tags: [algorithmic-bias, fairness, perinatal-depression, maternal-health, electronic-health-records, clinical-ai-ethics, de-biasing, smote, false-positives, frontiers-in-psychiatry]
source_papers: ["fpsyt-16-1734102.pdf"]
---

# Bias Algoritmico ed Equità nell'IA per la Salute Mentale Perinatale

## Definizione Operativa
Il **Bias Algoritmico nell'IA per la Salute Mentale Perinatale** definisce la presenza di disparità sistematiche nell'accuratezza predittiva, nei tassi di falsi positivi/falsi negativi e nell'allocazione delle risorse clinico-assistenziali a danno di specifiche sottopopolazioni (minoranze etnico-razziali, donne a basso reddito, madri migranti) all'interno dei modelli di Machine Learning applicati allo screening della depressione perinatale e postpartum (PPD) (Ruger-Navarrete et al., 2026; *Frontiers in Psychiatry*, doi: 10.3389/fpsyt.2025.1734102).

**Rilevanza Clinica ed Etica:** Nelle applicazioni ospedaliere basate su cartelle cliniche elettroniche (EHR/EMR), l'addestramento ingenuo su dataset storici non calibrati rischia di perpetuare disuguaglianze strutturali: un eccesso di falsi positivi induce sovra-medicalizzazione, allarme ingiustificato e stigma, mentre un eccesso di falsi negativi priva madri vulnerabili di interventi preventivi tempestivi (Park et al., 2021; Liu et al., 2024).

## Evidenze dalla Letteratura

### 1. Bias Razziale ed Etnico nei Modelli EHR Ospedalieri
L'analisi empirica condotta su sistemi ospedalieri statunitensi evidenzia pattern precisi di disparità algoritmica:
- **L'Evidenza di Park et al. (2021):** Valutando diversi modelli di machine learning addestrati su cartelle elettroniche per la predizione della PPD, gli autori hanno rilevato che i modelli non calibrati producono sistematiche distorsioni razziali, con tassi di falsi positivi significativamente più elevati per le donne afroamericane e ispaniche rispetto alle pazienti caucasiche.
- **La Soluzione di Liu et al. (2024) per l'Uso Ospedaliero (*Bedside Deployment*):** In uno studio su tre ampi set di cartelle cliniche elettroniche ospedaliere, Liu et al. hanno dimostrato che l'inclusione della variabile demografica esplicita "razza/etnia" funge da scorciatoia statistica che amplifica il bias. Rimuovendo tale variabile e ricalibrando i predittori clinici oggettivi, il modello mantiene l'elevata capacità discriminativa eliminando la discrepanza nel tasso di falsi positivi.

### 2. Gestione del Forte Disequilibrio di Classe
La prevalenza della PPD (10-20%) induce i modelli a classificare erroneamente i soggetti come sani.
- **Tecniche di Over-Sampling e SMOTE (Shin et al., 2020; Fazraningtyas et al., 2025):** L'applicazione della *Synthetic Minority Over-sampling Technique* (SMOTE) e del bootstrapping stratificato sintetizza esempi della classe minoritaria, migliorando la sensibilità.
- **Modellazione Neurale con Ottimizzazione Bio-Ispirata (Tang et al., 2024):** L'integrazione di reti neurali con algoritmi *Artificial Bee Colony* (ABC) e *Proximal Policy Optimization* (PPO) abbatte la varianza dell'errore su popolazioni ad alto rischio.

### 3. Selezione di Feature e Controllo dell'Overfitting
- **Fast Feature Selection (FFS-RF) e SVM (Zhang et al., 2020):** L'impiego combinato di algoritmi di selezione rapida delle feature isola un sottoinsieme parsimonioso di variabili determinanti, azzerando il rumore e garantendo generalizzabilità su piccoli campioni.

**Riferimenti Bibliografici:**
- Ruger-Navarrete, A., et al. (2026). Artificial intelligence in the prevention and early detection of postpartum depression: a systematic review and meta-analysis. *Frontiers in Psychiatry*, 16, 1734102.
- Fazraningtyas, W. A., et al. (2025). A predictive model for postpartum depression: ensemble learning strategies in machine learning. *Indonesian Journal of Electrical Engineering and Computer Science*, 37, 443–451.
- Liu, Y., et al. (2024). Preparing for the bedside - optimizing a postpartum depression risk prediction model for clinical implementation in a health system. *Journal of the American Medical Informatics Association*, 31, 1258–1267.
- Park, Y., et al. (2021). Comparison of methods to reduce bias from clinical prediction models of postpartum depression. *JAMA Network Open*, 4(4), e213909.
- Shin, D., et al. (2020). Machine learning-based predictive modeling of postpartum depression. *Journal of Clinical Medicine*, 9(9), 2899.
- Shivaprasad, S., et al. (2024). Explainable machine learning methods to predict postpartum depression risk. *Systems Science & Control Engineering*, 12(1), 2427033.
- Tang, Y., et al. (2024). Postpartum depression identification: integrating mutual learning-based artificial bee colony and proximal policy optimization for enhanced diagnostic precision. *International Journal of Advanced Computer Science and Applications*, 15(4), 332–347.
- Zhang, W., et al. (2020). Machine learning models for the prediction of postpartum depression: application and comparison based on a cohort study. *JMIR Medical Informatics*, 8(4), e15516.

## Relazioni
- Vedi anche: [[fpsyt-16-1734102]], [[ai-perinatal-depression-prediction]], [[pediatric-ai-bias-and-vulnerabilities]], [[misurazione-bias-razziale-llm]], [[embedded-ethics-interface]], [[traffic-light-quality-appraisal-clinical-ai]], [[modello-centauro-clinico]], [[clinical-decision-making-and-artificial-intelligence]]
