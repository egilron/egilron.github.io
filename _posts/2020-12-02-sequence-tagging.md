---
published: true
title: Sequence tagging
---
Når vi skal trene modell for targeted sentimentanalyse, har jeg valgt å gjøre det som _sequnece tagging_. Det vil si at vi for hver setning skal finne sekvenser som inneholder det vi er ute etter. Vi bruker en setning fra en konsertanmeldelse av Veronica Maggio som eksempel:

> Maggios myke soulvokal og tidvis fengende låter redder den uinspirerte opptredenen fra å bli en fadese .

De som har annotert denne setningen har sagt at her er det en sekvens som får positivt sentiment, og en sekvens som får negativt sentiment. Det positive targetet, eller "sentimentobjektet" som jeg kanskje tør kalle det på norsk, er _Maggios myke soulvokal og tidvis fengende låter_. Det negative sentimentobjektet er _opptredenen_.

Når vi skal mate denne informasjonen inn til et nevralt nettverk, begynner vi med å presentere dataene i conll format. (I dette ordet skal de fleste bokstavene være store (CoNLL tror jeg). Jeg er litt motstander av slik hompetitten-notering, både på OsloMet, og på NoReC. Jeg synes det gir dårlig leseflyt. Så siden jeg kan bestemme sjøl her på bloggen, så bruker jeg mest små bokstaver. Jeg tør ikke endre på skriveformen til NoReC, for jeg kjenner de folka, og vil gjerne være venner med de framover også :) ) (Smilefjes med parentes slutt)

Jeg bruker BIO-formatet, som gir første ord i sekvensen vi er ute etter en B, og resten av ordene i sekvensen får en I, og de som er utafor sekvensene får O.
Da kan setningen over bli representert slik som vist under. Skillet mellom ordet og taggen er egentlig kun ett mellomrom. Jeg la til noen flere for å se om det ble lettere å lese.

```
Maggios 	B-targ-positive
myke 		B-targ-positive
soulvokal 	I-targ-positive
og 			I-targ-positive
tidvis 		I-targ-positive
fengende 	I-targ-positive
låter 	I-targ-positive
redder 	O
den 	O
uinspirerte	O
opptredenen	B-targ-negative
fra 	O
å 	O
bli	O
en	O
fadese	O
.	O
```
