---
tags: [llm-assisted-clustering, clustering-semantico, human-in-the-loop, nlp, sintesi-letteratura, metodologia-ricerca]
tipo_fonte: scientifica
source_papers: ["1-s2.0-S0272735826000917-main.pdf"]
---

# LLM-Assisted Semantic Clustering

## Definizione Operativa
- Metodologia ibrida di raggruppamento e categorizzazione semantica di costrutti testuali non strutturati che combina la scalabilità computazionale dei Large Language Model (es. GPT-5 nano) con la supervisione continua, esperienziale e teorica di esperti umani (*Human-in-the-Loop*).
- Supera i limiti del clustering non supervisionato rigido ("hard" clustering come k-means) consentendo appartenenze sfumate (*fuzzy/overlapping clusters*), strutture gerarchiche e l'adattamento progressivo delle tassonomie concettuali.
- **Utilità CBT / Ricerca Clinica:** Consente di processare centinaia di etichette eterogenee utilizzate in letteratura clinica per sintetizzare mappe concettuali coerenti, riducendo le allucinazioni del modello e preservando al contempo le sfumature cliniche e teoriche.

## Evidenze dalla Letteratura
- Nello studio di scoping review di Hofmann et al. (2026), 778 studi pubblicati dal 2007 riportavano 684 processi di cambiamento terapeutico. Il workflow iterativo HITL in Python con GPT-5 nano li ha aggregati in 32 macro-cluster coerenti con i modelli teorici evidence-based.
- L'output del modello era vincolato a un formato JSON strutturato (identificativo del cluster, etichetta, frasi assegnate). La supervisione umana iterativa ha corretto errate attribuzioni, rimosso o accorpato categorie superflue e confrontato ogni frase con l'elenco originale per eliminare le voci allucinate (Hofmann et al., 2026).
- L'approccio ibrido offre una soluzione scalabile per superare la frammentazione terminologica della ricerca clinica senza cadere nell'arbitrarietà di tassonomie chiuse a priori.

## Riferimenti Bibliografici
- Hofmann, S. G., Pahlen, L., Westhoff, M., Hossner, K., Quintarelli, H., Usée, F., Stenzel, K., & Stangier, U. (2026). Processes in psychotherapy: A scoping review with LLM-assisted clustering. *Clinical Psychology Review*, 128, Article 102782. https://doi.org/10.1016/j.cpr.2026.102782

## Relazioni
- Vedi anche: [[1-s2-0-s0272735826000917-main]], [[hofmann-et-al-2026]], [[processes-of-change-in-psychotherapy]], [[hybrid-ai-research-workflows]], [[human-in-the-reasoning]], [[llm-assisted-synthesis]], [[structured-literature-reviews]], [[terminological-fragmentation]], [[jingle-fallacy]], [[jangle-fallacy]]
