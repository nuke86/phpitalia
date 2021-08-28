---
title: Separazione delle istruzioni
parent: Sintassi di base
grand_parent: Guida al linguaggio
nav_order: 3
---

# Separazione delle istruzioni
Come in C o Perl, PHP richiede che le istruzioni vengano terminate con un punto e virgola alla fine di ogni istruzione. Il tag di chiusura di un blocco di codice PHP implica automaticamente un punto e virgola; non è necessario che il punto e virgola termini l'ultima riga di un blocco PHP. Il tag di chiusura per il blocco includerà la nuova riga immediatamente successiva, se presente.

**Esempio n. 1 Esempio che mostra il tag di chiusura che racchiude la nuova riga finale**

```
<?php echo "Del testo"; ?>
Nessuna nuova riga
<?= "Ma ora nuova riga qui" ?>
```

L'esempio precedente produrrà:

```
Un po' di testoNessuna nuova riga
Ma ora nuova riga qui
```

Esempi di entrata e uscita dal parser PHP:

```
<?php
    echo 'Questo è un test';
?>

<?php echo 'Questo è un test' ?>

<?php echo 'Abbiamo omesso l'ultimo tag di chiusura';
```


### Nota:
```
Il tag di chiusura di un blocco PHP alla fine di un file è facoltativo e in alcuni casi ometterlo è utile quando si utilizza include o require, quindi non si verificheranno spazi bianchi indesiderati alla fine dei file e sarà comunque possibile aggiungere intestazioni alla risposta successiva. È anche utile se si utilizza il buffering dell'output e non si desidera visualizzare spazi bianchi indesiderati aggiunti alla fine delle parti generate dai file inclusi.

```