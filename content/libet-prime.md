# Libet Prime

**Summary**: Tutor clinico-didattico basato su LLM (Gemini Gem) specializzato sul modello LIBET (Life Themes and Plans in CBT), progettato per guidare gli allievi di psicoterapia nell'apprendimento teorico e nel ragionamento clinico attraverso un'architettura bimodale e maieutica.
**Sources**: 07-10 Riunione_ Test e Valutazione di “Libet Prime” (Tutor AI per Libet_CBT), Trainer Simulator e Piano Operativo.txt, 05-08 Riunione_ Sviluppo Knowledge Base AI, Etica e Applicazioni Cliniche.txt
**Last updated**: 2026-08-27
---

## Definizione e Finalità Didattiche

**Libet Prime** è un agente conversazionale specializzato (*Gem* su piattaforma Google Workspace / Gemini) sviluppato per la rete di scuole di psicoterapia cognitivo-comportamentale di SC Formazione (*Studi Cognitivi*).

L'obiettivo primario del sistema non è fornire un mero motore di risposte automatiche o un surrogato di ChatGPT, bensì operare come **tutor didattico-clinico** per allenare le competenze di concettualizzazione e ragionamento dell'allievo, con particolare riferimento ai primi due anni di specializzazione.

### Cosa fa
- Chiarisce e discrimina i costrutti del modello LIBET (*Life Themes and Plans in CBT*) e delle psicoterapie cognitivo-comportamentali.
- Aiuta a distinguere costrutti teoricamente o lessicalmente vicini provenienti da nomenclature e modelli differenti.
- Guida lo studente nell'analisi di vignette cliniche, nella formulazione del caso e nella definizione di un razionale d'intervento prudente e ipotetico.
- Interroga attivamente l'allievo attraverso quesiti maieutici per verificarne la comprensione profonda.

### Cosa NON è (Guardrails di Perimetro)
- **Non è un terapeuta**: Non interagisce con pazienti reali né eroga trattamenti.
- **Non è un supervisore clinico**: Non valida decisioni su casi clinici reali né sostituisce la supervisione umana.
- **Non è uno strumento diagnostico**: Rifiuta categoricamente di emettere diagnosi definitive o etichette nosografiche da informazioni parziali.
- **Non è un oracolo generico**: Rigetta richieste estranee al dominio teorico-clinico di riferimento (*out-of-domain rejection*).

---

## Architettura di Sistema e Routing a 5 Modalità

Libet Prime è strutturato su un macro-prompt che governa un motore di **routing dinamico** tra 5 modalità funzionali:

```mermaid
graph TD
    User([Input Utente / Allievo]) --> Router{Routing Engine}
    Router -->|Quesito Teorico| M1[1. Spiegazione Teorica]
    Router -->|Distinzione Costrutti| M2[2. Confronto e Discriminazione]
    Router -->|Vignetta Clinica / Log| M3[3. Ragionamento su Formulazione]
    Router -->|Pianificazione Strategica| M4[4. Razionale e Ipotesi Intervento]
    Router -->|Richiesta Esercitazione| M5[5. Interrogazione Maieutica]
    M1 --> Output([Risposta Diretta e Rigorosa])
    M2 --> Output
    M3 --> Dialogue([Dialogo Socratico & Domande Guida])
    M4 --> Dialogue
    M5 --> Dialogue
```

1. **Spiegazione Teorica**: Esposizione rigorosa dei concetti fondanti del modello (es. tema di vita, piani di protezione/prevenzione, credenze di base, metacontrollo).
2. **Confronto e Distinzione di Costrutti**: Analisi differenziale tra concetti analoghi (es. credenza patogena vs credenza di base; piani di sicurezza vs comportamenti di sicurezza).
3. **Ragionamento sulla Formulazione del Caso**: Analisi strutturata di dati clinici e vignette, guidando l'allievo nell'identificazione del legame tra attivatori, credenze nucleari e piani.
4. **Razionale e Ipotesi di Intervento**: Supporto nell'elaborazione del razionale logico alla base della scelta delle tecniche (es. prioritizzazione tra sintomo acuto e ristrutturazione dei piani).
5. **Interrogazione e Stimolo Riflessivo**: Modalità maieutica in cui l'agente pone quesiti all'allievo, fornendo feedback graduali e rilanci metacognitivi.

---

## Postura Bimodale: Rigore Teorico vs Dialogo Socratico

Una caratteristica distintiva del design di Libet Prime è il **comportamento bimodale**:
- **Ambito Teorico**: Risposte scolastiche dirette, esaustive, con definizioni puntuali, esempi clinici standard ed errori tipici di comprensione.
- **Ambito Clinico**: Postura dialogica e maieutica (*[[human-in-the-reasoning]]*). L'agente non "risolve" il caso per l'allievo ma pone domande di rilancio ("*Quali elementi della vignetta ti portano a considerare questo piano come obbligato anziché opzionale?*"), forzando il ragionamento clinico ed evitando la delega acritica.

---

## Knowledge Base e Controllo delle Regressioni

- **Knowledge Base Dedicata**: L'agente è alimentato da un corpus proprietario di **33 capitoli e oltre 230 pagine**, redatto dagli autori del modello e ottimizzato per il retrieval da parte dei modelli linguistici.
- **Prevenzione delle Regressioni (*Prompt Over-Constraining*)**: Durante il passaggio dalle versioni 1.0/1.1 alla 1.2, l'accumulo di istruzioni vincolanti aveva mostrato rischi di appiattimento qualitativo. Il versioning viene validato tramite script di test standardizzati per garantire che le modifiche al prompt non degradino le capacità di ragionamento.

---

## Related pages
- [[07-10_Riunione_Test_Libet_Prime]]
- [[trainer-simulator]]
- [[human-in-the-reasoning]]
- [[simulazione-pazienti-ai]]
- [[clinical-ai-simulation]]
- [[05-08_Riunione_Knowledge_Base]]
- [[ai-assisted-psychotherapy]]
