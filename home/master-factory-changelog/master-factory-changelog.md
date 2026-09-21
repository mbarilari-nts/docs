# Master Factory ChangeLog

## Nella prossima release…

### 2026-07-08

* :warning::gear: Migliorata comunicazione dispositivi Marposs, migliorati messaggi di log e riconnessione.
* :warning::gear::boom: Migliorata comunicazione con FactoryHub.

{% hint style="warning" %}
**ATTENZIONE**: Questo aggiornamento deve essere fatto insieme a Factory Hub dalla versione\
Changelog Factory Hub | 2026 06 17
{% endhint %}

### 2026-07-06

* :warning::gear: Corretta aggiunta automatica allarmi a seguito di richieste esterne con alarmID inesistente.
* :plus: Aggiunta funzionalità reasonMissing - Verifica che l’operatore abbia inserito il “giustificativo” rispetto alla reason impostata nella proprietà ReasonNoProd nell’equipment.

### 2026-07-02

* ?? Migliorati log errori e riconnessione NetItBroker per sistemi Marposs.

### 2026-05-18

* :gear: Ripartizione tempi uomo-macchina nei Gruppi come richiesto da oggi diventa lo standard ripartire in base al “peso” cioè la durata della fase dell’ordine di lavoro proporzionale alle altre appartenenti al gruppo.

## Rilascio setup 2026-05-14

### 2026-05-13

* :plus\_sign: NetItBroker – migliorato l’aggiornamento del `clientTry2Fix` aggiorno forzato dei topic mqtt (`_Hmi.Sys.SrIstQty[1]` e `_Hmi.Sys.QtyScrap` quando qualcosa va in RUN da comando X5)

## Rilascio setup 2026-03-31

### 2026-03-31

* ? Aggiunta integrazione per conferma InBound attraverso Business, ora è possibile utilizzare una pre-conferma da Master Factory.
* ????? Corretta lettura da HmiT UdM InBound, l’UdM veniva lasciato in WIP.
* ???? Ottimizzazione serializzazione comunicazione messaggi Server e Web.

{% hint style="warning" %}
**ATTENZIONE**: Questa patch è legata alle modifiche al Client versione 2026-03-20 e al Server Web versione 2026-03-31
{% endhint %}

### 2026-02-24

* ????? Corretta chiusura del personel al cambio stato da RUN a UNLOAD. Le persone potevano rimanere collegate all’ordine in modo indefinitio
* ????? Il messaggio 255 del servizio REST HRC ora esegue correttamente la dichirazione di produzione.

### 2026-02-16

* ????? Rimossa funzionalità utenti ghost per le personnel, permetteva di recuperare le person attive nell’ordine precedente. Verrà rivalutata più avanti una gestione migliorata.

### 2026-02-10

* ?? Ottimizzazioni varie nelle letture parametri macchina.
* ????? Corretto split delle utilization per il Personnel a seguito di un logout prima della sospensione. Prima poteva rimanere attiva la Person.
* ? Aggiunta funzionalità di chiusura ordine tramite API REST (ERP Business), chiusura OutBound e InBound.

### 2026-02-02

* ??? ?? Corretta logica sulle singole operazioni. In alcuni sporadici casi operazioni complesse potevano saltare il salvataggio di alcune operazioni intermedie causando anomalie nelle utilization delle Person.

### 2026-01-27

* ??? ?? Modificata logica del limite massimo esportazione record delle tabelle EXP\_ Personnel/Material/Equipment actual; ora è forzata l’esportazione di tutti i record dell’ultima ora in aggiunta ai 500. Prima esportava massimo 500 record ogni ora.

{% hint style="warning" %}
ATTENZIONE: valutare la frequenza di impostazione del task; frequenze elevate possono causare un alto utilizzo di CPU e Database.
{% endhint %}

## Rilascio setup 2026-01-27

* ??? Le proprietà numeriche passate dai servizi esterni (ad esempio gestionali) vengono trattate con la `CultureInfo.InvariantCulture`, che ha le seguenti caratteristiche uguali per tutti:
  * Separatore decimale: Viene sempre usato il punto (.)
  * Separatore delle migliaia: Viene sempre usata la virgola (,)
  * Formato data: Segue il modello MM/DD/YYYY
*   ? Ora è possibile specificare la porta di Factory Hub per la configurazione HrcFH50Broker nella proprietà value dell’Equipment, default 5002 se non specificata.

    Estratto Server.xml

    ```xml
    <!-- Configurazione Factory Hub -->
    <object id="HrcFH50Broker"
        type="TTisa95.Server.Services.HrcFH50Broker, TTisa95.Server.Services"
        singleton="true" lazy-init="false" init-method="Init">
      <property name="BrokerName" value="172.20.21.79"></property>
      <property name="TopicPrefix" value="NTSM/MF40/"></property>
      <property name="ResolutorFromResource">
        <dictionary>
          <entry key="M4" value="172.20.1.25:5002" />
        </dictionary>
      </property>
    </object>
    ```
* ? Al presentarsi di più Segment requirements che corrispondono allo stesso sottolotto ora è possibile spostare ed avviare automaticamente il primo in sequenza su un Equipment alternativo, questo avviene caricando nella baia di ingresso il sottolotto designato al consumo. Se il materiale da consumare del Segment requirement ha come specifica lotto o materiale, il comportamento rimane inalterato; solo con un solo ordine questo viene spostato ed avviato automaticamente. La seguente modifica richiede che la versione server, server web e client siano almeno della versione 2025-11-11.

## Rilascio setup 2025-11-17

* ??? Corretto filtro Commessa nel tab Pianificazione -> Ordini in HMI, se veniva inserito il carattere % (percentuale) non venivano restituiti risultati; ora il carattere % permette una ricerca parziale delle commesse.

## Rilascio setup 2025-10-17

### 2025-10-03 ??

* ? Aggiunta rilevazione mancanza codice SAP nella funzionalità StkGenerator.
*   ??? Corretta l'attivazione di una UdM quando nella rotta venivano valorizzate proprietà che corrispondevano ai MaterialRequirement, in caso di errore restituiva nell’error log come segue:

    ```log
    ERROR TTisa95.DataModel.OqlExtensions [(null)] - System.NullReferenceException: Object reference not set to an instance of an object.
        at TTisa95.DataModel.OqlExtensions.MatchExact(PropertiesInstanceGroups instanceGroup, PropertiesInstanceGroups comparedInstanceGroup, Boolean allRequired, Boolean containsAll) in C:\\Lavoro\\TTisa95\\Server\\TTisa95.DataModel.Common\\Extension\\OqlExtensions.cs:line 143
    ERROR TTisa95.DataModel.OqlExtensions [(null)] - System.NullReferenceException: Object reference not set to an instance of an object.
        at TTisa95.DataModel.OqlExtensions.Match(PropertiesInstanceGroups instanceGroup, PropertiesInstanceGroups comparedInstanceGroup) in C:\\Lavoro\\TTisa95\\Server\\TTisa95.DataModel.Common\\Extension\\OqlExtensions.cs:line 76
    ```

### Rilascio setup 2025-09-26

#### 2025-09-24

* ??? Corretta integrazione FactoryHub.
* ? Implementata integrazione AVEX.

#### 2025-09-24 ??

* ??? Corretto invio parametri per la creazione dei calendari del Job di Hangfire.

#### 2025-09-16

* ? Modificato comportamento OpMode4: ora è possibile impostare material diversi in ingresso e uscita.
* ? Aggiunto ProductRequestID e SegmentRequiredID nel messaggio per la funzionalità StkGenerator.

#### 2025-09-15

* ??? Corretto controllo di archiviabilità dell'ordine, verificando le UdM prodotte dall'ordine di lavoro che si sta tentando di archiviare, che oltre ad essere con Quantity != 0 e in uno Stato != "OK" siano nelle rotte di UNLOAD della macchina sul quale l'ordine sta lavorando.

#### 2025-09-04 ??

* ??? corretta chiamata api/v1/sdk/{tenantID}/sendHmiCommand che non permetteva l'invio degli args in formato array di stringhe, ma solamente in array di BYTE. vedi Invio comandi tramite sendHmiCommand negli errori conosciuti.

#### 2025-08-29

* ? Invio mail a seguito di errore oppure UdM non trovati StkGenerator

#### 2025-08-07

* ? Opzione che permette il trasferimento in un UdM già esistente nella location. Il comportamento è condizionato dalla proprietà StorageMode: se impostata ad 1 il deposito destinatario accumula nell’UdM già esistente, solo per stesso articolo e stesso lotto.

#### 2025-08-05 ??

* ??? Corretta verifica Test Materials, anche sul client HMI

#### 2025-08-04 ??

* ??? nel file di configurazione predefinito server.xml, la voce TTisa95.DataModel.OrdersItems\_SavingChanges non ha alcun effetto, eliminata. Nel file è già presente una voce TTisa95.DataModel.OrderItems\_SavingChanges che è quella corretta.
* ??? Aggiunti controlli di coerenza sui parametri inviati alla SaveMaterialQualificationTestResults, TestDefinitionId deve esistere.
* ??? Corretto in ImportTransaction delle API REST i valori errati nei campi: EquipmentId e ParentEquipmentId.
* ??? Corretto in ChangeSegmentRequirement delle API REST il valore errato nel campo: EquipmentId.

#### 2025-03-10 ??

* ?? Passaggio a .Net Framework 4.6.2 a 4.7.2

## Errori conosciuti

Quando si aggiorna una versione è necessario verificare TUTTI questi punti per evitare malfunzionamenti di difficile DEBUG.

<details>

<summary>Invio comandi tramite sendHmiCommand</summary>

Dalla versione 2025-03-10 alla 2025-09-04 le chiamate verso la risorse api/v1/sdk/{tenantID}/sendHmiCommand potevano fallire in caso effettuate come array di stringhe invece che array di bytes, di seguito un esempio di chiamata tramite API REST che provoca l’errore:

```json
{
    "node": "607",
    "event": "ChangeOrderStatus",
    "wrk": "Hmi.Server",
    "user": "admin",
    "process": "HRC",
    "args": [ // NOTA: la notazione è un array di stringhe, invece che un array di BYTE
        "",
        "20250259-07",
        "7",
        "",
        "EXECUTABLE",
        "",
        "EXECUTABLE",
        "admin",
        "HMI.Server"
    ]
}
```

</details>
