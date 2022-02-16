---
published: false
---

## Personer og organisasjoner i NoReC-fine

NoReC-Fine er et datasett for detaljer sentimentanalyse, og jeg har brukt det til å finne hva konkret som blir omtalt positivt eller negativt i hver setning. Jeg har altså bare brydd meg om sentiment targets. Jeg har brukt sequence labelling, også kalt sequence tagging som framgangsmåte. Dette er samme framgangsmåte som er vanlig i Named Entity Recognition NER. Se tidligere innlegg der jeg trener en modell for norsk NER.
Det har nylig kommet ut en ferdigtrent modell for nordisk NER. Den har inkludert data fra NorNE. Transformer-modellen som er brukt, er også nokså ny. Så nå har jeg brukt den modellen til å NER-tagge NoReC-Fine. Det jeg skal med dette, er å se på hvordan vi best og enklest mulig kan trekke ut dokumentets samlede sentiment mot personer og virksomheter. Altså at selv om dokumentet kan uttrykke ulike sentimenter mot ulike targets, hvordan kan vi oppsummere dokumentets totale sentiment mot en gitt person eller virksomhet? Med NER får vi tagget personer som PER, og virksomheter som ORG. NER taggeren treffer veldig bra på test-splitten til de treningsdata som er brukt. Og jeg antar at taggingen av NoReC-Fine vil være temmelig presis også. 
