---
published: true
title: Timeseries med LSTM i Keras
---
### En liten avsporing

I løpet av studiet innen språkteknologi har jeg jobbet mye med LSTM. Det er et nyttig verktøy for analyse av tekst. Men tekst har sine særegenheter, og jeg har hatt lyst til å bruke LSTM med andre data også. Da en venn spurte meg for artighet om vi skulle lagd en modell som spår aksjekurser, så ble det en anledning til å utforske time series. Jeg har for det meste brukt pyTorch til nevrale nett, men dette ble en anledning til å prøve Keras, som er en forenklende overbygging på TensorFlow. 

Så siden LSTM er en nyttig sak å kunne innen språkteknologi generelt, så nevner jeg det her, sjøl om det ikke har noe annet til felles med emnet for bloggen ellers.
![Tesla-aksjekursen]({{site.baseurl}}/img/lstm_predict_tesla.png)

Notebooken ligger i et eget repo [her](https://github.com/egilron/misc/blob/main/lstm_keras_224.ipynb), siden det har så lite å gjøre med de andre tingene.