---
published: false
---

Det er en jobb å få tekst-dataene våre til å passe med det nevrale nettverket vi bruker, og her har vi god nytte av overbygninger som [simpletransformers](https://simpletransformers.ai/).
Det kan være fristende å stoppe minst mulig ved dataene, og fortest mulig komme i gang med modellene. Men jeg anbefaler å ta litt ekstra tid med dataene, slik at du er trygg på hva det er du mater inn til modellen og hvorfor.

### CoNLL
Det du skal mate inn, er ei treningsfil, og ei testfil. I starten bruker vi dev-test til evaluering. Jeg presenterte conll-formatet i posten om [sequence tagging](https://egilron.github.io/2020/12/02/sequence-tagging.html). Pass på følgende:
- Conll-filer kan skille ord og tag med tabulator eller mellomrom. For simpletransformers bruker vi mellomrom.
- Pass på at settet av tagger er det samme i de to filene. Hvis du bruker B-TARGET-POSITIVE i ei fil, kan du ikke bruke B-TARG-POS i ei anna fil. Jeg sjekker alltid de tingene før jeg laster inn filene.
- Pass på at du ikke har gjort ting med dataene slik at den tomme linja mellom setninger har forsvunnet.
- Pass på at det ikke er mellomrom inni ordet. Når det er mellomrom som skiller ord og tag, kan det ikke være mellomrom inni ordet, som det ville være hvis man tok "New York" som et ord. Det er ikke slike mellomrom i mine data eller i dataene i Norec-fine - repoet, men veldig nyttig å ha et bevisst forhold til. Uansett hvor fint tidsskrift folk har publisert i, kan du ikke ta for gitt at koden deres er godt håndverk.
