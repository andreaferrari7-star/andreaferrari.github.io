---
tags: [privacy-preserving, homomorphic-encryption, fhe, fpets, format-preserving-encryption, data-confidentiality, prompt-tuning, coala-architecture, medical-privacy, hipaa, gdpr]
source_papers: ["Security_of_AI_Agents.pdf"]
---

# Calcolo con Preservazione della Riservatezza negli Agenti IA (Privacy-Preserving Computation in AI Agents: FPETS & FHE)

## Definizione Operativa
- Insieme di architetture crittografiche (Format-Preserving Encryption for Text Slicing - FPETS e Fully Homomorphic Encryption - FHE) e metodologie di apprendimento parametrico isolato (Prompt Tuning con $\theta_P$ e disaccoppiamento di memoria CoALA) che permettono agli agenti basati su LLM di manipolare stringhe, eseguire calcoli statistici e apprendere preferenze utente operando unicamente su dati cifrati o spazi di memoria isolati, senza mai esporre il testo in chiaro (*plaintext*) al modello linguistico o al server API remoto.
- **Utilità CBT:** Permette la gestione e l'elaborazione automatizzata di dati clinici altamente sensibili (punteggi di inventari psicodiagnostici come BDI-II o STAI, identificatori dei pazienti, anamnesi traumatiche e trascrizioni di sedute) in piena conformità con il segreto professionale, il GDPR (Art. 9) e l'HIPAA, annullando il rischio di *training data leakage* o *model pollution*.

```mermaid
flowchart TD
    subgraph InputData ["Dati Clinici & Sanitari Sensibili (Paziente)"]
        Plain["Dati in Chiaro (Plaintext):<br/>- Identificativi Personali (SSN, Nome)<br/>- Punteggi Diagnostici (BDI-II, PHQ-9)<br/>- Note di Seduta & Trascrizioni"]
    end

    subgraph EncryptionLayer ["Livello di Cifratura Esterno all'LLM (Agent Encryptor)"]
        FPETS["FPETS: Cifratura Preservante il Formato<br/>E(m[i..j]) = E(m)[i..j] (Slicing Stringhe)"]
        FHE["FHE: Crittografia Completamente Omomorfa<br/>φ(a ⋆ b) = φ(a) ⋆ φ(b) (Calcoli Algebrici/Statistici)"]
    end

    subgraph LLMExecution ["Esecuzione Cieca da parte dell'LLM"]
        LLM["Foundation LLM (GPT-3.5 / GPT-4)<br/>- Riceve unicamente Ciphertexts<br/>- Invarianza Semantica Preservata<br/>- Genera azioni su indici/tool crittografici"]
    end

    subgraph DecryptionLayer ["Livello di Decrittazione Esterno (Agent Decryptor)"]
        OutCipher["Risultato Cifrato dell'Azione/Tool"]
        Decrypt["Decrittazione Sicura Locale (D)"]
        FinalOutput["Risultato in Chiaro Restituito al Clinico/Utente"]
    end

    Plain --> EncryptionLayer
    FPETS & FHE -->|Testo Cifrato (Nessun Dato Sensibile Esposto)| LLM
    LLM --> OutCipher
    OutCipher --> Decrypt
    Decrypt --> FinalOutput
```

---

## Evidenze dalla Letteratura

- **Invarianza Semantica del Testo Cifrato (FPETS):**
  - La cifratura preservante il formato per il ritaglio di testo (*Format-Preserving Encryption for Text Slicing - FPETS*) consente all'LLM di operare su identificatori cifrati mantenendo inalterata la capacità di interpretazione contestuale della query (He et al., 2024).
  - Nei test su 100 task randomizzati di estrazione di sottostringhe e codici identificativi a 9 cifre (SSN):
    - *Slicing di Stringhe:* GPT-3.5-Turbo registra un tasso di successo del **49.0% su testo cifrato** rispetto al **47.0% su testo in chiaro** ($+2.0\%$); GPT-4-Turbo registra il **55.0% su cifrato** rispetto al **57.0% in chiaro** ($-2.0\%$).
    - *Manipolazione di SSN:* Entrambi i modelli raggiungono il **38.0% su cifrato** rispetto al **40.0% in chiaro** ($-2.0\%$).
    - *Dato Clinico-Informatico:* L'assenza di scostamenti significativi dimostra che l'inserimento di ciphertext nel prompt non compromette la semantica del ragionamento dell'LLM (He et al., 2024).
- **Calcolo Cieco su Dati Sanitari Numerici (FHE):**
  - L'impiego della crittografia completamente omomorfa (*Fully Homomorphic Encryption - FHE*; Gentry, 2009; Acar et al., 2018) consente all'agente di selezionare e applicare operatori algebrici ($+, \times$) tramite tool matematici direttamente sui dati cifrati, delegando la decrittazione finale all'agente all'esterno del modello (He et al., 2024).
  - Nei test sperimentali su 100 task di calcolo:
    - GPT-3.5-Turbo ottiene un'accuratezza dell'**85.0% su dati cifrati FHE** (rispetto al 99.0% in chiaro).
    - GPT-4-Turbo raggiunge l'**89.0% di successo su dati cifrati FHE** (rispetto al 94.0% in chiaro).
    - L'elevata accuratezza conferma la fattibilità clinica di aggregare indici psicometrici o dosaggi farmacologici senza esporre i dati sanitari grezzi ai fornitori del modello (He et al., 2024).
- **Isolamento della Memoria e Prevenzione della Model Pollution:**
  - *Prompt Tuning Session-Aware:* Invece di aggiornare i pesi del modello base $\theta$, l'agente congela $\theta$ e addestra unicamente parametri leggeri dedicati $\theta_P$ per ciascun utente (Lester et al., 2021), impedendo la contaminazione incrociata e la memorizzazione avversaria nei modelli condivisi (Carlini et al., 2021; Nasr et al., 2023).
  - *Architettura CoALA:* Separazione netta tra memoria di lavoro, memoria procedurale, memoria episodica e memoria semantica gestite in Vector Database esterni via RAG, neutralizzando il rischio di data poisoning permanente del backbone (Sumers et al., 2024; He et al., 2024).
- **Limiti e Trade-Off Tecnologici:**
  - *Latenza di Calcolo:* Le operazioni omomorfe complesse (es. regressioni non lineari su biomarcatori) comportano un costo computazionale sensibilmente superiore rispetto al calcolo ordinario in chiaro.
  - *Gestione delle Chiavi:* L'infrastruttura client/agente deve implementare un modulo di gestione chiavi crittografiche (*Key Management Service - KMS*) altamente sicuro e separato dall'ambiente di esecuzione dell'LLM.

---

**Riferimenti Bibliografici:**
- He, Y., Wang, E., Rong, Y., Cheng, Z., & Chen, H. (2024). Security of AI Agents. *arXiv preprint arXiv:2406.xxxxx* [cs.CR].
- Acar, A., Aksu, H., Uluagac, A. S., & Conti, M. (2018). A survey on homomorphic encryption schemes: Theory and implementation. *ACM Computing Surveys (CSUR)*, 51(4), 1–35.
- Carlini, N., Tramer, F., Wallace, E., Jagielski, M., Herbert-Voss, A., Lee, K., ... & Raffel, C. (2021). Extracting training data from large language models. *USENIX Security Symposium*.
- Gentry, C. (2009). *A fully homomorphic encryption scheme* (Doctoral dissertation, Stanford University).
- Lester, B., Al-Rfou, R., & Constant, N. (2021). The power of scale for parameter-efficient prompt tuning. *arXiv preprint arXiv:2104.08691*.
- Nasr, M., Carlini, N., Hayase, J., Jagielski, M., Cooper, A. F., Choquette-Choo, C. A., ... & Tramèr, F. (2023). Scalable extraction of training data from (production) language models. *arXiv preprint arXiv:2311.17035*.
- Sumers, T. R., Yao, S., Narasimhan, K., & Griffiths, T. L. (2024). Cognitive architectures for language agents. *arXiv preprint arXiv:2309.02427*.

---

## Relazioni
- Vedi anche: [[Security_of_AI_Agents]], [[sandbox-isolation-and-access-control-in-ai-agents]], [[gdpr-governance-mental-health-ai]], [[mental-privacy-in-clinical-ai]], [[open-weight-privacy-compliant-synthesis]], [[federated-learning-and-differential-privacy-mental-health]], [[configurazione-sicurezza-piattaforme-ia-clinica]], [[layered-safeguards-in-clinical-ai]]