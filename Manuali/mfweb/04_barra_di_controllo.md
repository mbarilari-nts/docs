# BARRA DI CONTROLLO
](./media/b
![img](barra-di-controllo.png))

La barra di controllo di *MASTER Factory®* è caratterizzata dalle aree di seguito descritte:

| 1   | Menù                              |
|:---:|-----------------------------------|
| 2   | Home page                         |
| 3   | Notifiche                         |
| 4   | Nome utente correntemente loggato |
|  5  | Allarmi in esecuzione             |

## MEN](./media/m

![img](menu.png))

Seguendo l'ordine dall'alto verso il basso delle voci del menu, le funzionalità offerte sono le seguenti:

### INFORMAZIONI CONFIGURAZIONE ISTANZA MF40
](./media/m
'Corso NTS Manufacturing' rappresenta nell'esempio dell'immagine precedente il **TenantID**, che di fatto identifica il nome dell'istanza di *MASTER Factory®* in esecuzione. Cliccando sopra questa voce del menù verrà visualizzata (in sola lettura) una pagina contenente tutti i parametri di configurazione dell'istanza corrente di MF40.

![img](menu-corso.png))

### MACCHINE

Cliccando su questo elemento, si verrà ridirezionati sulla pagina di visualizzazione delle macchine.

### TE](./media/t MACCHINA
](./media/t
Pagina contenente il Gantt giornaliero (con eventuali causali) di tutte le macchine. Cliccando sopra di una casella rappresentante un orario, verranno elencati tutti gli eventi (con relative causali) verificatisi all'interno dell'ora selezionata.

![img](tempi-macchina.png))

![img]](./media/empi-macchina-causali.png))

### PERSONALE PRESENTE

Elenco del personale loggato al sistema
](./media/m
![img](elenco-personale.png))
](./media/f
### MA](./media/pZINO

Vista sull'intero contenuto dei magazzini:
](./media/p
![img](magazzini.png))
](./media/f](./media/m
Cliccando sul tasto![img](freccia-dx.png)) apparirà la seguente maschera per la gestione dell'UDM selezionata:](./media/f](./media/m
](./media/f
![img](popup-operazioni-udm.png))

- `PROPRIETA'`: Elenco delle proprietà, con relativo valore ed unità di misura (se valorizzati)
 ![img](proprieta-udm.png))
- `RIS](./media/tPA UDP`: Viene ristampata l'etichetta relativa all'UDP corrente
- `TRASFERISCI` :Pagina attraverso cui è possibile trasferire un UDM in un magazzino, raggiungibile attraverso una delle rotte definite nella pagina ROTTE DI MAGAZZINO dell'applicazione *MASTER Factory®* (versione Desktop), per cui si rimanda al manuale dedicato. Per trasferire l'UDM sul magazzino desiderato, è sufficiente cliccare sul tasto![img](freccia-dx.png)) all'interno della riga relativa all'UDM.![img](media/mfweb/trasferisci.png)))))
- `RETTIFICA`: Lo scopo di questa pagina è quello di consentire all'utente di rettificare la quantità di materiale (riferita alla relativa unità di misura) all'interno di un UDM. È sufficiente specificare la nuova quantità e quindi cliccare sul tasto![img](freccia-dx.png)).![img](media/mfweb/rettifica.png)))))
- `SPLITSL`: Mediante questa pagina è possibile suddividere un UDM in due UDM più piccoli, specificando nel campo 'Quantità' la quantità di materiale da allocare sul secondo UDM e quindi cliccando sul tasto![img](freccia-dx.png)). Ad esempio, ipotizzando di avere un UDM con Quantità iniziale 50 KG, specificando 10 KG come quantità di 'Split', verrà creato un nuovo UDM con 10 KG di materiale. mentre l'UDM originario si ritroverà 40 KG come 'Quantità'.

### TE](./media/v

Elenco di tutti i test eseguiti sui materiali e sulle macchine.

![img](test.png))

### VIRTUAL KEYBOARD

Attivando la checkbox 'Virtual Keyboard', ogni volta che l'applicazione richiederà l'inserimento di un testo da parte dell'utente, apparirà a video una tastiera virtuale.

![img](virtual-keyboard.png))
