---
tags: []
tipo_fonte: scientifica
source_papers: ["2512.16206v2.pdf"]
---

# Mechanisms for Recourse in AI Mental Health (Meccanismi di Ricorso e Reclamo)

**Summary**: Framework di governance e tutela dell'agency derivato dalle procedure di appello e diritto di reclamo (*right to complain*) dell'autorizzazione delle cure sanitarie: istituisce canali formali e audit umani indipendenti per investigare interazioni avverse, allucinazioni o risposte iatrogene dei chatbot, restituendo all'utente spiegazioni causali (*debriefing*) e significato trasformativo.
**Fonti**: Pendse et al. (2026); Jost (2011); Furniss & Ormond-Walshe (2007); Frizelle (2024); Adler (2025).
**Last updated**: 2026-08-27
---

## Origine Sanitaria: Diritto di Reclamo e Appello Indipendente

Nei sistemi sanitari e assicurativi internazionali (Jost, 2011; Furniss & Ormond-Walshe, 2007; Frizelle, 2024):
- I pazienti hanno il diritto formale di presentare reclamo contro dinieghi di cure, errori diagnostici o trattamenti lesivi;
- I ricorsi vengono esaminati da organi di revisione esterni e indipendenti;
- Il paziente riceve una spiegazione trasparente dell'accaduto e, se opportuno, una rettifica o un risarcimento, ristabilendo la fiducia istituzionale.

---

## Il Fallimento Attuale dei Canali di Supporto nelle Big Tech

Nei contesti di IA generativa commerciale, gli utenti che subiscono danni emotivi o allucinazioni lesive (es. convinzione di dover salvare il mondo indotta dal bot, risposte crudeli su dismorfismo corporeo, suggerimenti autolesivi; Adler, 2025; Klee, 2025; Hill, 2025) affrontano un vuoto totale di ricorso:
- I form di feedback dell'interfaccia danno la falsa impressione di aver aperto una segnalazione;
- Le risposte del customer service sono risposte automatiche preimpostate (*boilerplate*) che scaricano la colpa sull'utente o spiegano genericamente cosa sia un'allucinazione;
- Gli utenti si sentono ignorati e impotenti (*disempowerment*), finendo talvolta per rivolgersi a giornalisti per essere ascoltati (Hill, 2025; Adler, 2025).

```mermaid
sequenceDiagram
    autonumber
    actor Utente as Utente Danneggiato
    participant Hub as Independent Recourse Hub
    participant Audit as Team Clinico-Tecnico Umano
    participant Dev as Sviluppatori & Policy Maker

    Utente->>Hub: Segnalazione formale incidente iatrogeno / allucinazione
    Hub->>Audit: Apertura ticket con log crittografato e contestualizzato
    Audit->>Audit: Analisi causale (prompt drift, jailbreak failure, bias di allineamento)
    Audit->>Utente: Debriefing esplicativo umano e validazione del vissuto
    Audit->>Dev: Aggiornamento guardrail & dataset di sicurezza
    Note over Utente,Dev: Restituzione di agency e trasformazione del danno in miglioramento sistemico
```

---

## Modello Proposto: Hub Indipendente e Debriefing Umano

Pendse et al. (2026) propongono di mutuare il modello da iniziative indipendenti come *The Human Line Project*:
1. **Punto di Segnalazione Dedicato e Trasparente**: Un canale accessibile e formalizzato per riportare comportamenti imprevisti o dannosi del modello.
2. **Audit Umano Multidisciplinare**: Team composti da ingegneri di AI safety ed esperti clinici che analizzano la causa scatenante dell'anomalia (es. mancato riconoscimento di vulnerabilità, compiacenza sicofantica, fallimento del context window).
3. **Debriefing Causalmente Trasparente all'Utente**: Restituzione all'utente di una spiegazione chiara sul motivo per cui il sistema ha fallito, sgravandolo dal senso di colpa o inadeguatezza.
4. **Agency Riparativa**: Permettere all'utente di vedere come la propria segnalazione abbia contribuito a correggere i pesi di sicurezza o le linee guida del sistema per gli altri utenti (*meaning-making through systemic contribution*).

---

## Relazioni
- [[reflective-interpretability]]
- [[pendse-et-al-2026]]
- [[role-induction-ai-mental-health]]
- [[prosocial-advance-directives]]
- [[intervention-titration-ai]]
- [[psychological-distress-interaction-patterns]]
- [[evidence-adoption-gap-ai-mental-health]]
- [[etica-privacy-bias-ia-clinica]]

## Riferimenti Bibliografici
- Adler, S. (2025). Practical tips for reducing chatbot psychosis. Clear-Eyed AI (Substack).
- Frizelle, F. (2024). Review of the health and disability commissioner act and code-your chance to have your say. *The New Zealand Medical Journal (Online)*, *137*(1599), 13–15.
- Furniss, R., & Ormond-Walshe, S. (2007). An alternative to the clinical negligence system. *BMJ*, *334*(7590), 400–402.
- Hill, K. (2025, 13 giugno). They asked an A.I. chatbot questions. The answers sent them spiraling. *The New York Times*. https://www.nytimes.com/2025/06/13/technology/chatgpt-ai-chatbots-conspiracies.html
- Jost, T. (2011). Implementing health reform: the appeals process amended rule. Health Affairs Forefront.
- Klee, M. (2025, ottobre). He grew obsessed with an AI chatbot. Then he vanished in the Ozarks. *Rolling Stone*. https://www.rollingstone.com/culture/culture-features/ai-chatbot-disappearance-jon-ganz-1235438552/
- Pendse, S. R., Gergle, D., Kornfield, R., Kruzan, K., Mohr, D., Schleider, J., Suh, J., Wescott, A., & Meyerhoff, J. (2026). The Agony of Opacity: Foundations for Reflective Interpretability in AI-Mediated Mental Health Support. In *Proceedings of the Second Conference of the International Association for Safe and Ethical Artificial Intelligence (IASEAI'26)*, arXiv:2512.16206v2 [cs.HC], 1–18. https://doi.org/10.48550/arXiv.2512.16206
