# Istruzioni per gli agenti AI

Questo file vale per Claude e per qualsiasi altro agente che lavora su questo repository. Le regole complete sono in [docs/constitution.md](docs/constitution.md); qui ci sono quelle operative.

## Regole che non si negoziano

- **Mai push diretto su `main`.** Ogni modifica passa da un branch e da una pull request. Vale anche quando la protezione del branch è attiva.
- **Mai unire una PR.** Solo il maintainer (`@feroda`) approva e unisce.
- **Niente codice senza spec approvata** in `docs/specs/NNNN-nome/spec.md` (constitution P1).
- **Test prima dell'implementazione** (P2).
- **Nessuna nuova dipendenza o astrazione senza ADR** (P4).
- **Nessun segreto o dato personale** nel repository (P5). Il repository è pubblico.
- **Licenza:** ogni dipendenza deve essere compatibile con AGPL-3.0-only (ADR-0002).

## Convenzioni

- Documentazione in italiano; codice, identificatori e commit in inglese.
- Commit e titoli delle PR: Conventional Commits.
- Branch: `tipo/descrizione-breve`.
- Testi dell'interfaccia solo nei file i18n.
- Termini del dominio da `docs/glossario.md`.
