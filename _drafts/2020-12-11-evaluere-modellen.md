---
published: false
title: Evaluere modellen
---

Når vi skal finne ut hvor bra modellen vår er, må den evalueres. Vi bruker den innebygde metoden for evaluering med
```
result, model_outputs, predictions = model.eval_model(dev_path)
```
`dev_path` er fila med testdata, enten dev eller test, avhengig av hvor du er i prosessen. Den fila inneholder nye data av samme type som treningsdataene. Tekstene der har også blitt annotert av menneskehender, så de inneholder tagger som er "sannheten" om  target og sentiment. Men når vi tester får ikke modellen vite hva disse taggene er. Nå er den ferdig med å lære, og skal bare vise hva den har lært. Modellen gir oss et resultat, og så sjekker vi mot "fasiten". Hvis modellen har markert de rette ordene for en sentiment target-sekvens, så blir det et treff. Hvis sekvensen er nesten rett, men ikke helt, blir det feil. Og hvis polaritet ikke stemmer, blir det feil. Tabellen under gir eksempler på situasjoner der modellen ikke gir helt riktig resultat, og da blir det feil.
![evaluering]({{site.baseurl}}/img/evaluation_metrics.jpg)

