---
title: I tag PHP
parent: Sintassi di base
grand_parent: Guida al linguaggio
nav_order: 1
---

# I tag PHP
Quando PHP analizza un file, cerca i tag di apertura e chiusura, che sono ```<?php``` e ```?>``` che dicono a PHP di avviare e interrompere l'interpretazione del codice che sta tra di loro. L'analisi in questo modo consente di incorporare PHP in tutti i tipi di documenti diversi, poiché tutto ciò che è al di fuori di una coppia di tag di apertura e chiusura viene ignorato dal parser PHP.

PHP include un breve tag echo ```<?=``` che è una scorciatoia per il più dettagliato ```<?php echo```.

**Esempio #1 Tag PHP di apertura e chiusura**

```
1.  <?php echo 'se vuoi inserire codice PHP in documenti XHTML o XML, usa questi tag'; ?>

2.  Puoi usare il tag breve <?= 'print this string' ?>.
    Che equivale a <?php echo 'print this string' ?>.

3.  <? echo 'questo codice usa i tag brevi, ma funziona solo '.
            'se short_open_tag è attiva'; ?>
```

I tag brevi (esempio tre) sono disponibili di default ma possono essere disabilitati tramite la direttiva ```short_open_tag``` del file di configurazione ```php.ini```, o sono disabilitati di default se PHP viene compilato con la configurazione ```--disable-short-tags```.

### Nota:
```
Poiché i tag brevi possono essere disabilitati, si consiglia di utilizzare solo i tag normali 
(<?php ?> e <?= ?>) per massimizzare la compatibilità.
```

Se un file contiene solo codice PHP, è preferibile omettere il tag di chiusura PHP alla fine del file. Ciò impedisce l'aggiunta accidentale di spazi bianchi o nuove righe dopo il tag di chiusura PHP, il che potrebbe causare effetti indesiderati perché PHP inizierà il buffering dell'output quando il programmatore non ha intenzione di inviare alcun output in quel punto dello script.

```
<?php
echo "Hello world";

// ... codice ...

echo "Ultima istruzione";

// lo script termina qui, senza nessun tag di chiusura
```