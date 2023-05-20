---
published: false
title: Norske data for sentimentanalyse
---
Når vi skal trene nevrale nettverk for Targeted Sentiment Analysis TSA, trenger vi masse eksempler. Grunnen til at det  i det hele tatt er aktuelt å skrive om TSA på norsk, er at vi i 2020 har fått datasettet NoReC-fine. Det inneholder over ti tusen setninger der folk har sittet og merket av hvor det er et sentiment target, og hvor vi har ordene som uttrykker dette sentimentet overfor target.

### Hente dataene for NoReC-fine
Datasettet er tilgjengelig i json-format [på github](https://github.com/ltgoslo/norec_fine). Jeg er ikke helt trygg på skriptet som skal konvertere til conll, så jeg har mine egne versjoner av de konverterte dataene. De ligger i [mitt repo her.](https://github.com/egilron/norec_fine_tools/tree/master/data/spaceseparated/norec_fine). Uansett hvor du tar det fra: Du skal ha over 5000 forekomster av tekststrengen "B-targ" i train-fila.