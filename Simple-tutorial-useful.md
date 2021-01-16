---
title: Qualcosa di utile
parent: Un semplice tutorial
grand_parent: Iniziamo
nav_order: 3
---

# Qualcosa di utile
Facciamo qualcosa di più utile adesso. Stiamo per verificare quale tipo di browser sta utilizzando il visitatore. Per questo, controlliamo la stringa dell'agente utente che il browser invia come parte della richiesta HTTP. Queste informazioni vengono memorizzate in una variabile . Le variabili iniziano sempre con un segno di dollaro in PHP. La variabile che ci interessa in questo momento è ```$_SERVER['HTTP_USER_AGENT']```.

Nota :

$_SERVER è una variabile PHP riservata speciale che contiene tutte le informazioni del server web. È noto come superglobale. Vedere la relativa pagina di manuale sulle superglobali per maggiori informazioni. Queste variabili speciali sono state introdotte in PHP »4.1.0. Prima di allora, utilizzavamo invece i vecchi array ```$HTTP_*_VARS```, come ```$HTTP_SERVER_VARS```. A partire da PHP 5.4.0 queste vecchie variabili sono state rimosse. (Vedi anche la nota sul vecchio codice).

Per visualizzare questa variabile, puoi semplicemente fare:

Esempio n. 1 Stampa di una variabile (elemento Array)

```
<?php
echo $_SERVER['HTTP_USER_AGENT'];
?>
```

Un output di esempio di questo script potrebbe essere:

```
Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)
```

Ci sono molti tipi di variabili disponibili in PHP. Nell'esempio sopra abbiamo stampato un elemento Array. Gli array possono essere molto utili.

```$_SERVER``` è solo una variabile che PHP ti rende automaticamente disponibile. Un elenco può essere visualizzato nella sezione Variabili riservate del manuale oppure è possibile ottenerne un elenco completo guardando l'output della funzione *phpinfo()* utilizzata nell'esempio nella sezione precedente.

Puoi inserire più istruzioni PHP all'interno di un tag PHP e creare piccoli blocchi di codice che fanno più di un semplice eco. Ad esempio, se desideri verificare la presenza di Internet Explorer, puoi farlo:

Esempio # 2 Esempio di utilizzo di strutture e funzioni di controllo

```
<?php
if (strpos($_SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE) {
    echo 'You are using Internet Explorer.<br />';
}
?>
```
Un output di esempio di questo script potrebbe essere:

```
Stai utilizzando Internet Explorer. <br />
```

Qui introduciamo un paio di nuovi concetti. Abbiamo una dichiarazione *if*. Se hai familiarità con la sintassi di base utilizzata dal linguaggio C, questa dovrebbe sembrarti logica. Altrimenti, dovresti probabilmente prendere un libro PHP introduttivo e leggere i primi due capitoli, o leggere la parte di riferimento del linguaggio del manuale.

Il secondo concetto che abbiamo introdotto è stata la chiamata alla funzione *strpos()*. **strpos()** è una funzione incorporata in PHP che cerca una stringa per un'altra stringa. In questo caso stiamo cercando 'MSIE' (cosiddetto ago) all'interno di ```$_SERVER['HTTP_USER_AGENT']``` (cosiddetto pagliaio). Se l'ago si trova all'interno del pagliaio, la funzione restituisce la posizione dell'ago rispetto all'inizio del pagliaio. Altrimenti, ritorna *false*. Se non ritorna *false*, l'espressione *if* restituisce *true* e il codice all'interno delle sue {parentesi graffe} viene eseguito. In caso contrario, il codice non viene eseguito. Sentiti libero di creare esempi simili, con *if*, *else* e altre funzioni come **strtoupper()** e **strlen()**. Ogni pagina di manuale correlata contiene anche esempi. Se non sei sicuro di come usare le funzioni, dovrai leggere sia la pagina di manuale su come leggere una definizione di funzione sia la sezione sulle funzioni PHP.

Possiamo fare un ulteriore passo avanti e mostrare come puoi saltare dentro e fuori dalla modalità PHP anche nel mezzo di un blocco PHP:

Esempio n. 3 Combinazione di modalità HTML e PHP

```
<?php
if (strpos($_SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE) {
?>
<h3>strpos() must have returned non-false</h3>
<p>You are using Internet Explorer</p>
<?php
} else {
?>
<h3>strpos() must have returned false</h3>
<p>You are not using Internet Explorer</p>
<?php
}
?>
```

Un output di esempio di questo script potrebbe essere:

```
<h3> strpos() deve aver restituito un valore non falso </h3>
<p> Stai utilizzando Internet Explorer </p>
```

Invece di usare un'istruzione echo PHP per produrre qualcosa, siamo saltati fuori dalla modalità PHP e abbiamo inviato semplicemente HTML. Il punto importante e potente da notare qui è che il flusso logico dello script rimane intatto. Solo uno dei blocchi HTML finirà per essere inviato al browser a seconda del risultato di strpos(). In altre parole, dipende dal fatto che la stringa MSIE sia stata trovata o meno.