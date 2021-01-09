---
published: true
title: Treningsepoker og xlm-roberta
---

Jeg kjørte noen tester der jeg så på effekten av antall epoker man trener modellen. (En epoke er at man kjører gjennom alle treningadataene en gang.) Jeg har brukt åtte epoker i mine forsøk med multilingual BERT og batch size på 32. Plottene under viser at det gir mening. Da jeg skulle ta i bruk xlm-roberta, fikk jeg minneproblemer på grafikkortet, og tok derfor ned batch size fra 32 til 16. Ved et uhell dro jeg i gang et forsøk med m-BERT og batch size på 16, men det er jo greit, så fikk vi sett på det alternativet også. 

Vi ser at m-BERT blir mer uryddig og ikke noe bedre med batch size 16. Vi ser at det gir mening å trene m-BERT for 8 epoker til vanlig, med batch size 32, og vi ser at xlm-roberta gjør det bra, og at også der, er åtte epoker et greit tall. Merk at disse tingene er avhengig av størrelsen på treningssettet. Med et mindre treningssett, kan det være greit å utforske om man skulle skrudd opp antall epoker.

Jeg har lagt ut en ny notebook der jeg har endret treningen til å evaluere underveis på testsettet, og der jeg samler inn evalueringsresultatene for hver epoke, og plotter de.
[Den finner du her:](https://github.com/egilron/norec_fine_tools/blob/master/Experiments21b_norec_xlmroberta.ipynb)

### M-BERT med batch size 16
![M-BERT epochs]({{site.baseurl}}/img/bert_epochs_batch_16.png)
### M-BERT med batch size 32
![M-BERT epochs]({{site.baseurl}}/img/bert_epochs_batch_32.png)
### Xlm-roberta med batch size 16
![xlm-roberta epochs]({{site.baseurl}}/img/xlm_roberta_epochs.png)