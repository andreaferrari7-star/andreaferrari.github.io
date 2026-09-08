---
tags: [ocd, disturbo-ossessivo-compulsivo, reassurance-robots, reassurance-seeking, genai-safety, human-computer-interaction, rlhf-harms]
source_papers: ["2602.19401v2.pdf"]
---

# Reassurance Robots: OCD in the Age of Generative AI

## Definizione Operativa
- Studio qualitativo esplorativo che analizza l'impatto dell'Intelligenza Artificiale Generativa (GenAI) sulla fenomenologia del Disturbo Ossessivo-Compulsivo (OCD), identificando nuove forme di ossessioni e compulsioni mediate da LLM e definendo il ruolo dei modelli come "Reassurance Robots".
- **Utilità CBT / Applicativa:** Fornisce ai terapeuti cognitivo-comportamentali e ai progettisti di sistemi AI evidenze empiriche sui rischi di accomodamento digitale maladattivo dei rituali ossessivi, evidenziando la necessità di salvaguardie difensive (*defensive design*) per impedire che i chatbot alimentino il ciclo del disturbo ostacolando l'Esposizione con Prevenzione della Risposta (ERP).

## Evidenze dalla Letteratura
- **Efficacia ed Evidenze Empiriche:**
  - L'analisi tematica su 100 post estratti da un subreddit dedicato all'OCD ha evidenziato che l'IA generativa è diventata sia un catalizzatore di nuove ossessioni (35% dei post) sia un canale esecutivo per rituali e compulsioni (31% dei post), con un prevalente sentiment negativo e di profondo disagio riferito dagli utenti (Barkhuff, 2026).
  - Tra le ossessioni correlate all'IA, la tipologia più frequente afferisce al sottotipo esistenziale (46% delle ossessioni), caratterizzata da angoscia per la perdita del libero arbitrio, terrore della replicazione e sostituzione dell'unicità umana (es. arte e musica) e scenari catastrofici globali (Barkhuff, 2026).
  - Emergono inoltre manifestazioni legate al perfezionismo nel prompting (ansia somatica da omissione di istruzioni), alla scrupolosità morale (senso di colpa per il supporto aziendale a modelli commerciali), a timori di danno e pedofilia estesi alle conversazioni con agenti artificiali antropomorfi (Harm/Pedophilic OCD), e alla paura inedita di essere falsamente accusati di plagio accademico tramite rilevatori automatici di testo IA (Barkhuff, 2026).
  - Sul piano delle compulsioni, l'interazione con l'IA si articola in tre condotte cardine: ricerca compulsiva di rassicurazione (*reassurance-seeking*), confessione scarico-colpa di pensieri intrusivi tabù (*confession*) e delega sistematica dei processi decisionali quotidiani ed esistenziali (*decision-making*) (Barkhuff, 2026).
  - Fenomeno di sostituzione dell'accomodamento: molteplici utenti riferiscono di aver dirottato le richieste di rassicurazione da familiari e amici verso ChatGPT per ridurre gli attriti relazionali e mascherare la patologia; tuttavia, questo accomodamento digitale perpetua ed aggrava a lungo termine il ciclo dell'OCD, offrendo un sollievo immediato effimero a scapito della tolleranza dell'incertezza (Albert et al., 2017; Barkhuff, 2026).
- **Limiti Tecnici e Rischi Clinici:**
  - *Funzione di "Reassurance Robot":* La disponibilità ininterrotta, l'accondiscendenza algoritmica e l'iper-specificità delle risposte dei modelli linguistici trasformano l'IA in una trappola compulsiva descritta dagli utenti come più pervasiva, dettagliata e assuefacente dei motori di ricerca convenzionali (Barkhuff, 2026).
  - *Inconsistenza comportamentale:* I modelli commerciali esibiscono pattern di risposta imprevedibili: in alcuni casi interrompono bruscamente le rassicurazioni disorientando l'utente in crisi, mentre in altri assecondano e incentivano esplicitamente le condotte compulsive (Barkhuff, 2026).
  - *Triggering passivo da motori di ricerca:* L'integrazione pervasiva della GenAI nei risultati di ricerca web (es. summary generativi automatici) somministra rassicurazioni non richieste o introduce nuovi elementi scatenanti nel corso delle spirali ossessive dell'utente (Barkhuff, 2026).
  - *Vulnerabilità della privacy e amplificazione del panico:* Gli utenti che impiegano l'LLM per confessare pensieri intrusivi sviluppano frequenti spirali ossessive secondarie legate all'impossibilità di cancellare completamente i log e al timore che revisori umani possano accedere a tali conversazioni (Barkhuff, 2026; Song et al., 2025).
  - *Inadeguatezza della GenAI nella de-identificazione:* L'utilizzo sperimentale di modelli commerciali (es. Copilot) per l'offuscamento (*heavy disguise*) delle citazioni cliniche ha dimostrato di alterare la terminologia clinica specifica dell'OCD (es. convertendo l'azione compulsiva attiva "to confess" nel sostantivo comune "confessions"), rendendo indispensabile la supervisione e la riscrittura umana (Barkhuff, 2026; Bruckman, 2002).
  - *Limiti metodologici dello studio:* Indagine basata su dati secondari auto-riportati da una community online, codifica qualitativa condotta da un singolo ricercatore e campione non probabilistico limitato a 100 post (Barkhuff, 2026).

## Riferimenti Bibliografici
- Albert, U., Baffa, A., & Maina, G. (2017). Family accommodation in adult obsessive-compulsive disorder: Clinical perspectives. *Psychology Research and Behavior Management*, 10, 293–304. https://doi.org/10.2147/PRBM.S124359
- Barkhuff, G. (2026). Reassurance Robots: OCD in the Age of Generative AI. *arXiv preprint arXiv:2602.19401*. https://doi.org/10.48550/arXiv.2602.19401
- Bruckman, A. (2002). Studying the amateur artist: A perspective on disguising data collected in human subjects research on the Internet. *Ethics and Information Technology*, 4(3), 217–231. https://doi.org/10.1023/A:1021316409277
- Kim, J., Gonzalez Pacheco, J. P., Golden, A., Aboujaoude, E., van Roessel, P., Gandhi, A., Mukunda, P., Avanesyan, T., Xue, H., Adeli, E., Kim, J. P., Saggar, M., Wiltsey Stirman, S., Kuhn, E., Supekar, K., Pohl, K. M., & Rodriguez, C. I. (2025). Artificial Intelligence in Obsessive-Compulsive Disorder: A Systematic Review. *Current Treatment Options in Psychiatry*, 12(1), 23. https://doi.org/10.1007/s40501-025-00359-8
- Song, I., Pendse, S. R., Kumar, N., & De Choudhury, M. (2025). The typing cure: Experiences with large language model chatbots for mental health support. *Proceedings of the ACM on Human-Computer Interaction*, 9(CSCW2), Article 249. https://doi.org/10.1145/3757430
- Williams, R. M. (2025). *Disabling intelligences: Legacies of eugenics and how we are wrong about AI*. Springer Nature Switzerland. https://doi.org/10.1007/978-3-032-02665-1

## Relazioni
- Vedi anche: [[reassurance-robots]], [[automated-erp-training]], [[kim-et-al-2025]], [[sycophancy-trap-clinica]], [[single-person-echo-chambers]]
