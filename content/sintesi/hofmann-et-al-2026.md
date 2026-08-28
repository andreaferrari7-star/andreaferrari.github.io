---
tags: [scoping-review, processi-di-cambiamento, process-based-therapy, cbt, fattori-comuni, llm-assisted-clustering, human-in-the-loop, prisma-scr]
source_papers: ["1-s2.0-S0272735826000917-main.pdf"]
---

# Processes in Psychotherapy: A Scoping Review with LLM-Assisted Clustering

## Sintesi dello Studio
- **Autori:** Stefan G. Hofmann, Lucie Pahlen, Marlon Westhoff, Karlin Hossner, Hicham Quintarelli, Franziska Usée, Kilian Stenzel, Ulrich Stangier (2026).
- **Rivista:** *Clinical Psychology Review*, Volume 128, Articolo 102782. https://doi.org/10.1016/j.cpr.2026.102782
- **Obiettivo:** Mappare sistematicamente il panorama empirico dei processi di cambiamento psicologico indagati negli studi di intervento psicoterapeutico dal 2007 al 2025 (in seguito all'articolo fondamentale di Kazdin, 2007) e sintetizzare l'eterogenea terminologia attraverso una procedura ibrida di clustering semantico assistita da Large Language Model (LLM) con supervisione umana (*Human-in-the-Loop*).

---

## Metodologia
1. **Disegno e Linee Guida:**
   - Scoping review condotta in conformità con le linee guida del *Joanna Briggs Institute* (JBI) e l'estensione *PRISMA for Scoping Reviews* (PRISMA-ScR).
   - Banche dati interrogate: PsycINFO, PsycArticles, PubMed, ScienceDirect, Web of Science (intervallo temporale: 2007–2025; parole chiave: `"process" AND "psychotherapy"` in titolo o abstract).
2. **Selezione degli Studi:**
   - 50.908 record iniziali identificati; 33.788 record unici sottoposti a screening su piattaforma Rayyan con doppio rater indipendente.
   - Criteri di inclusione: studi empirici quantitativi su interventi psicoterapeutici (RCT, studi a gruppo singolo, N-of-1) che indagavano processi psicologici o variabili di cambiamento intra-paziente o relazionali.
   - Campione finale incluso: **778 studi**, da cui sono state estratte **1.170 menzioni di processi**, corrispondenti a **684 etichette di processo uniche**.
3. **Workflow di Clustering Assistito da LLM (Human-in-the-Loop):**
   - Implementato in Python 3.12 via API OpenAI con modello **GPT-5 nano** (openai v2.15.0).
   - Inserimento iterativo a blocchi di 100 frasi con *few-shot prompting* teoricamente informato.
   - Ispezione, correzione e raffinamento manuale da parte di ricercatori clinici ad ogni ciclo (riallocazione, split/merge di cluster, eliminazione di allucinazioni).
   - Re-assegnazione finale vincolata di tutte le 684 etichette uniche all'insieme armonizzato di categorie sovraordinate, preservando la formulazione originale e ammettendo appartenenze multiple per costrutti multidimensionali.

---

## Risultati Principali
1. **Identificazione di 32 Cluster di Processo:**
   - I 684 processi unici sono stati organizzati in **32 cluster sovraordinati** (dimensioni da 5 a 77 etichette per cluster).
   - **Cluster Principali per Ricchezza Terminologica:**
     - *Therapeutic Alliance & Collaboration Processes* (77 processi, il più numeroso).
     - *Interpersonal Functioning Processes* (52 processi).
     - *Cognitive Reappraisal & Belief Change Processes* (52 processi).
     - *Metacognitive Processes* (48 processi).
     - *Emotional Regulation Processes* (40 processi).
     - *Emotional Activation Processes* (40 processi).
     - *Self-Concept Processes* (34 processi).
     - *Cognitive and Memory Processes* (24 processi).
     - *Attachment, Relational & Boundary Processes* (22 processi).
     - *Behavioral Activation, Change & Activity Processes* (22 processi).
     - *Motivation Processes* (22 processi).
     - *Therapy Outcome Specific Processes* (22 processi).
2. **Distribuzione tra Fattori Comuni e Fattori Specifici:**
   - I cluster riconducibili ai **fattori comuni** (*Alleanza Terapeutica & Collaborazione* e *Funzionamento Interpersonale*) rappresentano il **20,6%** di tutti i processi unici investigati.
   - I restanti processi appartengono in prevalenza a fattori specifici di matrice cognitivo-comportamentale (CBT e Terza Onda: ristrutturazione cognitiva, defusione, attivazione comportamentale, accettazione, problem-solving).
3. **Processi più Frequentemente Studiati:**
   - *Alleanza terapeutica* (67 studi), *Working alliance* (24), *Elaborazione emotiva* (21), *Alleanza* (19), *Insight* (18), *Mindfulness* (18), *Relazione terapeutica* (15), *Flessibilità psicologica* (14), *Mentalizzazione* (14), *Meccanismi di difesa* (13), *Regolazione emotiva* (13), *Autoefficacia* (10).
   - I primi 30 processi rappresentano il 33,7% di tutte le menzioni; circa la metà di tutti i processi estratti (48,3%) è stata esaminata in un solo studio, segnalando una marcata **frammentazione terminologica**.
4. **Stagnazione Temporale (2007–2025):**
   - Nonostante i frequenti appelli accademici verso la ricerca sui processi, la percentuale di studi focalizzati sui processi rispetto alla letteratura psicoterapeutica complessiva è rimasta **sostanzialmente invariata** nei quattro quinquenni analizzati (circa lo 0,3%–0,6% per i fattori comuni e l'1,9%–2,4% per gli altri processi).

---

## Implicazioni Cliniche e Metodologiche (Utilità CBT)
- **Distinzione Concettuale Indispensabile:**
  - *Interventi / Tecniche del Terapeuta:* Azioni e procedure messe in atto dal clinico (es. esposizione, ristrutturazione cognitiva, dialogo socratico).
  - *Processi di Cambiamento:* Meccanismi dinamici intra-personali, progressivi e multilivello nel paziente (es. variazioni nella valutazione cognitiva, accettazione, regolazione affettiva).
  - *Indicatori di Implementazione e Aderenza:* Esecuzione degli homework, dosaggio, fedeltà terapeutica.
  - *Indicatori Prossimali di Esito:* Variazioni sintomatiche intermedie nel corso del trattamento.
- **Superamento della Mediazione Lineare Semplice:** I modelli a singolo mediatore non catturano i sistemi dinamici e i circuiti di retroazione (*feedback loops*) tipici dell'adattamento psicologico. È necessario adottare modelli di rete idionomici e multivariati (*Process-Based Therapy* - PBT).
- **Risoluzione della "Jingle-Jangle Fallacy":** L'uso di definizioni rigorose ed empiricamente ancorate è essenziale per evitare che termini identici celino meccanismi dissimili o che etichette diverse frammentino lo stesso costrutto sottostante.
- **Valore del Ruolo Relazionale come Contesto Facilitatore:** L'alleanza e l'empatia costituiscono contesti interpersonali necessari per permettere l'attuazione e la generalizzazione delle strategie di cambiamento cognitivo e comportamentale nella vita quotidiana del paziente.

---

## Riferimenti Bibliografici
- Hofmann, S. G., Pahlen, L., Westhoff, M., Hossner, K., Quintarelli, H., Usée, F., Stenzel, K., & Stangier, U. (2026). Processes in psychotherapy: A scoping review with LLM-assisted clustering. *Clinical Psychology Review*, 128, Article 102782. https://doi.org/10.1016/j.cpr.2026.102782

---

## Relazioni e Collegamenti
- [[process-of-change]]
- [[llm-assisted-clustering]]
- [[common-vs-specific-factors]]
- [[terminological-fragmentation]]
- [[process-based-therapy]]
- [[jingle-fallacy]]
- [[jangle-fallacy]]
- [[hybrid-ai-research-workflows]]
