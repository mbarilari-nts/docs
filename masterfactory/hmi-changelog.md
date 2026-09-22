---
title: Master Factory HMI ChangeLog
description: 
published: true
date: 2026-09-22T08:46:39.210Z
tags: changelog, masterfactory-hmi
editor: markdown
dateCreated: 2026-09-22T08:46:39.210Z
---

# Master Factory HMI ChangeLog

## Nelle prossime release…

### Rilascio 2026-06-??

#### 2026-06-08

- :hammer: Correzione aggiuntiva maschera BEM che blocca il pulsante PRECONFIRM quando è CONFIRM.

#### 2026-06-01

- :hammer: Ora non è più possibile riaprire le BEM in stato CONFIRMED.

#### 2026-05-18

- :hammer:  Corretta colonna tempo in Analisi ? Tempi di produzione uomo. Necessario reset griglia.

#### 2026-04-27

- :hammer: Corretto consumo UdM al carico nella maschera operatore HmiB. In alcune condizioni era possibile consumare su ODL in stato ARCHIVED.

#### 2026-04-22

- :heavy_plus_sign: ? Migliorata visualizzazione capacità materiali nella maschera di sequenza.

### Rilascio setup 2026-03-31

#### 2026-03-20

- :heavy_plus_sign: Aggiunto pulsante Inbound Preconferma -> PRECONFIRM nei ricevimenti che permette la pre-conferma a Business
- :heavy_plus_sign: Aggiunta in Analisi Dati ? Produzione le descrizioni di Tecnologia, Macchina
- :gear: Migliorato il dispatcher Allarmi, ora permette nuove modalità di dock

#### 2026-03-11

- :gear: Nuovo Dispatcher Docking.
- :gear: Migliorato feedback chiusura Inbound/Outbound.

#### 2026-03-02

- :heavy_plus_sign: Nella schermata Pianificazione ? Fasi ? Sequenza: Migliorata gestione Drag & Drop per sequenziazione ordini, ora selezionando più ordini consecutivi è possibile spostarli in gruppo.

### Rilascio setup 2026-01-27

#### 2026-02-16

- :hammer: Risolto un errore critico che si verificava in assenza di rotte configurate nei flussi inbound.
- :heavy_plus_sign: Introdotta la selezione rapida della stampante tramite un nuovo pulsante posizionato nella testata.
- :heavy_plus_sign: Al presentarsi di più Segment requirements che corrispondono allo stesso sottolotto ora è possibile spostare ed avviare automaticamente il primo in sequenza su un Equipment alternativo, questo avviene caricando nella baia di ingresso il sottolotto designato al consumo. Se il materiale da consumare del Segment requirement ha come specifica lotto o materiale, il comportamento rimane inalterato; solo con un solo ordine questo viene spostato ed avviato automaticamente. La seguente modifica richiede che la versione server, server web e client siano almeno della versione 2025-11-11.

### Rilascio setup 2025-11-17

#### 2025-11-14

- :heavy_plus_sign: Nella schermata Pianificazione -> Ordini, aggiunti controlli durante la creazioni di ordini di lavoro:
  - deve avere almeno 1 Produced con quantità maggiore di 0;
  - deve essere presente almeno una macchina sul quale eseguirlo;
  - deve avere almeno una fase.
- :hammer: Corretta creazione nuovo utente, ora il flag non è modificabile alla creazione di un nuovo utente.

### Rilascio setup 2025-09-26

#### 2025-09-16

- Da questa versione è richiesto il runtime Microsoft Edge WebView2, tramite il file MicrosoftEdgeWebView2RuntimeInstallerX64.exe presente nella cartella prerequisiti.
- :gear: Aggiornata versione browser SCADA a versione EDGE, aggiungendo la proprietà PLCWEBPATTERN (non presente di default) nell'Equipment. Nella pagina della Macchina in Produzione viene visualizzata una pagina con l’url specificato.

#### 2025-08-04

- :hammer: In Situazione magazzino, corretta la disattivazione del filtro Magazzino-Materiale che si disattivava, premendo sul filtro UdM.
- :hammer: Corretto il cursore nella tabella in Ricevimento merce che rimaneva sempre con l'icona ridimensionamento.
- :hammer: Corretto il comportamento nel Popup di modifica proprietà materiali in Macchina; premendo il pulsante Annulla, venivano comunque salvate le proprietà modificate.

#### 2025-08-03 ??

- :heavy_plus_sign: Rinnovamento grafico interfaccia: aggiunta possibilità di scegliere la skin del programma, spostato menu ribbon superiore nella sidebar a sinistra, aggiornato set di icone per migliorare l'usabilità dell'applicazione.
- :hammer: Miglioramento globale performance, usabilità e risoluzione di bug.

