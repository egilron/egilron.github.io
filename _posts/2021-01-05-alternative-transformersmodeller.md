---
published: false
---
Så langt har vi gjort Targeted sentemintanalyse med multilingual BERT som forhåndstrent språkmodell (pretrained language model). Men det kommer jo stadig nye modeller, så hva skal til for at vi kan bruke andre modeller til denne jobben? Det som skal til, er:


1. Modellen må være trent på norske data.
1. Modellen må fungere i [NER-oppsettet til Simpletransformers](https://simpletransformers.ai/docs/ner-specifics/#supported-model-types).

For å få til det første, trenger vi en flerspråklig modell. Jeg kjenner ikke til noen enspråklige norske modeller tilgjengelig, så vi må bruke en flerspråklig.  Hos [Huggingface](https://huggingface.co/transformers/multilingual.html) ser vi at de flerspråklige modellene er av type XLM, BERT, og XLM-RoBERTa. XLM fungerer ikke til denne oppgaven, men BERT og XLM-RoBERTa fungerer.
### Flerspråklige modeller som skal fungere til norsk targeted sentimentanalyse med Simpletransformers:

`bert-base-multilingual-uncased` 
Dette er den første multilingual BERT. "Uncased" betyr "lowercased", altså at stor bokstav er gjort liten. Dette er den første modellen de ga ut, men det anbefales nå å bruke cased. Jeg har bare prøvd cased.

`bert-base-multilingual-cased` 
Dette er modellen jeg har brukt til de fleste av mine eksperimenter. Fungerer bra på min maskin.

`xlm-roberta-base` 
Denne har jeg prøvd et par ganger, og den ga markant bedre resultat enn m-BERT. Men jeg slet med at GPU-minnet ble fullt, så jeg måtte skru ned batch-størrelsen.

`xlm-roberta-large` 
Akkurat som at BERT har en large-modell, så har denne det også. I stedet for en kuleis med to kuler og strø, går man for en dansk tolv-kulers is med guff og alt sammen. large-modellene er større og bedre, men derfor også tyngre og breiere, og siden jeg slet med å kjøre xlm-roberta-base, så prøvde jeg meg ikke på large-versjonen.

**Er det bedre, jo større de er?** Når vi driver med eksperimentering og forskning, er vi ofte bare ute etter den modellen som gir det beste resultatet på oppgaven vi har. Men når modellen skal brukes til noe fornuftig, sammen med andre komponenter som også bruker tid, er det en grense for hvor stor modellen kan være, før den blir uhåndterlig i praksis. Noen ganger er ett sekund for lenge å vente på et resultat, og noen ganger skal modellene brukes på maskiner som ikke takler alle mulige slags kompleksiteter. Derfor ser du at flere av modellene som Huggingface har gjort tilgjengelige, ikke er unike med at de er større og bedre enn forgjengerne, men at den er mindre og mer effektiv, men allikevel "god nok" til mange praktiske oppgaver.

**Kan man bruke modeller som andre har trent, og som ikke Huggingface har lagt ut?** Det går i hvert fall an å bruke ["community"-modellene hos Huggingface](https://huggingface.co/transformers/model_sharing.html?highlight=community%20models). Simpletransformers har opplegg for å importere disse modellene.
