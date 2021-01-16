---
title: Cosa può fare PHP?
parent: Iniziamo
nav_order: 2
---

# Cosa può fare PHP?
Ogni cosa. PHP si concentra principalmente sullo scripting lato server, quindi puoi fare tutto ciò che qualsiasi altro programma CGI può fare, come raccogliere dati di moduli, generare contenuti di pagine dinamiche o inviare e ricevere cookie. Ma PHP può fare molto di più.

Ci sono tre aree principali in cui vengono utilizzati gli script PHP.

* Scripting lato server. Questo è il campo di destinazione più tradizionale e principale per PHP. Hai bisogno di tre cose per farlo funzionare: il parser PHP (CGI o modulo server), un server web e un browser web. È necessario eseguire il server Web, con un'installazione PHP collegata. È possibile accedere all'output del programma PHP con un browser Web, visualizzando la pagina PHP tramite il server. Tutto ciò può essere eseguito sulla tua macchina domestica se stai solo sperimentando la programmazione PHP. Vedere la sezione delle istruzioni di installazione per ulteriori informazioni.
* Scripting della riga di comando. Puoi creare uno script PHP per eseguirlo senza server o browser. Hai solo bisogno del parser PHP per usarlo in questo modo. Questo tipo di utilizzo è ideale per script eseguiti regolarmente utilizzando cron (su * nix o Linux) o Utilità di pianificazione (su Windows). Questi script possono essere utilizzati anche per semplici attività di elaborazione del testo. Vedere la sezione sull'utilizzo della riga di comando di PHP per ulteriori informazioni.
* Scrittura di applicazioni desktop. PHP probabilmente non è il linguaggio migliore per creare un'applicazione desktop con un'interfaccia utente grafica, ma se conosci molto bene PHP e vorresti usare alcune funzionalità PHP avanzate nelle tue applicazioni lato client puoi anche usare PHP-GTK per scrivere tali programmi. Hai anche la possibilità di scrivere applicazioni multipiattaforma in questo modo. PHP-GTK è un'estensione di PHP, non disponibile nella distribuzione principale. Se sei interessato a PHP-GTK, visita »il suo sito web.

PHP può essere utilizzato su tutti i principali sistemi operativi, incluso Linux, molte varianti Unix (inclusi HP-UX, Solaris e OpenBSD), Microsoft Windows, macOS, RISC OS e probabilmente altri. PHP ha anche il supporto per la maggior parte dei server web oggi. Ciò include Apache, IIS e molti altri. E questo include qualsiasi server web che può utilizzare il binario PHP FastCGI, come lighttpd e nginx. PHP funziona sia come modulo che come processore CGI.

Quindi, con PHP, hai la libertà di scegliere un sistema operativo e un server web. Inoltre, puoi anche scegliere di utilizzare la programmazione procedurale o la programmazione orientata agli oggetti (OOP) o una combinazione di entrambe.

Con PHP non sei limitato all'output HTML. Le capacità di PHP includono l'output di immagini, file PDF e persino filmati Flash (utilizzando libswf e Ming) generati al volo. Puoi anche produrre facilmente qualsiasi testo, come XHTML e qualsiasi altro file XML. PHP può generare automaticamente questi file e salvarli nel file system, invece di stamparli, formando una cache lato server per il contenuto dinamico.

Una delle caratteristiche più forti e significative di PHP è il supporto per un'ampia gamma di database . Scrivere una pagina Web abilitata per database è incredibilmente semplice utilizzando una delle estensioni specifiche del database (ad esempio, per mysql), o utilizzando un livello di astrazione come PDO, oppure connettersi a qualsiasi database che supporti lo standard Open Database Connection tramite l'estensione ODBC. Altri database possono utilizzare cURL o socket, come CouchDB.

PHP supporta anche la comunicazione con altri servizi tramite protocolli come LDAP, IMAP, SNMP, NNTP, POP3, HTTP, COM (su Windows) e innumerevoli altri. Puoi anche aprire socket di rete non elaborati e interagire utilizzando qualsiasi altro protocollo. PHP supporta il complesso scambio di dati WDDX tra praticamente tutti i linguaggi di programmazione Web. Parlando di interconnessione, PHP supporta la creazione di istanze di oggetti Java e il loro utilizzo in modo trasparente come oggetti PHP.

PHP ha utili funzioni di elaborazione del testo , che includono le espressioni regolari compatibili con Perl (PCRE) e molte estensioni e strumenti per analizzare e accedere ai documenti XML. PHP standardizza tutte le estensioni XML sulla solida base di libxml2 ed estende il set di funzionalità aggiungendo il supporto SimpleXML, XMLReader e XMLWriter.

Esistono molte altre estensioni interessanti, classificate sia in ordine alfabetico che per categoria. E ci sono estensioni PECL aggiuntive che possono essere documentate o meno all'interno del manuale PHP stesso, come »XDebug.

Come puoi vedere questa pagina non è sufficiente per elencare tutte le funzionalità e i vantaggi che PHP può offrire. Continua a leggere nelle sezioni sull'installazione di PHP e vedi la parte di riferimento della funzione per la spiegazione delle estensioni menzionate qui.