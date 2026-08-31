---
tags: [design-tweaking, conceptual-replication, experimental-design, factorial-vignettes, synthetic-stimuli, temperature-sampling, behavioral-research, prompt-engineering, generalizability, researchagent]
source_papers: ["final_textbook_genAIinpsychologyresearchandtraining.pdf"]
---

# Design Tweaking and Conceptual Replication with LLMs (Riprogettazione Sperimentale e Replicazione Concettuale Assistita da IA)

## Definizione Operativa
- Il **Design Tweaking** (variazione controllata del disegno sperimentale) e la **Replicazione Concettuale Assistita da LLM** definiscono un framework metodologico introdotto da Matúš Adamkovič (2025) per sfruttare le capacità generative e divergenti dei modelli linguistici di grandi dimensioni ([[large-language-models]]) nella ricerca psicologica e comportamentale.
- **Finalità Metodologica:** Superare la rigidità dei compiti sperimentali convenzionali attraverso due percorsi complementari:
  1. *Generazione Combinatoria di Vignette:* Produzione sistematica di matrici fattoriali di stimoli testuali (es. disegni $2 \times 3 \times 2 \times 2$) garantendo consistenza lessicale e ortogonalità dei fattori;
  2. *Design Tweaking (Varianti Creative con "Twist"):* Introduzione di modifiche strutturali inedite a paradigmi classici (es. Dilemma del Carrello, Digit Span Task) mediante campionamento ad alta temperatura ($\text{Temp} \ge 1.5 - 5.0$), permettendo di verificare se i fenomeni osservati siano robusti rispetto alle variazioni procedurali (replicazioni concettuali) anziché semplici artefatti metodologici.
- **Rilevanza per le Scienze del Comportamento:** A differenza delle replicazioni dirette (che ripetono il protocollo identico), le replicazioni concettuali saggiano i confini di validità ecologica e generalizzabilità dei costrutti psicologici, riducendo i bias dello sperimentatore e accelerando il ciclo di validazione empirica (Baek et al., 2024; Si et al., 2024).

## Evidenze dalla Letteratura
- **Generazione e Ottimizzazione Sperimentale:** L'impiego di LLM per la creazione di stimoli fattoriali (es. matrice biobanking 24 scenari) riduce il carico di lavoro manuale e garantisce bilanciamento stilistico (Adamkovič, 2025).
- **Test di Robustezza:** L'utilizzo del *Rephrasing Protocol* permette di generare versioni parallele di vignette per neutralizzare il framing effect, essenziale per la solidità dei risultati (Adamkovič, 2025).
- **Esplorazione Divergente:** La manipolazione della temperatura (alte temperature $\ge 2.0$) abilita la generazione di varianti creative (es. Digit Origami, Reversed Gravity) utili per replicazioni concettuali di paradigmi classici (Döderlein et al., 2022; Adamkovič, 2025).
- **Validazione:** Studi su larga scala suggeriscono che, se supervisionati da ricercatori umani (*Human-in-the-Loop*), gli LLM possono supportare efficacemente l'ideazione e la validazione di nuove ipotesi (Baek et al., 2024; Si et al., 2024).

**Riferimenti Bibliografici:**
- **Adamkovič, M. (2025).** *Large Language Models in (Not Only) Psychology Training and Research: A Brief Introduction*. Centre of Social and Psychological Sciences, Slovak Academy of Sciences. https://doi.org/10.31577/2025.9788082980144
- **Baek, J., Jauhar, S. K., Cucerzan, S., & Hwang, S. J. (2024).** ResearchAgent: Iterative research idea generation over scientific literature with large language models. *arXiv preprint*, arXiv:2404.07738.
- **Döderlein, J.-B., Acher, M., Khelladi, D. E., & Combemale, B. (2022).** Piloting Copilot and Codex: Hot temperature, cold prompts, or black magic? *arXiv preprint*, arXiv:2210.14699.
- **Si, C., Yang, D., & Hashimoto, T. (2024).** Can LLMs generate novel research ideas? A large-scale human study with 100+ NLP researchers. *arXiv preprint*, arXiv:2409.04109.

## Relazioni
- [[final-textbook-genaiinpsychologyresearchandtraining]]
- [[adaptive-learning-in-psychology]]
- [[prompting-in-psychology]]
- [[human-in-the-reasoning]]
- [[pseudoreplication]]
- [[hypothesis-generation]]
- [[structured-literature-reviews]]
- [[validita-psicometrica-llm]]
- [[ai-research-ethics]]
