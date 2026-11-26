# ADR-0002: Licenza AGPL-3.0-only e repository pubblico

- **Stato:** Proposto
- **Data:** 2026-11-26
- **Decisori:** Lucafero (maintainer)
- **Spec collegate:** —

> Il numero 0001 resta riservato alla scelta dello stack tecnico, come previsto dalla constitution.

## Contesto

- Il maintainer vuole rendere pubblico il repository fin da subito, anziché attendere il raggiungimento di un introito stabile come ipotizzato all'inizio.
- Su GitHub Free le regole di protezione dei branch non sono applicate ai repository privati di un'organizzazione: un repository pubblico le rende applicabili senza costi.
- Il codice pubblico senza licenza non è riutilizzabile da nessuno e non consente contributi.
- Il maintainer vuole conservare la possibilità di ricavare un introito dal progetto, per esempio vendendo licenze commerciali a chi non vuole rispettare gli obblighi di una licenza copyleft (doppia licenza).
- Il gioco potrà essere offerto online: una licenza copyleft "classica" (GPL) non obbliga chi lo ospita come servizio a pubblicare le proprie modifiche.

Alternative considerate:

| Opzione | Pro | Contro |
|---|---|---|
| Tutti i diritti riservati | Massimo controllo | Nessun riuso né contributo: open source solo di facciata |
| MIT / Apache-2.0 | Massima diffusione | Chiunque può creare una versione chiusa e rivenderla; la doppia licenza perde valore |
| GPL-3.0 | Copyleft | Non copre l'uso come servizio di rete |
| **AGPL-3.0** | Copyleft anche per l'uso via rete; compatibile con la doppia licenza | Alcune aziende evitano l'AGPL: riduce l'adozione commerciale gratuita (che qui è voluto) |

## Decisione

Adottiamo la licenza **GNU Affero General Public License v3.0, solo questa versione** (SPDX: `AGPL-3.0-only`) per tutto il codice e la documentazione del repository, e rendiamo pubblico il repository.

- Si sceglie `-only` e non `-or-later` per non vincolare il progetto a versioni future della licenza non ancora scritte.
- Il copyright resta in capo al maintainer. Per preservare la doppia licenza, i **contributi esterni sono accettati solo dopo aver adottato un Contributor License Agreement (CLA)**, che sarà oggetto di un ADR successivo.
- Asset non software (grafica, audio, testi di gioco) potranno avere una licenza diversa, decisa con un ADR dedicato quando esisteranno.

## Conseguenze

- Il repository può diventare pubblico; le protezioni del branch `main` diventano applicabili.
- Chi distribuisce il gioco, o lo offre come servizio in rete, deve pubblicare il codice sorgente, comprese le modifiche, sotto AGPL-3.0.
- Il maintainer può offrire licenze commerciali separate, finché detiene tutti i diritti sul codice.
- Le dipendenze future devono avere licenze compatibili con AGPL-3.0 (verifica in CI, constitution P5).
- La pubblicazione è di fatto irreversibile: le copie già fatte da terzi restano anche se il repository tornasse privato.
- Da questo momento gli indirizzi email nei commit sono pubblici: usare l'indirizzo noreply di GitHub.
