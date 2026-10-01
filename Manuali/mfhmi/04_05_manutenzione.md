# MANUTENZIONE

| Icona | Funzionalità |
| :---- | :---- |
| ![img](icon-manutenzione.png) | All'interno di questa sezione vengono gestite le manutenzioni dei macchinari. |

## RICHIESTE

In questa interfaccia avviene la creazione delle richieste di manutenzione sulle macchine.

![img](manutenzione.png)

Nella tabella **R2** vengono visualizzate tutte le manutenzioni che rispettano i filtri sopra applicati **R1**. Cliccando sul tasto ![img](icon-nuova-spedizione.png) si aprirà la seguente finestra che permetterà di creare una nuova richiesta:

![img](manutenzione-nuova-richiesta.png)

Una volta compilata e cliccato il tasto `Conferma` verrà aggiunto, alla tabella **R2,** un nuovo record con lo stato `Edit` ![img](magazzino-icon-edit.png).

Successivamente alla creazione, lo stato del record potrà essere cambiato in `Ignored` ![img](magazzino-icon-ignored.png) cliccando sul tasto `Ignora`
**R4**, e quindi la richiesta non potrà più essere avanzata, in `End` ![img](manutenzione-icon-end.png) tramite il pulsante `Chiudi`
**R5** oppure potrà essere avanzata in `Scheduled` ![img](manutenzione-icon-scheduled.png) utilizzando il tasto ![img](manutenzione-pulsante-scheduled.png), compilando tutti i campi delle schede elencate come segue:

![img](manutenzione-pianificazione-intervento.png)

Se la richiesta di manutenzione è ancora in avanzamento si può visualizzare il suo contenuto tramite il bottone `Mostra Intervento Pianificato` **R3**, invece, anche se la richiesta è terminata, si possono modificare i dati precedentemente compilati
![img](manutenzione-icon-modifica.png) oppure eliminare direttamente il record ![img](manutenzione-icon-elimina.png).

## PIANIFICAZIONE

Quando sarà completata la fase di preparazione della richiesta, si potrà, tramite la seguente interfaccia, creare un rapporto di manutenzione:

![img](manutenzione-rapporti.png)

Al suo interno si trova una tabella **PN1** che mostra le richieste che soddisfano i seguenti filtri:

![img](manutenzione-filtri.png)

Cliccando sul tasto `Crea rapporto` **PN2**, si aprirà la segue finestra tramite la quale avverrà la creazione di un nuovo rapporto:

![img](manutenzione-nuovo-rapporto.png)

Al suo interno vengono riportati i dettagli della richiesta **RM1,** che possono essere modificati, e tre sezioni **RM2,** nelle quali vengono rispettivamente specificati:

### PROBLEMA

Viene riportata la causa del problema e l'eventuale soluzione.

### PERSONALE IMPIEGATO

Viene gestito tutto il personale che è stato impegnato nello svolgimento di questa manutenzione.

### MATERIALE CONSUMATO

Viene elencato tutto il materiale utilizzato nel corso dell'operazione.

Infine, se si vuole chiudere la richiesta e quindi mandarla in `End` ![img](manutenzione-icon-end.png), cliccare il tasto `Chiudi Intervento` **RM4**; se si vuole salvare le modifiche e mandare in `Run` ![img](image328.png) la manutenzione, cliccare il tasto `Salva Modifiche` **RM3**.

Se, una volta creato il rapporto, si vuole modificarlo, utilizzare il tasto `Modifica Rapporto` **PN3**.

![img](manutenzione-icon-dettaglio-rapporto.png) Serve per visualizzare il rapporto associato alla richiesta una volta in `Run`.

![img](manutenzione-icon-modifica.png) Va in modifica della richiesta che è ancora in `Scheduled`.

![img](manutenzione-icon-elimina.png) Elimina l'intero Ordine di Intervento.

## ESECUZIONE

All'interno di questa interfaccia vengono visualizzate, raggruppate per macchina, tutte le manutenzioni che hanno o stanno eseguendo il loro processo lavorativo:

![img](manutenzione-dettaglio-manutenzioni.png)

Il tasto `Modifica` ![img](manutenzione-icon-modifica.png) può essere  utilizzato, a differenza delle altre sezioni, anche sugli Ordini di Intervento che
sono in *End*; invece, il pulsante `Elimina` ![img](manutenzione-icon-elimina.png) può essere utilizzato solo sui record che ancora non hanno terminato il loro processo lavorativo.
