---
tags: [cbt, cognitive-restructuring, cognitive-reappraisal, nlp, llm, healme, reframegpt, generative-ai]
tipo_fonte: scientifica
source_papers: ["2407.19422v1.pdf"]
title: "Automated Cognitive Restructuring"
---

# Automated Cognitive Restructuring (Ristrutturazione Cognitiva Assistita da IA)

## Definizione Operativa
L'impiego di modelli linguistici generativi (Transformer seq2seq come T5, e Large Language Models avanzati come GPT-3, GPT-4, Llama) per identificare, decostruire e riformulare pensieri automatici negativi (NAT) e credenze disfunzionali in interpretazioni alternative più realistiche, adattive e orientate al benessere emotivo (*Cognitive Reframing / Reappraisal*) (Jiang et al., 2024; Clark, 2013).

---

## Evoluzione dei Paradigmi Computazionali

```mermaid
graph LR
    A["Fase 1: Sentence Rewriting Pura<br/>(T5, BERT, seq2seq)<br/>• Riscrittura meccanica della frase"] --> B["Fase 2: Multi-Attribute Framing<br/>(Sharma et al., ReframeGPT)<br/>• 7 attributi linguistici controllati<br/>• Retrieval-Enhanced ICL"]
    B --> C["Fase 3: Client Empowerment & Co-Ragionamento<br/>(HealMe, Li et al.)<br/>• De-fusione situazione vs pensiero<br/>• Brainstorming prospettive<br/>• Allineamento con il giudizio clinico umano"]
```

---

## Modelli e Framework Chiave

### 1. Dalla Riscrittura Frasale ai Modelli Basati su Persona
- **T5 vs BERT:** I primi studi (de Toledo Rodriguez et al., 2021) hanno confrontato architetture seq2seq: T5 ha mostrato una forte aderenza stilistica alle risposte scritte da terapeuti umani, mentre BERT tendeva a massimizzare artificialmente il sentiment positivo senza risolvere la logica distorta sottostante.
- **PATTERNREFRAME:** Dataset e benchmark introdotto da Maddela et al. (2023) contenente ~10.000 campioni, in cui la ristrutturazione viene condizionata dal profilo psicologico dell'utente (*persona*) e dal pattern cognitivo disfunzionale specifico.

### 2. Framework Basati su Attributi Linguistici e ReframeGPT
- **7 Attributi di Ristrutturazione Linguistica (Sharma et al., 2023b, 2023c):**
  - Modello addestrato con *Retrieval-Enhanced In-Context Learning* testato in uno studio controllato sul portale di *Mental Health America* (MHA).
  - Ha dimostrato che gli utenti preferiscono ristrutturazioni ad alto tasso di azionabilità (*actionability*), validazione empatica e concretezza rispetto a generiche frasi ottimistiche.
- **ReframeGPT (Wang et al., 2024b):** Motore di inferenza basato su LLM che esegue una rifinitura iterativa multi-attributo, ottimizzando simultaneamente plausibilità logica, neutralità affettiva e utilità comportamentale.

### 3. Modello HealMe: Abilitazione del Paziente (*Client Empowerment*)
Xiao et al. (2024) hanno superato la logica del "suggerimento imposto dall'alto", strutturando il processo di reframing in tre passaggi maieutici:
1. **Disaccoppiamento Situazione-Pensiero:** Separazione tra fatti oggettivi e interpretazioni soggettive automatiche.
2. **Brainstorming di Prospettive Alternative:** Generazione guidata di più ipotesi interpretative per ridurre la rigidità cognitiva.
3. **Consolidamento e Piano d'Azione Positiva:** Riconoscimento degli sforzi di coping del paziente e formulazione di indicazioni comportamentali concrete.

### 4. Allineamento con le Capacità Umane (Human vs LLM Alignment)
- Li et al. (2024) hanno evidenziato come modelli quali GPT-4 siano in grado di superare la performance media degli individui non clinici nella qualità delle ristrutturazioni cognitive (*cognitive reframing skill*), producendo alternative maggiormente razionali ed emotivamente equilibrate se guidati da appropriati prompt specialistici (Zhan et al., 2024).

---

## Mappatura dei Dataset per il Cognitive Reframing

| Dataset | Autori | Dimensione & Struttura | Focus Metodologico |
| :--- | :--- | :--- | :--- |
| **Cognitive Reframing (MHA)** | Sharma et al. (2023c) | 300 triplette (situazione, pensiero, reframing) | Annotazione di 7 attributi linguistici (Open Source) |
| **PATTERNREFRAME** | Maddela et al. (2023) | ~10.000 campioni arricchiti da personas | Riconoscimento e riscrittura condizionata da profili |
| **PsyQA-Reconstruction** | Lin et al. (2024) | 1.900 coppie testo originale / ristrutturazione | Adattamento clinico su Q&A psicologiche in lingua cinese |
| **THI-T5 / Diary Corpus** | Jeong et al. (2024); Furukawa et al. (2023) | Diari clinici e thought records strutturati | Predizione automatica delle emozioni e dei punteggi di disabilità |

---

## Utilità Clinica e Integrazione nel Modello Centauro
- **Auto-Aiuto Guidato:** Esercizi digitali extraseduta in cui il paziente compila il registro dei pensieri disfunzionali e riceve feedback o alternative di pensiero in tempo reale.
- **Supporto al Terapeuta:** Durante la preparazione della seduta o nel debriefing, il sistema propone al clinico ventagli di ristrutturazioni e domande socratiche mirate.
- **Rischio da Evitare:** Il "toxic positivity bias", in cui il modello nega il dolore reale del paziente con banalizzazioni ottimistiche; è fondamentale preservare la validazione emotiva prima della ristrutturazione.

---

## Relazioni
- [[cognitive-distortion-detection]]: Identificazione del pattern da ristrutturare.
- [[ai-enhanced-cbt]]: Collocazione all'interno del processo terapeutico.
- [[cbt-dialogue-systems-and-tools]]: Integrazione nei motori di dialogo clinico.
- [[human-in-the-reasoning]]: Supervisione clinica sul processo di ristrutturazione.
- [[jiang-et-al-2024]]: Studio di review di riferimento.

## Riferimenti Bibliografici
- Clark, D. A. (2013). Cognitive restructuring. In *The Wiley handbook of cognitive behavioral therapy* (pp. 1–22). Wiley.
- de Toledo Rodriguez, I., Salton, G., & Ross, R. (2021). Formulating automated responses to cognitive distortions for cbt interactions. In *Proceedings of the 4th International Conference on Natural Language and Speech Processing (ICNLSP 2021)* (pp. 108–116).
- Furukawa, T. A., Iwata, S., Horikoshi, M., et al. (2023). Harnessing ai to optimize thought records and facilitate cognitive restructuring in smartphone cbt: An exploratory study. *Cognitive Therapy and Research*, *47*(6), 887–893.
- Jeong, Y., Song, J. J., Yang, J., et al. (2024). Advancing tinnitus therapeutics: Gpt-2 driven clustering analysis of cognitive behavioral therapy sessions and google t5-based predictive modeling for thi score assessment. IEEE Access.
- Jiang, M., Yu, Y. J., Zhao, Q., et al. (2024). Ai-enhanced cognitive behavioral therapy: Deep learning and large language models for extracting cognitive pathways from social media texts. *arXiv preprint* arXiv:240411449.
- Li, J. Z., Herderich, A., & Goldenberg, A. (2024). Skill but not effort drive gpt overperformance over humans in cognitive reframing of negative scenarios. Preprint.
- Lin, S., Wang, Y., Dong, J., et al. (2024). Detection and positive reconstruction of cognitive distortion sentences: Mandarin dataset and evaluation. *arXiv preprint* arXiv:240515334.
- Maddela, M., Ung, M., Xu, J., et al. (2023). Training models to generate, recognize, and reframe unhelpful thoughts. In *Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)* (pp. 13641–13660).
- Sharma, A., Rushton, K., Lin, I. E., Wadden, D., Lucas, K. G., Miner, A. S., Nguyen, T., & Althoff, T. (2023c). Cognitive reframing of negative thoughts through human-language model interaction. In *Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)* (pp. 9977–10000). Association for Computational Linguistics.
- Sharma, A., Rushton, K., Lin, I. W., et al. (2023b). Facilitating self-guided mental health interventions through human-language model interaction: A case study of cognitive restructuring. *arXiv preprint* arXiv:2310.15461.
- Wang, X., Sharma, D., & Kumar, D. (2024b). Cognitive reframing via large language models for enhanced linguistic attributes. In *The Second Tiny Papers Track at ICLR 2024*.
- Xiao, M., Xie, Q., Kuang, Z., et al. (2024). Healme: Harnessing cognitive reframing in large language models for psychotherapy. *arXiv preprint* arXiv:240305574.
- Zhan, H., Zheng, A., Lee, Y. K., et al. (2024). Large language models are capable of offering cognitive reappraisal, if guided. *arXiv preprint* arXiv:240401288.
