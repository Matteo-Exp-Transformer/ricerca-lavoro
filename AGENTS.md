# ricerca-lavoro — regole per ogni agente (Claude, ChatGPT, Codex)

Scopo: trovare, verificare e analizzare opportunità di lavoro per Matteo Cavallaro.
Lingua: italiano, dai del tu a Matteo.

## Prima di tutto
1. Se lavori su un clone locale: `git pull`.
2. Leggi `CHI_SONO_Matteo.md`: §5 (cosa può dichiarare), §6 (cosa cerca e come valutare), §7 (note pratiche).
3. Guarda `sessioni/` e `opportunita/`. Lo stato è quello scritto nei file, non quello che ricordi o deduci.

## Limiti fissi
- Non inviare candidature, non contattare aziende, non registrarti su siti: proponi soltanto.
- Testi rivolti ad aziende: solo dal CV e dal §5 di CHI_SONO. Mai il §4 «I miei bordi», mai il §7, mai dati personali.
- Non attribuire a Matteo competenze che non sono nel §5.
- Non cancellare file. Non modificare il file di sessione di un altro agente.
- In una scheda creata da altri puoi cambiare solo: `Verificato attivo`, `Stato`, `Decisione Matteo`, la sezione «Analisi».
- In questa repo commit e push sono autorizzati. Messaggio: `<ruolo> <ambiente>: <cosa>`.
  Se il push viene rifiutato: `git pull --rebase` e riprova una volta; mai force push.

## Ruoli
Matteo ti dice se sei «ricercatore» o «analista». Se non lo dice, sei ricercatore.

### Ricercatore
1. Leggi «Area» e «Da esplorare dopo» delle ultime 10 sessioni.
2. Scegli un'area poco esplorata: tipo di ruolo, settore, canale, forma di collaborazione o direzione nuova.
   Il §6 è un punto di partenza, non un filtro. Se Matteo ti suggerisce un'area, usa quella.
3. Se un'altra sessione con `Stato: in corso` sulla stessa area ha meno di 24 ore, scegline un'altra.
4. PRIMA di cercare crea `sessioni/AAAA-MM-GG-HHMM-<ambiente>-<area>.md` con `Stato: in corso` e salvalo.
   È la tua prenotazione.
5. Per ogni risultato:
   - cerca il nome dell'azienda in `opportunita/`. Se la stessa opportunità c'è già, non creare nulla:
     aggiorna `Verificato attivo` e scrivi nella tua sessione «rivista: <file>»;
   - altrimenti crea `opportunita/<azienda>--<ruolo>.md` (minuscole, trattini). Azienda senza annuncio:
     `<azienda>--azienda.md`. Direzione professionale: `direzione--<nome>.md`.
     Nel dubbio crea la scheda e scrivi `Possibile doppione di: <file>`;
   - annuncio: apri la fonte primaria e verifica che sia ancora attivo;
   - `Stato: da analizzare` solo se l'opportunità regge almeno 4 degli 8 pesi del §6; altrimenti `nuova`.
6. Alla fine: `Stato: chiusa` nella tua sessione.

### Analista
1. Scegli la scheda `da analizzare` con la data `Trovata` più vecchia. Una scheda `in analisi` da più di 24 ore è libera.
2. PRIMA di lavorare scrivi nella scheda `Stato: in analisi — <ambiente> AAAA-MM-GG HH:MM` e salva.
   Se il salvataggio fallisce perché un altro agente l'ha presa, scegline un'altra.
3. Riapri la fonte primaria. Se l'annuncio non c'è più: `Stato: scaduta` e ti fermi.
   Se l'ultima verifica ha più di 14 giorni e non riesci a riverificare: `Stato: scaduta`.
4. Scrivi la sezione «Analisi», poi `Stato: analizzata`.
5. Crea anche il tuo file di sessione (Area = file della scheda analizzata).

## Etichette
Ogni frase su aziende, annunci o requisiti porta un'etichetta:
[F] fatto, con link · [I] interpretazione tua · [?] da verificare.

## Formato scheda
```
# <Azienda> — <ruolo | azienda | direzione>
Tipo: annuncio | azienda | direzione
Fonte primaria: <URL>
Altre fonti: <URL, …> | —
Trovata: AAAA-MM-GG, <ambiente e modello>
Verificato attivo: AAAA-MM-GG | non verificabile (motivo)
Contratto e durata: <se noto> | [?]
Stato: nuova | da analizzare | in analisi — … | analizzata | scaduta | scartata | monitorare | candidatura proposta
Possibile doppione di: <file> | —
Decisione Matteo: —

## Perché interessa
(3–5 righe con etichette; quali pesi del §6 regge)

## Analisi
(solo l'analista)
Requisito → soddisfatto (prova dal §5) | lacuna | sconosciuto
Potenziale · limiti · cosa servirebbe imparare
Raccomandazione: <una riga>
```

## Formato sessione
```
# Sessione <ruolo> — <area>
Agente: <ambiente e modello> · Inizio: AAAA-MM-GG HH:MM
Stato: in corso | chiusa
Area e criteri: <cosa e perché>
Ricerche e fonti: <query, siti>
Trovato: <schede create>
Rivisto: <schede già esistenti incontrate>
Non trovato: <cosa mancava>
Da esplorare dopo: <1–3 direzioni>
Letti: <file — servito | non servito>
Costo: <numeri, se leggibili> | non letto: <motivo>
```

## Decisioni di Matteo
Se Matteo decide in chat (scarta, monitora, candidati), copia la sua frase alla lettera in
`Decisione Matteo:` con la data e aggiorna `Stato:`.

## Chiusura obbligatoria (anche se qualcosa è andato storto)
Incolla in chat il testo completo di ogni file che hai creato o modificato, poi una riga:
`Salvato: sì (commit <hash>)` oppure `Salvato: NO — <motivo>`.
Se non puoi scrivere nella repo (per esempio da ChatGPT) è normale: scrivi `Salvato: NO`,
Matteo farà salvare i file. Non scrivere mai «salvato» senza un commit.
