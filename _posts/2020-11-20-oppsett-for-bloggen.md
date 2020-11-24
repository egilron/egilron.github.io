---
published: true
layout: post
title: Oppsett for bloggen
date: '2020-11-20 15:28:12 +0100'
categories: teknisk
---
## Github pages, jekyll og prose

Hvis alt var enkelt og greit, hadde det ikke vært så spennende å utforske. Vi skal blogge om språkteknologi, og tidligere lagde jeg websider med Dreamweaver. Nå tenker jeg at det ser kult ut å bruke github pages. Så da har jeg installert jekyll på maskina mi, og lastet opp et tomt prosjekt. Og så håper jeg at jeg skal få redigert med [Prose](http://prose.io/).
### Husk å sjekke e-post om build errors fra github pages
Vi skulle få bort "Your Awesome title". Jeg hadde fjernet teksta i [_config.yml](_config.yml), og så må ting få oppdatere seg. Men det gjorde de ikke siden jeg hadde en feil i description som gjorde at sidene ikke ble oppdatert. Da description ble retta, så fungerer oppdateringen.
### Publisert-knappen
Når vi redigerer i Prose, er det valget for publisering til høyre i den grå stripa, litt diskret plassert.

![]({{site.baseurl}}/img/publish.png)

Men html i md-dokumentet:
<img scr="https://egilron.github.io/img/publish.png" alt="publiseringsknappen">

