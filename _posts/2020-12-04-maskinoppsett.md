---
published: false
---
Det er ikke bare-bare å sette opp ei datamaskin for maskinlæring på grafikk-kortet. Men veldig artig når det er gjort. Jeg kjøpte meg en MSI bærbar med GTX 1070 grafikk-kort. Jeg installerte Linux på snurre-harddisken slik at jeg har dual boot. Jeg gjorde dette før jeg begynte å bruke den disken til noe annet, slik at jeg kunne la installasjonen styre med disken som den ville, men jeg lot en god partisjon bli NTFS slik at den kan brukes av begge systemene.

#### Valg av linux:
Jeg installerte pop!OS fordi de har en egen installasjon for NVIDIA grafikk-kort. Det var mye enklere enn å bruke Ubuntu. Det er en open-source driver-versjon som kommer inn som default, men den kan ikke brukes med CUDA, som er grensesnittet mellom grafikk-kortet og maskinlæringsprogrammene. Med pop!OS blir disse driverne riktig ved installering, og systemet er en renslig og fin Ubuntu-variant ellers.

#### Versjons-stabelen.
I de to årene jeg har hatt denne maskina nå, har jeg oppdatert CUDA en gang, og jeg oppdaterte OS fra 18.04 til 20.04. Det er et styr, og det å oppdatere til 20.04 var nok ikke verdt det, sånn midt i oppgaveskrivinga. Jeg kom ikke utenom å oppdatere CUDA, på grunn av oppdateringer i Simpletransformers og pyTorch, tror jeg det var. Hele rekka med CUDA, pyTorch, Python, Transformers og Simpletransformers trenger å spille sammen. Hovederfaringen er: Bruk alltid viruelle python-miljøer, og når ting fungerer, ikke rør det før du må.
![Programvarestabelen]({{site.baseurl}}img/hardwaresetup.jpg)
