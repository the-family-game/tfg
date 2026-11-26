# Constitution di TFG – The Family Game

- **Versione:** 1.0.0
- **Stato:** Bozza, in attesa di approvazione del maintainer
- **Ultima modifica:** 2026-11-26

Questo documento definisce le regole che valgono per tutto il progetto. Ogni spec, piano, ADR e riga di codice deve rispettarlo. In caso di conflitto tra questo documento e qualsiasi altro, prevale la constitution.

Le parole **DEVE**, **NON DEVE**, **DOVREBBE** e **PUÒ** hanno il significato di RFC 2119 (MUST, MUST NOT, SHOULD, MAY).

## 1. Scopo

TFG è un gioco per famiglie:

- **per famiglie:** pensato per essere giocato insieme, da più generazioni;
- **accessibile a tutte le età:** utilizzabile da bambini, adulti e anziani, con attenzione all'accessibilità (WCAG come riferimento);
- **sicuro per i minori:** nessuna funzione può esporre un minore a contenuti, contatti o raccolte di dati non adatti.

## 2. Principi non negoziabili

### P1. Spec prima del codice
Nessun codice viene scritto senza una spec approvata dal maintainer. Il flusso è: `spec.md` → approvazione → `plan.md` → `tasks.md` → implementazione. Una PR di codice DEVE citare la spec che implementa.

### P2. Test prima dell'implementazione
Ogni criterio di accettazione di una spec ha almeno un test automatico. I test vengono scritti prima del codice che li fa passare. Una PR che chiude un criterio senza un test NON DEVE essere unita.

### P3. Privacy dei minori
Si raccolgono solo i dati strettamente necessari (minimizzazione). Il progetto DEVE rispettare GDPR (incluso l'art. 8 sul consenso dei minori) e COPPA. Ogni spec che tratta dati personali DEVE contenere una sezione "Privacy" che elenca dati raccolti, finalità, conservazione e base giuridica. Nessun tracciamento pubblicitario, nessuna profilazione di minori.

### P4. Semplicità
Nessuna nuova dipendenza esterna e nessuna nuova astrazione architetturale senza un ADR approvato. Si preferisce la soluzione più semplice che soddisfa la spec.

### P5. Pronto per l'open source
Il repository DEVE poter diventare pubblico in qualsiasi momento senza interventi di pulizia:
- licenza chiara e dichiarata in `LICENSE`;
- nessun segreto (chiavi, token, password, dati personali) nel repository né nella sua storia;
- dipendenze con licenze compatibili, verificate in CI.

### P6. Lingua e traducibilità
- La documentazione è scritta in **italiano**.
- Una lingua per file: le traduzioni vivono accanto all'originale con il suffisso della lingua (es. `spec.md` e `spec.en.md`).
- I termini del dominio sono definiti in [`docs/glossario.md`](glossario.md) e usati in modo coerente.
- Spec, requisiti, criteri e ADR hanno **ID stabili** che non cambiano con la traduzione o la rinumerazione.
- Codice, identificatori e messaggi di commit sono in **inglese**.
- Nessun testo dell'interfaccia è scritto nel codice: tutti i testi visibili all'utente stanno in file i18n.

## 3. Vincoli tecnici

- **Stack:** lo stack tecnico è scelto in **ADR-0001** e cambia solo con un nuovo ADR che lo sostituisce.
- **CI obbligatoria:** nessun merge su `main` senza CI verde. La CI esegue almeno lint, test e controllo delle licenze delle dipendenze.
- **Commit:** [Conventional Commits](https://www.conventionalcommits.org/) (es. `feat:`, `fix:`, `docs:`).
- **Versioni:** [Semantic Versioning](https://semver.org/). Le modifiche sono registrate in `CHANGELOG.md`.
- **Branch:** `main` è protetto; ogni modifica passa da una pull request.

## 4. Governance

- **Maintainer unico:** Lucafero (GitHub `@feroda`). Solo il maintainer approva spec, ADR e pull request.
- **Agenti AI:** gli agenti AI (es. Claude) propongono spec, piani, task, ADR e codice esclusivamente tramite pull request. Non uniscono le proprie PR.
- **Modifiche alla constitution:** solo con una PR dedicata, che modifica unicamente questo documento e ne aumenta la versione:
  - MAJOR: rimozione o ridefinizione di un principio;
  - MINOR: nuovo principio o vincolo;
  - PATCH: chiarimenti senza effetti sostanziali.

## Storico delle versioni

| Versione | Data | Modifica |
|---|---|---|
| 1.0.0 | 2026-11-26 | Prima stesura |
