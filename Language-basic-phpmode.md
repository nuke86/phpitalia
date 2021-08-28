---
title: Integrazione HTML
parent: Sintassi di base
grand_parent: Guida al linguaggio
nav_order: 2
---

# Integrazione HTML
Tutto ciò che rimane al di fuori di una coppia di tag di apertura e chiusura viene ignorato dal parser PHP che consente ai file PHP di avere contenuti misti. Ciò consente di incorporare PHP nei documenti HTML, ad esempio per creare modelli.


```
<p>Questo viene ignorato da PHP e visualizzato dal browser.</p>
<?php echo 'Invece questo viene generato da PHP.'; ?>
<p>Questo nuovamente ignorato da PHP e visualizzato dal browser.</p>
```

Funziona come previsto, perché quando l'interprete PHP trova i tag di chiusura ?>, inizia semplicemente a emettere tutto ciò che trova (tranne la nuova riga immediatamente successiva - vedi separazione delle istruzioni) fino a quando non incontra un altro tag di apertura a meno che nel mezzo di un'istruzione condizionale in tal caso l'interprete determinerà l'esito del condizionale prima di prendere una decisione su dove saltare. Vedi il prossimo esempio.
Utilizzo di strutture con condizioni

**Esempio n. 1 Integrazione avanzata usando le condizioni**

```
<?php if ($expression == true): ?>
  Questo viene visualizzato se expression è true.
<?php else: ?>
  Altrimenti viene mostrato questo.
<?php endif; ?>
```

In questo esempio PHP salterà i blocchi in cui la condizione non è soddisfatta, anche se sono al di fuori dei tag di apertura/chiusura PHP; PHP li salta in base alla condizione poiché l'interprete PHP salterà sui blocchi contenuti in una condizione che non è soddisfatta.
Per l'output di grandi blocchi di testo, l'abbandono della modalità di analisi PHP è generalmente più efficiente rispetto all'invio di tutto il testo tramite echo o print.

### Nota:
```
Se PHP è incorporato in XML o XHTML, il normale PHP <?php ?>deve essere 
utilizzato per rimanere conforme agli standard.
```
