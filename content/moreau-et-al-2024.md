---
tags: [ocpd, machine-learning, five-factor-model, neuroimaging, cortical-thickness]
source_papers: ["nihms-2055764.pdf"]
---

# Leveraging Normative Personality Data and ML to Examine Brain Correlates of OCPD

## Definizione Operativa
- Studio che utilizza algoritmi di Machine Learning (es. *elastic net regression*) per prevedere i tratti del Disturbo Ossessivo-Compulsivo di Personalità (OCPD) a partire dai dati normativi sulla personalità del Modello a Cinque Fattori (FFM, misurati via NEO-PI-R), per poi mapparli su ampi dataset di neuroimaging strutturale.
- **Utilità CBT / Applicativa:** Permette di stimare la gravità dei tratti OCPD anche in assenza di valutazioni cliniche dirette, usando test di personalità standard. Fornisce evidenze sul fatto che l'OCPD sia un'estremizzazione disadattiva di tratti normativi (es. coscienziosità estrema, bassa apertura, alto nevroticismo), aiutando a concettualizzare gli interventi CBT non come cura di una patologia categorica, ma come rimodulazione di tratti di personalità dimensionali.

## Evidenze dalla Letteratura
- **Risultati (Modello FFM):** Il Machine Learning ha dimostrato che i tratti OCPD possono essere previsti con moderata accuratezza dai 5 fattori del FFM (in particolare dalle sfaccettature di Coscienziosità e Apertura). A livello neuroanatomico, punteggi predetti di OCPD più elevati sono risultati significativamente associati a un maggiore spessore corticale nel giro frontale superiore destro (rSFG), un'area chiave per il controllo inibitorio e le funzioni esecutive (Moreau et al., 2024).
- **Limiti:** Nonostante il collegamento univariato con il rSFG, i modelli multivariati che tentavano di prevedere l'OCPD partendo *esclusivamente* dalle caratteristiche cerebrali hanno mostrato performance scadenti. Questo suggerisce che le alterazioni cerebrali legate all'OCPD sono caratterizzate da effetti (effect sizes) molto piccoli, difficili da catturare in modo robusto anche con il Machine Learning (Moreau et al., 2024).

## Riferimenti Bibliografici
- Moreau, A. L., Gorelik, A. J., Knodt, A., Barch, D. M., Hariri, A. R., Samuel, D. B., Oltmanns, T. F., Hatoum, A. S., & Bogdan, R. (2024). Leveraging normative personality data and machine learning to examine the brain structure correlates of Obsessive-Compulsive Personality Disorder traits. *Journal of Psychopathology and Clinical Science*, 133(8), 656–666. https://doi.org/10.1037/abn0000919

## Relazioni
- Vedi anche: [[ffm-ocpd-prediction]], [[ocpd-neural-correlates]]
