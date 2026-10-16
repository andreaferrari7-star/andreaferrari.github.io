---
tags: [prompt-engineering, cbt, pensieri-automatici, system-prompt, pacing-terapeutico]
tipo_fonte: [scientifica, interna]
source_papers: ["Ricerca Prompting LLM Clinico Sanitario.pdf"]
---

# LLM4CBT

## Definizione Operativa
- **LLM4CBT** è un modello di prompting per la terapia cognitivo-comportamentale che separa le istruzioni tra messaggio di sistema e messaggio utente, per guidare l'LLM verso comportamenti terapeutici validati ed evitare soluzioni premature (Kim et al., 2025; cfr. [[ricerca-prompting-llm-clinico-sanitario]]).
- **Utilità CBT:** è pensato per l'elicitazione dei pensieri automatici nei percorsi digitali di matrice CBT. Spinge il modello a privilegiare riflessione e normalizzazione rispetto ai consigli diretti e a regolare il ritmo del colloquio sul coinvolgimento del paziente (Kim et al., 2025).

## Evidenze dalla Letteratura
- **Messaggio di sistema:** definisce la persona del clinico («Act as if you're a professional therapist») e introduce i concetti CBT di base, cioè i pensieri automatici e la tecnica della freccia discendente. Include anche l'istruzione di chiedere una formulazione sintetica quando il paziente esprime pensieri complessi (Kim et al., 2025).
- **Messaggio utente:** contiene i comportamenti preferiti («riflettere lo stato mentale del paziente e normalizzare la situazione invece di offrire una soluzione») e il compito attivo, cioè la trascrizione in ingresso con la direttiva di controllo (Kim et al., 2025).
- **Pacing:** secondo la rassegna interna, il modello monitora il coinvolgimento del paziente e introduce pause ed esitazioni quando l'utente mostra resistenza o difficoltà a collaborare (Kim et al., 2025; cfr. [[ricerca-prompting-llm-clinico-sanitario]]).
- **Limite della base documentale:** il paper originale non è presente in `raw/`. Questa sintesi si basa sulla descrizione della rassegna interna; risultati quantitativi e condizioni sperimentali vanno verificati sul paper `[da verificare]`.

## Riferimenti Bibliografici
- Kim, Y., Choi, C.-H., Cho, S., Sohn, J.-Y., & Kim, B.-H. (2025). Aligning large language models for cognitive behavioral therapy: A proof-of-concept study. *Frontiers in Psychiatry*, *16*, 1583739. https://doi.org/10.3389/fpsyt.2025.1583739

## Relazioni
- Vedi anche: [[ricerca-prompting-llm-clinico-sanitario]], [[coast-framework-clinical-prompting]], [[modello-rocco]], [[clinical-chain-of-thought-paradox]]
