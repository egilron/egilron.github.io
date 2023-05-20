---
published: false
title: Oppsett parametere
---
Nå skal vi sette opp simpletransformers til å ta imot dataene våre, og sette parameterene. 
Kjernfunksjonene er i bare tre linjer: Definere modellen, trene modellen, og evaluere modellen. Hos meg skjer det med kodelinjene:
```
    model = NERModel(family,transformersmodel , labels = tags,args=model_args)
    model.train_model(train_path, output_dir= out_d)
    result, model_outputs, predictions = model.eval_model(dev_path)
```
Jeg definerer disse variablene i andre linjer, for at det skal være enkelere å sette i gang sløyfer med flere eksperimenter. Min notebook for dette finner du [her:](https://github.com/egilron/norec_fine_tools/blob/master/Experiments21_norec_bert.ipynb)

Parameterne for treningen er noe du kan eksperimentere med. Simpletransformers fikk nytt opplegg for å sette parametre til denne type oppgaver nå i 2020, så jeg måtte skrive om koden jeg hadde fra siste vinter.
Her er mine parametre:
```
    model_args = NERArgs() # New args loading fall 2020
    model_args.train_batch_size = 32
    model_args.num_train_epochs = 3
    model_args.weight_decay = 0.001
    model_args.overwrite_output_dir = True
    model_args.silent = False
    model_args.save_steps = 200000
```
Jeg gjorde mine eksperimenter med åtte epoker, men tre skulle egentlig holde. Bruk 1 epoke først for å se at opplegget fungerer. Jeg har lagt til kode som skal lagre resultatene fra hvert eksperiment etter hvert som de kjører, og noe kode som samler alle eksperimentene til slutt. 