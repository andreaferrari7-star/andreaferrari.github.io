---
tags: [revisioni-letteratura, generative-ai, triangolazione, saturazione, integrita-scientifica]
tipo_fonte: scientifica
source_papers: ["JML_1001.pdf"]
---

# Triangolazione tra strumenti e all'interno dello stesso strumento (Between- e Within-Tool)

## Definizione Operativa
- Coppia di strategie per ridurre opacità, bias e variabilità degli strumenti di IA generativa nelle revisioni strutturate della letteratura (Tingelhoff et al., 2024):
  - il **confronto tra strumenti** (*between-tool*) esegue lo stesso compito con più strumenti e ne confronta gli output;
  - il **confronto all'interno dello strumento** (*within-tool*) ripete lo stesso prompt sullo stesso strumento.
- **Utilità applicativa:** nelle rassegne assistite da LLM, la convergenza tra strumenti e tra ripetizioni indica quanto un risultato sia stabile, mentre le divergenze segnalano i punti da verificare a mano.

## Evidenze dalla Letteratura
- **Confronto tra strumenti:** serve a mitigare l'opacità e i potenziali bias dei singoli strumenti. Gli autori lo assimilano alla triangolazione dei dati, metodo consolidato per gestire opacità e bias delle fonti (Tingelhoff et al., 2024).
- **Confronto all'interno dello strumento:** serve a gestire i problemi di qualità legati alla natura generativa degli strumenti. Ripetere lo stesso prompt verifica che i dati estratti includano tutte le informazioni rilevanti che lo strumento può produrre. Il criterio è la saturazione della grounded theory: il punto oltre il quale nuove interrogazioni difficilmente aggiungono informazioni rilevanti (Tingelhoff et al., 2024).
- Le due strategie fanno parte della guida in otto passaggi degli autori, che trasferisce all'uso dell'IA generativa nelle revisioni metodi già validati in altri contesti di ricerca (Tingelhoff et al., 2024; vedi [[eight-step-genai-research-workflow]]).

## Riferimenti Bibliografici
- Tingelhoff, F., Brugger, M., & Leimeister, J. M. (2024). A guide for structured literature reviews in business research: The state-of-the-art and how to integrate generative artificial intelligence. *Journal of Information Technology*, 1–23. https://doi.org/10.1177/02683962241304105

## Relazioni
- Vedi anche: [[jml-1001]], [[criteria-centric-genai-integration]], [[eight-step-genai-research-workflow]], [[structured-literature-reviews]]
