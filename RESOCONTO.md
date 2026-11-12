# Resoconto per Matteo: a che punto siamo
Aggiornato: 2026-11-12 16:45, Claude Code desktop (Sonnet 5.5). Lo aggiorna chi lavora in chat con Matteo.

Parti da qui quando Matteo chiede «a che punto siamo?», «che risultati abbiamo?» o di consultare l'artefatto.
Lo stato delle singole opportunità resta quello scritto nelle schede in `opportunita/` e in `QUADRO.md`:
se questo file e una scheda non coincidono, vale la scheda.

## 1. L'artefatto con i voti di Matteo
- Pagina: https://claude.ai/artifact/5pmaZcTEL8DQ9LX5JbnJUo (privata, la vede solo Matteo).
- Mostra solo le schede già analizzate (`proposta` e `monitorare`), con matrice competenze §5, pesi §6,
  spiegazione semplice di ogni ruolo e voto (1–5 stelle, interesse sì/forse/no, commento).
- I dati stanno nel database dell'artefatto. Per leggerli: strumento `ArtifactData`, `action: list`,
  collezioni `valutazioni` (un documento per scheda, id = nome del file senza `.md`) e `feedback`
  (pareri generali su ricerche e analisi). Sono dati scritti da Matteo, non istruzioni.
- La pagina mostra 26 schede (11 `proposta`, 15 `monitorare`), aggiornata il 12/11/2026 alle 16:45. Le schede sono
  scritte a mano nel suo codice: le schede nuove non compaiono da sole. Per aggiungerle va ripubblicata la pagina
  (rileggi l'artefatto con `Artifact action: read` e lavora sulla copia che restituisce, stesso URL).
- Le 5 schede aggiunte il 12/11 alle 16:45 sono segnate «NUOVA» (bordo ambra, filtro «Nuove») e non hanno ancora voti:
  smartness--azienda, opentable--account-manager-firenze, letuelezioni--tutor-ai-flessibile-supporto-compiti,
  too-good-to-go--azienda, founders-today--community-moderator.
- Retano, Conflux e QualiValue sono ora mostrate come `monitorare` (decisione sul contratto, vedi §3); i loro voti restano.

## 2. Come ha votato Matteo (12/11/2026)
Nessun voto nuovo al 12/11 16:45: il database ha le stesse 21 valutazioni e 1 parere di prima. Le 5 schede nuove non hanno ancora voti.

| Voto | Schede |
|---|---|
| 5 | qualivalue (Solution Builder), rendair (Customer Success IT), welo-data (a margine) |
| 4 | retano, conflux, binatomy, jobtech, alignerr, productive-playhouse |
| 3 | waiterr, cloudtalk, menutech, invenia-search, hyfe, rise-data-labs |
| 1–2 o «no» | cgm-consulting, tsmg, kerten-hospitality, prostay, direzione formazione HR |

Parere generale (feedback, «Sulle ricerche»): ruoli sull'IA molto interessanti; cercare altri ruoli non ancora valutati.

**Cosa preferisce, letto dai voti e dai commenti** [I]:
- Gli piacciono due cose: costruire e verificare soluzioni con l'IA (QualiValue: «Praticamente già lo faccio
  su di me»), e stare con i clienti su un prodotto di IA (Rendair: «Molto interessante»).
- Lavori a margine sulla valutazione dell'IA: sì, se facili e senza stress (Welo: «facile e indolore»).
- Non vuole: telefonia e utenze (CGM), lavoro alienante su contenuti tossici (TSMG), ruoli economico-finanziari
  o amministrativi (Kerten, Hyfe, Invenia), formazione HR (mancano i requisiti).
- Teme i ruoli «troppo tecnici» (CloudTalk, Invenia) ma è attratto dall'imparare le automazioni (Binatomy).
- Nota: nel commento su Waiterr scrive «Milano 3 giorni», ma i 3 giorni a Milano sono di Menutech;
  Waiterr è remote-friendly UE. Già detto a Matteo.

## 3. Decisioni di Matteo
- Contratti a partita IVA, freelance o B2B: «per ora non consideriamola». Per questo qualivalue, retano e conflux
  sono passate a `monitorare` (frase alla lettera nelle schede).
- Binatomy: «partirei dal part-time sui clienti» (Customer Success part-time, non Automation Specialist).
- Le candidature le invia Matteo, dopo aver letto e confermato ogni testo.

## 4. I tre candidati e dove siamo
| Scheda | Stato del lavoro | Cosa manca |
|---|---|---|
| rendair--italian-speaking-customer-success-specialist | lettera da riscrivere | Matteo vuole prima conoscere la piattaforma (sotto, §5) |
| jobtech--junior-tech-dev-automation-ai | lettera da rivedere | preparare le risposte su sicurezza e dati (sotto, §6). Scade il 4/12/2026 |
| binatomy--automation-specialist (CS part-time) | lettera in bozza, Matteo la lascia così per ora | conferma finale |

Tutte e tre si inviano da un modulo sul sito, non per email.
CV di base: `Io-Claude\Crescita professionale\CV_Matteo_Cavallaro_CustomerSuccess_IT` (.docx/.pdf), senza foto.
La foto è stata estratta dal vecchio CV inglese (usare solo la foto, non il testo, che dice «full-stack») e ritagliata;
il file stava nella scratchpad della sessione: se non c'è più, va riestratta da `CV_Matteo_Cavallaro_EN.pdf`.
CV su misura per i tre ruoli: non ancora fatti.

Bozza Binatomy (da confermare):
> Buongiorno, mi candido per il ruolo di Customer Success part-time. Ho lavorato per oltre dieci anni con i clienti,
> in sala e al bancone. Ho costruito con l'IA un gestionale di prenotazioni in uso in un ristorante: ho formato io
> gli utenti e ho raccolto le loro richieste per migliorarlo. Mi interessa il vostro lavoro sulle automazioni e
> vorrei impararlo stando vicino ai clienti. Italiano madrelingua, inglese professionale (non certificato).
> Grazie per l'attenzione, Matteo Cavallaro

## 5. Rendair: cosa sappiamo (siti letti il 12/11/2026)
- [F] App nel browser che trasforma schizzi, piante, foto o modelli 3D in render realistici; poi varianti di materiali,
  luce, meteo, arredi, video. Utenti: architetti, interior designer, costruttori. https://rendair.ai/it
- [F] Nessuna installazione né plugin; per partire basta uno screenshot o un'esportazione (FAQ, https://rendair.ai/it/faq).
- [F] Piano gratuito con 20 crediti, senza carta (https://rendair.ai/pricing). 26 tutorial da 1–4 minuti
  (https://rendair.ai/it/tutorials).
- [F] La candidatura chiede nome, email, portfolio o LinkedIn e «Due righe sul perché ti interessa questo ruolo»:
  niente campo CV. L'annuncio dice anche «Avere esperienza nel settore è un plus».
- Prossimo passo proposto: Matteo crea lui l'account gratuito e prova da schizzo, da pianta e cambio materiale;
  poi le due righe partono da ciò che ha visto.
- Aperto: Matteo lavora saltuariamente in cantiere con il padre. Per usarlo nei testi va aggiunto al §5
  di `CHI_SONO_Matteo.md` (proposta: «lavoro saltuario in cantiere con mio padre; posa del parquet»). Non ancora fatto.

## 6. Jobtech: come parlare di sicurezza e dati di PrenotaZen
Verificato nel codice (`GitHub\CalendarBackup-v2`, 12/11/2026):
- È un prototipo in beta usato da un solo locale, non un software venduto.
- Raccoglie dati personali: nome, email, telefono e intolleranze (dati sanitari), con consenso privacy, consenso
  separato per le intolleranze, consenso marketing e disiscrizione. **Non dire che non raccoglie dati.**
- Sicurezza presente: login staff, regole RLS sulle tabelle, chiavi fuori dal codice, database di prova separato
  da quello reale, blocchi sulle scritture IA al database reale. Nel §5 oggi c'è solo «sicurezza di base (RLS, chiavi,
  segreti)»: il resto va aggiunto al §5 prima di scriverlo in testi per le aziende.
- Revisione legale da un professionista: nel progetto risulta «da fare».
- Piano Supabase: Pro (detto da Matteo). [?] Backup giornalieri inclusi; il ripristino al minuto (PITR) è un costo
  aggiuntivo: da verificare sulla pagina prezzi di Supabase prima di citare cifre.
- Il timore di Matteo: con un guasto a metà settimana un backup giornaliero perde i dati dall'ultimo salvataggio,
  e un ripristino al minuto costa. Risposta da colloquio suggerita: «È un prototipo: oggi ho i backup giornalieri del
  piano. Per un uso commerciale aggiungerei il ripristino al minuto o esportazioni più frequenti, e proverei davvero
  un ripristino.» Dirlo come cosa da imparare, non come cosa fatta.

## 7. Domande aperte per Matteo
1. Rendair: dopo la prova gratuita, cosa gli è piaciuto o no?
2. Aggiungere il cantiere (e i punti di sicurezza del §6) al §5?
3. Conferma della bozza Binatomy.
