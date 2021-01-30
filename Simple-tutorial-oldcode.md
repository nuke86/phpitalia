---
title: Utilizzo del vecchio codice con le nuove versioni di PHP
parent: Un semplice tutorial
grand_parent: Iniziamo
nav_order: 5
---

# Utilizzo del vecchio codice con le nuove versioni di PHP
Ora che PHP è diventato un popolare linguaggio di scripting, ci sono molti archivi pubblici e librerie contenenti codice che puoi riutilizzare. Gli sviluppatori PHP hanno ampiamente cercato di preservare la retrocompatibilità, quindi uno script scritto per una versione precedente verrà eseguito (idealmente) senza modifiche in una versione più recente di PHP. In pratica, di solito saranno necessarie alcune modifiche.

Due delle modifiche recenti più importanti che interessano il vecchio codice sono:

* I vecchi array ```$ HTTP _ * _ VARS``` non sono disponibili a partire da PHP 5.4.0. I seguenti array superglobali sono stati introdotti in PHP »4.1.0. Sono: ```$ _GET```, ```$ _POST```, ```$ _COOKIE```, ```$ _SERVER```, ```$_FILES```, ```$ _ENV```, ```$ _REQUEST``` e ```$ _SESSION```.
* Le variabili esterne non sono più registrate nell'ambito globale per impostazione predefinita. In altre parole, a partire da PHP »4.2.0 la direttiva PHP register_globals è disattivata di default in ```php.ini```. 
Il metodo preferito per accedere a questi valori è tramite gli array superglobali menzionati sopra. I vecchi script, libri e tutorial possono fare affidamento su questa direttiva on. Se fosse on, ad esempio, si potrebbe usare ```$ id``` dall'URL http://www.example.com/foo.php?id=42. Sia attivato che disattivato, è disponibile ```$ _GET ['id']```.

Per maggiori dettagli su queste modifiche, vedere la sezione sulle variabili predefinite e sui collegamenti ivi contenuti.