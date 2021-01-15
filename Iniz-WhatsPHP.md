---
title: Cos'è PHP?
parent: Iniziamo
nav_order: 1
---

# Cos'è PHP?
PHP (acronimo ricorsivo per PHP: Hypertext Preprocessor) è un linguaggio di scripting generico open source ampiamente utilizzato che è particolarmente adatto per lo sviluppo web e può essere incorporato in HTML.

Bello, ma cosa significa? Un esempio:

Esempio # 1 Un esempio introduttivo

```
<!DOCTYPE html>
<html>
    <head>
        <title>Example</title>
    </head>
    <body>

        <?php
            echo "Ciao, io sono uno script PHP!";
        ?>

    </body>
</html>
```

A differenza di molti comandi per produrre HTML (come si vede in C o Perl), le pagine PHP contengono HTML con codice incorporato che fa "qualcosa" (in questo caso, output "Ciao, sono uno script PHP!"). Il codice PHP è racchiuso in speciali istruzioni di inizio e fine elaborazione **<?php** e **?>** che ti consentono di entrare e uscire dalla "modalità PHP".

Ciò che distingue PHP da qualcosa come JavaScript lato client è che il codice viene eseguito sul server, generando HTML che viene quindi inviato al client. Il client riceve i risultati dell'esecuzione di quello script, ma non sa quale sia il codice sottostante. Puoi persino configurare il tuo server web per elaborare tutti i tuoi file HTML con PHP, e quindi non c'è davvero modo che gli utenti possano dire cosa produci all'interno.

La cosa migliore nell'usare PHP è che è estremamente semplice per un nuovo arrivato, ma offre molte funzionalità avanzate per un programmatore professionista. Non aver paura di leggere il lungo elenco di funzionalità di PHP. Puoi saltare, in breve tempo, e iniziare a scrivere semplici script in poche ore.

Sebbene lo sviluppo di PHP sia incentrato sullo scripting lato server, puoi farci anche molto di più. Continua a leggere e scopri di più nella sezione Cosa può fare PHP? o vai direttamente al Tutorial introduttivo se sei interessato solo alla programmazione web.