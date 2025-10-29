##### --- Lezione 8 ottobre 2025 ---



###### VERIFICA E VALIDAZIONE

Sono due termini simili, entrambi devono valutare e misurare il corretto funzionamento del Software.

Esistono diverse tipologie di questi due.

**Verifica**: mostra che un sistema è conforme alle sue specifiche. (se nella prima fase abbiamo estratto delle specifiche, vediamo se dopo la fase di progettazione e modellazione effettivamente fa queste cose). Non possiamo essere soddisfatti dopo la fase di verifica perché non sappiamo effettivamente al cliente va bene.

**Validazione**: dimostrazione che un sistema soddisfa le aspettative di un cliente.

L'ispezione e la revisione può essere effettuata in qualsiasi momento della fase del processo Software.



La tecnica più utilizzata è quella del testing, do al Software con degli Input per vedere se da gli Output attesi. In piccoli progetti si fa test anche durante lo sviluppo.



TEST

-- diagramma



**Test dei componenti**: come linee di codice, file, classi, intero componente Software per vedere se funziona.

Un componente è l'unità fondamentale del Software.

Il componente viene testato singolarmente **in isolamento** simulando il resto del Software che non è disponibile.



**Test del sistema**

Testare il sistema completo, come verrà distribuito, apre ad una criticità: passaggio dal test delle singole componenti al componente totale.

Integrazione:

Maggiore è la complessità finale, più integrazioni verranno fatte durante il processo di Software-



**Test del cliente**

Test del sistema finale con i dati reali del cliente e test con il cliente.



La fase di testing è iterativa, se trovo un errore torno al passo precedente ritestando il componente, e lo è finchè l'utente finale non è soddisfatto.



###### EVOLUZIONE

Il Software continua ad essere di competenza anche una volta uscito.

Adattamento del Software a diverse esigenze di mercato, lo fa evolvere anche per correggere degli errori della versione finale.



Sempre meno Software è totalmente nuovo, c'è sempre una base esistente o librerie (o componenti Software riusabili).

Il Software è modificato continuamente nella sua vita, in base ai nuovi vincoli.

Avviene in diverse fasi



Può avvenire dopo il rilascio per:\\

* correzione di difetti
* migliorare qualità del Software
* adattare il sistema ai mutamenti del sistema operativo

Queste attività fanno evolvere il sistema in nuovi sistemi.



##### MODELLI DI PROCESSI SOFTWARE

***Definizione*** **modello del ciclo di vita del software** (CVS) di W. Scacchi: “Un modello del ciclo di vita del software è una caratterizzazione descrittiva o prescrittiva di come un sistema software viene o dovrebbe essere sviluppato”.



Definizione standard IEEE: "framework che contiene processi, attività e task che fanno parte dello sviluppo di un prodotto Software che va dalla definizione dei requisiti alla terminazione del suo uso".





PROCESSO VS. MODELLO

Non esiste un processo universale, spiegazione di un modello ad alto livello e istanziato poi nel concreto in maniera differente.

Il modello cerca di descrivere semplicemente



Una volta conosciuti si possono estendere e adattarli ad un'esigenza reale.



PUNTI DI VISTA DEL PROCESSO

Ogni processo ha diverse possibili descrizioni:

* architetturali: descrizione della sequenza delle attività senza fornire dettagli sulle specifiche attività
* data-flow: come vengono trasformati i dati durante il processo
* role/action: si focalizza sulle persone, definisce i ruoli e le responsabilità delle persone coinvolte nel processo



DESCRIZIONE PROCESSO SOFTWARE

La descrizione del processo Software include:

* **Attività** da svolgere e l'ordine e l'ordine tra le attività
* **Prodotti** risultanti da ciascuna attività
* **Ruoli** persone coinvolte nel processo e le loro responsabilità
* **Pre e Post-condizioni**: per iniziare un'attività devo avere delle pre-condizioni e al termine dell'attività voglio che si siano realizzate delle post-condizioni



COME SCEGLIERE IL MODELLO - SCELTA DEL MODELLO

Ci sono differenti tipi di modelli adatti a diversi tipi di prodotto, due tipologie per il corso:

* **plan-driven** ogni fase è ben definita (può entrare una strategia agile nelle piccole attività)
* **agili**





MODELLO A CASCATA

Primo modello, per le sue caratteristiche percepito come vetusto, applicato allo sviluppo Software di tutti i giorni.

Processo **plan-driven**: ciascuna fase segue quella precedente, va tutto deciso in anticipo prima di iniziare lo sviluppo del Software.

Gli Output di una fase sono gli Input della fase successiva.

Le fasi riflettono le attività di sviluppo fondamentali del Software.

È un processo **centrato sui documenti**: è fondato sulla produzione di documentazione che rende tracciabile l'intero andamento del processo, al termine di ogni fase produco un documento (il dettaglio lo decide il processo), che venga approvato (se non approvato, rifaccio la fase) e la fase successiva è congelata finché non riceve il documento approvato della fase precedente.

È un processo **rigido**, i prodotti di una fase validata non sono più modificabili, se non attraverso un processo formale e sistematico di modifica. La fine di ogni fase è un punto rilevante del processo (milestone). Definizione di milestone è importante per valutare l'avanzamento del processo.

È un processo **monolitico**, il cliente interagisce con il Software solo al termine della cascata (scopro solo al termine se il processo ha degli errori).



Vantaggi

* fasi ben definite
* Output di ogni fase sono precisamente individuati

Svantaggi

* Richiede una conoscenza completa, immediata e stabile di tutti i requisiti (nel mondo reale i requisiti possono variare durante lo sviluppo)
* Time to Market: sviluppo di eccessiva documentazione, spesso non richiesta, genera perdita di tempo
* Poco flessibile: se durante il ciclo di sviluppo del processo bisogna gestire modifiche (problemi o requisiti) bisogna aprire un processo formale di modifica

Il modello è adatto a Software che richiedono documentazione, a sistemi integrati dove il Software deve interfacciarsi con sistemi hardware non flessibili.

Non è adatto se i requisiti cambiano rapidamente o se si lavora in piccoli team.



Il modello a cascata è adatto se i requisiti sono ben chiari dall'inizio e non cambino i requisiti nel processo.



MODELLO A CASCATA CON RETROAZIONE

In ciascuna fase viene introdotta la retroazione (feedback), così, se nella fase successiva ci si accorge che c'è un problema posso tornare nella fase precedente.

La retroazione mitiga la monoliticità del processo a cascata: non devo attendere il termine del processo per modificare il prodotto, non lo rende completamente flessibile.

Modello utile quando il processo avrà pochi cambiamenti nel percorso.



MODELLO A V

Estensione del modello a cascata.

team di progettazione e team di testing che possono lavorare in parallelo.

Ramo superiore dove c'è la fase di progetto e un ramo inferiore con le fasi di verifica e validazione. Tendenzialmente due team differenti che vanno a collaborare tra loro.

Nella specifica dei requisiti e di sistema siamo già in grado di sviluppare un grado di test per il cliente, può anticipare la validazione.



##### --- Lezione lunedì 13 ottobre 2025 ---



###### MODELLI EVOLUTIVI

Modelli chiari a contesti dove i requisiti non sono congelabili all'inizio del processo, due macromodelli:

* sviluppo/consegna incrementale: lavoro con il cliente per sviluppare i requisiti iniziali, evolvere con iterazioni durante il processo, raffinamenti successivi con il cliente per arrivare al prodotto finale
* modello prototipale: capire quali sono i requisiti del sistema, sviluppando il prototipo per capire quali sono i requisiti del sistema



MODELLO A SVILUPPO INCREMENTALE

diagramma

Sviluppata un'implementazione iniziale, sviluppo i requisiti, avviene in contemporanea la fase di sviluppo e testing, dove rilascio degli incrementi (versioni successive) fino ad arrivare alla versione finale.

Parte da pochi requisiti ben compresi o da una descrizione sommaria degli stessi.

Attività di specifica, sviluppo e convalida sono intrecciate, con feedback veloci tra le attività.

La versione iniziale implementa i requisiti della descrizione sommaria e viene esposta agli utenti (clienti o proxy di clienti), più semplice dare feedback su una versione iniziale (come demo).

L'utente suggerisce ulteriori funzionalità e requisiti che sono implementati in versioni intermedie successive, solitamente non mostrate al cliente.

La versione finale rappresenta l'ultimo incremento del sistema rilasciata al cliente e corrisponde ad un'evoluzione della versione iniziale.



MODELLO A CONSEGNA INCREMENTALE

Il sistema viene consegnato a incrementi, non vengono attese versioni finali da rilasciare al cliente (non per forza tutti), vengono consegnati al cliente e installati nel loro ambiente operativo gli incrementi.

**Vantaggio**: feedback più realistico, il cliente testa il sistema effettivamente

**Limitazione**: il cliente non ha competenze-tempo per dare dei feedback corretti all'incremento

Ogni incremento rilascia una parte definita delle funzionalità richieste, in aggiunta alle precedenti. Con il cliente vengono definiti i requisiti da rilasciare prima, assegnando delle priorità, nel mentre gli altri requisiti possono evolvere.



diagramma

Parto da una descrizione sommaria dei requisiti, andando a fare un planning: assegnare ciascun requisito a uno o più incrementi, pianificando le versioni da sviluppare.

La convalida viene fatto a ciascun incremento.

Svolgo integration test e test di sistema complessivo, ottengo una versione successiva.



CONSEGNA VS SVILUPPO INCREMENTALE

Nello sviluppo incrementale la valutazione della prima versione è effettuata da un proxy del cliente, le versioni intermedie non sono tendenzialmente rilasciate al cliente.

La consegna incrementale permette una valutazione più realistica.



Vantaggi (di entrambi):

* ho un feedback sulla versione preliminare, invece di far validare una versione di progetto immaginaria
* possibilità di cambiare i requisiti prima della consegna finale
* possibilità di consegnare versioni preliminari con le funzionalità fondamentali
* possibilità di utilizzare una versione intermedia per capire i requisiti poco chiari dell'incremento successivo

Problemi

* il processo è più fumoso, non ho il tempo di fare una documentazione ad ogni incremento, minore visibilità di ciò che è stato fatto ad ogni incremento
* software mal strutturato per continui cambiamenti e aggiunte, dal momento che non seguo un piano specifico

Applicabilità

* quando i componenti sono di piccoli-medie dimensioni
* sistemi destinati a vita breve
* quando mi interfaccio con requisiti fortemente volatili



MODELLO PROTOTIPALE

Prototipo: versione iniziale di un intero sistema o di parte di esso.

Viene sviluppato rapidamente per contenere i costi e poter sperimentare con il cliente prima della consegna, nelle fasi iniziali del processo.

Il prototipo è usa e getta, dev'essere scartato dopo la validazione perchè non rappresenta una buona base per sviluppare il sistema finale.

Anche se realizza le funzionalità richieste potrebbe non rispettare vincoli fondamentali e potrebbe non avere documentazione.

La rapidità di sviluppo e frequenti modifiche ne deteriora la qualità.



diagramma

Bisogna stabilire gli obiettivi del prototipo all'inizio del processo, se gli obiettivi non sono chiari gli utenti finali possono fraintendere la funzione del prototipo e la prototipazione risulta inefficace.

Devo circoscrivere le funzionalità del prototipo, definisce lo schema architetturale del prototipo. Ci permette di avere un focus sulle attività critiche per svilupparlo nel minor tempo possibile.

Il valutatore dev'essere formato sull'utilizzo di ogni prototipo prima della valutazione.

Problemi della rappresentatività:

* prototipo non è parte del sistema reale
* i valutatori potrebbero essere non rappresentativi degli utenti finali
* il modo di usare il prototipo può differire dall'utilizzo del sistema reale



immagine

Lo sviluppo prototipale può essere integrato all'interno di altri cicli di vita classici (può essere usato per identificare, validare e raffinare i requisiti).



immagine

uso i requisiti estratti dalla fase di prototipazione con più modelli di progettazione



BACK-TO-BACK TESTING

immagine

Il prototipo può essere utilizzato nella fase di validazione per controllare che il sistema sviluppato si comporti come modellato ne prototipo nelle fasi iniziali del progetto.

Comparo i risultati del prototipo del sistema e del sistema applicativo, per capire dov'è il problema nel codice



MODELLI ORIENTATI AL RIUSO

Il riuso non avviene solo in maniera informale, può anche essere un approccio sistematico.

Approccio orientato al riuso:

* componenti software riutilizzabili
* interi sistemi

Sfrutta framework di integrazione, software che consentono di comporre i componenti per creare il sistema finale che si adattano ai requisiti del cliente.

Approccio diffuso grazie a standard per la specifica dei componenti.



immagine-diagramma

Requisiti essenziali specificati in maniera non eccessivamente dettagliata.

Vengono ricercati componenti e sistemi che possono fornire le funzionalità dei requisiti, i candidati vengono valutati per vedere se soddisfano i requisiti essenziali e se sono disponibili per essere utilizzati.

I requisiti vengono perfezionati usando le informazioni sulle applicazioni e componenti riutilizzabili che sono stati trovati, la specifica viene aggiornata con i requisiti perfezionati.

Verifico se ci sono sistemi interamente disponibili o singole componenti, nel caso dove ho un sistema configurabile che mi realizza le funzionalità lo adatto, nel caso ci siano delle componenti le posso adattare e svilupparle da me, integrandole nel sistema finale.



**Vantaggi**:

* riduce la quantità di codice da sviluppare da capo
* riduce costi e rischi
* maggiore velocità di consegna

**Svantaggi**:

* compromessi nei requisiti --> sistema potrebbe non soddisfare tutte le reali necessità degli utenti
* evoluzione dei componenti non controllata direttamente (se la libreria cambia le interfacce potrei esser fregato)



MODELLI TRASFORMAZIONALI

sono dei metodi formali, definiscono con i linguaggi formali:

* specifiche algebriche
* modelli di stato

Usa tecniche di model checking per provare la correttezza.

Le specifiche formali sono trasformate in codice:

* la correttezza è preservata
* la verifica è ottenuta implicitamente



Un documento in linguaggio formale dei requisiti, presenta una comprensione chiara e non ambigua, le specifiche sono verificate automaticamente prima di essere trasformate da opportuni strumenti.



La descrizione formale viene astratta e dettagliata, fino a ottenere specifiche di basso livello eseguibili. Le trasformazioni, questo processo può trarre vantaggi da componenti riusabili, possono essere eseguite manualmente o supportate da appositi strumenti.



Problemi

* necessità di competenze specifiche in linguaggi formali
* difficile specificare formalmente alcune parti del sistema
* difficile per il cliente convalidare i requisiti

Applicabilità

* non adatti per sistemi di grandi dimensioni
* usati per parti critiche, dove la validità va dimostrata by construction



##### --- Lezione 15 ottobre 2025 ---

SVILUPPO AGILE DEL SOFTWARE

La necessità di essere agili nello sviluppo nasce da 3 segnali di un report del 2000:

* meno del 30% dei progetti software aveva successo
* progetti grandi fallivano più spesso
* solo metà delle feature richieste era effettivamente rilasciata

E dal problema di instabilità dei requisiti del software: molti progetti presentavano requisiti non chiari, instabili e variabili, il cliente si accorgeva di funzionalità da richiedere durante la fase di sviluppo.



###### SUCCESSI DEI PROCESSI PLAN-DRIVEN

Utilizzati ancora oggi per i progetti più critici (come il modello a V).



###### INSUCCESSI DEI PROCESSI PLAN-DRIVEN

ero in bagno



###### SVILUPPO RAPIDO NEL SOFTWARE

Contesto ricco dove ognuno può diventare sviluppatore, dove le opportunità hanno rapido cambiamento e presentano prodotti concorrenti, spesso è importante prevedere la prossima funzionalità richiesta dal mercato.

La **rapidità di sviluppo e consegna** è spesso il requisito più critico per i sistemi software.

Al termine degli anni 90 sono emersi i primi metodi agili per lo sviluppo software che erano mirati alla produzione software in tempo ridotto.



###### AGILITÀ

Hanno sviluppato il significato si **agilità**:

* Efficace risposta ai cambiamenti
* Efficace comunicazione fra tutti gli stakeholder
* Portare il cliente nel team di lavoro per avere feedback rapido

L'agilità consente di avere una rapida ed incrementale consegna del Software.



###### CARATTERISTICHE DEI METODI AGILI

**Documentazione minima**

* focus sul codice, invece che sulla progettazione
* niente specifiche dettagliate, avremo dei requisiti che evolvono con la comunicazione con l'utente e l'osservazione del mercato
* overhead di documentazione limitati (non si cancella ma striminzita)

**Consegna rapida ed incrementale**

* sistema sviluppato in incrementi rilasciati frequentemente, ogni due-tre settimane
* stakeholder coinvolti nella specifica e nella valutazione di ogni incremento, definendo insieme gli incrementi successivi

**Strumenti di supporto**

* utilizzo di strumenti al supporto del processo di sviluppo (come automatizzazione dei test)



###### PROCESSI PLAN-DRIVEN VS AGILI

* **Plan-driven**: processi dove le attività sono pianificate in anticipo e il loro avanzamento è misurato rispetto a quanto previsto dal piano. Fasi del processo Software sono distinte tra loro e gli output di ciascuna fase sono necessari per la fase successiva.
* **Agili**: pianificazione incrementale e continua durante lo sviluppo. Più facile modificare il processo per adeguarsi alle modifiche dei requisiti del cliente o del prodotto. Requisiti, progettazione e implementazione avvengono assieme.



###### PROCESSI PLAN-DRIVEN E AGILI

Pratiche plan-driven e agili possono coesistere nello stesso processo, ma in momenti diversi (o nello stesso momento):

* processi agili possono produrre documentazione di progettazione quando ritenuto necessario e possono includere attività pianificate. Lo scopo è di supporto per comunicazione e comprensione, sapendo che possono essere incompleti o imprecisi.
* processi plan-driven possono essere incrementali

Per grandi sistemi serve trovare un compromesso tra processi pianificati e processi agili.



DISCLAIMER: Gli incrementi esistono anche nei plan-driven.



PRINCIPI AGILI

Coinvolgimento del cliente: i clienti sono coinvolti in tutto il processo di sviluppo.

Intervengono a ciascuna iterazione del prodotto:

* valutano e validano l'iterazione
* forniscono nuovi requisiti del sistema o propongono modifiche alle iterazioni proposte
* assegnano priorità a ciascun requisito richiesto

Accettare cambiamenti

* prodotto non pianificato rigidamente
* prevedere che i requisiti possono cambiare

Mantenere semplicità

* prodotto e processo di sviluppo devono essere il più semplice possibile
* quando possibile, lavorare attivamente per eliminare le complessità dal sistema

Sviluppo incrementale

* software sviluppato incrementalmente
* cliente specifica i requisiti da includere in ciascun incremento

Persone, non processi

* processo di sviluppo non dev'essere fortemente prescrittivo
* membri del team devono essere liberi di sviluppare il software secondo i loro metodi
* membri del team devono poter sviluppare il software secondo i loro metodi (evitare standard inutili)



APPLICABILITÀ DEI METODI AGILI

* Per prodotti di piccoli o medie dimensioni, prodotti personalizzati per cui c'è un chiaro impegno del cliente nell'essere coinvolto nel processo di sviluppo.
* Prodotti dove ci sono pochi stakeholder e non bisogna rispettare rigidi regolamenti.
* Team fisicamente vicini: le comunicazioni informali e facilitate.



VANTAGGI

* consegne predicibili: impegno periodico
* rapida risposta ai cambiamenti dei requisiti
* rischi attenutati grazie ai cicli di consegna brevi
* sensazione di alta produttività
* clienti soddisfatti perché si sentono ascoltati e responsabilizzati
* il successo dei progetti evolve attraverso multiple brevi iterazioni



##### TECNICHE AGILI

###### METODI AGILI

Diverse proposte di metodi agili:

* Extreme Programming
* SCRUM
* Feature Driven Development
* Crystal
* DSDM

Ognuno di questi metodi propone un diverso processo, condividono gli stessi principi.



###### EXTREME PROGRAMMING

Metodo agile più conosciuto, spinge le  pratiche di sviluppo a un livello estremo.

Ha un approccio iterativo estremo ed ha piccoli e frequenti incrementi rilasciati al cliente.



immagine



Requisiti espressi come storie utente (scenario di utilizzo base del software per ottenere un risultato), per decidere quali funzionalità includere come incremento di sistema.

Scenari divisi in task (costituiscono le unità principali dell'implementazione) di sviluppo più semplici che vengono implementate direttamente.

La pianificazione è presente però è flessibile e non appesantita da documentazione eccessiva.

I programmatori lavorano a coppie (pair programming) e sviluppano test per ogni task prima di scrivere codice. Tutti i test devono essere eseguiti con successo quando il nuovo codice viene integrato nel sistema.

Il cliente è coinvolto nello sviluppo, valida la release corrente, fornisce requisiti nuovi o modificati, partecipa alla selezione delle storie utente, definisce i test di accettabilità.





Coinvolgimento del cliente: rappresentante del cliente on-site, parte del team di sviluppo.

Accettare i cambiamenti: quando un task viene concluso, viene integrato nel sistema.

Sviluppo incrementale: piccoli e frequenti rilasci che aggiungono in modo incrementale nuove funzionalità.

Mantenere la semplcità: progetto più semplice possibile che soddisfi i requisiti correnti e costante attività di miglioramento del codice (refactoring).

Persone, non processi: programmazione in coppia, proprietà collettiva del codice, sviluppo non richiede orari di lavoro eccessivamente lunghi e non sono accettabili troppi straordinari.



INFLUENZA DELL'EXTREME PROGRAMMING

XP come proposta originaria non è quasi mai adottato.

Non è pratico perché richiede un cambio radicale nel modo di lavorare di un'organizzazione.

Le pratiche chiave dell'XP hanno ispirato tutti gli approcci agili e spesso incorporate nei processi di sviluppo:

* storie utente
* refactoring
* sviluppo preceduto dai test
* pair programming





###### STORIE UTENTE

Chiamate anche scenari, descrivono i requisiti degli utenti come scenari d'uso dove l'utente dovrebbe trovarsi.

Descritte da cliente e team su schede (**story cards**) che il team di sviluppo suddivide in **task** da implementare.

I task rilevati sono la base per definire la pianificazione delle iterazioni e le stime dei costi.



In XP il cliente è parte del team ed il suo compito è prendere decisioni sui requisiti con il team.

Cliente e team definiscono una priorità e una stima dei costi per ciascuna storia, oltre ai criteri di accettazione.

Sulla base di queste informazioni, cliente e team scelgono le storie che saranno incluse nella prossima versione del prodotto.



**PRO**

* integrano la deduzione dei requisiti con lo sviluppo, invece di avere apposite attività di ingegneria dei requisiti, in modo da gestire i cambiamenti nei requisiti
* più semplice relazionarsi con storie utente, coinvolgendo così maggiormente l'utente
* ordinate in base a quelle che possono fornire un supporto utile all'azienda
* se i requisiti cambiano, vengono aggiunte story cards e le storie non ancora realizzate possono essere modificate o scartate

**CONTRO**

* stabilire se le storie utente coprono completamente i requisiti di sistema non è semplice
* descrizione incompleta del requisito: i clienti esperti potrebbero omettere scenari o task considerati ovvi



###### REFACTORING

Progettare pensando al cambiamento, riduce i costi di manutenzione futura.

XP rinuncia a gestire in anticipo i cambiamenti perché ritiene che le modifiche non si possano prevedere con certezza.

Fowler propone il termine di **refactoring** per rendere più semplice l'implementazione delle eventuali modifiche future, rappresenta un processo di miglioramento del codice che viene riorganizzato e riscritto per renderlo più efficiente e comprensibile, senza cambiarne le funzionalità.

* il team di sviluppo cerca proattivamente aspetti del software da migliorare e implementa i miglioramenti immediatamente
* il miglioramento può riguardare anche situazioni dove non c'è necessità immediata
* un codice di più alta qualità riduce la necessità di documentazione e facilita le modifiche future



PRO

* lo sviluppo incrementale tende a portare al deterioramento del codice, il refactoring continuo mitiga il deterioramento, migliorando la struttura e la leggibilità del codice
* esistenza di tool per automatizzare (o proporre suggerimenti) alcune operazioni di refactoring

CONTRO

* a volte il refactoring a livello di codice non basta per supportare un cambiamento, però è necessaria una modifica dell'intera architettura che è più costosa
* bisogna trovare un compromesso tra tempo dedicato allo sviluppo di nuove funzionalità e refactoring

##### 

##### --- Lezione 20 ottobre 2025 ---

###### REFACTORING

Progettare pens

###### 

###### SVILUPPO PRECEDUTO DAI TEST

Progettare pens



###### PAIR PROGRAMMING

Progettare pens

