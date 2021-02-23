---
published: false
---
Når vi gjør Targeted Sentiment Analysis, ønsker vi å finne hva i teksten som omtales positivt eller negativt. 

Når vi gjør Named Entity Recognition, ønsker vi å finne hva i teksten som representerer en person, en virksomhet eller et geografisk sted.

Men så har vi spørsmålet om hvilke at disse som refererer til **samme** person eller virksomhet. Det er veldig interessant, og jeg fant en artikkel i [Medium](https://towardsdatascience.com/from-text-to-knowledge-the-information-extraction-pipeline-b65e7e30273e) som beskriver et eksempel på hvordan denne prosessen kan se ut. Han har en pipeline på [Github](https://github.com/tomasonjo/trinity-ie) som er satt sammen av flere interessante komponenter. Som han nevner i artikkelen, er det vanskelig å få installert de forskjellige modulene slik at de snakker sammen og er fornøyd med hverandre. Men det kan anbefales. Jeg kom i havn med Python 3.6, Spacy 2.3 og å clone ned neuralcoref og openNRE og installere de lokalt.

Uansett, så har jeg trukket ut den første biten fra det repoet som er [Wikifier](http://www.wikifier.org/). 







Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
