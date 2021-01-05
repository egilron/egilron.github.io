---
published: false
---
Så langt har vi gjort Targeted sentemintanalyse med multilingual BERT som pretrained language model. Men det kommer jo stadig nye modeller, så hva skal til for at vi kan bruke andre modeller til denne jobben? Det som skal til, er:


1.Modellen må være trent på norske data.
1.Modellen må fungere i (NER-oppsettet til Simpletransformers)[https://simpletransformers.ai/docs/ner-specifics/#supported-model-types]

For å få til det første, 

https://huggingface.co/transformers/model_summary.html#autoencoding-models