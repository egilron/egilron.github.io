---
published: true
title: Oppsummering og forslag til pipeline
---
### Oppsummering
I denne bloggen har jeg sett på sentimentanalyse, og fire komponenter som det er interessant å sette i sammenheng: 
- Targeted sentimentanalyse (Det som jeg kan mye om)
- Named Entity Recognition (Som jeg kan en god del om)
- Wikifier (Et grensesnitt mot Wikipedia som identifiserer hvilke ord i en tekst som omtaler hvilke personer eller steder med wikipedia-side).
- Coreference resolution (Finne hvilke andre ord, som pronomener, som henviser til samme omtalte noe).

Jeg har vist at vi får til Targeted Sentimentanalyse og NER på norsk, med multilingual Bert og xlm-RoBERTa. Jeg har ikke vist hvordan vi oversetter norsk tekst til og fra engelsk, for å bruke engelsk coreference resolution. Jeg har brukt google translate API og _fastalign_ for dette.

### Et spennende verktøy
Disse verktøyene samlet, kan utgjøre en svært potent helhet som gir oversikt over hvordan personer og virksomheter blir omtalt. Man kan spore utvikling over tid, og spore forskjeller mellom publikasjoner i Oslo, og resten av landet, og så videre. Etter at man har trent modeller på data fra Norec-fine og NorNe, kan man la disse modellene kverne på dataene fra [Norsk aviskorpus](https://www.nb.no/sprakbanken/ressurskatalog/oai-nb-no-sbr-4/). Med en pipeline av komponentene nevt tidligere i teksten, kan man finne data om for eksempel _Scibsted_:
![Sentimentsporing]({{site.baseurl}}/img/sentimentsporing_eksempel.jpg)
Jeg har ikke satt sammen pipelinen, og når jeg gjør det tenker jeg å ikke publisere den, siden det er verktøy som er såpass kommersielt interessante. Ta kontakt via issues, for eksempel.


