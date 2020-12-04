---
published: true
title: Oppsett maskin og programmer
---
Det er ikke bare-bare å sette opp ei datamaskin for maskinlæring på grafikk-kortet. Men veldig artig når det er gjort. Jeg kjøpte meg en MSI bærbar med GTX 1070 grafikk-kort. Jeg installerte Linux på snurre-harddisken slik at jeg har dual boot. Jeg gjorde dette før jeg begynte å bruke den disken til noe annet, slik at jeg kunne la installasjonen styre med disken som den ville, men jeg lot en god partisjon bli NTFS slik at den kan brukes av begge systemene.

#### Valg av linux:
Jeg installerte [pop!OS](https://pop.system76.com) fordi de har en egen installasjon for NVIDIA grafikk-kort. Det var mye enklere enn å bruke Ubuntu. Det er en open-source driver-versjon som kommer inn som default, men den kan ikke brukes med CUDA, som er grensesnittet mellom grafikk-kortet og maskinlæringsprogrammene. Med pop!OS blir disse driverne riktig ved installering, og systemet er en renslig og fin Ubuntu-variant ellers.

#### Versjons-stabelen.
I de to årene jeg har hatt denne maskina nå, har jeg oppdatert CUDA en gang, og jeg oppdaterte OS fra 18.04 til 20.04. Det er et styr, og det å oppdatere til 20.04 var nok ikke verdt det, sånn midt i oppgaveskrivinga. Jeg kom ikke utenom å oppdatere CUDA, på grunn av oppdateringer i Simpletransformers og pyTorch, tror jeg det var. Hele rekka med CUDA, pyTorch, Python, Transformers og Simpletransformers trenger å spille sammen. Hovederfaringen er: Bruk alltid virtuelle python-miljøer, og når ting fungerer, ikke rør det før du må. Begynn hos [pyTorch](https://pytorch.org/get-started/locally/) og på på plass en CUDA-versjon som de har i oppsettet sitt, og ta det derfra.

![Programvarestabelen]({{site.baseurl}}/img/hardwaresetup.jpg)

#### Hva med Windows?
Personlig har jeg mye erfaring med Windows, og bruker det i hverdagen. Men jeg har plundret så mye med språkteknologi og UTF8-problematikk, at jeg har gitt det opp for alle prosjekter med norsk tekst. Jeg lar aldri norske språkdata være innom Windows på veien. Og siden jeg derfor trenger et Linux-miljø, gjør jeg alt på Linux. WLS2 på Windows er fint, men det er ingen kobling mot CUDA ennå, så for dette prosjektet er det uaktuelt.

#### Skyløsning
Egentlig burde man sikkert ikke styre med å sette opp si ega maskin til dette i det hele tatt, men kjøre det i skya. Google sin løsning lar deg visst gjøre mye på gratis-kontoen. Vel, jeg trengte ei ny maskin uansett, og det er litt tilfredsstillende å få det til, så jeg rapporterer på det jeg har gjort.
