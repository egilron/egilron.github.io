---
published: true
title: Norsk NER med xlm-RoBERTa
---
I [forrige innlegg](https://egilron.github.io/2021/01/27/norne-NER.html) viste jeg at jeg enkelt fikk 5% bedre resultater på Named Entity Reckognition NER på norsk, ved å bruke m-BERT, sammenlignet med min gamle LSTM-CRF-baserte modell som jeg hadde jobbet mye med å fininstille. Jeg har nå sjekket hvordan det gikk hvis vi brukte xlm-RoBERTa is stedet for m-BERT. Jeg har også sett på hvordan det gikk hvis vi forenklet taggene ned til de fire viktigste. 

Det fulle settet med tagger er: 
['PER', 'ORG', 'GPE_LOC', 'DRV', 'PROD', 'LOC', 'GPE_ORG',  'MISC', 'EVT', 'O']

Det reduserte settet er:
['MISC','PER',  'LOC', 'ORG', 'O']

I det fulle settet, er LOC delt i to: GPE_LOC er stedsbetegnelser som er en geopolitisk enhet, slik som "London" og "Singapore". Mens mindre enheter og beskrivelser som fokuserer på den fysiske lokasjonen, som "Nygårdsparken", er LOC i det fulle settet. Tilsvarende er gjort med ORG og GPE_ORG.

I det reduserte settet er disse slått sammen:
```
Product (PROD)
Event (EVT)
Miscellaneous (MISC)
Derived(DRV)
```
De fire taggene i det reduserte settet tilsvarer kategoriene som ble brukt i en CoNLL-2003 shared task. Se ellers [dokumentasjonen for NorNE](https://github.com/ltgoslo/norne) for mer info om kategoriene.

Det jeg fikk ved å trene modeller for NER på norsk ved hjelp av m-BERT og xlm-RoBERTa i 8 epoker, var følgende F-score:
```
			M-BERT	Xlm-RoBERTa
4 labels	0.901	0.931
All labels	0.901	0.91
```
Det er interessant hvordan m-BERT klarer seg like bra med det fulle tagsettet. Det kan jo være en feil, men Precision og Recall er ulike for de to eksperimentene, så jeg sjekker ikke resultatene noe mer. Vi ser at xlm-RoBERTa er litt bedre, og tre prosentpoeng forbedring er ikke dårlig når vi er over 90%.

Du finner jupyter notebooken og hjelperutinene i [norec_fine_tools](https://github.com/egilron/norec_fine_tools).