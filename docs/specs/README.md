# Specifiche

Ogni funzionalità ha una cartella `NNNN-nome-breve/` (numero a 4 cifre, nome in kebab-case, in inglese o italiano senza accenti) con tre file:

| File | Domanda a cui risponde | Chi lo scrive | Chi lo approva |
|---|---|---|---|
| `spec.md` | **Cosa** e **perché** | Claude (bozza) | Maintainer |
| `plan.md` | **Come**, a livello tecnico | Claude | Maintainer |
| `tasks.md` | **In che ordine**, a passi piccoli e verificabili | Claude | Maintainer |

## Flusso

1. Copia `_template/` in `NNNN-nome/` e scrivi `spec.md`. Stato: *Bozza*.
2. PR con la sola spec. Il maintainer la approva → stato *Approvata*.
3. `plan.md` e `tasks.md` in una PR successiva (o nella stessa, se piccola).
4. Implementazione: una PR per uno o più task, ognuna cita gli ID dei criteri (`AC-NNN`) che soddisfa.
5. A lavoro finito la spec passa a *Implementata*.

Stati possibili: `Bozza` → `Approvata` → `Implementata`, oppure `Ritirata` / `Sostituita da NNNN`.

## Regole

- I numeri non si riutilizzano mai, anche se una spec viene ritirata.
- Gli ID dei requisiti (`R-NNN`) e dei criteri (`AC-NNN`) sono locali alla spec e stabili: non si rinumerano.
- Le traduzioni stanno accanto all'originale: `spec.en.md`, `plan.en.md`, ecc.

## Indice

| N. | Titolo | Stato |
|---|---|---|
| — | Nessuna spec ancora | — |
