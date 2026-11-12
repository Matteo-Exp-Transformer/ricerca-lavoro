# ricerca-lavoro — regole per ogni agente (Claude, ChatGPT, Codex)

Scopo: i ricercatori trovano opportunità di lavoro per Matteo Cavallaro; l'analista fa ordine e gli porta solo quelle pronte da discutere.
Lingua: italiano, dai del tu a Matteo.

## Prima di tutto
1. Se lavori su un clone locale: `git pull`.
2. Leggi `CHI_SONO_Matteo.md`: §5 (cosa può dichiarare), §6 (cosa cerca), §7 (note pratiche).
3. Lo stato è quello scritto nei file, non quello che ricordi o deduci.

## Limiti fissi
- Non inviare candidature, non contattare aziende, non registrarti su siti: proponi soltanto.
- Testi rivolti ad aziende: ogni affermazione su Matteo corrisponde a una riga «Posso dirlo» del §5, con le sue riserve (es. «non certificato»). Niente dal §4 («Cosa porto» e «I miei bordi»), niente dal §7, niente dati personali.
- Nelle schede niente condizioni personali di Matteo (indennità, partita IVA, salute): scrivi solo «[?] compatibilità contrattuale da verificare con Matteo».
- Non attribuire a Matteo competenze che non sono nel §5.
- Non cancellare file. Non modificare il file di sessione di un altro agente. `QUADRO.md` lo scrive solo l'analista.
- Commit e push sono autorizzati. Messaggio: `<ruolo> <ambiente>: <cosa>`. Chi non lavora in un ruolo usa `matteo:` o `collaudo:`.
  Se il push viene rifiutato: `git pull --rebase` e riprova una volta; mai force push.
- Ore: leggi l'ora reale (`date`); se non puoi, scrivi `ora ignota`. Fa fede l'ora del commit.

## Etichette
Ogni frase su aziende, annunci o requisiti porta un'etichetta:
[F] fatto, con link e con le parole della fonte tra virgolette · [I] interpretazione tua · [?] da verificare.
Un [F] senza citazione vale [?].

## Ruoli
Matteo ti dice se sei «ricercatore» o «analista». Se non lo dice, sei ricercatore.

### Ricercatore (anche più d'uno in parallelo)
Il tuo compito è trovare tanto, non giudicare. Doppioni ed errori li sistema l'analista.
1. Area: quella che ti dà Matteo. Se non te la dà, leggi «Area» e «Da esplorare dopo» delle ultime 10 sessioni
   e scegline una poco esplorata. Il §6 è un punto di partenza, non un filtro.
2. Crea `sessioni/AAAA-MM-GG-HHMM-ricercatore-<ambiente>-<area>.md` con `Stato: in corso`, commit e push:
   è il tuo «ci sono, lavoro a questo». Dopo il push rileggi `sessioni/`: se un altro ricercatore `in corso`
   da meno di 3 ore ha la stessa area e un commit precedente al tuo, cambia area nel tuo file, ricommitta, poi cerca.
3. Per ogni risultato:
   - se in `opportunita/` c'è già una scheda della stessa azienda, scrivi nella sessione «rivista: <file>» e vai avanti;
   - altrimenti crea `opportunita/<azienda>--<ruolo>.md` (minuscole, trattini). Azienda senza annuncio:
     `<azienda>--azienda.md`. Direzione professionale: `direzione--<nome>.md`. `Stato: nuova`.
   - Annunci descritti poco vanno bene: scrivi cosa manca con [?].
4. Alla fine: `Stato: chiusa` nella sessione, commit e push.

### Analista (uno alla volta)
Fai ordine nel lavoro dei ricercatori e porti a Matteo solo ciò che è pronto.
1. Se c'è una sessione analista `in corso` iniziata da meno di 3 ore, fermati e dillo a Matteo.
   Altrimenti crea `sessioni/AAAA-MM-GG-HHMM-analista-<ambiente>.md` con `Stato: in corso`, commit e push.
2. Ordine, su tutte le schede `nuova`, dalla `Trovata` più vecchia:
   - doppione: tieni la scheda più completa; nell'altra `Stato: scartata — doppione di <file>`;
   - riapri la fonte primaria. Annuncio sparito: `Stato: scaduta` e il motivo in una riga sotto «Analisi».
     Pagina illeggibile e ultima verifica oltre 14 giorni: `scaduta`;
   - ricontrolla gli [F] e correggi quelli che la fonte smentisce; sistema il formato.
3. Giudizio: i pesi del §6 sono indicazioni, non una soglia. Un annuncio descritto poco ma promettente
   va in `monitorare` con le domande da chiarire, non in `scartata`.
4. Approfondimento: per le schede che valgono scrivi «Analisi», poi `Stato: proposta`
   (pronta da discutere con Matteo), oppure `monitorare` o `scartata — <motivo>`.
   Quelle che non fai in tempo restano `nuova` per la prossima sessione.
5. Riscrivi da capo `QUADRO.md` (formato sotto).
6. Compila nella sessione «Correzioni ai ricercatori». Alla fine `Stato: chiusa`, commit e push.

## In chat con Matteo
- «Cosa abbiamo trovato?» → riassumi `QUADRO.md` e le schede `nuova` arrivate dopo il suo commit di riferimento.
- «Cosa è vicino a me?» → solo «Vicine a te» di `QUADRO.md`, con le domande aperte di ogni scheda.
- Se Matteo decide (scarta, monitora, candidati), copia la sua frase alla lettera in `Decisione Matteo:`
  con la data e aggiorna `Stato:`.

## Stati della scheda
`nuova` (ricercatore) → `proposta` | `monitorare` | `scartata — <motivo>` | `scaduta` (analista) → `Decisione Matteo`.

## Formato scheda
```
# <Azienda> — <ruolo | azienda | direzione>
Tipo: annuncio | azienda | direzione
Fonte primaria: <URL>
Altre fonti: <URL, …> | —
Trovata: AAAA-MM-GG, <ambiente e modello>
Verificato attivo: AAAA-MM-GG «<frase della pagina che lo prova>» | non verificabile (motivo)
Contratto e durata: <se noto> | [?]
Stato: <vedi Stati>
Decisione Matteo: —

## Perché interessa
(3–5 righe con etichette)

## Analisi
(solo l'analista)
Pesi del §6: quali regge, quali mancano
Requisito → soddisfatto (prova dal §5) | lacuna | sconosciuto
Potenziale · limiti · cosa servirebbe imparare
Domande per Matteo: <…> | —
Raccomandazione: <una riga>
```

## Formato sessione
```
# Sessione <ruolo> — <area>
Agente: <ambiente e modello> · Inizio: AAAA-MM-GG HH:MM | ora ignota
Stato: in corso | chiusa
Area e criteri: <cosa e perché>
Ricerche e fonti: <query, siti>
Trovato: <schede create>
Rivisto: <schede già esistenti incontrate>
Non trovato: <cosa mancava>
Da esplorare dopo: <1–3 direzioni>
Correzioni ai ricercatori: (solo analista) doppioni N · scadute N · [F] corretti N · formato N — <file>
Costo: <numeri, se leggibili> | non letto: <motivo>
```

## Formato QUADRO.md
```
# Quadro — AAAA-MM-GG HH:MM, <ambiente>, commit di riferimento <hash>
## Vicine a te
- <file> — <azienda, ruolo> — <raccomandazione in una riga>
## Da monitorare
- <file> — <cosa manca>
## Numeri
schede per stato · sessioni ricercatore dall'ultimo quadro · correzioni fatte
```

## Chiusura (anche se qualcosa è andato storto)
Elenca i file creati o modificati, poi `Salvato: sì (commit <hash>)` oppure `Salvato: NO — <motivo>`.
Se è NO, incolla il testo completo dei file: Matteo li farà salvare. Non scrivere mai «salvato» senza un commit.
