---
title: Lavoriamo con i moduli
parent: Un semplice tutorial
grand_parent: Iniziamo
nav_order: 4
---

# Lavoriamo con i moduli
Una delle caratteristiche più potenti di PHP è il modo in cui gestisce i moduli HTML. Il concetto di base che è importante capire è che qualsiasi elemento del modulo sarà automaticamente disponibile per i tuoi script PHP. Si prega di leggere la sezione del manuale sulle variabili da fonti esterne per ulteriori informazioni ed esempi sull'uso dei moduli con PHP. Ecco un esempio di modulo HTML:

Esempio # 1 Un semplice modulo HTML

```
<form action = "action.php" method = "post">
 <p> Il tuo nome: <input type = "text" name = "name" /> </p>
 <p> La tua età: <input type = "text" name = "age" /> </p>
 <p> <input type = "submit" /> </p>
</form>
```

Non c'è niente di speciale in questo modulo. È un semplice modulo HTML senza tag speciali di alcun tipo. Quando l'utente compila questo modulo e preme il pulsante di invio, viene chiamata la pagina *action.php*. In questo file dovresti scrivere qualcosa del genere:

Esempio # 2 Stampa di dati dal nostro modulo

```
Ciao <?php echo htmlspecialchars($_POST['name']); ?>.
Hai <?php echo (int)$_POST['age']; ?> anni.
```

Un output di esempio di questo script potrebbe essere:

```Ciao Joe. Hai 22 anni.```

A parte *htmlspecialchars()* e *(int)*, dovrebbe essere ovvio cosa fa. **htmlspecialchars()** si assicura che tutti i caratteri speciali in html siano codificati correttamente in modo che le persone non possano inserire tag HTML o Javascript nella tua pagina. Per il campo età, poiché sappiamo che è un numero, possiamo semplicemente convertirlo in un intero che eliminerà automaticamente tutti i caratteri non voluti. Puoi anche fare in modo che PHP esegua questa operazione automaticamente utilizzando l'estensione del filtro. 

Le variabili ```$_POST['name']``` e ```$_POST['age']``` vengono impostate automaticamente da PHP. In precedenza abbiamo utilizzato ```$_SERVER``` superglobale; sopra abbiamo appena introdotto il superglobale ```$_POST``` che contiene tutti i dati POST. Nota come il metodo del nostro modulo è POST. Se usassimo il metodo GET, le informazioni del nostro modulo risiederebbero invece nel superglobale ```$_GET```. Puoi anche utilizzare il superglobale ```$_REQUEST```, se non ti interessa la fonte dei dati della tua richiesta. Contiene le informazioni unite di dati GET, POST e COOKIE.

Puoi gestire l'input di XForms in PHP, anche se ti troverai a tuo agio con i form HTML ben supportati per un bel po' di tempo. Sebbene lavorare con XForms non sia per principianti, potresti essere interessato a loro. Abbiamo anche una breve introduzione alla gestione dei dati ricevuti da XForms nella nostra sezione delle caratteristiche.