---
title: Coreference resolution
published: false
---

I forrige innlegg så vi hvordan vi kangjøre oppslap mot Wikipedia for å finne ut hvilke navn som nevnes i en tekst, er knyttet til hvilke virkelige personer. Det gikk ikke så verst, untatt at Marion Ravn var over alt og ikke lot seg kategorisere.

Nå ser vi på hvilke ord i en setning som referer til samme omtalte "noe". Den plasserer personlige pronomener og slikt til hovedomtalen. Det er jo vanlig på mange språk å først presentere noen litt skikkelig, før man bruker pronomen for å referere til samme person senere. __I går møtte jeg Martin Schanke som har vunnet flere medaljer enn alle bikkjene i nabolaget mitt. Han hadde det travelt__ . 
Men det går an med en liten teaser først, før den skikkelige presentasjonen: __I går møtte jeg verdensmesteren. Martin Schanke var på besøk i kulturhuset vårt.__ I begge setninger er det __Martin Schanke__ som en hovedsaken, og __han__ og __verdensmesteren__ (og __som__ ?) er refereanser til denne hovedsaken. __bikkjene i nabolaget mitt__ blir ikke referert til av noe pronomen i setningene.
Jeg jobber fortsatt i [norec_fine_tools](https://github.com/egilron/norec_fine_tools) og har lastet opp `coref_prep.ipynb`og `coref_demo.py`. I notebooken henter vi fram den engelske oversettelsen av artikler i Norec_fine som inneholder "Mari". I `coref_demo.py` går vi gjennom dfisse artiklene, og finner coreferanser, og tar vare på de som inneholder "Mari". Grunnen til at vi bruker engelsk oversettelse, er at motoren i å finne coreferanser, er trent kun på engelsk. Vi får ut ting som dette: 
~~~
Real Madrid star Ángel Di Maria: [Real Madrid star Ángel Di Maria, his, the Argentina star]
Maria Mena: [Maria Mena, Maria Mena, her, She, herself, her, Maria Mena, She, she, she, she, Maria Mena, her, her, she, her, Mena, She, her]
Maria Mena: ": [Maria Mena: ", Maria Mena, She, Maria Mena, her, Maria Mena, She, her, Mena, her, Mena]
Marion Ravn: [Marion Ravn, her, she, she, her, she, She, Ravn, Marion Ravn, It, her]
the US Marines: [the US Marines, their]
Maria Kannegaard trio: ": [Maria Kannegaard trio: ", The trio]
Maridalsveien: [Maridalsveien, Maridalsveien]
 ~~~

Når vi analyserer sentiment i setningene, og er ute etter alle steder som refererer til en gitt person, så er dette et interessant verktøy.
