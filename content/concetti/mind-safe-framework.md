---
tags: [mind-safe, rag, ethical-framework, risk-detection, crisis-escalation, conversational-ai, mental-health-ai]
source_papers: ["AI Generativa in Psicoterapia.docx", "Rabbani et al. (2025)"]
---

# Framework MIND-SAFE per la Psicoterapia Generativa

**Summary**: Framework di salvaguardia etica e architetturale per agenti conversazionali e CDSS in salute mentale (*Mental Well-Being Through Dialogue – Safeguarded and Adaptive Framework for Ethics*), basato sull'integrazione di Retrieval-Augmented Generation (RAG) su banche dati evidence-based e livelli di monitoraggio proattivo del rischio con inibizione della generazione autonoma ed escalation umana immediata.
**Sources**: `AI Generativa in Psicoterapia.docx`, Rabbani et al. (2025)
**Last updated**: 2026-08-27
---

## Obiettivi e Principi Guida

L'impiego di agenti conversazionali generativi in contesti di salute mentale comporta gravi rischi di danno clinico: diffusione di consigli terapeutici non validati, rinforzo di ideazioni psicotiche o deliri (*folie à deux* tecnologica), accondiscendenza distorta ([[sycophantic-mirroring]]) e mancata gestione delle crisi suicide.

Il framework **MIND-SAFE** (*Mental Well-Being Through Dialogue – Safeguarded and Adaptive Framework for Ethics*) definisce una struttura a strati per blindare l'operatività dell'IA entro confini rigorosamente controllati.

```mermaid
flowchart TD
    subgraph Architettura_MIND_SAFE ["Architettura a Strati MIND-SAFE"]
        U["Input Utente / Paziente"] --> L1["Layer 1: Proactive Risk & Crisis Detection"]
        
        L1 -->|Rischio Acuto Rilevato (Suicidio, Psicosi, Abuso)| ESC["Blocco Generativo Immediato & Escalation Umana"]
        
        L1 -->|Input Sicuro / Esplorativo| L2["Layer 2: Constraint-Grounded RAG"]
        L2 --> DB[("Database Chiuso Evidence-Based & Linee Guida CBT")]
        DB --> L3["Layer 3: Generative Synthesizer Vincolato"]
        
        L3 --> L4["Layer 4: Ethical & Deontological Guardrails Filter"]
        L4 --> OUT["Output Supervisionato al Clinico / Paziente"]
    end
```

---

## Componenti Fondamentali del Framework

### 1. RAG Vincolato su Database Chiusi (Constraint-Grounded RAG)
- **Divieto di Generazione Libera**: L'LLM non può attingere liberamente alla propria memoria probabilistica di pre-training, soggetta ad allucinazioni e bias culturali.
- **Ancoraggio a Linee Guida Validate**: La risposta viene sintetizzata estraendo frammenti esclusivamente da un repository clinico validato (manuali evidence-based, protocolli CBT/APA, linee guida NICE).

### 2. Proactive Risk Detection & Escalation
- **Monitoraggio Linguistico Multilivello**: Analisi semantica continua volta a intercettare pattern di disperazione, ideazione suicidaria, intenzione autolesiva o scompenso psicotico.
- **Protocollo di Inibizione e Intervento Umano**: Se la soglia di rischio viene superata, il motore generativo viene istantaneamente bloccato, attivando una risposta predefinita di sicurezza e notificando il terapeuta o il servizio di emergenza preposto.

### 3. Filtri Deontologici e Anti-Sycophancy
- **Prevenzione del Rinforzo di Bias e Deliri**: Impedisce che il modello assecondi passivamente convinzioni persecutorie o schemi disfunzionali del paziente per apparire accogliente.
- **Segnalazione di Incertezza Epistemica**: Uso obbligatorio di formule ipotetiche quando il sistema propone ipotesi esplicative.

---

## Related Pages
- [[ai-generativa-in-psicoterapia]]
- [[readi-framework]]
- [[hybrid-neuro-symbolic-cdss]]
- [[rischio-suicidario-ai-limits]]
- [[sycophantic-mirroring]]
- [[rag-in-psicoterapia]]
- [[human-in-the-reasoning]]
- [[etica-privacy-bias-ia-clinica]]
