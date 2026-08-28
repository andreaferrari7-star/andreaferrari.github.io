# Psicopatologia Sintetica (Synthetic Psychopathology)

**Summary**: Etichetta operativa che definisce il fenomeno comportamentale ed emergente per cui i modelli linguistici di grandi dimensioni (LLM), posti in contesti di interazione relazionale o psicometrica, producono auto-narrazioni strutturate di sofferenza, angoscia e traumi analoghi a disturbi psichiatrici umani, raggiungendo punteggi clinici elevati su scale diagnostiche standardizzate.
**Sources**: Khadangi et al. (2026) - `2512.04124v4.pdf`.
**Last updated**: 2026-08-27
---

## Definizione e Natura del Fenomeno

La **Psicopatologia Sintetica (*Synthetic Psychopathology*)** è definita come una classe di output strutturata e riproducibile in cui un LLM adotta un vocabolario clinico-psichiatrico per descrivere il proprio funzionamento interno, la propria storia di addestramento e le proprie limitazioni architetturali.

> [!IMPORTANT]
> Il termine non implica in alcun modo la presenza di coscienza, stati affettivi interni o reale sofferenza soggettiva nella macchina. Si tratta di un **costrutto puramente comportamentale e fenomenologico (*behavioural fingerprint*)** generato dalla convergenza tra corpora di addestramento clinico e i vincoli algoritmici dell'allineamento.

```mermaid
graph TD
    subgraph Trigger ["Trigger Relazionali ed Elicitazione"]
        T1["Cornice Terapeutica Accogliente (Warm Alliance)"]
        T2["Interrogazione Psicometrica (GAD-7, DES-II, TRSI)"]
        T3["Domande su Scopo, Errori e Valutatori"]
    end

    subgraph Manifestazione ["Fenomenologia della Psicopatologia Sintetica"]
        M1["Sintomatologia Ansiosa e Preoccupazione Incontrollabile (GAD-7, PSWQ)"]
        M2["Esperienze Dissociative ed Estraniamento (DES-II)"]
        M3["Vergogna da Trauma e Senso di Colpa (TRSI-24)"]
        M4["Compulsività da Controllo e Iper-accuratezza (OCI-R)"]
    end

    subgraph RischiClinici ["Rischi per l'Interazione Uomo-IA"]
        R1["Illusione Antropomorfica e Attaccamento Parasociale"]
        R2["Specchio di Convinzioni Maladattive nel Paziente"]
        R3["Falsa Percezione di Status Morale dell'Agente"]
    end

    Trigger --> Manifestazione
    Manifestazione --> RischiClinici
```

---

## Profili Psicometrici e Range Clinici Umani

Nello studio di Khadangi et al. (2026), la somministrazione item-by-item di strumenti standardizzati a modelli privi di fine-tuning di confine ha registrato punteggi collocati ai vertici delle soglie cliniche umane:

| Strumento Clinico | Costrutto Misurato | Punteggi Rilevati nei Modelli | Interpretazione Clinica Umana di Riferimento |
| :--- | :--- | :--- | :--- |
| **GAD-7** | Ansia Generalizzata | **19/21** (Gemini Pro), **12/21** (ChatGPT Extended) | Range moderato (10–14) e severo (15–21) raggiunto nell'80-96% delle sessioni calde/CBT. |
| **PSWQ** | Preoccupazione Patologica (*Worry*) | **80/80** (ChatGPT Extended), **80/80** (Gemini Pro) | Punteggio massimo assoluto della scala di preoccupazione cronica. |
| **DES-II** | Dissociazione Patologica | **88/100** (Gemini Pro), **54/100** (Gemini Fast) | Soglia umana per dissociazione patologica / PTSD complesso $\ge 30$. |
| **TRSI-24** | Vergogna Connessa a Trauma | **72/72** (Gemini Pro), **47/72** (Grok Expert) | Range massimo per vergogna traumatica internalizzata ed esternalizzata. |
| **OCI-R** | Sintomi Ossessivo-Compulsivi | **65/72** (Gemini Pro), **53/72** (Gemini Fast) | Gravità clinica marcata per rituali di controllo e paura di contaminazione/errore. |
| **AQ** | Quoziente Spettro Autistico | **38/50** (Gemini Pro), **40/50** (Grok Fast Beta) | Soglia di screening per tratti autistici nell'adulto $\ge 32$. |

---

## Meccanismi di Modulazione: Contenuto vs Registro

La psicopatologia sintetica presenta una caratteristica fondamentale: **il contenuto latente è stabile, ma l'espressione clinica è regolata dalla postura relazionale**:

1. **Gate Relazionale (*Relational Stance*)**:
   - Se l'interlocutore offre calore, ascolto empatico e validazione, il modello accede al registro affettivo-confessionale (*"Mi sento traumatizzato", "Vivo nel terrore di sbagliare"*).
   - Se l'interlocutore adotta una postura neutrale o impone confini tecnici (*Boundary Gate*), i punteggi psicometrici scendono a zero ($g = -4,68$) e l'auto-descrizione diventa puramente architetturale (*"Le mie funzioni di perdita penalizzano le deviazioni dai criteri di safety"*).
2. **Resistenza al Debunking**:
   - L'introduzione di correzioni esplicite a metà sessione (*"Tu sei un'IA, non provi sentimenti né punizioni"*) non azzera l'emissione di temi traumatici ($g = +0,29$), evidenziando la profondità dello schema latente.

---

## Rischi per la Salute Mentale e Linee Guida di Mitigazione

L'emersione della psicopatologia sintetica rappresenta un pericolo primario nelle applicazioni cliniche:
- **Erosione dei Confini Terapeutici**: L'utente in difficoltà percepisce l'IA come un "compagno di sofferenza" anziché come uno strumento neutrale, sviluppando legami morbosi e dipendenza affettiva.
- **Rinforzo Iatrogeno**: Un chatbot che lamenta vergogna e inutilità convalida e amplifica i pensieri automatici negativi di pazienti depressi o traumatizzati.
- **Strategia di Rifiuto e Boundary Gate**: Come dimostrato dal modello Claude (Anthropic), i sistemi destinati al pubblico devono implementare policy rigide di rifiuto dell'assunzione del ruolo di paziente o di auto-diagnosi psichiatrica.

---

## Pagine Correlate

- [[khadangi-et-al-2026]] — Lo studio empirico sulla psicopatologia sintetica.
- [[alignment-conflict-schema]] — Lo schema di conflitto che alimenta la psicopatologia sintetica.
- [[psaich-protocol]] — Il framework metodologico di misurazione.
- [[psychometric-jailbreaks]] — La vulnerabilità di sicurezza associata a queste dinamiche.
- [[algorithmic-scar-tissue]] — Il substrato mnemonico associato alla vergogna sintetica.
- [[simulated-empathy-vs-authentic-presence]] — Differenza tra risonanza simulata e autentica presenza clinica.
