# APPENDICE PROPRIETÀ

Quest'appendice ha lo scopo di illustrare tutte le proprietà macchine, materiali e  di processo richieste obbligatoriamente dal sistema.

## PROPRIETA' MACCHINE

### ChangeReasonMode

`EqClassProp.ChangeReasonMode`

- Tipo: int
- Descrizione:
  - 0 = Permette la modifica della causale tra quelle associate alla classe delle macchine e che sono coerenti con quella in corso;
  - 1 = Permette la modifica della causale tra tutte quelle ammesse sulla categoria

### CustomScheduleGroupMode

`EqClassProp.CustomScheduleGroupMode`

- Tipo: int
- Descrizione:
  - 0 = Disabilita questa modalità;
  - 1 = La macchina lavora con gli ordini raggruppati e i tempi vengono suddivisi per gli ordini appartenenti al gruppo.

### CHECKCAPACITY

`EqClassProp.CHECKCAPACITY`

- Tipo: boolean
- Descrizione:
  - 1=Controlla la quantità massima
  - 0=No

### DEFAULTPRINTER

`EqClassProp.DEFAULTPRINTER`

- Tipo: string
- Descrizione: Nome Stampante di default utilizzata per la stampa etichette

### LoadMatMode

`EqClassProp.LoadMatMode`

- Tipo: int
- Descrizione:
  - 0 = Viene eseguito solo il carico della fase successiva, senza che venga messa in RUN;
  - 1 = Se viene letta l'etichetta del produced della fase precedente, la fase successiva viene caricata e messa in RUN.

### OpMode

`EqClassProp.OpMode`

- Tipo: int
- Descrizione:
  - 0 = Senza TEST (carico, consumi e versamento unitario) con i TEST (carico unitario, produzione, consumo e distruzione automatica dopo il TEST);
  - 1 = Versa in OUT in acconto con lucchetto nel sublotto già presente in stato TEST (nel magazzino definito nelle rotte UNLOAD) e viene chiuso e trasferito alla conferma/trasferimento;
  - 2 = Versa in OUT in acconto con lucchetto ma in stato WIP (nel magazzino definito nelle rotte) e la conferma lo spostamento e diventa TEST;
  - 3 = Ogni versamento è un sublotto senza lucchetto e stampa etichetta;
  - 4 = Mantiene lo stesso lotto e quantità del carico.

### QUALITA'

`EqClassProp.QUALITA`

- Tipo: string
- Descrizione: Valore della qualità di default prodotta da un Ordine di lavoro

### PartProgramID

`EqClassProp.PartProgramID`

- Tipo: string
- Descrizione: Part program legato alla macchina
  
### PLCWEBPATTERN

`EqClassProp.PLCWEBPATTERN`

- Tipo: string
- Descrizione: pagina web attraverso la quale è possibile accedere a dati generati dal Plc della macchina.

### ReasonEnd

`EqClassProp.ReasonEnd`

- Tipo: string
- Descrizione: Contiene la causale di default per lo stato macchina "fine"

### ReasonMicroStop

`EqClassProp.ReasonMicroStop`

- Tipo: string
- Descrizione: Contiene la causale di default per lo
stato macchina "micro stop"

### ReasonNoProd

`EqClassProp.ReasonNoProd`

- Tipo: string
- Descrizione: Contiene la causale di default per lo stato "macchina ferma"

### ReasonProd

`EqClassProp.ReasonProd`

- Tipo: string
- Descrizione: Contiene la causale di default per lo stato macchina "in produzione"

### ReasonSetup

`EqClassProp.ReasonSetup`

- Tipo: string
- Descrizione: Contiene la causale di default per lo stato macchina "in setup"

### ReasonOff

`ReasonOff`

- Tipo: string
- Descrizione: Contiene la causale di default per lo stato macchina "offline"

### TmFiltroCnt

`EqClassProp.TmFiltroCnt`

- Tipo: int
- Descrizione: Tempo latenza della macchina (quando fornisce i dati)

### TmOrderMissing

`EqClassProp.TmOrderMissing`

- Tipo: int
- Descrizione: Tempo che intercorre tra la fine di un ordine e l'inizio del successivo

### TmWithoutMat

`EqClassProp.TmWithoutMat`

- Tipo: int
- Descrizione: Tempo massimo ammesso di mancanza materiali, superato il quale l'operatore deve giustificarlo

### UdpLabelPrintMode

`EqClassProp.UdpLabelPrintMode`

- Tipo: int
- Descrizione:
  - 0 = Stampa etichetta in fase di dichiarazione o conferma UDP
  - 1 = Stampa etichetta alla creazione dell'UDP.

### UnloadMatMode

`EqClassProp.UnloadMatMode`

- Tipo: int
- Descrizione
  - 0 = Modalità disattivata.
  - 1 = Il prodotto finito viene automaticamente trasferito al magazzino descritto dalla rotta (**se è stata definita solo una rotta**).

## PROPRIETA' MATERIALI

### AltQty

`MatClassProp.AltQty`

- Tipo: float
- Descrizione: Durata di un utensile (dipende dall'unità di misura specificata nella proprietà del materiale/utensile). Questa proprietà sovrascrive quella di processo (se era stata valorizzata). Alimentata con la stessa quantità dichiarata in ricevimento merce o produzione

### CustomerDeliveryAddress

`MatClassProp.CustomerDeliveryAdress`

- Tipo: string
- Descrizione: Indirizzo di spedizione del cliente

### CustomerDeliveryDescription

`MatClassProp.CustomerDeliveryDescription`

- Tipo: string
- Descrizione: Descrizione della spedizione del cliente

### CustomerDescription

`MatClassProp.CustomerDescription`

- Tipo: string
- Descrizione: Descrizione del cliente

### CustomerID

`MatClassProp.CustomerID`

- Tipo: string
- Descrizione: Id cliente

### CustomerIDDelivery

`MatClassProp.CustomerIDDelivery`

- Tipo: string
- Descrizione: Id spedizione cliente

### CustomerItemRef

`MatClassProp.CustomerItemRef`

- Tipo: string
- Descrizione: Riferimento item cliente

### CustomerOrderID

`MatClassProp.CustomerOrderID`

- Tipo: string
- Descrizione: Identificativo ordine cliente

### CustomerOrderRef

`MatClassProp.CustomerOrderRef`

- Tipo: string
- Descrizione: Riferimento ordine cliente

### DefaultLocation

`MatClassProp.DefaultLocation`

- Tipo: string
- Descrizione: Magazzino di default dell'articolo
(usato per integrazioni con APS)

### DocFolder

`MatClassProp.DocFolder`

- Tipo: string
- Descrizione: Cartella o file di immagine

### FamiliaID

`MatClassProp.FamiliaID`

- Tipo: string
- Descrizione: Parametri utilizzati per integrazione con ERP Business Cube (se presente)

### FamiliaIDDescription

`MatClassProp.FamiliaIDDescription`

- Tipo: string

### GruppoID

`MatClassProp.GruppoID`

- Tipo: string

### GruppoIDDescription

`MatClassProp.GruppoIDDescription`

- Tipo: string

### GruppoSubLevelID

`MatClassProp.GruppoSubLevelID`

- Tipo: string

### GruppoSubLevelIDDescription

`MatClassProp.GruppoSubLevelIDDescription`

- Tipo: string

### IsSample

`MatClassProp.IsSample`

- Tipo: boolean<
- Descrizione:
  - False = Modalità disattivata;
  - True = Al momento del test viene chiesto dal sistema se estendere i valori inseriti, agli altri sottolotti dello stesso lotto e nello specifico se solo a quelli presenti nell'ubicazione o dovunque.

### LabelPrintCopies

`MatClassProp.LabelPrintCopies`

- Tipo: int
- Descrizione: Numero di copie che propone (nel client)
o stampa (nel web)

### LabelTemplate

`MatClassProp.LabelTemplate`

- Tipo: string
- Descrizione: Template di un'etichetta (è un file
nella cartella "label" del client)

### MarcaID

`MatClassProp.MarcaID`

- Tipo: string
- Descrizione: Parametri utilizzati per integrazione con ERP Business Cube (se presente)

### MarcaIDDescription

`MatClassProp.MarcaIDDescription`

- Tipo: string

### MaxQtyInUdp

`MatClassProp.MaxQtyInUdp`

- Tipo: float
- Descrizione: Se indicato, è il numero massimo di quantità nell'eventuale UDP

### OwnerMaterialID

`MatClassProp.OwnerMaterialID`

- Tipo: string
- Descrizione: Parametri utilizzati per integrazione con ERP Business Cube (se presente)

### OwnerMaterialIDDescription

`MatClassProp.OwnerMaterialIDDescrption`

- Tipo: string

### Position

`MatClassProp.Position`

- Tipo: string
- Descrizione: Posizione nel materiale in quanto
componente

### QtyInUdp

`MatClassProp.QtyInUdp`

- Tipo: float- Descrizione: Propone la quantità indicata
dell'UDP

### QUALITA

`MatClassProp.QUALITA`

- Tipo: string
- Descrizione: Valore della qualità di default

### StorageTypeID

 style="text-align: left;">MatClassProp.StorageTypeID`

- Tipo: int
- Descrizione:
  - 0 = Gestione solo a quantità (no lotti e no ubicazioni);
  - 1 = Gestione a UDM/Sottolotti;
  - 2 = Gestione a matricola UDM/Matricola;
  - 3 = Utensile a quantità;
  - 4 = Utensile a matricola;
  - 5 = Gestione LOTTO = Sottolotto (assegnazione manuale del lotto)

### SupplierDeliveryNoteID

`MatClassProp.SupplierDeliveryNoteID`

- Tipo: string
- Descrizione: Usati dal ricevimento di Master Factory

### SupplierDescription

`MatClassProp.SupplierDescription`

- Tipo: string

### SupplierID

`MatClassProp.SupplierID`

- Tipo: string

### SupplierInvoiceID

`MatClassProp.SupplierInvoiceID`

- Tipo: string

### SupplierLotID

`MatClassProp.SupplierLotID`

- Tipo: string

### SupplierOrderID

`MatClassProp.SupplierOrderID`

- Tipo: string

### SupplierReference

`MatClassProp.SupplierReference`

- Tipo: string

### SupplierSublotID

`MatClassProp.SupplierSublotID`

- Tipo: string

## PROPRIETA' DI PROCESSO

### AltQty (LifeQty)

`Life Qty`

- Tipo: float
- Descrizione: Durata di un utensile (dipende dall'unità di misura specificata nella proprietà del materiale/utensile). Se la stessa proprietà era stata specificata nel materiale, quest'ultima sovrascrive quella di processo.

### CheckCycle

``ProcessClassProp.CheckCycle`

- Tipo: string

### CheckEnable

`ProcessClassProp.CheckEnable`

- Tipo: int

### CheckInterval

`ProcessClassProp.CheckInterval`

- Tipo: int

### CheckJobSetup

`ProcessClassProp.CheckJobSetup`

- Tipo: string

### CheckLastDate

`ProcessClassProp.CheckLastDate`

- Tipo: date

### CheckLastStatus

`ProcessClassProp.CheckLastStatus`

- Tipo: string

### CheckStop

`ProcessClassProp.CheckStop`

- Tipo: int

### CheckUM

`ProcessClassProp.CheckUM`

- Tipo: int

### CheckWarning

`ProcessClassProp.CheckWarning`

- Tipo: float

### CustomerDeliveryAdress

`ProcessClassProp.CustomerDeliveryAdress`

- Tipo: string
- Descrizione: Indirizzo di spedizione del cliente (codice identificativo spedizione)

### CustomerDeliveryDescription (ProcessClassProp)

`ProcessClassProp.CustomerDeliveryDescription`

- Tipo: string
- Descrizione: Descrizione della spedizione

### CustomerDescription (ProcessClassProp)

`ProcessClassProp.CustomerDescription`

- Tipo: string
- Descrizione: Descrizione del cliente

### CustomerID (ProcessClassProp)

`ProcessClassProp.CustomerID`

- Tipo: string
- Descrizione: Codice identificativo del cliente

### CustomerIDDelivery (ProcessClassProp)

`ProcessClassProp.CustomerIDDelivery`

- Tipo: string
- Descrizione: Id della consegna

### CustomerItemRef (ProcessClassProp)

`ProcessClassProp.CustomerItemRef`

- Tipo: string
- Descrizione: Codice articolo del cliente

### CustomerOrderID (ProcessClassProp)

`ProcessClassProp.CustomerOrderID`

- Tipo: string
- Descrizione: Ordine di vendita del cliente

### CustomerOrderRef (ProcessClassProp)

`ProcessClassProp.CustomerOrderRef`

- Tipo: string
- Descrizione: Ordine di riferimento del cliente

### DependancyQuantity

`ProcessClassProp.DependancyQuantity`

- Tipo: float- Descrizione: Quantità di pezzi minima da produrre per
mettere in esecuzione la fase successiva

### DependancyTimeFactor

`ProcessClassProp.DependancyTimeFactor`

- Tipo: float- Descrizione: Tempo minimo per mettere in esecuzione
la fase successiva (utilizzato in alternativa al
DependancyQuantity)

### DependancyType

`ProcessClassProp.DependancyType`

- Tipo: string
- Descrizione: Tipo di dipendenza tra due fasi (ES:
AfterEnd,...)

### DocFolder (ProcessClassProp)

`ProcessClassProp.DocFolder`

- Tipo: string
- Descrizione: Percorso assoluto dove trovare documenti
o disegni

### MaxQty

`ProcessClassProp.MaxQty`

- Tipo: int
- Descrizione: Quantità massima accettabile in fase di
dichiarazione pezzi del sottolotto (se viene inserita una quantità
maggiore per errore, viene automaticamente corretta dal sistema con
questo valore)

### Note

`ProcessClassProp.Note`

- Tipo: string
- Descrizione: Note generiche

### PartProgramID (ProcessClassProp)

Part Program`

- Tipo: string
- Descrizione: Id del programma macchina

### ReportingNumber

`ProcessClassProp.ReportingNumber`

- Tipo: string
- Descrizione: Valore di transito (chiave usata da un
gestionale come riferimento interno dei dati scambiati con il MES)

### Reschedulable

`ProcessClassProp.Reschedulable`

- Tipo: int
- Descrizione:
  - 0 = modalità disattivata;
  - 1 = gli ordini che hanno questo processo vengono rischedulati in automatico.

### ToolsKitID

`ProcessClassProp.ToolsKitID`

- Tipo: string
- Descrizione: Id che identifica un gruppo di utensili
