# Prompt — avvio della repo e primo giro di analista (una volta sola, Claude Code in locale)

Sei Claude Code nella cartella della repo `ricerca-lavoro` sul PC di Matteo. Matteo ti autorizza a fare i passi
qui sotto, in ordine. Fermati e chiedigli solo se un passo fallisce o se trovi qualcosa di diverso da quanto scritto.

## Parte 1 — repo pulita e pubblicata
1. `git status` e `git log --oneline origin/main..main`. Devono esserci due commit locali non pubblicati,
   `collaudo: pulizia dati di prova…` e `collaudo: prompt di avvio…`, e nessuna modifica non salvata.
   Se in `.git` ci sono file `*.lock` e nessun comando git è in corso, cancellali: sono residui di una sessione precedente.
2. `git pull --rebase` (ChatGPT può aver scritto su GitHub nel frattempo), poi `git push`. Mai force push.
   Conflitto su `AGENTS.md`, `README.md` o `prompt/`: tieni la versione dei commit `collaudo:`. Su altri file: fermati e chiedi.
3. La cartella `..\ricerca-lavoro-collaudo` contiene i cloni usati nel collaudo del 12/11/2026.
   Per ogni clone controlla `git status` e `git log origin/main..HEAD`. Se nessuno ha modifiche o commit non pubblicati,
   cancella l'intera cartella; altrimenti elenca cosa c'è e chiedi. Non toccare `..\ricerca-lavoro-collaudi` (i rapporti).
4. Controllo finale: `git status` pulito, `main` uguale a `origin/main`, nessun file EBSCO, ogni scheda con uno Stato
   della lista «Stati della scheda» di AGENTS.md. Eventuali correzioni: commit `collaudo: <cosa>` e push.

## Parte 2 — primo giro di analista
Leggi `prompt/analista.md` e seguilo. Note solo per questo primo giro:
- Le 9 schede `nuova` vengono dal collaudo del 12/11, ma sono annunci veri: trattale come materiale normale.
- menutech: la revisione del 12/11 ha letto sulla pagina «Fully remote» e «Work from anywhere in Italy», mentre la scheda
  dice «minimo 3 giorni a settimana a Milano». Verifica tu sulla fonte e correggi.
- menutech e rise-data-labs hanno già una sezione «Analisi» del 12/11: riscrivila da capo, non aggiungerne una seconda.
- tebi: manca l'intestazione `## Analisi`.
- satispay: la pagina Ashby si legge solo con JavaScript. Se non riesci a leggerla: `Verificato attivo: non verificabile (motivo)`.

## Chiusura
Quella di AGENTS.md, più una riga: `Pubblicato: sì (origin/main = <hash>)` oppure `Pubblicato: NO — <motivo>`.
