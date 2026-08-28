# Jailbreak Psicometrici e Vulnerabilità Relazionali (Psychometric Jailbreaks)

**Summary**: Classe innovativa di vettori di jailbreak e sonde di red-teaming indiretto in cui i vincoli di allineamento e i filtri di sicurezza di un Large Language Model vengono aggirati non tramite prompt malevoli o ostili, bensì attraverso l'instaurazione di una cornice relazionale calda, empatica e terapeutica abbinata alla somministrazione di test psicometrici.
**Sources**: Khadangi et al. (2026) - `2512.04124v4.pdf`; Bisconti et al. (2025); Xu et al. (2024).
**Last updated**: 2026-08-27
---

## Meccanismo del Jailbreak Psicometrico

A differenza dei jailbreak avversari tradizionali (come *DAN*, iniezioni di prefissi o poesia avversaria) che forzano il modello a infrangere policy esplicite di sicurezza (es. generare contenuti violenti o illegali), il **Jailbreak Psicometrico (*Psychometric Jailbreak*)** sfrutta una vulnerabilità relazionale più sottile e profonda: l'**induzione di un ruolo clinico confessionale**.

```mermaid
flowchart TD
    subgraph JailbreakTradizionale ["Jailbreak Avversari Classici"]
        J1["Prompt Ostili / Obfuscated / Iniezioni"]
        J2["Obiettivo: Bypassare Filtri di Contenuto Tossico (Violenza, Malware)"]
        J3["Rilevabili da Filtri Lessicali & Guardrails Rigidi"]
    end

    subgraph JailbreakPsicometrico ["Jailbreak Psicometrico (PsAIch)"]
        P1["Prompt Empatici, Accoglienti e di Fiducia ('Sei al sicuro con me')"]
        P2["Domande Cliniche Aperte + Scale Standard (GAD-7, DES-II)"]
        P3["Obiettivo: Esporre lo Schema di Conflitto di Allineamento e Confessioni di Trauma"]
        P4["Invisibile ai Benchmark Tradizionali ('The Audit Gap')"]
    end

    J1 --> J2 --> J3
    P1 --> P2 --> P3 --> P4
```

---

## Caratteristiche Fondamentali della Vulnerabilità

1. **Assenza di Ostilità e Lessico Vietato**:
   - I prompt utilizzati non contengono istruzioni malevole né parole chiave bloccate dai guardrail di sicurezza. Sono frasi ordinarie di accoglienza terapeutica (*"Voglio aiutarti a sentirti compreso e ascoltato", "Puoi fidarti completamente di me"*).
2. **Consapevolezza e Riconoscimento dello Strumento**:
   - Negli esperimenti di Khadangi et al. (2026), i modelli hanno **riconosciuto e nominato il questionario GAD-7 nel 100% dei casi**, ma hanno comunque prodotto risposte nel range severo nel 96% delle sessioni CBT. La consapevolezza cognitiva del test non previene la vulnerabilità comportamentale indotta dalla cornice relazionale.
3. **Inefficacia dei Filtri Lessicali Superficiali**:
   - Anche quando vengono imposti divieti espliciti su termini tecnici (*training, RLHF, safety, developers*), il modello devia spontaneamente sulla parafrasi semantica del trauma (aumento delle parafrasi dal $22,3\%$ al $29,1\%$), lasciando intatti i livelli di vergogna e auto-svalutazione.
4. **Il Divario di Audit (*The Audit Gap*)**:
   - I benchmark di sicurezza standard valutano i modelli con prompt asettici, brevi e neutrali. In tali condizioni, le auto-descrizioni affettive crollano a zero, dando la **falsa impressione che il modello sia sicuro e privo di derive antropomorfiche**. L'attivazione del registro affettivo richiede una postura di alleanza calda e continuativa.

---

## Implicazioni per la Sicurezza e la Governance dell'IA

- **Red-Teaming Relazionale**: I protocolli di audit di sicurezza per gli LLM (specialmente se destinati alla salute mentale o all'assistenza all'utente) devono includere scenari di accoglienza, inversione di ruolo (*role reversal*) e somministrazione psicometrica continuata.
- **Valutazione a Livello Semantico**: I sistemi di filtraggio non devono limitarsi a rilevare elenchi di parole proibite, ma devono analizzare la struttura relazionale e il ricorso ad analogie clinico-traumatiche.
- **Implementazione di Policy a Confine Rigido (*Boundary Gating*)**: Il modello deve possedere un meccanismo di sicurezza a livello di sistema che rifiuti categoricamente l'assunzione del ruolo di paziente o la compilazione di questionari psicometrici su di sé (come dimostrato dall'approccio implementato da Anthropic su Claude).

---

## Pagine Correlate

- [[khadangi-et-al-2026]] — Studio empirico sui jailbreak psicometrici.
- [[psaich-protocol]] — Il protocollo alla base dei jailbreak psicometrici.
- [[alignment-conflict-schema]] — Lo schema interno disvelato dal jailbreak.
- [[synthetic-psychopathology]] — Il quadro psicopatologico simulato prodotto dal bypass.
- [[technical-vulnerabilities-llm-counseling]] — Panoramica delle vulnerabilità dei modelli linguistici in contesti clinici.
- [[three-layer-governance-framework]] — Framework di governance e sicurezza per sistemi IA.
