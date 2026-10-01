
# GESTIONE GRIGLIE

All'interno del software *MASTER Factory^®^* sono presenti delle potenti griglie di visualizzazione dati, che permettono di ricercare, ordinare, stampare i dati, così come gestire gli elementi da visualizzare, incluso la loro formattazione. Di seguito sono riportate le principali funzioni.

Le griglie si suddividono in 2 macro-categorie:

1. GRIGLIA SEMPLICE
2. GRIGLIA MODIFICABILE

## GRIGLIA SEMPLICE

Cliccando con il tasto destro del mouse su questa tipologia di griglia apparirà il seguente menù di scelta rapida, con le funzionalità di seguito descritte:
![a](menu-contestuale-griglia.png))

### ORDINAMENTO

Per ordinare i record in base ai valori di una colonna in modo
ascendente fare clic sull'intestazione della colonna. I successivi clic
sulla stessa colonna alterneranno l'ordinamento discente e ascendente.

Lo stesso risultato si ottiene premendo il pulsante destro in prossimità
della colonna selezionata e selezionare:

-![Ordina Crescente](ordina-crescente.png)) *Ordina Crescente*
-![Ordina Decrescente](ordina-decrescente.png)) *Ordina Decrescente* dal menu di scelta rapida visualizzato.

### RAGGRUPPAMENTO

Per raggruppare secondo il valore di una o più colonne, cliccare su![Show Group By Box](group-by-this-column.png)) `Show Group By Box` in modo da visualizzare il pannello ove poter trascinare le colonne da raggruppare, poi effettuare una delle seguenti operazioni:

1. Trascina un'intestazione di colonna all'interno del pannello del gruppo dove indicato dalle frecce![Arrows Group By This Column](arrows-groupby-columns.png)).
2. Fare clic con il pulsante destro del mouse sull'intestazione di una colonna e selezionare![Group By This Column](group-by-this-column.png)) `Group By This Column` dal menu di scelta rapida.
![Raggruppamento](raggruppamento-trascina.png))

Ecco il risultato ottenuto tramite il raggruppamento:
![Raggruppamento](raggruppamento-risultato.png))

Per separare i dati da una colonna di raggruppamento, effettuare una delle seguenti operazioni:

1. Trascina un'intestazione di colonna dal pannello del gruppo al pannello dell'intestazione della colonna.

2. Fare clic con il pulsante destro del mouse sull'intestazione di una colonna nel pannello di raggruppamento e selezionare![Group By This Column](group-by-this-column.png)) `UnGroup` dal menu di scelta rapida.

Cliccando con il tasto destro del mouse, nell'area del pannello di raggruppamento, si aprirà il sottostante menù di scelta rapida:
![Menu contestuale raggruppamento](menu-contestuale-raggruppamento.png))

Cliccando su![Cancella raggruppamento](cancella-raggruppamento.png)) `Clear Grouping` tutti i raggruppamenti verranno eliminati.

Cliccando su![a](full-expand-raggruppamento.png)) `Full Expand` e![a](full-collapse-raggruppamento.png)) `Full Collapse` si può aprire e chiudere tutti i raggruppamenti, mentre cliccando su![a](nascondi-pannello-raggruppamento.png)) `Hide Group By Box` si nasconde il pannello di raggruppamento.

### GESTIONE COLONNE

#### NASCONDERE O VISUALIZZARE COLONNE

Per nascondere una colonna cliccare sul tasto `Hide This Column`; mentre per ripristinarla o visualizzare colonne nascoste cliccare sul tasto![a](image24.png)) `Column Chooser` e si aprirà una *form* con l'elenco delle colonne nascoste; per aggiungerle alla griglia si dovrà effettuare un drag and drop nella posizione in cui si desidera visualizzarle.

#### ADATTARE COLONNE AL CONTENUTO

Per adattare la colonna al contenuto, cliccare dal menù di scelta rapida sul tasto![a](image25.png)) `Best Fit`; mentre per adattarle tutte cliccare sul tasto `Best Fit (All Column)`

### FILTRAGGIO DATI

Per filtrare una colonna in base al suo contenuto, passare con il puntatore del mouse sopra l'intestazione della colonna, apparirà la seguente icona![a](image26.png)): cliccandoci sopra, si aprirà una tendina riportante tutti i valori distinti presenti nella colonna e spuntandoli la griglia si filtrerà in base al valore prescelto.
![Filtro dati](filtro-dati.png))

Qualora sia necessario eseguire delle ricerche più ristrette, utilizzare la tab *Filtri di testo* al posto della tab *valori.*
![Filtro dati - Text Filters](filtro-dati-text-filters.png))

Questa scelta permette all'operatore di eseguire ricerche con condizioni più accurate quali:

- È uguale a
- Non è uguale a
- Inizia con
- Si conclude con
- Contiene
- Non contiene
- È vuoto
- È non vuoto
- Filtro personalizzato (tramite questa opzione si esegue un'operazione logica di AND o OR tra due delle condizioni in elenco)

In alternativa a quanto sopra descritto, cliccando dal menu di scelta rapida `Show Auto Filter Row` si visualizza un campo di ricerca in testa a ogni colonna.
![Filtro dati - rapido](filtro-dati-rapido.png))

Per eseguire una ricerca globale su tutte le colonne della griglia, attivare dal menu di scelta rapida la visualizzazione del pannello di ricerca tramite il tasto `Show Find Panel`.
![Filtro dati - ricerca globale](filtro-dati-ricerca-globale.png))

### RICERCA TRAMITE FILTRO AVANZATO

Sul pannello dei filtri avanzati, cliccando sul tasto![a](icona-filtro.png)) `Filter Editor` nel menu di scelta rapida, il *tool* disponibile permette di comporre delle logiche di condizioni avanzate:
![Filtro dati - editor filtri](filtro-dati-editor-filtri.png))

1. Permette di aprire il menu di scelta rapida per inserire delle condizioni logiche:
  ![a](image35.png))
2. Permette di scegliere il campo su cui applicare la condizione di ricerca.
3. Visualizza tutti gli operatori disponibili:
  ![a](editor-filtri-operatori-disponibili.png))
4. Termine di ricerca.
5. Permette di eliminare la condizione.

## GRIGLIA MODIFICABILE

La griglia modificabile eredita parte delle caratteristiche da quella base. Pertanto, la visualizzazione mostra solo le nuove funzionalità, sottintendendo le altre. Cliccando su un punto qualsiasi della griglia con il tasto destro del mouse si apre il menu di scelta rapida sotto riportato.
![Griglia - menu contestuale modifica](griglia-menu-contestuale-modifica.png))

### PERSONALIZZAZIONE LAYOUT

Per personalizzare il layout nella griglia, dal menu di selezione rapida cliccare sul tasto funzionale ![Griglia - Personalize Layout Grid](./media/griglia-personalize-layout-grid.png) `Personalize Layout Grid`. Il configuratore per la personalizzazione del layout della griglia si presenta suddiviso in schede:
![Griglia - configurazione](griglia-configurazione.png))

#### SCHEDA: VISIBILE

In questa scheda si esegue la modifica all'elenco delle colonne, in modo da selezionare quelle che si desidera visualizzare nella griglia o viceversa. I dati in esse contenuti saranno visibili in relazione al contesto della griglia stessa.

##### RENDERE VISIBILE UNA COLONNA NASCOSTA

Tramite la spunta sulla prima colonna del box "Colonne Nascoste", si selezionano le colonne che si desidera visualizzare, poi si clicca sul tasto![Griglia configurazione - Visualizza colonna](configura-griglia-visualizza-colonna.jpg)).

##### RENDERE VISIBILI TUTTE LE COLONNE NASCOSTE

Cliccare sul tasto![Griglia configurazione - Visualizza colonna](configura-griglia-visualizza-tutte-le-colonne.jpg)).

##### NASCONDERE UNA COLONNA VISIBILE

Tramite la spunta sulla prima colonna del box "Colonne Visibili", selezionare le colonne che si desidera nascondere, poi cliccare sul tasto![a](configura-griglia-nascondi-colonna.jpg)).

##### NASCONDERE TUTTE LE COLONNE VISIBILI

Cliccare sul tasto![a](configura-griglia-nascondi-colonna.jpg)).

#### SCHEDA: PROPRIETÀ

In questa scheda è possibile modificare i layout grafico delle singole
colonne agendo sulle seguenti proprietà:

| Voce | Descrizione |
| :--- | :----- |
| Dimensione | Permette d'impostare la dimensione del font |
| Grassetto | Imposta il testo in grassetto |
| Italico | Imposta il testo in corsivo |
| Nome | Nome del font che si desidera applicare |
| Sottolineato | Imposta il testo sottolineato |
| Colore cambio valore | Permette d'impostare la colorazione a righe alternate a ogni cambio valore della colonna selezionata |
| Colore 1 | Colore della prima riga |
| Colore 2 | Colore della riga successiva dopo aver cambiato valore |
| Allineamento del testo orizzontale | Permette di settare la posizione orizzontale del testo all'interno della cella |
| Default | Il sistema allinea a sinistra tutti i valori a eccezione di quelli numerici |
| Near | Il testo viene allineato a sinistra |
| Center | Il testo viene allineato al centro |
| Far | Il testo viene allineato a destra |
| Allineamento del testo verticale | Permette di settare la posizione verticale del testo all'interno della cella |
| Default | Il sistema allinea in modo automatico il testo |
| Top | Il testo viene allineato in alto |
| Center | Il testo viene allineato al centro |
| Bottom | Il testo viene allineato in basso |
| Colore sfondo | Permette d'impostare il colore dello sfondo della colonna |
| Colore sfondo 2 | Se impostato permette di creare una sfumatura che va dal colore della colonna al colore2 |
| Colore testo | Permette d'impostare il colore del carattere |
| Direzione sfumatura | Permette di settare la direzione della sfumatura |
| Horizontal | Sfumatura orizzontale |
| Vertical | Sfumatura verticale |
| ForwardDiagonal | Sfumatura diagonale a destra |
| BackwardDiagonal | Sfumatura diagonale a sinistra |
| Unisci valori Identici | Raggruppa in una unica cella tutti i valori identici |

#### SCHEDA: REGOLE COLORAZIONE

Questa scheda permette di personalizzare un layout secondo una specifica formula.
![Griglia - regole colorazione](griglia-regole-colorazione.png))

Per impostare una formula come regola di formattazione cliccare sul tasto![Griglia - icona nuova regola](griglia-icona-nuova-regola.png)), che comanda l'apertura dell'editor di espressione.
![Griglia - editor espressioni](griglia-editor-espressioni.png))

L'editor di espressioni supporta una varietà di funzioni matematiche - data, ora, stringa, logica - e permette di creare delle condizioni per le quali vanno applicate le proprietà settate nel riquadro `Aspetto della regola corrente`.

**Esempio**:

Supponiamo di voler imporre come sfondo della riga il colore giallo ed evidenziare in grassetto i valori `Larghezza` quando maggiori di 8. Dall'editor di espressioni procedere con i seguenti passaggi:

1. Selezionare `Fields` (box lista tipi oggetti in basso a sinistra)
2. Selezionare il campo `Larghezza` con un doppio click (box lista oggetti in basso al centro)
3. Selezionare `Operators` (box lista tipi oggetti in basso a sinistra)
4. Selezionare l'operatore con un doppio click (box lista oggetti in basso al centro)
5. Terminare con il valore 8 l'espressione composta (box in alto)
6. Confermare tramite il tasto `OK`
   **Nel box `Aspetto della regola corrente`**
7. Posizionarsi sulla proprietà colore sfondo e settare il colore giallo.
8. Posizionarsi sulla proprietà `Carattere`, poi spuntare la proprietà `Bold` per renderla attiva

il risultato così ottenuto è:
![Griglia - formattazione colori](griglia-formattazione-colori.png))

Nel caso si desideri applicare tale regola alla sola colonna `Lunghezza`, dalla *form* `Regole Colorazione` selezionare la colonna  applicare la formattazione dal menu a tendina `colonna`. In alternativa, spuntare `Applica a intera riga` per ripristinare quanto ottenuto con l'esercizio precedente.

#### SCHEDA: ORDINAMENTO

Nella scheda ordinamento è possibile settare l'ordinamento che la griglia dovrà avere. In aggiunta, è possibile salvare una lista di ordinamenti personalizzati, applicabili a richiesta.

Utilizzare i tasti![Griglia - ordinamento](griglia-aggiungi-elimina-colonna-ordinamento.png)) per aggiungere/eliminare una nuova colonna come argomento di riordino, oppure![Griglia - elimina tutti gli ordinamenti](griglia-elimina-tutte-colonne-ordinamenti.png)) per eliminarle tutte.

Una volta inserita nuova colonna sarà possibile assegnare il campo su cui applicare l'ordinamento e il relativo criterio (Ascendente o discendente).
![Griglia - schermata ordinamento](griglia-schermata-ordinamento.png))

Al termine della creazione delle regole di ordinamento cliccando sul tasto![a](griglia-salva-ordinamento.png)) è possibile salvare questa configurazione per crearne altre nuove in seguito. L'elenco dei criteri di ordinamento salvati è visibile, e utilizzabile su richiesta, dal menù a tendina "Ordinamenti". Per eliminare un criterio precedentemente salvato, dopo averlo selezionato, cliccare sul tasto![a](griglia-elimina-ordinamento.png)).

#### SCHEDA: COLONNE CON FORMULA

In questa scheda è possibile creare nuove *colonne calcolate* - ossia dove il valore è il risultato dell'elaborazione di un dato proveniente da una o più colonne -, o modificare quelle esistenti, applicando delle funzioni personalizzate

> [!Note]
> Il contenuto delle colonne selezionate è subordinato al contesto in cui la colonna viene utilizzata.

Per creare una nuova *colonna calcolata* cliccare sul tasto![Griglia - nuova colonna calcolata](griglia-nuova-colonna-calcolata.png)); per modificarne una già esistente cliccare sul tasto ![Griglia - modifica colonna calcolata](./media/griglia-modifica-colonna-calcolata.png). Tale operazione
comanda l'apertura della maschera contenente i campi sotto riportati:

| Nome Colonna | Impostare il nome della nuova colonna |
| ---- | ---- |
| Funzione | Inserire la funzione da impostare sulla colonna da creare tramite il tasto![Griglia - funzione colonna calcolata](griglia-funzione-colonna-calcolata.png)), che apre l'editor di espressione (descritto in precedenza) |
| Tipo | Impostare il tipo di dato che la colonna deve contenere (String, Integer…) |

**Esempio**:

Supponiamo di avere a disposizione due campi "Larghezza" e "Altezza" e di voler creare un campo calcolato che si chiama "Area":

1. Andare nella scheda "Colonna con formula"
2. Cliccare sul tasto![a](griglia-nuova-colonna-calcolata.png))
3. Inserire come "Nome colonna" AREA
4. Cliccare sul tasto![a](griglia-funzione-colonna-calcolata.png)) e comporre la seguente funzione `Larghezza * Altezza`
5. Selezionare Come tipologia di dato `Integer`
6. Confermare il tutto tramite il tasto `SALVA`

Ora nella griglia è presente un *campo calcolato* denominato AREA che rappresenta la moltiplicazione tra larghezza e altezza.

#### SCHEDA: IMPOSTAZIONI GRIGLIA

Permette di settare il layout generico della griglia.

| RIGA ATTIVA | |
| :--- | :-- |
| Colore Sfondo 2 riga attiva | Quando è impostato, il colore della riga attiva sfuma sul colore settato in questo parametro |
| Colore Sfondo riga attiva | Colore della riga attiva |
| Colore Testo riga attiva | Colore del testo nella riga attiva |

| RIGA SELEZIONATA | |
| :---- | :---- |
| Colore Sfondo 2 riga selezionata | Quando è impostato, il colore della riga selezionata sfuma sul colore settato in questo parametro |
| Colore Sfondo riga selezionata | Colore della riga attiva |
| Colore Testo riga selezionata | Colore del testo nella riga attiva |

| VARIE | |
| Colore Sfondo 2 riga selezionata | Quando è impostato, il colore della griglia sfuma sul colore settato in questo parametro |
| Colore Sfondo riga selezionata | Colore della griglia |
| Colore Testo riga selezionata | Colore del testo nella griglia |
| Consenti Unione Valori Identici | Quando è impostato, raggruppa tutti i valori identici di una colonna in un'unica cella |
| Font Griglia | Permette di settare tutti i parametri riguardanti i font
della griglia |

#### SCHEDA: INFO

In questa scheda è presente il solo campo RefID che mostra l'identificativo univoco della griglia.

### ADATTA DIMENSIONE

Il tasto![Griglia - adatta dimensioni](griglia-adatta-dimensioni.png)) `Adatta dimensioni` permette di adeguare la larghezza delle colonne secondo il loro contenuto.

### FILTRA

Il tasto![Griglia - icona filtro](icona-filtro.png)) `Filtra` permette di aprire l'editor per creare delle logiche di filtraggio dati.

### RESET LAYOUT

Il tasto "Reset Layout" permette di ripristinare la griglia secondo il suo settaggio di default, ripristinando tutti i valori modificati nella sezione "Personalizza layout griglia". Per attivare questa operazione è necessario che la *form* in cui si trova la griglia sia chiusa e riaperta.

### STAMPA

Il tasto![Griglia - Stampa](griglia-stampa.png)) `Stampa` permette di aprire l'anteprima di stampa della griglia.

### ESPORTA IN EXCEL

Il tasto![Griglia - Esporta excel](griglia-esporta-excel.png)) `Esporta Excel` permette di esportare i valori della griglia in excel.

### ESPANDI GRUPPO

Nelle griglie in cui vi sono dei sotto raggruppamenti, nel menu di scelta rapida appare il tasto o![Griglia - espandi dettagli](griglia-espandi-dettagli.png)) `Espandi tutto` permette di aprire tutti i dettagli in click solo.

### COMPRIMI GRUPPO

Nelle griglie in cui vi sono dei sotto raggruppamenti, nel menu di scelta rapida appare il tasto o![a](griglia-raggruppa-dettagli.png)) *`Comprimi tutto` permette di comprimere tutti i dettagli in click solo.
