---
published: false
---
I forrige innlegg viste jeg at jeg enkelt fikk 5% bedre resultater på Named ENtity Reckognition NER på norsk, ved å bruke m-BERT, sammenlignet med min gamle LSTM-CRF-baserte modell som jeg hadde jobbet mye med å fininstille. Jeg sjekket hvordan det gikk hvis vi brukte xlm-RoBERTa is stedet for m-BERT. Jeg har også sett på hvordan det gikk hvis vi forenklet taggene ned til de fire viktigste.
Det fulle settet med tagger er: 
['PER', 'ORG', 'GPE_LOC', 'DRV', 'PROD', 'LOC', 'GPE_ORG',  'MISC', 'EVT', 'O']

Det reduserte settet er:
['MISC','PER',  'LOC', 'ORG', 'O']

