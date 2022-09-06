---
title: 'Sentimenttianalyysi kertoo tekstin sävyn'
date: 2022-09-06
permalink: /posts/2022/09/sentimenttianalyysi/
image: /images/sentimentti/medieval.png
largeimage: /images/sentimentti/medieval.png
summary: 'Blogi | Sentimenttianalyysi kertoo tekstin sävyn: onko se positiivinen, neutraali tai negatiivinen. Tekoäly on tehokas apu siinä.'
tags:
  - AI
  - tekoäly
  - sentimenttianalyysi
---

Sentimenttianalyysi kertoo, onko jokin tekstin sävy positiivinen, negatiivinen tai neutraali. Tässä tekstissä kuvataan lyhyesti, miten
sentimenttianalyysiä voi tehdä OpenAI:n GPT-3:lla.

Sentimenttianalyysi 
=====

Helppo tapa tehdä sentimenttianalyysiä on käyttää listaa yksittäisten sanojen sävystä ja laskea tekstin sanojen sävyjen summa. Toinen tapa on opettaa keinotekoinen neuroverkko aineiston avulla
arvioimaan tekstin sävyä. Uusien, suurten kielimallien tulon jälkeen myös niiden käyttö onnistuu hyvin.
Tässä käytetään OpenAI:n GPT-3 -kielimallia, jossa on 175 miljardia parametria. 

Sentimenttianalyysiin tarvitsee vain tunnukset OpenAI:n GPT-3:een. Ne saa luomalla tunnuksen osoitteessa 
[https://openai.com/api/](https://openai.com/api/).
Kun tunnukset on luotu, voi GPT-3:a käyttää sentimenttianalyysiin Playgroundissa. 
Jos tarve on analysoida suurempia tietomääriä, onnistuu
se ohjelmallisesti vaikkapa Pythonista.

Ja sitten vain itse sentimenttianalyysiin, joka onnistuu komentamalla GPT-3:a suomeksi.
Aloitetaan testaamalla, miten variaatiot "Huomenta, Turku" lauseesta sovittuvat sentimentiksi:
Kokeillaan variaatioita lauseesta GPT-3:lla. Kielimallia "komennetaan" antamalla syöte, jota
malli jatkaa. Tässä tapauksessa sitä pyydetään analysoimaan lauseen sentimentti.

![Sentimentti](/images/sentimentti/+2.png)

*Kuva 2. Sentimentti lauseelle "Erittäin hyvää huomenta, Turku.*

Tulosten mukaan 

| Syöte | Sentimentti | 
| -------- | -------- | 
| Erittäin surkeaa huomenta, Turku | -2 | 
| Surkeaa huomenta, Turku | -1 | 
| Huomenta, Turku | 0 | 
| Hyvää huomenta, Turku | +1 | 
| Erinomaista huomenta, Turku | +2 |

GPT-3 selvitti tämän testin hienosti. Asetuksina tässä käytettiin lämpötilaa 0, jolloin GPT-3 antaa parhaaksi katsomansa
vastauksen. Sentimenttianalyysin teko on helppoa ja tulokset ovat yllättävän oikeita kielimallilla tehtynä. Aivan kaikkea ei malli ymmärrä,
mutta suuri kuva vaikuttaa olevan oikein. Työläintä sentimenttianalyysissä on aineiston kerääminen. Itse analyysi sujuu kielimallilla
sutjakkaasti.
