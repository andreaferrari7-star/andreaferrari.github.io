---
created: 2026-08-31
updated: 2026-08-31
tags: [innovative-moment-assessment, narrative-therapy, ai-psychotherapy, process-of-change]
---

# Innovative Moment Assessment (IMA)

## Definizione Operativa
Metodologia di valutazione computazionale e clinica *process-oriented* che quantifica l'efficacia dei dialoghi psicoterapeutici attraverso il tracciamento degli *Innovative Moments* (IM) nel discorso del paziente. Basato sulla teoria di Gonçalves et al. (2011, 2012), l'IMA classifica 6 tipologie di IM su due livelli gerarchici e calcola la metrica di *IM Salience* per monitorare la progressione longitudinale del cambiamento narrativo.

IMA traduce l'*Innovative Moments Coding System (IMCS)* in una procedura rigorosa di valutazione automatica per sistemi di IA clinica.

## Evidenze dalla Letteratura
Nella ricerca sui processi psicoterapeutici ([[process-of-change]]), i **Momenti Innovativi (Innovative Moments - IM)** sono episodi in cui il paziente esprime contenuti che contraddicono la narrazione satura di problema (*problem-saturated narrative*), segnalando l'emergere di narrazioni alternative preferite (White, 2007; Gonçalves et al., 2011).

Le metriche convenzionali di NLP (come BLEU o BERTScore) falliscono nel catturare la **traiettoria dinamica e longitudinale della trasformazione clinica**. Feng et al. (2025) dimostrano che l'IMA supera i benchmark standard, misurando non solo l'empatia, ma la capacità dell'agente di guidare il paziente verso la trasformazione narrativa.

### Tassonomia dei Momenti Innovativi (IM)

#### Livello 1: Distanziamento dal Problema
Fasi precoci di esplorazione e decostruzione:
1. **Action I**: Azioni intraprese per superare il problema.
2. **Reflection I**: Consapevolezza degli effetti del problema e intenzione di contrastarlo.
3. **Protest I**: Rifiuto delle premesse del problema.

#### Livello 2: Centratura sul Cambiamento
Fasi avanzate di *re-authoring* e *re-membering*:
1. **Action II**: Generalizzazione proiettata nel futuro o nuovi progetti.
2. **Reflection II**: Contrasto tra sé passato/presente e trasformazione identitaria.
3. **Protest II**: Assertività matura e affermazione dei propri diritti.

### Regole di Codifica e Calcolo della Salienza
La metrica di **IM Salience** misura il peso percentuale del discorso orientato al cambiamento:
$$\text{Salience}(I_i) = \frac{\sum_{t=1}^N \text{WordCount}(C_t \cap I_i)}{\sum_{t=1}^N \text{WordCount}(C_t \cup T_t)}$$

**Riferimenti Bibliografici:**
- Gonçalves, M. M., et al. (2011). *Innovative moments in psychotherapy*.
- White, M. (2007). *Maps of Narrative Practice*.
- Feng, Y., et al. (2025). *Innovative Moment Assessment for AI Clinical Systems*.
- Montesano, A., et al. (2017). *Change processes in psychotherapy*.

## Relazioni
- [[feng-et-al-2025]]
- [[interactive-narrative-therapist]]
- [[terapia-narrativa-ia]]
- [[process-of-change]]
- [[clinical-fidelity-assessment]]
- [[process-based-therapy]]
- [[simulazione-pazienti-ai]]
