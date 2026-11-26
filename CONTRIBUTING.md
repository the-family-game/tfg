# Contribuire a TFG

Grazie per l'interesse. Prima di tutto leggi la [constitution](docs/constitution.md): le sue regole valgono per ogni contributo.

## Il flusso in breve

1. **Issue.** Ogni lavoro parte da una issue (bug, proposta di funzionalità o di decisione tecnica).
2. **Spec.** Per una nuova funzionalità si scrive `docs/specs/NNNN-nome/spec.md` partendo da [`_template`](docs/specs/_template/) e si apre una PR con la sola spec.
3. **Approvazione.** Il maintainer approva la spec. Senza spec approvata non si scrive codice.
4. **Piano e task.** `plan.md` e `tasks.md`, eventuali ADR in `docs/adr/`.
5. **Codice.** Prima i test, poi l'implementazione. Ogni PR cita la spec e i criteri (`AC-NNN`) che soddisfa.

Per le correzioni minori (refusi, documentazione) basta una PR.

## Regole pratiche

- **Branch:** `tipo/descrizione-breve`, es. `feat/0003-family-profile`, `docs/fix-typo`.
- **Commit:** [Conventional Commits](https://www.conventionalcommits.org/) in inglese: `feat:`, `fix:`, `docs:`, `test:`, `refactor:`, `chore:`, `ci:`. Una modifica incompatibile si segnala con `!` o con `BREAKING CHANGE:`.
- **Lingua:** documentazione in italiano, codice e commit in inglese, testi dell'interfaccia solo nei file i18n.
- **Segreti:** mai committare chiavi, token, password o dati personali. Se succede, avvisa subito il maintainer: va ripulita anche la storia.
- **CHANGELOG:** aggiungi una riga in `## [Unreleased]` per ogni modifica visibile.
- **CI verde** obbligatoria prima del merge.

## Contributi da agenti AI

Gli agenti AI propongono modifiche solo tramite pull request e non uniscono mai le proprie PR. La PR deve indicare che è stata generata da un agente.

## Licenza dei contributi

La licenza del progetto non è ancora stata definita (vedi [LICENSE](LICENSE)). Finché non lo sarà, non vengono accettati contributi esterni.

## Codice di condotta

Partecipando accetti il [Codice di condotta](CODE_OF_CONDUCT.md).
