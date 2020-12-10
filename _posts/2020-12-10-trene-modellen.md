---
published: true
title: Trene modellen
---
Når parametrene er satt til noe nogenlunde meningsfullt, er det bare tut og kjør og trene modellen.
Jeg har lagd en del kode som gjør at jeg kan kjøre flere treninger etter hverandre, og samle inn resultatene. Merk at det kan bli trang på stedet du har satt som `out_d`. Det blir fort noen GB der, så pass på å slette lagringer du ikke har bruk for.

### Anvende modellen
I dag har jeg lagt til kode for å bruke modellen på din egen tekst, og også hvordan laste inn en lagret modell. Eksempelsetningene i [min notebook](https://github.com/egilron/norec_fine_tools/blob/master/Experiments21_norec_bert.ipynb) viser litt av hva modellen får til, og hva den ikke får til. Vi ser at modellen tagger _"Mannen på scenen synger stygt"_ annerledes enn _"Damen på scenen synger stygt"_. Det er dessverre slik det er i en uperfekt verden. Legg gjerne igjen en kommentar på *Discussions* på [norec_fine_tools](https://github.com/egilron/norec_fine_tools) hvis du har prøvd koden, og enten har fått det til eller ikke fått det til. Discussions er noe nytt på github som jeg aktiverte i dag, og håper jeg har gjort det som trengs for at du kan ta det i bruk. Hvis du som jeg synes det er litt skummelt å legge inn "issue", så kan dette sikkert fungere som en mer lavterskel metode for å legge igjen en kommentar.
