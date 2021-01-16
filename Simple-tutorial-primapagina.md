---
title: La tua prima pagina PHP
parent: Un semplice tutorial
grand_parent: Iniziamo
nav_order: 2
---

# La tua prima pagina PHP
Crea un file chiamato *hello.php* e mettilo nella directory principale del tuo server web ( DOCUMENT_ROOT ) con il seguente contenuto:

Esempio # 1 Il nostro primo script PHP: *hello.php*

```
<html>
 <head>
  <title>PHP Test</title>
 </head>
 <body>
 <?php echo '<p>Hello World</p>'; ?> 
 </body>
</html>
```

Usa il tuo browser per accedere al file con l'URL del tuo server web, che termina con il riferimento al file */hello.php*. Quando si sviluppa localmente, questo URL sarà qualcosa come *http://localhost/hello.php* o *http://127.0.0.1/hello.php* ma questo dipende dalla configurazione del server web. Se tutto è configurato correttamente, questo file verrà analizzato da PHP e il seguente output verrà inviato al browser:

```
<html>
 <head>
  <title> Test PHP </title>
 </head>
 <body>
 <p> Hello World </p>
 </body>
</html>
```

Questo programma è estremamente semplice e non hai davvero bisogno di usare PHP per creare una pagina come questa. Tutto quello che fa è visualizzare: *Hello World* usando l'istruzione *echo* di PHP. Nota che il file non deve essere in alcun modo eseguibile o speciale. Il server scopre che questo file deve essere interpretato da PHP perché hai utilizzato l'estensione "*.php*", che il server utilizza per passare i file a PHP. Pensa a questo come a un normale file HTML che ha una serie di tag speciali a tua disposizione che fanno molte cose interessanti.

Se hai provato questo esempio e non ha prodotto nulla, è stato richiesto il download, o vedi l'intero file come testo, è probabile che il server su cui ti trovi non abbia PHP abilitato o non sia configurato correttamente. Chiedere al proprio amministratore di abilitarlo utilizzando il capitolo Installazione del manuale. Se stai sviluppando localmente, leggi anche il capitolo sull'installazione per assicurarti che tutto sia configurato correttamente. Assicurati di accedere al file tramite http con il server che ti fornisce l'output. Se si richiama il file dal proprio file system, non verrà analizzato da PHP. Se i problemi persistono comunque, non esitare a usare una delle tante [»opzioni di supporto PHP](https://www.php.net/support.php).

Il punto dell'esempio è mostrare il formato speciale del tag PHP. In questo esempio abbiamo usato *<?php* per indicare l'inizio di un tag PHP. Poi abbiamo messo la dichiarazione PHP e lasciato modalità PHP con l'aggiunta del tag di chiusura, *?>*. Puoi entrare e uscire dalla modalità PHP in un file HTML come questo ovunque tu voglia. Per maggiori dettagli, leggi la sezione del manuale sulla sintassi PHP di base.