---
published: false
---
Når vi gjør Targeted Sentiment Analysis, ønsker vi å finne hva i teksten som omtales positivt eller negativt. 

Når vi gjør Named Entity Recognition, ønsker vi å finne hva i teksten som representerer en person, en virksomhet eller et geografisk sted.

Men så har vi spørsmålet om hvilke at disse som refererer til **samme** person eller virksomhet. Det er veldig interessant, og jeg fant en artikkel i [Medium](https://towardsdatascience.com/from-text-to-knowledge-the-information-extraction-pipeline-b65e7e30273e) som beskriver et eksempel på hvordan denne prosessen kan se ut. Han har en pipeline på [Github](https://github.com/tomasonjo/trinity-ie) som er satt sammen av flere interessante komponenter. Som han nevner i artikkelen, er det vanskelig å få installert de forskjellige modulene slik at de snakker sammen og er fornøyd med hverandre. Men det kan anbefales. Jeg kom i havn med Python 3.6, Spacy 2.3 og å clone ned neuralcoref og openNRE og installere de lokalt.

Uansett, så har jeg trukket ut den første biten fra det repoet som er [Wikifier](http://www.wikifier.org/). 





Individuals found in the training set, containing 'mari':

> Mentions of Fredrikke Marie Qvam in the training set, according to Wikifier:
[Web page: ](http://no.wikipedia.org/wiki/Fredrikke_Marie_Qvam)
Hun har bakgrunn som journalist i Klassekampen , og utga i 2013 en biografi om Fredrikke Marie Qvam , en av strategene bak kvinnenes seier i kampen for stemmerett .

Mentions of Maria I av England in the training set, according to Wikifier:
Web page: http://no.wikipedia.org/wiki/Maria_I_av_England
Dette er Maria Menas nyeste plate :
Maria Kannegaard trio :
Maria Mena :
Å « synge sin dagbok » er det Maria Mena gjør .
```
Mentions of Maria Mena in the training set, according to Wikifier:
Web page: http://no.wikipedia.org/wiki/Maria_Mena
Årets album viser Maria Mena fra en lysere side , der mye av musikken er gitarbasert , gode og varierte låter i et fengende , melodisk poplandskap .
« Mellow » befester Maria Menas stilling som en av våre unge , dyktige låtskrivere .

Mentions of Maria Mittet in the training set, according to Wikifier:
Web page: http://no.wikipedia.org/wiki/Maria_Mittet
Maria Mena synger bedre enn noen gang .

Mentions of Mariann Thomassen in the training set, according to Wikifier:
Web page: http://no.wikipedia.org/wiki/Mariann_Thomassen
Factor » betyr ikke nødvendigvis at din egen popkarriere får et oppsving - bare spør Mira Craig eller Mariann Thomassen .

Mentions of Mario Götze in the training set, according to Wikifier:
Web page: http://no.wikipedia.org/wiki/Mario_G%c3%b6tze
Mario Götze erstattet tidenes mestscorende i VM-historien , Miroslav Klose , etter 88 minutter .
Og i 2014 var det altså unggutten Mario Götze som ble den store helten , til tross for at han ikke har vært fast på det tyske laget de siste VM-kampene .

Mentions of Marion Ravn in the training set, according to Wikifier:
Web page: http://no.wikipedia.org/wiki/Marion_Ravn
Marion Ravn debuterer i samme rolle i morgen kveld , og for at vi ikke skal være i tvil om hvorfor hun er med lanserte hun sin nye singel på P4 i går .
```



Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
