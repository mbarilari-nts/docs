# PRODUZIONE

## MACCHINE

| Icona | Funzionalità |
| :---- | :---- |
| ![img](icon-produzione.png) | Permette agli operatori la gestione completa di tutte le fasi sulle macchine, a seconda delle loro autorizzazioni. |

La vista dei macchinari che compaiono nella scheda operatore è subordinata alla selezione effettuata nell'albero nodi. Selezionando la `production line` si ottiene il risultato riepilogativo di tutte le macchine, come quella mostrata qui di seguito:

![img](vista-linea-produzione.png)

Ogni riquadro rappresenta un macchinario, e la colorazione ne identifica il suo status:

| Colore | Stato |
| :----- | :--------------------- |
| <span style="background-color:#000000;display:block;">&nbsp;</span> | Macchina inattiva |
| <span style="background-color:#92D050;display:block;">&nbsp;</span> | Macchina in RUN |
| <span style="background-color:#FF0000;display:block;">&nbsp;</span> | Macchina in allarme |
| <span style="background-color:#FFFF00;display:block;">&nbsp;</span> | Macchina in Setup |

All'interno del riquadro - che rappresenta la macchina - sono presenti le seguenti informazioni:

![img](quadro-macchina.png)

|  1  | Rappresenta il nome della macchina   | 5   | Quantità di pezzi da produrre |
|:---:|--------------------------------------|-----|-------------------------------|
|  2  | Indica lo status della macchina      | 6   | Durata dello stato            |
|  3  | Codice dell'articolo                 | 7   | Indicativo della fase         |
|  4  | Identificativo dell'ordine di lavoro | 8   | Quantità di pezzi prodotti    |

In caso di allarme, cliccare sul riquadro colorato che indica lo status della macchina **2** per aprire una maschera che permette di assegnare una causale di fermo per motivi d'allarme.

![img](modifica-reason.png)

Nel riquadro **A1** sono disponibili le seguenti opzioni:

- `Modifica causale in corso`: una volta che la causale è stata scelta (tra quelle proposte nella griglia **A2**), il sistema provvede ad assegnare tale causale all'allarme in corso.
- `Cambia causale da ora in poi`: una volta che la causale è stata scelta (tra quelle proposte nella griglia **A2**), il sistema provvede ad assegnare tale causale all'allarme dal momento della selezione in poi, lasciando invariato il periodo precedente.
- `Modifica causale dal`: si comporta come l'opzione precedente, con la differenza che è possibile decidere il periodo d'inizio del cambio della causale.

Quando si clicca sul riquadro della macchina (fatta eccezione nell'area del riquadro dello status **2**) si accede all'interno della relativa scheda di gestione dati. Tale scheda è suddivisa nelle seguenti sezioni (poste nella parte bassa della maschera evidenziata all'interno del riquadro rosso):

![img](tab-produzione-dettaglio-ordine.png)

| PRODUZIONE | PREPARAZIONE | CARICO | UDP | FERMI | UTENTI |
|------------|--------------|--------|-----|-------|--------|

In ogni schermata è presente - in basso a destra - il seguente tasto ![img](icon-torna-vista-linea.png) che permette di tornare alla vista riepilogativa di tutte le macchine.

### TAB PRODUZIONE

La scheda "produzione" permette all'operatore di gestire tutte le fasi degli ordini di produzione per la macchina selezionata. Nello specifico, l'operatore può cambiare gli status di ogni fase, sempre mantenendo sotto controllo tutti i dati associati, quali materiali, macchine richieste, personale, ecc. Nell'immagine sottostante, si mostra come appare l'interfaccia.

![img](tab-produzione-stato-fase.png)

La seguente sezione, visibile nella Tab `Produzione`, è descritta nel capitolo `DISPATCH DI UN ODL`.

![img](tab-produzione-dettaglio-ordine.png)

Le fasi visibili in questa griglia sono filtrabili per il loro status, rappresentato graficamente da un colore.

| Colore | Stato |
| :----- | :---------- |
| <span style="background-color:#FF9933;display:block;">&nbsp;</span> | Eseguibile |
| <span style="background-color:#ff0000;display:block;">&nbsp;</span> | Pausa |
| <span style="background-color:#C5E0B3;display:block;">&nbsp;</span> | Setup |
| <span style="background-color:#9CC2E5;display:block;">&nbsp;</span> | Scarico |
| <span style="background-color:#FFD85B;display:block;">&nbsp;</span> | Preparazione |
| <span style="background-color:#00B050;display:block;">&nbsp;</span> | In Esecuzione |
| <span style="background-color:#0000ff;display:block;">&nbsp;</span> | Lavorato |

Le funzioni disponibili per le fasi dell'ordine di lavoro sono le seguenti:

| PREPARA    | AVVIA    |
|------------|----------|
| DICHIARA   | PAUSA    |
| SETUP      | TERMINA  |
| ESEGUIBILE | SEQUENZA |

#### PREPARA

**P1** permette di preparare gli UDC in base al materiale richiesto dalle lavorazioni presenti in macchina. La preparazione di un UDC è possibile solo se lo stato dell'ordine è in `PREPARAZIONE`, altrimenti viene permesso di apportare solo la modifica. Cliccando sul tasto `Prepara` si apre la seguente maschera:

![img](image199.svg)

In **P.A1** è mostrato il gruppo per il quale è in atto la preparazione dei materiali. Per ogni gruppo, sono visualizzate le righe **P.A2** dei materiali richiesti, raggruppati per classe merceologica. L'icona ![img](image200.png) indica che per tale gruppo non è stato ancora caricato alcun materiale. Facendo clic sopra ogni riga si aprirà il seguente pannello:

![img](prepara-fase-materiale.png)

Nella griglia **P.B1** è mostrato il materiale e la relativa quantità richiesta per il gruppo. Qualora siano presenti due fasi lavorative appartenenti allo stesso gruppo, allora la gestione del materiale per loro richiesto viene eseguita insieme.

Per preparare gli UDC con il materiale richiesto, cliccare sul tasto **P.B3** `Preleva per l'ordine selezionato`, in modo da fare aprire la seguente maschera:

![img](prepara-fase-materiale-prelievo.png)

Questa maschera permette all'operatore di prelevare dal magazzino il materiale richiesto, specificandone la quantità. Nel pannello azzurro sono contenute le informazioni generali del materiale richiesto. Il pannello grigio contiene il campo UDM **P.C1**: una volta inserito il codice identificativo dell'UDM (manualmente o letto tramite barcode), il pannello permette di vedere le specifiche e assegnare la quantità prelevata **P.C2**. Per confermare l'operazione premere il tasto
**P.C3** `Conferma`. Nel caso in cui non si desideri prelevare l'intero UDM, ma solo parte di esso, e si voglia aggiornare la sua etichetta, procedere come di seguito descritto: dopo aver indicato in **P.C2** la quantità da prelevare, premere il tasto **P.C4** `Conferma e stampa` in modo da confermare il carico del materiale e inoltre avviare la stampa di due nuove etichette, una con i dati per l'UDM prelevato e l'altra con i dati per l'UDM rimanente.

> [!Note]
> Solo quando si trattano i gruppi di fasi si deve tenere conto dell'ordine di carico: in questo caso il software impone di eseguire il carico del materiale partendo dall'ultima fase del gruppo (l'ordine di inserimento è descritto nella prima colonna **P.B7**), al fine di ottenere il materiale ordinato in base alle lavorazioni da eseguire.

![img](ordine-inserimento-preparazione-materiale.png)

##### ELIMINARE UNA PREPARAZIONE

Selezionando l'UDM da **P.B2** e poi cliccando sul tasto **P.B4** `Rendi` si può eliminare l'intero materiale assegnato o una parte di esso, come mostrato dalla maschera sottostante:

![img](rendi-da-preparazione.png)

In **P.D1** si indica la quantità di materiale da rendere, mentre in **P.D2** se ne indica la causale.

Nel box `UDM sulla quale trasferire` **P.D3** si sceglie su quale UDM si desidera spostare il materiale. Ecco l'elenco delle scelte possibili:

- STESSA UDM: disassociare l'UDM dall'UDC mantenendo lo stesso identificativo
- UDM ORIGINARIA: ricollocare il materiale nell'UDM da cui è stato prelevato
- UDM ESISTENTE: assegnare il materiale a una UDM già esistente, indicandone il codice identificativo solo se appartengono allo stesso lotto
- NUOVA UDM: creare una nuova UDM assegnando (previa autorizzazione) i vari
attributi **P.D4** e lo storage zone **P.D5** in cui essa sarà creata. È anche possibile creare una nuova etichetta spuntando la voce `Stampa`

##### CONSUMARE MANUALMENTE UN MATERIALE

L'operazione di dichiarare manualmente il consumo di un materiale viene eseguita quando si desidera consumare le quantità di materiale disponibile e attribuirgli una causa di consumo oppure di scarto. Si proceda nel modo seguente: selezionare il materiale e cliccare sul tasto `Consuma`, in modo da fare aprire la maschera (immagine sottostante) in cui l'operatore imposta la quantità di materiale consumato e la causale.

![img](consuma-da-produzione.png)

##### CHIUSURA UDC E TERMINAZIONE PREPARAZIONE

Terminato il carico del materiale, è possibile chiudere l'UDC e passare ai successivi gruppi oppure terminare l'intera preparazione.

Per chiudere l'UDC, cliccare sul tasto `chiudi UDC` **P.A6**: questa operazione permette di terminare di caricare il materiale e passare al gruppo successivo. Una volta eseguita l'operazione non è più consentito modificare il materiale già caricato; si può solo caricarne del nuovo per eseguire una sovrapproduzione.

Se non vi sono ulteriori gruppi da preparare, e si è già proceduto alla chiusura di tutti gli UDC esistenti, allora si può portare a termine l'intera operazione di preparazione: cliccando sul tasto **P.A4** `Termina preparazione e rendi eseguibile` si termina la preparazione e si cambia lo stato delle fasi coinvolte, che passano da `PREPARAZIONE` a `ESEGUIBILE`.

##### MATERIALE PREPARATO

Una volta eseguita la preparazione del materiale, è possibile vedere un resoconto del lavoro di preparazione selezionando da **P.A6** la tab `Materiale preparato`. Qualora si volesse apportare delle modifiche ai carichi, selezionare l'UDM da modificare e cliccare sul tasto `Modifica UDC`, che fa aprire la scheda di preparazione in cui apportare le modiche.

##### STORAGE ZONE

Selezionando da **P.A6** la tab `Storage Zone` è possibile consultare l'interfaccia di ricerca materiali nel magazzino.

#### DICHIARA

Il tasto **P2** `Dichiara` permette di dichiarare manualmente il quantitativo di produzione oppure il quantitativo di scarti. Tale funzionalità è disponibile solo sulle macchine in cui non è attivo un servizio di conteggio di produzione automatico e su quelle fasi in cui lo stato è *In Esecuzione.* La maschera di questa operazione è mostrata qui di seguito:

![img](image211.png)

Scegliendo in **P.E2** se si tratta di materiale prodotto o scartato, in **P.E1** si può anche inserire la quantità. In **P.E3** è contenuto l'elenco dei materiali richiesti insieme alla loro disponibilità, mentre in **P.E5** sono contenute le caratteristiche a essi associate. Nella fase di dichiarazione di produzione, qualora il quantitativo inserito - in **P.E1** - fosse superiore a quello dei materiali richiesti caricati, allora il dichiarato verrà corretto automaticamente alla massima produzione ammissibile. Per completezza in **P.E4** vengono mostrati gli UDM di appartenenza del materiale.

#### SETUP

Il tasto **P3** `setup` permette di mettere la fase in stato di `Setup`. Questa operazione è necessaria per procedere alla messa in lavorazione l'ordine. Nel caso fossero presenti più ordini in fase di setup, la sequenza di lavorazione è vincolata all'ordine visualizzato nella griglia. In questo status è possibile passare ai seguenti stati:

- Eseguibile (**P4**)
- In Esecuzione (**P5**)
- Termina (**P7**)

#### ESEGUIBILE

Il tasto **P4** permette di mettere la fase in stato di `Eseguibile`. In questo status è possibile passare ai seguenti stati:

- Setup (**P3**)
- Termina (**P7**)

#### AVVIA

Il tasto **P5** permette di mettere la fase in stato di `In Esecuzione`. In questo status è possibile passare ai seguenti stati:

- Pausa (**P6**)

#### PAUSA

Il tasto **P6** permette di mettere la fase in stato di *Pausa.* In questo status è possibile passare ai seguenti stati:

- Eseguibile (**P4**)
- In Esecuzione (**P5**)
- Termina (**P7**)

#### TERMINA

Il tasto **P7** permette di terminare la lavorazione e passare allo status di `Lavorato`

#### SEQUENZA

Il tasto **P8** permette di sequenziare le fasi lavorative. Tale funzionalità è stata descritta nei capitoli precedenti. In questo contesto essa si differenzia solo per il fatto che, considerato che essa svolge l'operazione da una maschera operatore, le funzionalità della gestione sono limitate alle sole fasi nei seguenti stati: Schedulato, Preparazione, Eseguibile. Questo avviene indipendentemente dai permessi attribuiti all'utente.

### TAB: PREPARAZIONE

La scheda di preparazione mostra un riepilogo di tutti i materiali che sono stati preparati in una zona di magazzino adiacente alla macchina: può essere utile sia per il carico sia per lo scarico. L'utilizzo di questa maschera è facoltativo, in quanto l'operatore potrebbe caricare direttamente il materiale in macchina passando dalla maschera nel tab `carico`. La maschera si presenta come nell'immagine sottostante e
offre le seguenti funzionalità:

![img](image212.png)

| | | | |
| - | - | - | - |
| **Pr2** | Carica in preparazione | **Pr3** | Escludi UDM impegnato |
| **Pr4** | Aggiorna | **Pr5** | Collaudo |
| **Pr6** | Prepara UDC | **Pr7** | Rettifica |
| **Pr8** | Trasferisci | **Pr9** | Trasferisci Qta |
| **Pr10** | Ristampa UDM | **Pr11** | Ristampa UDC |

> Funzioni attive solo su UDM non impegnati

#### CARICA IN PREPARAZIONE

Si può caricare manualmente del materiale in preparazione inserendo il relativo codice identificativo nel campo **Pr1** e poi cliccando sul tasto `Carica in preparazione`, che farà aprire la *form* di trasferimento materiale:

![img](trasferimento.png)

In questa maschera l'operatore può scegliere in quale gate **Pr.A1** trasferire i materiali e le quantità indicate in **Pr.A2**. Qualora venissero rilevate delle incongruenze tra il quantitativo indicato nell'UDM e l'effettiva quantità fisica dell'UDM stesso, allora contestualmente si può selezionare la voce `Rettifica quantità` in modo da apportare le rettifiche di giacenza. In fase di trasferimento materiale è anche possibile inserire dati aggiuntivi quali:

- la data del movimento (per default, è quella odierna) **Pr.A3**.
- causale di trasferimento **Pr.A4**.
- eventuali note **Pr.A5**.

Apponendo la spunta sulla voce **Pr.A6** `Stampa`, in fase di conferma viene avviata anche la stampa della nuova etichetta.

Eseguita questa procedura, nella griglia **Pr0** viene aggiunta una nuova riga. La nuova riga è facilmente identificabile in quanto "non impegnata", poiché non è stata assegnata a nessun ODL (la prima colonna della griglia non presenta il simbolo del lucchetto ![img](icon-lucchetto.png)).

#### ESCLUDI UDM IMPEGNATO

Impostando il check **Pr3** è possibile visualizzare nella griglia **Pr0** solo i materiali che non sono impegnati, ossia tutti quelli che non appartengono ad alcun ODL. Nella prima colonna non è presente il lucchetto ![img](icon-lucchetto.png).

#### AGGIORNA

Il tasto **Pr4** `Aggiorna` permette di aggiornare il contenuto della griglia **Pr0**.

#### COLLAUDO

Il tasto **Pr5** `Collaudo` permette l'esecuzione di un test qualitativo sul materiale preparato. Selezionare il materiale e pigiare il tasto **Pr5** `Collaudo` per aprire la seguente maschera:

![img](test-materiale.png)

Nel box **Pr.B1** si vedono tutti i dati inerenti il materiale prescelto, mentre la griglia **Pr.B2** mostra tutti i collaudi compatibili per i quali si possono eseguire i test. Tramite la selezione di un collado **Pr.B2**, e poi cliccando sul tasto **Pr.B3** `Carica collaudo selezionato`, si visualizza nel riquadro **Pr.B4** tutti i dati di cui il collaudo prescelto impone la compilazione. Una volta
eseguita la compilazione dei dati richiesti, cliccare sul tasto `OK` per validare e rendere effettivo il collado stesso.

#### PREPARA UDC

Il tasto **Pr6** permette di associare degli UDM a un UDC nuovo o già esistente, in modo da permettere la gestione della movimentazione simultanea degli UDM. Per eseguire questa operazione è necessario selezionare in **Pr0** il materiale e poi cliccare sul tasto **Pr6** `Prepara UDC` per mostrare la maschera, come da esempio sottostante.

![img](prepara-udc.png)

Ora è possibile eseguire 3 operazioni:

- Inserire l'UDM scelto in un UDC esistente
- Eliminare un UDM da un UDC
- Creare un nuovo UDC e inserire l'UDM scelto al suo interno

##### INSERIRE L'UDM SCELTO IN UN UDC ESISTENTE

Inserendo l'identificativo dell'UDC nel campo **Pr.C1**, e premendo il tasto INVIO dalla tastiera[^tastiera], la griglia **Pr.C5** mostrerà tutti gli UDM contenuti nell'UDC inserito. Poi, cliccando il tasto `Dettagli`, saranno visualizzate tutte le proprietà dell'UDC selezionato. Inserendo l'identificativo dell'UDM nel campo **Pr.C4** e premendo il tasto INVIO dalla tastiera[^tastiera], il sistema assocerà in automatico l'UDM all'UDC.

##### ELIMINARE UN UDM DA UN UDC

Inserendo l'identificativo dell'UDC nel campo **Pr.C1**, e premendo il tasto INVIO dalla tastiera[^tastiera], la griglia **Pr.C5** mostrerà tutti gli UDM contenuti nell'UDC inserito. Poi, inserendo nel campo **Pr.C4** un codice UDM presente nella lista **Pr.C5** e premendo il tasto INVIO dalla tastiera[^tastiera], la finestra mostrerà il tasto `Disassocia` che permette di rimuovere l'UDM dall'UDC.

##### CREARE UN NUOVO UDC E INSERIRE L'UDM SELEZIONATA AL SUO INTERNO

Per inserire un UDM dentro un Nuovo UDC, è necessario cliccare sul tasto **Pr.C2** `Crea UDC`, in modo da aprire una maschera che riporta il nuovo codice assegnato al nuovo UDC e tutte le caratteristiche. All'operatore è lasciata la possibilità d'inserire la descrizione.

![img](crea-udc.png)

Una volta che l'UDC è stato creato, si potrà inserire l'UDM nella modalità descritta nel paragrafo precedente (Inserire l'UDM scelto in un UDC esistente)

[^tastiera]: operazione non è necessaria in caso di utilizzo di barcode reader.*

#### RETTIFICA

Il tasto **Pr7** `rettifica` è attivo solo quando si seleziona un UDM che non è impegnato (non è presente il simbolo ![img](icon-lucchetto.png)) in alcun ordine; questo permette di modificare la quantità di materiale **Pr.D1**
precedentemente associato e assegnare la causale **Pr.D2**. Qui di seguito è mostrata la maschera per eseguire quanto descritto.

![img](media/mfhmi/rettifica.png)

Nel campo **Pr.D1** `Rettifica Quantità`, inserire il nuovo quantitativo e poi cliccare su **Pr.D3** `Conferma` per validare e rendere attiva la modifica. Questa operazione è necessaria nel caso in cui si rilevino delle incongruenze tra il quantitativo indicato nell'UDM e l'effettiva quantità fisica dell'UDM stesso.

#### TRASFERISCI

Il tasto **Pr8** `Trasferisci` è attivo solo quando viene selezionato un UDM che non è impegnato in alcun ordine (non è presente il simbolo ![img](icon-lucchetto.png)). Esso permette di spostare l'intero quantitativo di un UDM a magazzino. Durante tale operazione è possibile apportare delle rettifiche di giacenza per rettificare eventuali incongruenze tra il quantitativo indicato nell'UDM e l'effettiva quantità fisica dell'UDM stesso. Per eseguire questo spostamento, selezionare l'UDM dalla lista **Pr0**, poi cliccare sul tasto **Pr8** `Trasferisci`, che farà aprire la maschera (sotto mostrata a titolo di esempio).

![img](media/mfhmi/trasferisci.png)

Selezionare dalla lista **Pr.E1** il magazzino su cui trasferire la quantità di materiale indicata nel box **Pr.E2**. Cliccare su `conferma` per validare e rendere effettivo il trasferimento.

#### TRASFERISCI QTA

Il tasto **Pr9** `Trasferisci Qta` permette di trasferire una parte o l'intero UDM in uno nuovo o già esistente. Tale procedura è stata descritta nel paragrafo [Preparazione di un UDM](#trasferisci-qta).

#### RISTAMPA UDM

Il tasto **Pr10** `Ristampa UDM` permette di ristampare l'etichetta dell'UDM selezionato.

#### RISTAMPA UDC

Il tasto **Pr11** `Ristampa UDC` permette di ristampare l'etichetta dell'UDC dell'UDM selezionato.

### TAB: CARICO

Ecco come appare la maschera della scheda `CARICO`.

![img](carico.png)

La griglia **C1** contiene tutti gli UDM che sono in corso di lavoro nel momento corrente, mentre la griglia **C2** contiene tutti gli UDM caricati in macchina, pronti per essere utilizzati nelle varie lavorazioni.

#### CARICA UDM

Il tasto **C0** `Carica` permette di caricare in macchina l'UDM indicato nel campo **C10**. A operazione terminata, la griglia mostrerà una nuova riga **C2**. Su tutti gli UDM presenti nella griglia **C2** è possibile eseguire le seguenti funzionalità:

#### CONSUMA

Il tasto **C5** `Consuma` permette di dichiarare manualmente il consumo di materiale. Quella sotto riportata è la maschera dove si effettua questa operazione.

![img](consuma.png)

In **C6.A1** è possibile inserire la data di rettifica (in automatico è configurata la data corrente) e poi inserire in **C6.A2** la quantità effettiva dell'UDM. Il sistema provvede in automatico a calcolare la differenza della quantità di materiale consumato. È inoltre possibile dichiarare il motivo della rettifica in **C6.A3**, scegliendo l'opzione tra quelle sotto riportate:

- Consumo: con relativa causale
- Scarto

Tale operazione non è fattibile se l'UDM non è stato mai consumato almeno una volta.

#### SCARICA

Il tasto **C6** `Scarica` permette di scaricare degli UDM a magazzino; se essi sono raggruppati in un UDC, allora viene scaricato l'intero UDC. Durante tale operazione è possibile apportare delle rettifiche alle eventuali incongruenze tra il quantitativo indicato nell'UDM e l'effettiva quantità fisica dell'UDM stesso. Per eseguire questo spostamento, selezionare l'UDM dalla lista **C2** e cliccare sul
tasto **C6** `Scarica`, che farà aprire la maschera (anche sotto riportata a titolo di esempio):

![img](scarica.png)

- **C6.A1** permette di selezionare dove verrà scaricato il materiale.
- **C6.A2** permette di selezionare la data di scarico.
- **C6.A3** permette di associare una causale allo scarico.
- **C6.A4** permette di scegliere se scaricare l'intera quantità o apportare una rettifica.
- **C6.A5** quando viene spuntata, questa funzione permette di eseguire la
stampa della nuova etichetta.

#### RENDI

Il tasto **C7** `Rendi` si comporta come il tasto **C6** `Scarica`, con la differenza che, quando un UDM appartiene a un UDC, allora esso viene disassociato dall'UDC stesso e il trasferimento avviene per il singolo UDM nei modi sottoelencati:

- Stessa UDM
- UDM originaria
- UDM Esistente
- Nuova UDM

La procedura è già stata descritta nel paragrafo PRODUZIONE – `Eliminare una preparazione`.

![img](rendi.png)

#### ATTIVA

Il tasto **C8** `Attiva` permette di attivare l'utilizzo di un materiale, esegue l'operazione contraria del tasto **C3** `Disattiva`.

#### COLLAUDO (UDM CARICATI)

Il tasto **C9** `Collaudo` permette di aprire la scheda di collaudo per il materiale selezionato in **C2**. La procedura di collaudo è descritta nel Capitolo Preparazione.

#### DISATTIVA

Il tasto **C3** `Disattiva` permette di disattivare l'utilizzo dell'UDM selezionato in **C1**. Questa operazione sposta l'UDM dalla griglia **C1** a **C2** permettendo di eseguire sull'UDM le operazioni di seguito descritte.

#### COLLAUDO (UDM IN LAVORAZIONE)

Il tasto **C4** `Collaudo` permette di aprire la scheda di collaudo per il materiale selezionato in **C1**. La procedura di collaudo è descritta nel Capitolo Preparazione.

### TAB: UDP

Il funzionamento della scheda UDP dipende dalla configurazione applicata in fase d'installazione del software. Si può scegliere se attribuire o no all'operatore la possibilità di suddividere un UDP (Presente nella griglia **U1**, e attiva solo in questo caso) in vari UDM; diversamente, il prodotto finito viene già assegnato a un nuovo UDM, che è generato in automatico.

![img](produzione-udp.png)

- **U1** elenco degli UDP in fase di WIP (Work In Progress) per i quali si può eseguire le seguenti funzionalità.
- **U2** elenco degli UDM sia `confermati` che `da confermare` per i quali è possibile eseguire le seguenti funzionalità.
- **U3** `Crea UDP` permette di creare degli UDM a partire dall'UDP selezionato (funzionalità descritta nel paragrafo [PRODUZIONE – Eliminare una preparazione](#eliminare-una-preparazione).)
- **U4** `Rettifica` Rettifica la quantità degli UDP presenti nella griglia, funzionalità descritta nel paragrafo [PREPARAZIONE – Rettifica](#rettifica).
- **U5** `Collaudi` permette di creare eseguire un collaudo sull'UDP selezionato, funzionalità descritta nel paragrafo [PREPARAZIONE – Collaudi](#collaudo) I collaudi eseguiti su questi UDP vengono ereditati da tutti gli UDM in seguito generati.
- **U6** Filtrare la visualizzazione ai solo `confermati` o `non confermati` o tutti.
- **U7** `Trasferisci` permette di trasferire l'intero UDM in magazzino, qualora  l'UDM fosse ![img](image228.png) *da confermare* dopo questa operazione diventa `confermato` (funzionalità descritta nel paragrafo [PREPARAZIONE - Preparazione di un UDM](#trasferisci)).
- **U8** `Rettifica` Rettifica la quantità degli UDM presenti nella griglia. Questa operazione determina anche la correzione della quantità prodotta sull'Ordine di lavoro (funzionalità descritta nel paragrafo [PREPARAZIONE – Rettifica](#rettifica)).
- **U9** `Trasferisci Qta` permette di trasferire una parte o l'intero UDM in uno nuovo o già esistente (funzionalità descritta nel paragrafo [PREPARAZIONE – Trasferisci Qta](#trasferisci-qta)).
- **U10** `Ristampa UDP` permette di ristampare l'etichetta di un UDP.
- **U11** `Prepara UDC` permette di preparare un UDC a partire dall'UDM selezionato (*funzionalità descritta nel paragrafo [PREPARAZIONE – Prepara UDC](#prepara-udc)).
- **U12** `Collaudo` permette di creare eseguire un collaudo sull'UDM selezionato (*funzionalità descritta nel paragrafo [PREPARAZIONE – Collaudi](#collaudo)).

### TAB: FERMI

In questa maschera è possibile vedere tutti i tempi di produzione della macchina in oggetto e modificarne la causale. Per modificare la causale, dopo aver selezionato una voce dalla griglia **T1**, cliccare sul tasto **T2** `Modifica causale`, che farà aprire la maschera riportante tutte le causali associabili al tempo macchina selezionato.

![img](produzione-fermi-modifica-causale.png)

Poi cliccare sulla causale prescelta e poi sul tasto `Conferma` per validare la variazione.

![img](produzione-fermi-scelta-nuova-causale.png)

Utilizzare i tasti ![img](pulsante-su.png) e ![img](pulsante-giu.png) del gruppo **T3** per allargare o restringere il range di ore dei tempi macchina visualizzati.

### TAB: UTENTI

In questa maschera sono presenti tutti gli utenti **U1** che sono autenticati sulla macchina selezionata. È possibile aggiungere degli operatori manualmente inserendo in **U2** il PIN *Personal Identification Number* dell'operatore e poi cliccando su **U3**. Per motivi di sicurezza in fase d'inserimento del PIN, la digitazione è
occultata.

![img](produzione-utenti.png)

Nel caso in cui si decidesse di disabilitare un operatore, dopo averlo selezionato da **U1** è necessario cliccare sul tasto `Disattiva` **U4**.

## MATERIALI RICHIESTI

| Icona | Funzionalità |
| :---- | :---- |
| ![img](icon-materiali-richiesti.png) | Permette di caricare i materiali richiesti nell'ordine sulle macchine. |

In questa interfaccia avviene la preparazione delle macchine, caricando i materiali richiesti nell'ordine **Mr11**. Essi si potranno scegliere tra le Udm disponibili nelle varie ubicazioni e verranno spostati nei magazzini di entrata o di preparazione delle corrispettive macchine.

![img](materiali-richiesti.png)

Le Udm che abbiamo nei vari magazzini vengono suddivise in sezioni, in base alla conformità con l'ordine e in quale ubicazione si trovano:

- **Mr6** `Udm caricabili` visualizza tutte le Udm, presenti nel magazzino di competenza, caricabili sulla macchina. Questi materiali potranno essere impegnati **Mr12** e quindi non potranno essere caricati, e successivamente si potrà rilasciare l'impegno **Mr13**.
- **Mr7** `Preparazione` sono presenti tutte le Udm che sono all'interno del magazzino di Preparazione.
- **Mr8** `Udm compatibili` Udm compatibili con il materiale o la fase di lavorazione dell'ordine.
- **Mr9** `Udm incompatibili` Udm non compatibili con il materiale o la fase di lavorazione dell'ordine.
- **Mr10** `Udm baia` Visualizza le Udm che sono già in carico sulla baia di ingresso della macchina.

### CARICA

Una volta che il codice dell'Udm è stato digitato manualmente **Mr1** o letto tramite barcode, cliccando sul pulsante carica **Mr2** si potrà trasferire il materiale all'interno delle ubicazioni di macchina.

![img](materiali-richiesti-carica.png)

### CARICA PARZIALE

Il tasto Carica parziale **Mr3** è praticamente identico al pulsante Carica **Mr2**, unica differenza è che al suo interno si può scegliere in che Udm trasferire il materiale.

![img](materiali-richiesti-carica-parziale.png)

### CARICA MULTIPLO

Il tasto Carica Multiplo **Mr4** ha la funzionalità di poter caricare più Udm alla volta.

![img](materiali-richiesta-trasferimento-multiplo.png)

### TRASFERIMENTO DA PREPARAZIONE

Con questa funzionalità **Mr5** si potrà effettuare il trasferimento delle Udm presenti all'interno del magazzino di Preparazione.

## ALLARMI

| Icona | Funzionalità |
| :---- | :---- |
| ![img](icon-allarmi.png) | Permette di visualizzare tutti gli allarmi e gli errori che vengono riscontrati durante la produzione. |

In questa sezione vengono riportate tutte le anomalie relative alle linee di produzione o alle singole macchine, in modo che si possa intervenire sul problema e, di conseguenza, verificarne le cause e arrivare ad una soluzione.

![img](allarmi.png)

Nella maschera degli allarmi troviamo una tabella **Al5** nella quale vengono riportate tutte le segnalazioni, le quali posso essere poi filtrate, cliccando il tasto Filtra **Al3**, rispettivamente per data **Al1**, aggiungendo dei parametri **Al3** oppure specificando il Livello di Allarme **Al4:**

![img](allarmi-livelli.png)

La maschera degli errori è pressoché identica a quella degli allarmi, cambiano solo i campi filtrabili di seguito riportati:

![img](allarmi-filtri.png)

## MAPPA REPARTO

| Icona | Funzionalità |
| :---- | :---- |
| ![img](icon-mappa-reparto.png) | Permette di creare delle mappe di reparto interattive. |

Nell'interfaccia `Mappe di reparto` è possibile creare delle mappe interattive per consultare lo status delle macchine. La visualizzazione della mappa è legata alla scelta effettuata sull'albero nodi dello stabilimento. Per ogni nodo è possibile avere una o più mappe. Di seguito è riportato un esempio di mappa:

![img](mappa-reparto.png)

**M1** è l'area in cui è visualizzata la mappa interattiva. La mappa mostra dei riquadri colorati riportanti i nomi delle macchine in essa presenti. Quando un riquadro viene cliccato, esso mostra i dati (nel riquadro **M2**) relativi alla macchina a esso associati. La colorazione di ogni singolo riquadro varia a seconda dello status della macchina e può avere le seguenti colorazioni:

| Colore | Stato |
| :----- | :----------- |
| <span style="background-color:#92D050;display:block;">&nbsp;</span> | In produzione |
| <span style="background-color:#FF0000;display:block;">&nbsp;</span> | Ferma |
| <span style="background-color:#FFFF00;display:block;">&nbsp;</span> | In fase di setup |
| <span style="background-color:#A6A6A6;display:block;">&nbsp;</span> | Inattiva |

Il riquadro **M2** è composto da due tabs.

Tramite un grafico a torta ![img](icon-linea.png) è possibile visionare la situazione di tutte le macchine presenti nella mappa:

![img](mappa-reparto-grafico-torta.png)

![img](icon-macchina.png) per visionare tutti i dati inerenti alla macchina selezionata.

![img](mappa-reparto-tabella-riepilogo.png)

- I tasti **M3** e **M4** permettono di zoomare il sinottico avanti e indietro; mentre il tasto **M5** abilita la funzione "PAN", ossia trasforma il cursore dell'applicazione in una mano. Il PAN permette di muovere l'immagine, in particolare quando essa viene zoomata. Tutte le modifiche visive apportate tramite i tasti **M3**, **M4** ed **M5** sono ripristinabili tramite il tasto **M6**. È possibile associare uno o più sinottici a ogni macchina; l'elenco delle viste disponibili è presente nel menu a tendina tasti **M7**. Tramite i tasti **M8**, **M9** e **M10** è possibile:

- ![img](icon-nuovo-sinottico.png) **M8** creare un nuovo sinottico.

- ![img](icon-elimina-sinottico.png) **M9** eliminare un sinottico presente nella lista **M7**.

- ![img](icon-modifica-sinottico.png) **M10** modificare un sinottico esistente presente nella lista **M7**.

### CREARE UN NUOVO SINOTTICO

Ecco un esempio guida che mostra come creare un sinottico e associarlo ai macchinari desiderati.

#### ESEMPIO DI CREAZIONE DI UN SINOTTICO

Si desidera ottenere come risultato finale il seguente sinottico

![img](mappa-reparto-immagine-risultato.png)

> [!Note]
> L'immagine rappresentante la nostra linea, sezione o reparto su cui andare a disegnare è il prerequisito fondamentale di questo esempio. Nota: l'immagine nell'esempio sarà da ora in avanti denominata **IMMBKG**:

![img](mappa-reparto-immagine-sfondo.jpeg)

Ora che si ha l'immagine a disposizione si proceda a creare il sinottico.

1. Selezionare la macchina cui sarà associato il sinottico dall'albero nodi
2. ![img](mappa-reparto-selezione-macchina.png)
3. Cliccare sul tasto ![img](icon-nuovo-sinottico.png) **M8** per creare un nuovo sinottico
4. Assegnare un nome alla nuova vista (es: Sin01)
  ![img](image257.png)
5. Ora si ha a disposizione un ambiente di sviluppo nel quale è possibile "disegnare" il sinottico

#### AMBIENTE DI SVILUPPO SINOTTICI

L'ambiente di sviluppo dei sinottici è il seguente:

![img](mappa-reparto-ambiente-di-sviluppo.png)

- **S1** È l'area in cui è possibile disegnare il sinottico
- **S2** Pannello delle proprietà degli elementi selezionati in **S1**. In mancanza di elementi, si utilizzino le proprietà dello stesso **S1**
- **S3** Permette d'importare le macchine nel sinottico (in seguito
maggiormente descritto)
- **S4** Permette d'inserire delle immagini nel sinottico.

Ora inseriremo l'immagine del nostro reparto (IMMBKG), che imposteremo come immagine di sfondo della nostra vista. Questa scelta ci offre l'opportunità di vedere come si applicano degli oggetti (esempio: linee, macchine ecc).

- Cliccare su **S1** per indicare a **S2** qual è l'oggetto per il quale si desidera visualizzare le proprietà.
- Cliccare sulla voce **Background🡪BackGroundImage** e selezionare l'immagine IMMBKG dal proprio pc

Se l'immagine dovesse risultare più grande rispetto al sinottico, allora potremmo agire sul parametro `BackgroundImageLayout` che mette a disposizione 5 modi diversi di visualizzare l'immagine - e selezionare `Stretch`,  che permette all'immagine di adeguarsi alla grandezza del sinottico. In alternativa, si può variare le dimensioni del sinottico stesso agendo sulla proprietà `DocumentSize`.

Il risultato ottenuto è il seguente:

![img](mappa-reparto-ambiente-sviluppo-sfondo.jpg)

Ora creiamo delle linee di delimitazione della macchina:

1. Cliccare con il tasto destro del mouse nel sinottico: sul menu che apparirà cliccare su `Shape` 🡪 `Polyline`. Questa operazione permette di disegnare una serie di righe congiunte a vostro piacimento
  ![img](mappa-reparto-ambiente-sviluppo-crea-polilinea.png)
2. Cliccare con il tasto sinistro nel punto in cui si desidera che parta la *polilinea* **V1**, poi eseguire un clic per ogni vertice (**V2**, **V3**) che si desidera creare. Per terminare la creazione della `polilinea` cliccare con il tasto destro del mouse sull'ultimo vertice **V4**.
  ![img](mappa-reparto-ambiente-sviluppo-applicazione-polilinea.png)
3. Ora desideriamo cambiare colore, formato e spessore della linea appena creata. Clicchiamo sopra la linea per selezionarla; poi, nel pannello delle sue proprietà, agiamo sui seguenti parametri:
   1. `Aspetto` 🡪 `LineStyle` 🡪 `LineColor`: scegliere il colore desiderato, ad esempio ciano.
   2. `Aspetto` 🡪 `LineStyle` 🡪 `DashStyle`: DashDot
   3. `Aspetto` 🡪 `LineStyle` 🡪 `LineWidth`: 3

Il risultato ottenuto sarà il seguente:

![img](mappa-reparto-ambiente-sviluppo-polilinea-con-stili.png)

In questo modo, replicando l'operazione su tutto il disegno, otteniamo quanto segue:

![img](mappa-reparto-ambiente-sviluppo-polilinee-con-stili.png)

A questo punto possiamo procedere con l'inserimento delle macchine. Cliccare sul tasto **S3** ![img](icon-mappa-reparto-scelta-macchine.png) per fare aprire il seguente elenco:

![img](mappa-reparto-ambiente-sviluppo-scelta-macchine.png)

Questo è l'elenco di tutte le macchine disponibili a essere importate nel sinottico. Per importarne una, eseguire doppio click sul nome. Questa operazione rende disponibile nel sinottico un rettangolo interattivo che rappresenta la macchina prescelta.

![img](mappa-reparto-ambiente-sviluppo-riquadro-macchina.png)

Ciò che si desidera ottenere è il seguente effetto grafico:

![img](mappa-reparto-ambiente-sviluppo-stile-riquadro-macchina.png) 🡪 ![alt text](mappa-reparto-ambiente-sviluppo-stile-finale-riquadro-macchina.png)

Cliccare una volta sul rettangolo per selezionarlo (una volta selezionato il bordo diventa di colore verde) così da agire sulle sue proprietà GENERALI, dove si potranno cambiare sia il font che la descrizione interna.

1. `Varie` 🡪 `LabelFont` 🡪 `Bold`: true
2. `Varie` 🡪 `LabelFont` 🡪 `Size`: 15
   Cliccando la seconda volta sul quadrato è possibile andare a modificare le proprietà grafiche del rettangolo stesso
3. `Aspetto` 🡪 `ShadowStyle`: cliccare su …
   ![img](proprietà-shadowstyle.png)
   Nella maschera che si è attivata potremmo applicare un'ombra prospettica al quadrato della macchina, e anche decidere i colori da applicare.
   ![img](stili-proprietà-shadowstyle.png)
   Tramite i tasti **C2** e **C3** possiamo selezionare i colori dell'ombra, creando un effetto *shadow*, ossia la sfumatura dell'ombra che parte da un colore e termina con un altro. Applicando la spunta su **C5** possiamo vedere il risultato in **C1**, in tempo reale. Tramite i tasti **C4** e **C5** possiamo eseguire un `offset` dell'ombra.
4. `Bounds` 🡪 `Size` 🡪 `Height`: 50
5. `Bounds` 🡪 `Size` 🡪 `Width`: 120

Il risultato ottenuto è il seguente:

![img](mappa-reparto-risultato-macchina.png)

> [!Note]
> Il colore dello sfondo non è applicabile dall'utente, in quanto varia a seconda dello stato della macchina.**

|     | In produzione    |
|-----|------------------|
|     | Ferma            |
|     | In fase di setup |
|     | Inattiva         |

| Colore | Stato |
| :----- | :----------- |
| <span style="background-color:#92D050;display:block;">&nbsp;</span> | In produzione |
| <span style="background-color:#FF0000;display:block;">&nbsp;</span> | Ferma |
| <span style="background-color:#FFFF00;display:block;">&nbsp;</span> | In fase di setup |
| <span style="background-color:#A6A6A6;display:block;">&nbsp;</span> | Inattiva |

Replicando le operazioni appena descritte per tutte le macchine presenti nell'immagine, il risultato ottenuto è il seguente:

![img](mappa-reparto-risultato-finale.png)

Ora, come ultimo passaggio, possiamo creare delle righe che collegano le macchine con le zone in cui esse sono ubicate.

Cliccando con il tasto destro sul sinottico, selezionare dal menu contestuale la voce `Shapes` 🡪 `Line`

![img](mappa-reparto-ambiente-sviluppo-nuova-linea.png)

Disegnare una linea (come descritto in precedenza per la `polilinea`) che colleghi il quadrato della macchina con la sua zona, in modo da ottenere il seguente risultato:

![img](mappa-reparto-ambiente-sviluppo-crea-linee-collegamento.png)

Replicando la procedura appena descritta per tutte le macchine, il risultato ottenuto sarà il seguente:

![img](mappa-reparto-ambiente-sviluppo-linee-collegamento-risultato.png)

Cliccare sul tasto ![img](icon-modifica-sinottico.png) **M10** per salvare il lavoro appena eseguito.

Ora il sinottico è pronto per essere utilizzato.
