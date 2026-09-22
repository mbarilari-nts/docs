---
title: Master Factory Web ChangeLog
description: 
published: true
date: 2026-09-22T08:51:06.279Z
tags: changelog, masterfactory-web
editor: markdown
dateCreated: 2026-09-22T08:51:06.279Z
---

# Master Factory Web ChangeLog

## Nelle prossime release…

## Rilascio setup 2026-06-??

### 2026-06-11

- :hammer: BREAKING CHANGE  Corretto pulsante *Rettifica* nel carico materiali nella maschera operatore, ora viene nascosto in caso l’UdM non sia in stato OK.
- :heavy_plus_sign: Aggiunta nuova permission OBBLIGATORIA se si vuole modificare la quantità da dichiarare *HmiB\_ProductionChangeQty*.

**ATTENZIONE:** è necessario aggiungere la permission HmiB\_ProductionChangeQty, altrimenti non sarà più possibile modificare la quantità durante le dichiarazioni.

### 2026-04-28

- :hammer: Corretto consumo UdM al carico nella maschera operatore HmiB. In alcune condizioni era possibile consumare su ODL in stato ARCHIVED.

in corso…

## Rilascio setup 2026-03-31

### 2026-03-31

- :hammer: Corretta lettura da HmiT UdM InBound, l’UdM veniva lasciato in WIP.
- :gear: Ottimizzazione serializzazione comunicazione messaggi Server e Web.

**ATTENZIONE**: Questa patch è legata alle modifiche al Client versione 2026-03-20 e al Server versione [2026-03-31](https://ntsmanufacturing.atlassian.net/wiki/spaces/NTSM/pages/2424841/Master+Factory+Server+changelog#2026-03-31-%E2%9A%A0%EF%B8%8F)

### 2026-03-03

- :hammer: Corretto aggiornamento dell’utente attualmente autenticato in alto a destra, ora se all’utente impersonificato scade la sessione, il nome utente viene correttamente aggiornato.
- :heavy_plus_sign: Aggiunta pagina `Dichiarazione quantità per gruppi di ordini`, è possibile accedere tramite la lista degli Equipment (l’opzione `Raggruppa` deve essere attiva). Nella pagina è possibile scegleire per quale ordine dichiarare, dopo aver dichiarato ritorna alla nuova maschera consentendo di selezionare un nuovo ordine dove dichiarare.

### 2026-02-16

- :heavy_plus_sign: Aggiunta dichiarazione a matricola (vedi proprietà StorageType=2 nell’Equipment). La schermata di dichiarazione permette l’inserimento della matricola, se la matricola è già stata dichiarata non permette l’inserimento restituendo un messaggio con l’errore.

### 2026-02-10

- :hammer: Corretto cambio macchina al gruppo (nelle versioni precedenti non veniva rispettato il vincolo del gruppo di ordini)
- :gear: Ottimizzazione velocità caricamento Maschera Operatore
- :heavy_plus_sign: Filtro sulla griglia di scelta degli ordini.

## Rilascio setup 2026-01-27

- :heavy_plus_sign: Aggiunti nella testata della pagina dell’Equipment i ProductionRequestID e CustomScheduleGroupID dell’ordine attivo.
- :hammer: Corretta anomalia nell’immissione delle cifre tramite interfaccia web, la problematica è legata al separatore delle migliaia. L’anomalia si presenta dalle versioni dei browser: Firefox 120+, Chrome 118+, Edge come Chrome.
- :heavy_plus_sign: Al presentarsi di più Segment requirements che corrispondono allo stesso sottolotto ora è possibile spostare ed avviare automaticamente il primo in sequenza su un Equipment alternativo, questo avviene caricando nella baia di ingresso il sottolotto designato al consumo. Se il materiale da consumare del Segment requirement ha come specifica lotto o materiale, il comportamento rimane inalterato; solo con un solo ordine questo viene spostato ed avviato automaticamente. La seguente modifica richiede che la versione server, server web e client siano almeno della versione 2025-11-11.

### 2026-01-22

- :hammer: Corretta chiusura utilization del Personnel, in alcune condizioni rimaneva aperta l’utilization non permettendo una corretta attribuzione dei tempi.
- :hammer: Corretta chiusura utilization degli Equipment lasciando invariate le Material alla sospensione dell’ordine, in alcune condizioni rimaneva aperta l’utilization non permettendo una corretta attribuzione dei tempi.
- :gear: Miglioramento delle performance cambi stato multipli.

## Rilascio setup 2025-11-17

### 2025-10-24

- :hammer: In condizioni particolari, alcune UdM non permettevano lo spostamento e l'attivazione di ordini da altre macchine, l'anomalia coinvolge unicamente la parte web.

## Rilascio setup 2025-09-26

### 2025-09-22

- :heavy_plus_sign: Aggiunto pulsante `Raggruppa`, che permette di raggruppare gli ordini per equipment nella schermata web nella pagina `EquipmentList`. L’utente può attivare la funzionalità, l’opzione viene memorizzata per nelle impostazioni utente. L’aggiornamento può non essere contestuale al cambio dell’opzione, ma può  avere un ritardo anche di alcuni secondi.

### 2025-09-11

- :heavy_plus_sign: Nella pagina `EquipmentList` ora gli ordini raggruppati vengono mostrati come un unico Equipment, prima venivano mostrati gli Equipment moltiplicati per il numero di ordini in RUN. Premendo su di esso si viene portati al primo ordine in RUN.
