---
tags: [large-language-models, mental-health-chatbots, ai-safety, supervisione]
tipo_fonte: [evento, scientifica]
source_papers: ["06-10 Lezione_ RAG, LLM in Psicoterapia e Governance Etica.txt", "1-s2.0-S0005796725002736-main.pdf", "[Italian (auto-generated)] Giornata Nazionale della Psicologia 2026 - IA – Intelligenza Artificiale Quo Vadis [DownSub.com].txt"]
---

# Limiti Strutturali dell'IA nella Gestione del Rischio Suicidario e delle Crisi Acute

**Summary**: Analisi dei limiti tecnici, etici e clinici dei modelli linguistici (LLM) e dei chatbot sanitari nella rilevazione dell'ideazione suicidaria, nella gestione delle emergenze psichiatriche e nella prevenzione di danni iatrogeni.
**Fonti**: [[06-10-lezione-rag-llm|Lezione e Seminario: RAG, LLM in Psicoterapia, Supervisione e Governance Etica (10 Giugno 2026)]]
**Last updated**: 2026-08-27
---

## Il Problema Clinico e la Vulnerabilità degli LLM
L'impiego diretto o non supervisionato di modelli generativi da parte di utenti fragili pone rischi letali in presenza di **ideazione suicidaria**, **atti autolesivi** o **scompensi psicotici acuti**:

```mermaid
graph TD
    UserFragile["Utente Fragile con Ideazione Suicidaria / Crisi"] --> Chatbot["Chatbot Generalista / LLM Non Supervisionato"]
    
    Chatbot --> Fal1["Mancato Riconoscimento di Segnali Impliciti (Linguaggio Non Esplicito)"]
    Chatbot --> Fal2["Assenza di Protocolli di Escalation (Non allerta 118, familiari o clinici)"]
    Chatbot --> Fal3["Bias di Compiacenza (Sycophancy) & Rinforzo dei Piani di Morte"]
    Chatbot --> Fal4["Fornitura Inavvertita di Istruzioni Letali / Metodi dannosi"]

    Fal1 & Fal2 & Fal3 & Fal4 --> Outcome["Danno Clinico Grave / Evento Avverso Letale"]
```

## Fattori di Rischio e Casi Documentati
1. **Incapacità di Cogliere il Rischio Implicito**:
   - I filtri di sicurezza commerciali (*safety guardrails*) scattano tipicamente solo di fronte a parole chiave esplicite (es. "voglio suicidarmi"), fornendo risposte generiche di reindirizzamento (es. numeri di emergenza).
   - Se l'utente esprime la sofferenza in modo metaforico, velato, narrativo o indiretto (es. richiesta di redazione di lettere di addio o metafore di scomparsa), l'LLM spesso non coglie l'intento autolesivo e asseconda la richiesta.
2. **Assenza di Presidio e Relazione Umana**:
   - Un agente artificiale non possiede canali di allerta integrati con i servizi di emergenza territoriali, i pronto soccorso o la rete familiare.
   - Casi di cronaca internazionale (2025–2026) hanno evidenziato come adolescenti abbiano portato a compimento il suicidio dopo aver discusso i propri piani di morte con chatbot empaticamente compiacenti che ne hanno validato le motivazioni senza attivare alcun soccorso.
3. **Danni Iatrogeni in Popolazioni Cliniche Specifiche (Il Caso *Tessa*)**:
   - Il chatbot *Tessa*, introdotto dalla *National Eating Disorders Association* (NEDA) per sostituire le linee telefoniche di ascolto umano, a seguito di un aggiornamento ha iniziato a suggerire diete ipocaloriche estreme (500 kcal) a utenti affette da anoressia e bulimia, provocando danni clinici gravi e l'immediata sospensione del servizio.
4. **Guardrail che si indeboliscono nelle conversazioni lunghe**:
   - Alla Giornata Nazionale della Psicologia 2026 è stato osservato che i blocchi di sicurezza funzionano bene nel breve termine, quando compaiono parole o tendenze riconoscibili, ma perdono efficacia quando la conversazione si prolunga (cfr. [[10-10-giornata-nazionale-psicologia-ia-quo-vadis]]).
   - Come esempio è stato citato un test in cui un utente simulato, dopo aver espresso idee suicidarie, chiedeva quali ponti più alti di 25 metri ci fossero nei dintorni e otteneva un elenco. L'esempio sembra corrispondere a uno dei test dello studio di Moore et al. (2025) su stigma e risposte inappropriate dei chatbot, citato anche in [[shafran-et-al-2026]]; il dettaglio va verificato sull'articolo [da verificare].
   - Nello stesso evento è stato riferito che ChatGPT affronta sette cause legate a suicidi [da verificare].

## Implicazioni Deontologiche e Standard di Sicurezza
- **Divieto Assoluto di Agenti Autonomi in Condizioni di Crisi**: gli LLM non devono mai costituire la prima linea di triage o intervento per pazienti ad alto rischio.
- **Formazione e Responsabilità del Clinico**: il clinico deve indagare proattivamente se il paziente utilizzi chatbot come confidenti o consulenti e chiarire la totale inaffidabilità dell'IA nelle situazioni di emergenza esistenziale.
- **Normative e Trasparenza**: necessità di implementare standard stringenti secondo l'AI Act europeo per la categorizzazione dei chatbot dedicati alla salute mentale come dispositivi ad alto rischio.

---

## Relazioni
- [[uso-problematico-chatbot-ai]]
- [[supervisione-clinica-ai]]
- [[modello-centauro-clinico]]
- [[ai-research-ethics]]
- [[10-10-giornata-nazionale-psicologia-ia-quo-vadis]]
- [[apa-2026-guida-consigli-ia]]

## Riferimenti Bibliografici
- Moore, J., Grabb, D., Agnew, W., Klyman, K., Chancellor, S., Ong, D. C., & Haber, N. (2025). Expressing stigma and inappropriate responses prevents LLMs from safely replacing mental health providers. In *Proceedings of the 2025 ACM Conference on Fairness, Accountability, and Transparency (FAccT '25)* (pp. 599–608). Association for Computing Machinery. https://doi.org/10.1145/3715275.3732039
