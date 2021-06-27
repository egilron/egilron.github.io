---
published: false
---
## Nye BERT-baserte språkmodeller for norsk

Da jeg begynte å lage løsninger for sentimentanalyse, var M-BERT det eneste alternativet for norsk tekst. Så kom RoBERTa, den har også norskedata i seg. Se tidligere innlegg i denne bloggen. Nå, et stykke ut i 2021, har vi fått to nye modeller basert på bare norsk tekst, tror jeg. 

Det ser ut til at Universitetet i Oslo og Nasjonalbiblioteket har en vennskapelig konkurranse gående, om å lage de beste modellene for norsk. Det er jo supert for oss oss som vil ta i bruk slike modeller. Jeg har begynt å lese [Large-Scale Contextualised Language Modelling for Norwegian](https://www.aclweb.org/anthology/2021.nodalida-main.4.pdf) som rapporterer resultatene de får, og sammenligner med M-BERT og Nasjonalbibliteket sin NB-BERT-Base. [Se også denne siden](http://wiki.nlpl.eu/Vectors/norlm/norbert) for sammanligninger. 

Modellene fra begge miljøene er heldigvis også tilgjengelige via HUggingface sitte repository, så det skulle gå greit å plugge de inn i eksisterende kode.

**Lenker:** 



