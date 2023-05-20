---
published: false
title: Nytt konverteringsskript for conll
---
Når vi har lastet ned repoet for NoReC-fine, trenger vi å konvertere fra json til conll. Jeg nevnte i innlegget "Norske data for sentimentanalyse" at jeg var usikker på konverteringsskriptet som ligger i NoReC-fine-repoet. Jeg har sett på det, og funnet hva som var greia: Det var en try-except seksjon som måtte skrives om. Jeg har lagt til den nye konverteringsfila som pull-request til NoReC-fine-repoet, og du kan hente den derfra, eller fra [min fork](https://github.com/egilron/norec_fine/blob/master/convert_to_bio.py). 

På denne måten slipper du å bruke mine versjoner av dataene. Jeg sammenlignet de to versjonene, og så at i mine versjoner har jeg handtert dette med motstridende sentiment litt annerledes. I en setning kan det være både et positivt og negativt utsagn om et sentiment target. Men vi bruker ikke "conflicting" som en tag, så vi skal ha det enten som positivt eller negativt. I min versjon lar jeg den sterkeste polariteten vinne, mens i  convert_to_bio.py er det altid siste polaritet som vinner. Jeg mener at det er en vurderingssak, og at det har ikke mye å si i praksis. Så jeg vil anbefale at du konverterer fra json til conll sjøl, ved hjelp av min convert_to_bio.py fra i desember.
