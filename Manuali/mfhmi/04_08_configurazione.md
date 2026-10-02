
# CONFIGURAZIONE

## GESTIONE UTENTI/GRUPPI

| Icona | Funzionalità |
| :---- | :---- |
|![img](./media/icon-gestione-utenti.png)) | La maschera gestione utenti gruppi, permette la gestione degli utenti che utilizzano il programma Masterfactory. |

L'interfaccia GESTIONE UTENTI/GRUPPI è suddivisa in tabs che permettono di eseguire le seguenti funzionalità:

- UTENTI: permette la creazione/gestione di un utente
- GRUPPI: permette la creazione/gestione di gruppi in cui raggruppare
  gli utenti
- POSTAZIONI: permette la creazione/gestione delle postazioni PC di
  lavoro (ovvero, dove ho installato Masterfactory)
- AZIONE OPERATORE: visualizza il log eventi generato da ogni operatore
- UTENTI ON-LINE: permette di visualizzare in tempo reale gli utenti che
  operano su Masterfactory

### TAB: UTENTI

La Tab UTENTI permette di gestire (creare, modificare, eliminare) un utente. L'interfaccia è quella di seguito mostrata:
](./media/u
![img](utenti.png))

**U1**](./media/uesenta l'elenco di tutti gli utenti che sono registrati nel sistema. Cliccare sul tasto **U3** per inserire un nuovo utente (**U2** in caso di modifica). La maschera che permette di eseguire questa funzionalità è mostrata qui di seguito.

![img](utenti-nuovo-utente.png))

**U3.1** Nome dell'utente in formato breve
**U3.2** Nome dell'utente in formato esteso
**U3.3** Eventuali note
**U3.4** Stato dell'utente:

- ATTIVO: può operare in Masterfactory
- DISATTIVO: all'utente è stata inibita la possibilità di operare in Masterfactory

**U3.5** Permette di associare all'utente un Person ID tra quelli memorizzati in `CONFIGURATORE` 🡪 `PERSONALE`
**U3.6** Permette d'impostare la lingua dell'utente, scegliendo tra quelle disponibili in `CONFIGURATORE` 🡪 `GENERALE` 🡪 `LINGUE`
**U3.7** Permette d'identificare il nuovo utente come `Utente di sistema`; nella versione corrente tale caratteristica è ininfluente, in quanto ne è previsto l'utilizzo nelle future versioni
**U3.8** Permette d'impostare il lasso di tempo dopo il quale l'utente deve obbligatoriamente cambiare la password. Qualora il valore venga settato su 0, ciò significa che non si attribuisce alcuna scadenza.
**U3.9** Permette d'impostare manualmente le password dell'utente; abilita i campi **U3.10 U3.11 U3.12 U3.13**
**U3.10** In caso di cambio password, operazione ammissibile solo in caso di modifica (pressione tasto **U2**). Per motivi di sicurezza è richiesta l'immissione della vecchia password.
**U3.11** Immissione della nuova password
**U3.12** Poiché, per motivi di sicurezza, il campo **U3.11** offusca le lettere digitate, viene richiesta una nuova immissione della password per eseguire il confronto e assicurare di avere digitato correttamente la password
**U3.12** Imposta la data di scadenza della password.

#### PERSONALIZZAZIONI LAYOUT UTENTE

Considerato che a ogni ad ogni utente è permesso personalizzare le griglie di Masterfactory (vedi capitolo GESTIONE GRIGLIE / GRIGLIE MODIFICABILI), qui di seguito si indica come importare /resettare tali personalizzazioni.

- `Reset User Layout` **U5** è possibile resettare tutte le personalizzazioni associate all'utente selezionato
- `Import Layout from User` **U6** permette di associare all'utente corrente le personalizzazioni di un altro utente: cliccando sul pulsante, apparirà l'elenco degli utenti da cui copiare il layout.

#### ASSOCIAZIONE AD UN GRUPPO

Una volta inserito un nuovo utente è necessario attribuirlo a un gruppo, tra quelli disponibili nella tab GRUPPI **U9**: cliccare sul tasto **U11**, poi spuntare i gruppi desiderati. Al termine dell'attribuzione, in **U9** si vedrà l'elenco dei gruppi cui appartiene l'utente selezionato.

#### ASSEGNAZIONE AUTORIZZAZIONI

A ogni utente sono assegnate delle autorizzazioni per eseguire le funzionalità di Masterfactory. Tali autorizzazioni si possono `ereditare` da:

- UN GRUPPO: tramite il tasto **U7**, selezionare il gruppo da cui importare i permessi
- OPERATORE: tramite il tasto **U8**, selezionare l'utente da cui importare i permessi](./media/u
- PERS](./media/uLIZZATE
  Per personalizzare le autorizzazioni è necessario selezionare la tab **U10**, che contiene una griglia dove sono elencati tutti i permessi associati all'utente  selezionato; cliccare sul tasto![img](utenti-pulsante-nuovo-utente.png)) per aggiungere nuove autorizzazioni, come spiegato anche nella maschera sottostante.

![img](utenti-nuove-autorizzazioni-utente.png))

Le autorizzazioni sono suddivise in 3 macroaree:

- **A1** Funzionalità
- **A2** Operatività su postazioni di lavoro](./media/u
- **A3** Operatività su client PC

Attraverso l'apposizione della spunta alle varie voci di ogni macroarea, si attribuiscono all'utente selezionato le funzionalità (quelle senza la spunta si considerano omesse). Per facilitare questa selezione, cliccare sul `check` e il sistema automaticamente selezionerà tutte le voci del riquadro; poi procedere a deselezionare i permessi che non s'intende concedere, rimuovendoli con il tasto![img](utenti-rimozione-autorizzione-utente.png)).

L'impostazione delle autorizzazioni, espresse sui 3 livelli appena descritti, permette un'elevata flessibilità di configurazione, aspetto più evidente nell'esempio che segue:

Esempio

Suppon](./media/uo che l'utente **0001** possa avere accesso alle **operazioni hmi** dell'equipment **x1** ma che, per ragioni di sicurezza, egli possa accederci solo dal pc situato a bordo macchina - denominato **workstation 007**- e che, inoltre, egli possa accedere alle **dashboard web** da qualsiasi pc, ma visualizzando solo i dati della macchina **x1**. Per impostare queste 2 configurazioni si devono spuntare le seguenti voci:

accesso alle **operazioni HMI** per equipment **X1** su **workstation 007**
](./media/u
![img](utenti-aggiunta-autorizzazione-utente-workstation.png))

accesso alle **dashboard web** da qualsiasi postazione pc, ma con i dati della sola macchina **X1**

![img]](./media/uenti-aggiunta-autorizzazione-utente-singola-macchina.png))

### TAB. GRUPPI
](./media/u
La Tab GRUPPI permette di creare e gestire i gruppi nei quali verranno associati gli utenti. La maschera di gestione dei gruppi è sotto riportata.

![img](utenti-gruppi.png))

In **G1** contiene l'elenco di tutti i gruppi creati, mentre **G9** contiene tutti gli utenti del gruppo selezionato. Per creare un nuovo gruppo è necessario cliccare sul tasto **G2**; per modificare un gruppo, cliccare sul tasto **G3**. In entrambi i casi, la maschera che appare come segue:
](./media/M
![img](utenti-modifica-gruppo.png))

Nella maschera vanno inseriti o variati i dati inerenti al gruppo, quali descrizione ed eventuali note.

#### PERSONALIZZAZIONI LAYOUT GRUPPO

Poiché ad ogni utente è permessa la personalizzazione delle griglie di Masterfactory (vedi capitol[GESTIONE GRIGLIE / GRIGLIE MODIFICABILI](Manuali/mfhmi/03_gestione_griglie.md#griglia_modificabile)))), tramite i seguenti tasti è possibile gestire le personalizzazioni a livello di gruppo.

- `Reset User Group Layout` **G5** permette di resettare tutte le personalizzazioni associate al gruppo selezionato
- `Import Layout from User` **G6** permette di associare al gruppo corrente le personalizzazioni di un utente: cliccare sul pulsante per visualizzare l'elenco degli utenti da cui copiare il layout

#### ASSOCIAZIONE UTENTE AL GRUPPO

Tramite il tab **G9**, cliccare sul tasto **G11**, poi spuntare gli utenti desiderati per includerli nel gruppo corrente.

#### ASSEGNAZIONE AUTORIZZAZIONI AL GRUPPO](./media/u

A ogni gruppo sono assegnate delle autorizzazioni per eseguire le funzionalità di Masterfactory. Tali autorizzazioni possono essere *ereditate* da:

- UN GRUPPO tramite il tasto **G7**, selezionare il gruppo da cui importare i permessi
- OPERATORE tramite il tasto **G8**, selezionare l'utente da cui importare i permessi
- PERSONALIZZATE
  Per personalizzare le autorizzazioni, selezionare la tab **G10** che contiene una griglia dove sono elencati tutti i permessi associati al gruppo selezionato; cliccare sul tasto![img](utenti-pulsante-nuovo-utente.png)) per aggiungere nuove autorizzazioni, come già spiegato in precedenza per  l'assegnazione dell'autorizzazione a un utente.
](./media/u
> [!Note]
> Le autorizzazioni sono gestite contemporaneamente sia a livello utente sia di gruppo, con priorità a quelle assegnate all'utente.

### TAB. STATION

La Tab Station permette di aggiungere, modificare o eliminare le *workstation* da assegnare alle varie installazioni *client*, che possono essere utilizzate per la gestione delle autorizzazioni. **S1** contiene l'elenco di tutte le workstation attualmente configurate.

![img](utenti-station.png))

Cliccando sul tasto **S2** per apportare le modifiche su una workstation.
Cliccando sul tasto **S3** per aggiungere nuove workstation.
Cliccando sul tasto **S4** per eliminare workstation esistenti.

### TAB. OPERATION ACTION
](./media/u
La Tab Operation Action permette di visualizzare un *log* di tutte operazioni effettuate su *MASTER Factory^®^*, filtrabili per:

- **L1** Data
- **L2** Equipment
- **L3** Azione
- **L4** Workstation
- **L5** Utente

![img]](./media/centi-operazioni-filtri.png))

### TAB. UTENTI ONLINE

La Tab UTENTI ONLINE permette di visualizzare, in tempo reale, tutti gli utenti che stanno utilizzando *MASTER Factory^®^*.

## CONFIGURATORE

Per accedere alla pagina cliccare sulla scheda `Configurazione`, quindi sul bottone `Configuratore`.

![img](configurazione.png))

La pagina Configuratore è suddivisa nelle seguenti sezioni e relative
sottosezioni:

1. GENERALE
   1. Unità di misura
   2. Tipi di Causale
   3. Causali
   4. Costanti
   5. Parametri
   6. Lingue
   7. Sequenze
   8. Gestione turni
   9. Traduzioni
2. MACCHINE
   1. Macchine
   2. Categoria macchine
   3. Proprietà delle categorie macchine
   4. Allarmi
   5. Livelli Allarme
   6. Priorità manutenzione
   7. Stati manutenzione
3. PERSONALE
   1. Personale
   2. Categorie personale
   3. Proprietà per categorie personale
4. MATERIALE
   1. Materiali
   2. Categorie dei materiali
   3. Proprietà delle categorie materiali
   4. Materiali sostitutivi
   5. Udc
   6. Tipi Udc
   7. Proprietà Udc
   8. Stati Udc
   9. Rotte di magazzino
5. TIPOLOGIA DI PROCESSO
   1. Tipologie
   2. Proprietà per tipologie processo
6. CICLI DI LAVORAZIONE
   1. Cicli di lavorazione
   2. Stati per le regole di produzione
7. ORD](./media/c
   1. Tipologie di ordine
   2. Proprietà per tipologie di ordine
8. ALA](./media/cMSG

### GENERALE
](./media/c
#### UNITA' DI MISURA

Elenco](./media/c tutte le unità di misura di interesse. Ogni unità di misura è caratterizzata da un Codice univoco, una descrizione e il numero di decimali visualizzabili:

![img](configurazione-generale-unita-di-misura.png))

#### TIPI DI CAUSALE
](./media/c
![img](configurazione-generale-tipi-di-causale.png))

Tabella contenente il massimale delle tipologie di causali utilizzabili nell'applicazione. Ciascuna causale è caratterizzata da un codice identificativo (Tipo causale), una descrizione, la categoria a cui si applica la causale e un colore. Ciascuna categoria può avere una o più tipologie di causali.

![img]](./media/cnfigurazione-generale-aggiungi-tipo-di-causale.png))

#### CAUSALI

![img](configurazione-generale-causali.png))
](./media/c
Massimale delle causali utilizzabili nell'applicazione. Le causali sono raggruppate per `Tipi di causali` e ciascuna è caratterizzata da un codice (Causale), una descrizione, il tipo di causale e un colore.

#### PARAMETRI

![img](configurazione-generale-parametri.png))

#### LINGUE

Tabell](./media/contenente l'elenco delle lingue gestite dall'applicazione. Ciascuna lingua è identificata da un Codice, una descrizione e un'immagine (opzionale).

![img](configurazione-generale-lingue.png))

#### SEQUENZE
](./media/c
Le sequenze rappresentano dei contatori, utilizzati all'interno dell'applicazione. Ciascuna sequenza, in fase di creazione, può essere limitata da un valore minimo (Min) e massimo (Max).

![img](configurazione-generale-sequenze.png))

#### G](./media/cIONE TURNI

Questa pagina consente la gestione dei turni di lavoro e delle festività.

##### TAB.TURNI
](./media/c
Questa sezione consente la creazione dei turni di lavoro. Ciascun turno è caratterizzato da un Id numerico e da una descrizione. All'interno del turno è possibile specificare la pianificazione giornaliera, contraddistinta da NUMERO GIORNO, NUMERO INTERVALLO, DA (orario hh:mm), A (orario hh:mm)

![img](configurazione-generale-gestione-turni.png))

##### ](./media/c. FESTIVITA'

Elenco delle festività. Ciascuna festività è caratterizzata da un nome, una descrizione, una durata temporale in giorni (valorizzando i campi `Dal` e `Al` con le date di interesse) o in alternativa (in caso di festività di un singolo giorno) può essere impostata una ricorrenza annuale valorizzando il campo `Valido ogni anno Giorno/Mese`. Infine, una festività può essere associata a tutte le risorse e le persone (spuntando le relative checkbox), o in alternativa essere associata a specifiche risorse e persone.

![img](configurazione-generale-gestione-turni-festivita.png))

##### TAB. ABBINA TURNI E MACCHINE
](./media/c
In questa sezione è possibile abbinare i turni alle macchine, per un determinato intervallo temporale.

![img]](./media/cnfigurazione-generale-gestione-turni-turni-macchine.png))

##### TAB. ABBINA TURNI E PERSONALE

Specularmente alla sezione precedente, in questa pagina è possibile associare i turni al personale.

![img](configurazione-generale-gestione-turni-turni.png))

#### TRADUZIONI

Tabell](./media/contenete la traduzione di tutte le stringhe dell'applicazione, per ciascuna lingua specificata nella tabella `Lingue`.

![img](configurazione-generale-traduzioni.png))
](./media/c
### MA](./media/cINE

#### TAB. MACCHINE

Questa pagina consente la creazione e la modifica dell'intero albero a nodi del sistema, contenente le caratteristiche di tutte le macchine ed i magazzini utilizzati.

![img](configurazione-macchine-macchine.png))

Selezionando un nodo dell'albero e cliccando quindi sul bottone per la creazione di un nuovo elemento, verrà visualizzata una maschera per la creazione di un nuovo nodo figlio di ciò che è stato selezionato (ES. Cliccando su Entreprise sarà possibile creare dei nodi figli di 'Categoria' SITE, mentre selezionando un nodo di categoria AREA sarà possibile creare dei nodi figli di categoria PRODUCTION LINE, STORAGE ZONE o STORAGE ZONE WIP). Se la categoria selezionata ha associate delle Proprietà (come nel caso delle macchine), queste verranno visualizzate nella sezione omonima, in cui sarà possibile valorizzarle.

![img](configurazione-macchine-crea-macchina.png))

I magazzini sono suddivisi su due livelli all'interno dell'albero a nodi: STORAGE ZONE e STORAGE UNIT. Ogni STORAGE ZONE può contenere una o più STORAGE UNIT che rappresentano fisicamente le singole unità di stoccaggio.

Una STORAGE UNIT può essere delle seguenti tipologie: INGRESSO (categoria **INL**), PREPARAZIONE (CATEGORIA **PRL**), USCITA (CATEGORIA **OUL**), STOCCAGGIO MATERIALE (CATEGORIA **STU**).

> [!Note]
> Il sistema necessita la creazione di almeno una STORAGE UNIT di tipologia INL e un'altra di tipologia OUL per ciascuna macchina (WORK CELL), secondo la seguente convenzione: ID_MACCHINA TIPO_MAGAZZINO (IN/OUT) NUM_PROGRESSIVO_MAGAZZINO.

Per la creazione delle singole STORAGE UNIT è quindi necessario creare innanzitutto la STORAGE ZONE di appartenenza (selezionando il nodo padre, di categoria AREA).

![img](configurazione-macchine-crea-storage-unit.png))

Creata](./media/c STORAGE ZONE, è quindi possibile la creazione dei vari livelli di STORAGE UNIT di cui è composta:

![img](configurazione-macchine-crea-storage-unit-livello.png))
](./media/c
![img]](./media/cnfigurazione-macchine-crea-storage-unit-categoria.png))
](./media/c
> [!Note]
> In alternativa alla creazione manuale dei nodi dell'albero, è possibile importare l'intera struttura da un file .csv.</span>

ESEMPIO FILE CSV DI IMPORT

```csv
4001,4](./media/c-Stampaggio inserti, WKC, 4000
4001 IN 01,4001 IN 01, INL, STW01
4001 OU 01,4001 OU 01, OUL, STW01
4001 P](./media/c1,4001 PR 01, PRL, STW01
3003,4001-Infilaggio rivetti, WKC, 3000
3003 IN 01,3003 IN 01, INL, STW01
3003 O](./media/c1,3003 OU 01, OUL, STW01
3003 PR 01,3003 PR 01, PRL, STW01
```

Questo file consente la creazione di due Work Cell (Stampaggio inserti e infilaggio rivetti) e per ciascuna la generazione dei 3 magazzini IN, PRL e OUT.

ESEMPIO

Prendi](./media/c come esempio la WORK CELL Pressa 1

![img](configurazione-macchine-esempio-configurazione-gate-in-out-1.png))

In questo caso l'Id macchina è 2001, perciò il sistema si aspetta la presenza di almeno le due STORAGE UNIT: 2001 IN 01 e 2001 OUT 01

![img](configurazione-macchine-esempio-configurazione-gate-in-out-2.png))

![img](configurazione-macchine-esempio-configurazione-gate-in-out-3.png))

![img](configurazione-macchine-esempio-configurazione-gate-in-out-4.png))

##### ROTTE DI MAGAZZINO

Per ciascun magazzino devono essere inoltre specificate delle `ROTTE DI MAGAZZINO`, attraverso le quali il sistema sarà in grado di valutare gli approvvigionamenti di materiale per i vari ordini di produzione. Le rotte possono essere impostate cliccando sulla scheda `Rotte di magazzino`, dopo aver selezionato il magazzino di interesse.

Ciascuna rotta di magazzino è contraddistinta da una causale (descrittiva del tipo di rotta: TRANSFER, LOAD, UNLOAD, RETTIFY, INBOUND), dai due valori contenenti i codici dei magazzini di partenza e destinazione (se la categoria selezionata è INBOUND non sarà possibile selezionare il magazzino di IN poiché in questo caso si considera una rotta proveniente dall'esterno della fabbrica)</u>, la **categoria** del materiale coinvolto nella rotta (impostando `*` la rotta verrà applicata a tutti i materiali), lo stato **attiva/non attiva** e lo stato **Auto**, ovvero la rotta viene calcolata in automatico in base a delle logiche predefinite in fase di configurazione del sistema.
](./media/c
![img](configurazione-macchine-rotte-di-magazzino.png))

**ROTTE NECESSARIE IN CASO DI ASSENZA DEL MAGAZZINO DI PREPARAZIONE MATERIALE**:

![img]](./media/cnfigurazione-macchine-rotte-senza-preparazione.png))

**ROTTE NECESSARIE IN CASO DI PRESENZA DEL MAGAZZINO DI PREPARAZIONE MATERIALE**:

![img](configurazione-macchine-rotte-con-preparazione.png))

#### TAB. CATEGORIA MACCHINE

Tabella che contiene l'elenco delle categorie che caratterizzano tutti i livelli dell'albero a nodi dell'impianto. Una categoria è caratterizzata da un codice identificativo, una descrizione, il livello dell'albero a nodi al quale è possibile associare la categoria (AREA, SITE, STORAGE UNIT, WORK CELL, ...), delle proprietà, una immagine e infine delle causali.
](./media/c
> [!Note]
> Tipicamente è richiesta la creazione di tutti i livelli elencati nell'immagine sottostante.
](./media/c
![img]](./media/cnfigurazione-macchine-categorie-ubicazioni.png))

#### TAB. PROPRIETA' DELLE CATEGORIE DI MACCHINARI

Lista del massimale delle proprietà associabili alle categorie macchine. Una proprietà è caratterizzata da codice, descrizione, unità di misura, dimensione, tipo di dato e se la proprietà ammette valori multipli.

> [!Note]
> E' obbligatorio valorizzare le seguenti proprietà, corrispondenti agli stati che una macchina può assumere. Ciascuna di queste proprietà sarà associata ad una causale.
](./media/c
| Causale | Descrizione |
| :---- | :---- |
| Reas](./media/cnd | Contiene la causale di default per lo stato "fine" |
| ReasonMicroStop | Contiene la causale di default per lo stato "micro stop" |
| ReasonNoProd | Contiene la causale di default per lo stato "macchina ferma" |
| ReasonProd | Contiene la causale di default per lo stato "in produzione" |
| ReasonSetup | Contiene la causale di default per lo stato "in setup" |
| ReasonOff | Contiene la causale di default per lo stato "offline" |

![img](configurazione-proprieta-macchine.png))
](./media/c
#### T](./media/c ALLARMI

Elenco degli allarmi gestiti dall'applicazione. Un allarme è caratterizzato dal Livello di allarme, il codice di allarme, una descrizione, la tipologia e una nota contenente eventualmente la sequenza di operazioni che l'operatore dovrà eseguire per risolvere il malfunzionamento che ha causato l'allarme.
](./media/c
![img](configurazione-allarmi.png))

#### TAB. LIVELLI ALLARME

Elenco](./media/c tutti i livelli associabili ad un allarme. Ciascun livello è caratterizzato da un codice, una descrizione ed un colore.

### PERSONALE

Sezione per la gestione del personale. Ciascun elemento è caratterizzato da un codice, un nome e una categoria (con relative proprietà).

![img](configurazione-personale.png))
](./media/c
### MATERIALE

![img](configurazione-materiale.png))

![img]](./media/cnfigurazione-materiale-modifica.png))

Anagrafica dei materiali utilizzati nel sistema. Un materiale è caratterizzato da: un codice, un alias, un codice EAN (European Article Number, famiglia di codici a barre usati per la marcatura dei prodotti destinati alla vendita al dettaglio), una categoria di materiale, un'unità di misura principale e una alternativa, le dimensioni e delle proprietà. Inoltre, è possibile associare ad un materiale anche
un'immagine e della documentazione.

#### T](./media/c UDC

Con unità di carico o UdC si intende l'unità di base di stoccaggio e trasporto posizionata su un supporto o imballaggio modulare (cassa, pallet, contenitore ecc.) al fine di ottenere una movimentazione efficace.
](./media/c
![img](configurazione-materiale-udc.png))

Una Udc è caratterizzata da un Prefisso (codice identificativo), un suffisso, un tipo, uno stato (il massimale di tutti i tipi e gli stati sono definiti nelle relative sezioni `Tipi Udc` e `Stati Udc`) e una posizione (in riferimento ad un nodo dell'albero definito nella pagina `Macchine`).

![img]](./media/cnfigurazione-materiale-crea-udc.png))
](./media/c
In fase di creazione è possibile gestire la creazione massiva di Udc, specificando nel campo Quantità il numero di Udc che si vogliono creare. All'interno del riquadro ‘Progressione' è inserita la logica per la generazione di prefissi progressivi, in caso di creazione massiva di UdC. È possibile specificare se i codici progressivi utilizzeranno una progressione numerica o alfabetica e il valore iniziale della sequenza. Infine, è anche possibile abilitare la generazione di un codice SSCC (Serial Shipping Container Code, standard logistico usato nella supply
chain per identificare le UdC) e stamparne l'etichetta contenente la codifica in formato codice a barre.

### TIPOLOGIE DI PROCESSO

Tabella contenente la lista di tutti i processi di lavorazione eseguibili.

![img](configurazione-processi-modifica.png))
](./media/c
![img](configurazione-processi.png))

Un processo è contraddistinto da una Tipologia (Identificatore), una descrizione, la durata del processo (in secondi) e la data di pubblicazione del processo. Ciascun processo può avere a sua volta delle proprietà specifiche (valorizzabili in fase di creazione del processo o attraverso la scheda `Proprietà`). Il massimale delle proprietà associabili ai processi è definito nella scheda `Proprietà per Tipologie di Processo`.

![img]](./media/cnfigurazione-processi-proprieta.png))

Mediante le schede nella parte bassa della pagina è possibile associare i processi anche alle seguenti entità:
](./media/c
#### PROCESSI - MACCHINE

![img]](./media/cnfigurazione-processi-macchine.png))

In fase di associazione macchina è necessario specificare il codice
macchi](./media/c la quantità di macchine della medesima tipologia e infine
valorizzare le proprietà macchina.

#### P](./media/cESSI - MATERIALI

![img](configurazione-processi-materiali.png))
](./media/c
È possibile associare un materiale al processo, specificando la categoria di materiale e quindi il materiale specifico e infine l'utilizzo che se ne farà del materiale. Inoltre, dovranno anche essere valorizzate le proprietà di interesse, associate alla categoria di materiale selezionato.

Nella ](./media/cione `Utilizzo Materiale` viene specificata la tipologia di materiale. Le categorie standard sono le seguenti:

![img](configurazione-processi-crea-specifica-materiale.png))

Quelli che troviamo maggiormente all'interno di un ordine di produzione sono: `Produced`, ovvero il prodotto finito/semilavorato che corrisponde al risultato della corrispettiva fase, `Consumed`, ovvero tutti i materiali dei quali si tiene registrata la quantità precisa rimasta/utilizzata (Es. tappi, scatole…) e infine `Consumable`, ovvero tutti i materiali la quale quantità non è registrata e viene calcolata in modo approssimativo (Es. colla, nastro adesivo…). Le restanti categorie sono: `Scrap`, che corrisponde al materiale non congruo con il risultato previsto e quindi considerato uno scarto, `Tool`, ovvero gli utensili e `Swarf`, il materiale di scarto che viene rilasciato durante la lavorazione.

#### PROCESSI - PERSONALE

![img](configurazione-processi-personale.png))

Un processo può essere associato a del personale specifico o a categorie di personale, in base alla selezione effettuata mediante radio button (vedi figura seguente). In relazione alla selezione effettuata, possono essere quindi valorizzate le relative proprietà.

![img](configurazione-processi-modifica-personale.png))

##### DIPENDENZE

In questa sezione è possibile descrivere delle relazioni di dipendenza tra processi. Nei campi `Tipologia di Processo` e `Prossima tipologia di processo` vanno inseriti i codici dei due processi su cui specificare la dipendenza. Il campo `Tipo Dipendenza` indica la relazione tra i due processi.

![img](configurazione-processi-modifica.png))

![img](configurazione-processi-modifica-tipo-dipendenze.png))

### CICLI DI LAVORAZIONE

I cicli di lavorazione definiscono i processi e le macchine richieste per ottenere dei prodotti finiti.

Nella parte sinistra della pagina è presente l'elenco dei prodotti ottenuti come risultato di uno o più cicli di lavorazione.

Ciascun record di questa tabella è caratterizzato da un codice materiale (che identifica il prodotto), una versione, una descrizione, una o più locazioni (magazzini) in cui può essere stoccato il prodotto, la data di pubblicazione e lo stato (abilitato/disabilitato). Nella parte bassa della pagina sono presenti delle schede per l'associazione al prodotto selezionato di proprietà (vengono mostrate le proprietà valorizzabili, associate ai processi selezionati all'interno dei cicli di lavorazione relativi al prodotto corrente), macchine, personale e dipendenze (definiscono le relazioni tra i processi selezionati all'interno dei cicli di lavorazione).

![img](configurazione-cicli-di-lavorazione.png))

A ciascun prodotto può essere associato uno o più cicli di lavorazione per la sua produzione.

Per la creazione di un nuovo ciclo di lavorazione cliccare sul bottone evidenziato nell'immagine sottostante e quindi selezionare il processo da utilizzare dalla nuova tabella apparsa a video.

![img](configurazione-cicli-di-lavorazione-tecnologia.png))

A questo punto andrà in esecuzione un Wizard per la creazione del ciclo di lavorazione vero e proprio:

![img](configurazione-cicli-di-lavorazione-wizard.png))

Inserire la descrizione e settare le seguenti impostazioni: AGGIUNGI UN PRODUCTED DEFAULT, AGGIUNGI LEGAME FASE PRECEDENTE, AGGIUNGI LEGAME COSUMED/PRDUCED DA FASE PRECEDENTE.

![img](configurazione-cicli-di-lavorazione-wizard-step1.png))

Impostare una durata (in secondi) del ciclo di lavorazione:

![img](configurazione-cicli-di-lavorazione-wizard-step2.png))

Selezionare le macchine coinvolte nella lavorazione:

![img](configurazione-cicli-di-lavorazione-wizard-step3.png))

Valorizzare le proprietà:

![img](configurazione-cicli-di-lavorazione-wizard-step3.png))

A questo punto la procedura sarà terminata:

![img](configurazione-cicli-di-lavorazione-wizard-step4.png))
