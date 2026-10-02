# CONTENITORE PRINCIPALE

Nel contenitore principale della home page vengono visualizzate tutte le macchine di cui l'utente loggato è stato autorizzato alla gestione.

La gestione degli utenti (con relative autorizzazioni) è accessibile esclusivamente attraverso l'applicazione *MASTER Factory®* versione Desktop; perciò, si rimanda alla sezione `GESTIONE UTENTI/GRUPPI` -> `TAB.UTENTI` -> `ASSEGNAZIONE AUTORIZZAZIONI` del manuale MasterFactory Desktop.

Esempio di setting autorizzazioni per utente, su applicazione Desktop:
](./media/c
![img](client-hmi-lista-utenti.png))

## MAC](./media/iNA

![img](image21.png))

| 1  | Nome della macchina  | 6 | Dichiarazione produzione |
| :--: | ---- | ---- | ---- |
| 2  | Operatori | 7  | Causale relativa allo stato attuale della macchina e durata dello stato corrente |
| 3  | Materiali | 8  | Codice ODL in esecuzione / codice fase |
| 4  | Test | 9  | Categoria materiale e descrizione articolo in produzione |
| 5 | Allarmi attivi sulla macchina  | 10 | `completamento pezzi` Q.ta da produrre/q.ta prodotta |

> [!Note]
> I tasti 2,3,4,5 possono assumere colorazioni diverse in base al livello di segnalazione da mostrare all'utente. Le colorazioni previste sono le seguenti:
>
> - GRIGIO: tasto non attivo, nessuna azione richiesta da parte dell'utente;
> - ROSSO: azione necessaria da parte dell'utente, cliccando sul tasto e compilando i dati richiesti sulla maschera visualizzata;
> - VERDE: nessuna azione richiesta da parte dell'utente. È tuttavia possibile navigare sulla pagina collegata al tasto.

### DETTAGLIO MACCHINA
](./media/d
Facend](./media/doppio click sopra l'area di colore bianco (zona campi 8,9,10 della figura precedente), all'interno di una cella identificativa di una macchina, verrà visualizzata una pagina contenente il dettaglio della macchina selezionata.

![img](dettaglio-macchina.png))

![img](dettaglio-operazioni.png))
](./media/d
Le aree cliccabili all'interno della pagina sono le seguenti:

#### DETTAGLIO CAUSALE

![img](dettaglio-macchina-gantt-giornaliero.png))

Dettaglio del Gantt giornaliero relativo alle causali macchina.

##### ORDINE/FASE

Codice](./media/dL/numero fase in esecuzione. Il tasto evidenziato dal riquadro `2`, consente di visualizzare un documento descrittivo della fase corrente.

##### DICHIARAZIONE PRODUZIONE

In questa sezione è possibile dichiarare la quantità prodotta dell'articolo in produzione, specificando nel campo Quantità un valore e cliccando quindi Conferma.

![img]](./media/dchiarazione-produzione.png))

##### QUANTITA' SOVRAPPRODUZIONE

Cliccando sul tasto `4`, apparirà una maschera in cui poter inserire la quantità di pezzi prodotti in sov](./media/iroduzione (cioè la quantità prodotta in più, rispetto a quella richiesta nell'ordine di produzione attivo). Per confermare l'inserimento della quantità specificata](./media/iiccare il tasto 'Invio' della tastiera o il tasto 'Accetta' sulla virtual keyboard
(se ab](./media/stata).

![img](dichiarazione-sovraproduzione.png))

##### QUANTITA' SCARTATA

Questa pagina mostra l'elenco degli scarti inseriti per la macchina selezionata. Cliccando sul tasto![img](icon-aggiungi.png)){style="height:1.4em"} è possibile inserire nuovi scarti, specificando sulla nuova maschera la quantità scartata e quindi cliccando il tasto![img](icon-conferma-scarto.png)){style="height:1.4em"} per confermare l'inserimento dello scarto.

![img](scarti.png))
](./media/t
##### ](./media/tUMENTO ARTICOLO

Il tasto evidenziato consente di visualizzare un documento descrittivo dell'articolo in produzione.

##### TEST MACCHINA
](./media/p
Elenco dei test di qualità eseguiti. Con un doppio click sopra alla riga relativa ad un test è possibile modificare i valori del test.

![img](test-dettaglio.png))

![img]](./media/lst.png))
](./media/l
##### PROPRIETA'

Lista delle proprietà (con valori, se presenti) associate al processo in esecuzione.

![img](proprieta-processo.png))

##### LISTA FASI

In questa sezione vengono visualizzate le fasi attivabili sulla macchina corrente (nel caso non ci sia una fase in esecuzione) oppure la fase correntemente in esecuzione:

![img](lista-fasi.png))

![img](lista-fasi-run.png](./media/i
](./media/d
Ciascuna cella ordine/fase può assumere i seguenti stati:

|     | Eseguibile     |
|-----|----------------|
|     ](./media/causa          |
|     | Setup          |
|     | Scarico        |
|     | Preparazione   |
|     | In Esecuzione  |
|     | Lavorato       |

Clicca](./media/c sull'icona![img](icon-conferma-scarto.png))verrà visualizzata una pagina con le informazioni di dettaglio sulla fase.
](./media/c
![img](dettaglio-fase-non-in-run.png))

##### CAMBIO STATO

Masche](./media/mattraverso la quale è possibile modificare lo stato della fase.

![img](cambio-stato.png))

Per confermare il cambio stato occorrerà successivamente inserire la password o il codice PIN dell'utente (quest'ultimo composto dalla concatenazione del codice utente e password).
](./media/m
##### SETUP

Questo tasto consente di impostare la fase selezionata in stato di setup e al contrario, di terminarla.
](./media/d
![img](cambio-stato-avvio-setup.png))

![img](cambio-stato-termina-setup.png))

##### ](./media/uTO ORDINE

In questa pagina viene visualizzato lo stato di tutti gli ordini di produzione attivi sulla macchina corrente.
](./media/u
![img](macchina-stato-ordini-attivi.png))

##### ](./media/mRATORI

Mediante questa pagina è possib](./media/i dichiarare quale operatore sta utilizzando la macchina.

![img](macchina-operatori.png))

La griglia `1` mostra i requirements sugli operatori richiesti dalla macchina (nell'esempio è richiesto che un operatore sia associato alla macchina). Nel caso nessun operatore fosse associato alla macchina, apparirebbe un allarme indicante la mancanza di personale sulla
macchina.

![img]](./media/mshboard-macchina-assenza-operatori.png))

Per associare un operatore alla macchina occorre inserire nella barra di ricerca `2` il codice utente e quindi cliccare sul tasto `Conferma`. Quindi nella griglia `3` verranno visualizzati i dati dell'operatore associato alla macchina. Cliccando il tasto `4` apparirà una maschera tramite cui è possibile disattivare l'operatore corrente.
](./media/p
##### ](./media/dNSILI

![img](utensili.png))

Questa pagina consente il caricamento degli utensili in macchina.

![img](utensili-inserimento.png))](./media/i
](./media/c
Per caricare un utensile è necessario inserire il codice UDM nella barra di ricerca evidenziata nell'immagine precedente e cliccare quindi sul tasto `Car](./media/i`. E' possibile visualizzare gli UDM eventualmente disponibili in baia o in preparazione cliccando sui tasti `UDM baia` e `UDM preparazione` (il numero presente all'interno delle parentesi `[` `]` indica la quantità di UDM disponibili).
](./media/p
![img]](./media/dcchina-carico-udm.png))
](./media/i
Clicca](./media/p quindi sul tasto![img](icon-conferma-scarto.png)){style="height:1.4em"} apparirà una maschera mediante la quale sarà possibile visualizzare le proprietà dell'UDM selezionato o eseguire una serie di operazioni sull'UDM selezionato, che verranno approfondite nel paragrafo successivo.

##### MATERIALE](./media/i
](./media/t
Le funzionalità offerte da questa pagina consentono la gestione dei materiali per la macchina selezionata.

All'interno della griglia `1` sono elencati i materiali (con relative quantità e livelli di qualità) richiesti dall'ordine in lavorazione, mentre nella griglia `3` è presente l'elenco dei materiali attualmente presenti in macchina. Se le quantità di materiali presenti nella griglia `3` non sono coerenti con quelle mostrate in griglia `1`, la macchina si troverà in stato di allarme – no materials.

![img](macchina-carico-materiali.png))

Per ogni materiale presente all'interno delle griglie è possibile visualizzare le proprietà ad esso collegate, utilizzando il pulsante `Proprietà`:

![img](popup-operazioni-materiali-proprieta.png))

![img]](./media/mttaglio-proprieta-materiale.png))

Il tasto `Preparazione` serv](./media/i caricare i materiali richiesti all'interno degli ordini di produzione inerenti alla macchina.
](./media/m
Il caricamento di un UDM può essere fatto in due modi:

1. INSERIMENTO MANUALE CODICE UDM: inserire nella barra di ricerca `2` il codice UDM che si vuole caricare in macchina e cliccare quindi il tasto `Carica`. A questo punto si verrà ridirezionati in una pagina dedicata al trasferimento di materiale di magazzino, in cui occorrerà scegliere la macchina su cui trasferire il materiale (unica scelta possibile), facendo doppio click sul tasto![img](icon-conferma-scarto.png)){style="height:1.4em"}.
 ![img](caricamento-udm.png))
2. SELEZIONE MATERIALE RICHIESTO DA GRIGLIA MATERIALI RICHIESTI: selezionare il materiale richiesto sulla griglia `1` facendo doppio click sul tasto![img](icon-conferma-scarto.png)){style="height:1.4em"}. Quindi nella maschera apparsa a video cliccare `Magazzino`, per visualizzare gli UDM del materiale selezionato, presenti a magazzino.
![img](popup-operazioni-materiali-magazzino.png))
 ![img](dettaglio-udm-magazz](./media/i.png))
  Clic](./media/me quindi sul tasto![img](icon-conf](./media/ma.png)), dopodiché apparirà a video la seguente maschera.
 ![img](popup-udm-carico.png))
  Le operazioni possibili sono:
   - TRASFERISCI: il controllo viene ridirezionato sulla pagina dedicata al trasferimento di materiale di magazzino. Facendo doppio click sul tasto![img](icon-conferma-scarto.png)){style="height:1.4em"} nella riga relativa al codice macchina su cui si vuole trasferire il materiale, sarà completato il trasferimento.
 ![img](trasferimento-udm.png))
   - IMPEGNA: il materiale viene impegnato (perciò non sarà possibileutilizzarlo per altri ordini), ma ancora non risulta trasferito sulla macchina. Riaprendo la maschera sarà possibile rilasciare l'impegno di materiale;
   - RISTAMPA UDP: ristampa etichetta identificativa UDP.

##### PRODUZIONE

Questa pagina contiene le informazioni di produzione relative alla macchina selezionata.

La griglia `1` contiene l'elenco degli articoli da produrre, con relative informazioni in merito alla quantità richiesta, quantità prodotta, quantità scartata, eventuale codice UDP, unità di misura e livello di qualità richiesta.

La griglia `2` invece rappresenta la lista di tutti gli UDM prodotti, integrata con le informazioni del codice del lotto, codice UDM, quantità prodotta, unità di misura, livello di qualità e data produzione.

![img](macchina-produzione.png))

Facendo click sul tasto![img](icon-conferma-scarto.png)){style="height:1.4em"} di uno degli articoli presenti all'interno della `griglia 1`, appariranno i seguenti pulsanti:

![img](materiale-produzione-pulsanti.png))

- `Riprendi Udp`: Ricarica l'Udp con le Udm già precedentemente utilizzate all'interno della macchina.
- `Proprietà`: Vengono visualizzate tutte le proprietà relative all'articolo.
- `Magazzino`: Visualizza gli articoli all'interno del magazzino.
- `Documento`: Mette a disposizione una schermata per allegare/visualizzare un documento inerente all'articolo.

Facendo click sul tasto![img](icon-conferma-scarto.png)){style="height:1.4em"} di uno degli articoli presenti all'interno della `griglia 2`, appariranno i seguenti pulsanti:

![img](macchina-udm-pulsanti-1-2.png)![img](macchina-udm-pulsanti-2-2.png))

- `Proprietà`: Vengono visualizzate tutte le proprietà relative all'articolo.
- `Test`: Visualizza i test collegati all'Udm selezionata.
- `Ristampa UDP`: Ristampa l'etichetta dell'UDP.
- `Conferma`: Toglie l'impegno dall'Udm.
- `SpiltSL`: Esegue lo split dell'articolo in una nuova Udm.
- `Rettifica`: Rettifica la quantità dell'Udm.
- `Trasferisci`: Trasferisce l'Udm all'interno di un'altra ubicazione.
