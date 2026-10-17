---
tags: [framework, reporting-guideline, diagnostic-accuracy, ai-clinical-trials]
tipo_fonte: scientifica
source_papers: ["TRIPOD+AI2024.pdf", "REFINE_2026.pdf", "GAMER2025.pdf"]
---

# STARD-AI

## Definizione Operativa
- Lo **STARD-AI** (*Standards for Reporting of Diagnostic Accuracy - Artificial Intelligence*) è l'estensione della linea guida STARD 2015 per gli studi che valutano l'accuratezza diagnostica di un test basato sull'intelligenza artificiale (Collins et al., 2024; Sounderajah et al., 2025).
- **Utilità CBT / Applicativa:** È fondamentale per i ricercatori e i revisori per valutare criticamente la validità, il rischio di bias e l'applicabilità clinica dei tool diagnostici AI (inclusi i modelli per la salute mentale computazionale), obbligando alla trasparenza metodologica sulla provenienza dei dati e sulle modalità di interazione dell'algoritmo con i clinici.

## Evidenze dalla Letteratura
- **Sviluppo:** lo Steering Group è stato annunciato nel 2020 (Sounderajah et al., 2020) e il protocollo pubblicato nel 2021 (Sounderajah et al., 2021). Nel 2024 TRIPOD+AI elencava STARD-AI come linea guida "in preparazione" (Collins et al., 2024); la versione definitiva è uscita nel 2025 su *Nature Medicine* (Sounderajah et al., 2025).
- **Struttura:** la versione AI parte dai 30 item di STARD 2015 (Bossuyt et al., 2015) e ne aggiunge o modifica 18 [da verificare: il numero non compare nelle fonti in `raw/`; la citazione precedente rimandava a QUADAS-AI, che è un altro strumento].
- Tra gli elementi introdotti dall'estensione vi sarebbero la trasparenza sulla provenienza dei dati di addestramento (*data provenance*), la descrizione dell'interazione Human-AI nel workflow clinico, la gestione del bias algoritmico e la generalizzabilità del modello [da verificare].
- **Differenza da TRIPOD+AI:** TRIPOD+AI riguarda gli studi che sviluppano o valutano un modello di *previsione*; STARD-AI riguarda la misura dell'accuratezza diagnostica (sensibilità, specificità, VPP, VPN) di un *test indice* rispetto a un test di riferimento (Collins et al., 2024).
- **Limiti per l'IA generativa:** STARD-AI e le linee guida coeve sono state sviluppate prima della diffusione degli LLM e coprono poco aspetti come la stocasticità degli output (Mese et al., 2026); trattano l'uso dell'IA generativa solo in casi specifici (Luo et al., 2025).

## Riferimenti Bibliografici
- Bossuyt, P. M., Reitsma, J. B., Bruns, D. E., Gatsonis, C. A., Glasziou, P. P., Irwig, L., et al. (2015). STARD 2015: An updated list of essential items for reporting diagnostic accuracy studies. *BMJ*, *351*, h5527. https://doi.org/10.1136/bmj.h5527
- Collins, G. S., Moons, K. G. M., Dhiman, P., Riley, R. D., Beam, A. L., Van Calster, B., Ghassemi, M., Liu, X., Reitsma, J. B., van Smeden, M., Boulesteix, A.-L., Camaradou, J. C., Celi, L. A., Denaxas, S., Denniston, A. K., Glocker, B., Golub, R. M., Harvey, H., Heinze, G., . . . Logullo, P. (2024). TRIPOD+AI statement: Updated guidance for reporting clinical prediction models that use regression or machine learning methods. *BMJ*, *385*, Article e078378. https://doi.org/10.1136/bmj-2023-078378
- Luo, X., Tham, Y. C., Giuffrè, M., Ranisch, R., Daher, M., Lam, K., Eriksen, A. V., Hsu, C. W., Ozaki, A., de Moraes, F. Y., Khanna, S., Su, K. P., Begagić, E., Bian, Z., Chen, Y., Estill, J., & The GAMER Working Group. (2025). Reporting guideline for the use of Generative Artificial intelligence tools in MEdical Research: The GAMER Statement. *BMJ Evidence-Based Medicine*, *30*(6), 390–400. https://doi.org/10.1136/bmjebm-2025-113825
- Mese, I., Akinci D’Antonoli, T., Bluethgen, C., Bressem, K., Cuocolo, R., Chaudhari, A., Tejani, A. S., Isaac, A., Ponsiglione, A., Meddeb, A., Khosravi, B., Le Guellec, B., Kahn, C. E., Jr., Suh, C. H., Pinto dos Santos, D., Koh, D.-M., Tzanis, E., Kotter, E., Colak, E., . . . Kocak, B. (2026). Reporting checklist for foundation and large language models in medical research (REFINE): An international consensus guideline. *Diagnostic and Interventional Radiology*. Advance online publication. https://doi.org/10.4274/dir.2026.263812
- Sounderajah, V., Ashrafian, H., Aggarwal, R., et al. (2020). Developing specific reporting guidelines for diagnostic accuracy studies assessing AI interventions: The STARD-AI Steering Group. *Nature Medicine*, *26*(6), 807–808. https://doi.org/10.1038/s41591-020-0941-1
- Sounderajah, V., Ashrafian, H., Golub, R. M., et al. (2021). Developing a reporting guideline for artificial intelligence-centred diagnostic test accuracy studies: The STARD-AI protocol. *BMJ Open*, *11*, e047709. https://doi.org/10.1136/bmjopen-2020-047709
- Sounderajah, V., Guni, A., Liu, X., et al. (2025). The STARD-AI reporting guideline for diagnostic accuracy studies using artificial intelligence. *Nature Medicine*, *31*(10), 3283–3289.

## Relazioni
- Vedi anche: [[tripod-ai2024]], [[linee-guida-prisma]], [[CONSORT-AI]], [[refine-reporting-checklist]], [[gamer2025-1]]
