---
title: 'Twiittien fiilis budjettiriihestä kääntyi negatiiviseksi'
date: 2022-09-07
permalink: /posts/2022/09/sentimenttianalyysi/
image: /images/sentimentti/medieval.png
largeimage: /images/sentimentti/medieval.png
summary: 'Blogi | Sentimenttianalyysi kertoo tekstin sävyn: onko se positiivinen, neutraali tai negatiivinen. Tekoäly on tehokas apu siinä.'
tags:
  - AI
  - tekoäly
  - sentimenttianalyysi
  - budjettiriihi
---

Budjettiriihessä tehtiin 1.9.2022 päätöksiä valtion varojen käyttökohteista. Budjettiriihestä ja budjetista käytiin
Twitterissä innokasta keskustelua sekä ennen budjettiriihtä että sen jälkeen. Alun positiivinen tunnelma kääntyi sentimenttianalyysin mukaan negatiiviseksi.

Budjettiriihi
=====

Oman tuntuman mukaan twitter-kupla tuntui suhtautuvan negatiivisesti budjettiriihen päätöksiin.
Mutta oliko oikeasti näin? Kuplautuminen helposti filtteröi eri mieltä olevien twiittejä.

![Sentimenttien jakauma](/images/sentimentti/kurronen.png)

*Kuva 1. Twitterissä kommentaari budjettiriihestä oli paikoin railakasta.*


Sentimenttianalyysi 
=====

Sentimenttianalyysi kertoo, onko jokin tekstin sävy positiivinen, negatiivinen tai neutraali. Helppo tapa tehdä sentimenttianalyysiä on käyttää
listaa yksittäisten sanojen sävystä ja laskea tekstin sanojen sävyjen summa. Toinen tapa on opettaa keinotekoinen neuroverkko aineiston avulla
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

Siirrytään sitten budjettiriihen pariin.

Budjettiriihen analyysi
=====

Haetaan Twitterin haulla twiitit aiheista _budjettiriihi_ ja _budjetti_, missä retwiittaukset on jätetty pois. 

Analysoidaan sitten sentimentti GPT:llä.
 Hieman yllättäen sentimentti on kokonaisuudessaan positiivinen: yli puolet twiiteistä suhtautuu positiivisesti budjettiriiheen.

![SEntimenttien jakauma](/images/sentimentti/riihi.png)

*Kuvio 3. Budjettiriihitwiittien sentimentten jakauma.*

Tässä muutama esimerkki twiitteistä ja niiden sentimenteistä

| Twiitti | Sentimentti |
| ----- | ----- |
| Alueellisen opintolainahyvityksen kokeilu on opiskelijoita epätasa-arvoistava päätös. Se kehittää opintotukijärjestelmää väärään suuntaan sitoen sitä entistä enemmän opiskelijoiden velkaantumiseen. #budjettiriihi @SYL_FIN |-2 |
| Tämä sotataloudessa oleminen on siitä huvittavaa, että mistään valtion menoista ei voi kiristää, vaan ainoa tapa pärjätä on ottaa lisää velkaa. #budjettiriihi | -1 |
| Budjettiriihi alkoi. Tuleeko hallituksen budjetista vaalibudjetti? Keskustelemassa @EmiliaKullas Anni Huhtala ja @Maliranta. Kuuntele #Politiikkaradio klo 13 @yleradio1.  | 0 |
| Yksi tärkeä #budjettiriihi päätös on varhaiskasvatusmaksujen pysyvä alentaminen, jolla tuetaan lapsiperheitä ja vahvistetaan työllisyyttä. Samalla se on askel kohti @Demarit tavoitetta maksuttomasta varhaiskasvatuksesta. | +1 |
| Suomi ei menesty ilman koulutusta ja osaamista. Opettajat rakentavat tulevaisuutta koko yhteiskunnan ja ty√∂markkinoiden hyväksi.
Opettajatarvetta on ennakoitava ajoissa. #opettajarekisteri #budjettiriihi | +2 |

Kaikkiaan analysoituja twiittejä on 1926 kpl, ja ne ovat aikaväliltä 30.8.2022 - 6.9.2022.

Ennen budjettiriiheä
-----
Erityisesti ennen budjettiriiheä kirjoitetut twiitit ovat positiivisia. Kuvio 4 näyttää twiittien sentimenttien jakauman.
Vajaat puolet twiiteistä on positiivisia tai erittäin positiivisia. Negatiivisia on hieman yli 30 prosenttia.

![SEntimenttien jakauma](/images/sentimentti/ennen.png)

*Kuvio 4. Sentimenttianalyysi ennen budjettiriiheä julkaistuista twiiteistä.*

Twiittien positiivisuus selittynee sillä, että eri tahot tarjoavat omia ehdotuksiaan budjettiriiheen. Esimerkiksi

| Twiitti | Sentimentti |
| ----- | ----- | 
| Eduskunnan AMK- ja työelämä -verkosto peräänkuuluttaa rahoituksen varmistamista ammattikorkeakoulujen sote-alan harjoittelulle. @SivistysTA @oajry @Arene_ry #budjettiriihi #osaajapula | 1 |
| EK ja SAK kannattavat hoiva-avustajien lisäkoulutusta. Hoiva-avustajia tarvitaan lisää mm. vanhusten hoivaan. Vuoden koulutuksella voidaan osaltaan helpottaa nopeammin terveydenhuollon osaajapulaa. #budjettiriihi @jyrihakamies @ElorantaJa | 1 |

Budjettiriihen jälkeen
-----

Budjettiriihen jälkeen kirjoitetut kallistuvat negatiivisiksi. Puolet twiiteistä on negatiivisia tai erittäin negatiivisia.
Positiivisten osuus pysyy myös noin puolena.

![SEntimenttien jakauma](/images/sentimentti/jalkeen.png)

*Kuvio 5. Sentimenttianalyysi budjettiriihen jälkeen julkaistuista twiiteistä.*

Positiivisissa twiiteissä mm. kehutaan omien tavoitteiden läpimenemisestä.

| Twiitti | Sentimentti |
| ----- | ----- | 
| Budjettiesityksen mukaan hyvinvointialueiden yleiskatteelliseen rahoitukseen on tulossa noin 200 miljoonaa euroa enemmän kuin kevään kehysbudjetissa alloikoitiin - riittääkö se? @sll_aaltonen #budjettiriihi #hyvinvointialueet #lääkärilehti #talous | 1 |
| Sote-henkilöstön saatavuutta parannetaan ja hoiva-avustajia koulutetaan lisää #talousarvioesitys #budjettiriihi. Lisää päätöksiä tarvitaan. Sääntelyä joustavaksi ja mitoitusten kiristykset jäihin. #hoitajamitoitus | 1 |

Negatiivisten twiittien joukossa on twiittejä, joista ilmenee pettymys siihen, ettei haluttuja kohteita rahoitettu. Toisaalta 
niissä näkyy huoli velkaantumisesta ja talouskasvun puutteesta.

| Twiitti | Sentimentti |
| ----- | ----- | 
| Nyt tehdään isoja arvovalintoja, joilla on kauaskantoiset vaikutukset. Budjettiriihi oli kuolinisku järjestöjen työllistämistoiminnalle. | -2 |
| Suomen ongelma on, että talous ei ole juuri kasvanut 15 vuoteen. Jos talous olisi kasvanut Ruotsin tahtiin, olisi budjetti 10 mrd ylijäämäinen. Kun elintasosta on haluttu pitää kiinni, erotus maksetaan velalla. Toimii hetken, kunnes tarvitaan joko kasvua tai elintason laskua. | -1 |
| Hallituksen budjetti saa kritiikkiä niin velanotosta kuin ilmastotoimien unohtamisestakin. #budjettiriihi | -1 |


Päivä budjettiriihen jälkeen kirjoitetuissa negatiivisuus korostuu. Nyt jo yli 60 prosenttia kaikista twiiteistä on 
negatiivisia tai erittäin negatiivisia.

![SEntimenttien jakauma](/images/sentimentti/jalkeen1pv.png)

*Kuvio 6. Sentimenttianalyysi päivän budjettiriihen jälkeen julkaistuista twiiteistä.*

Budjettiriihen tunnelma jää tosiaan negatiiviseksi. Ehkä oma kuplani Twitterissä oli kuitenkin oikeassa.

Huomioita analyysistä
-----

Pääosin sentimentit on analysoitu oikein, mutta analyysissä on myös selviä huteja:

| En voi olla tyytyväinen oman puolueen @vihreat päätökseen tukea lentämisen alv-kannan laskemista nollaan! #budjettiriihi #ilmastonmuutos  | +2 |

Jos analyysiä haluaisi tarkentaa, voisi twiittien kirjoittajat jaotella ryhmiin. Esimerkiksi ekonomistitwitteriin, 
etujärjestöjen twiitterihin tai poliittisen kannan mukaan, kuten kuvassa 7. Tämä varmasti valottaisi sentimenttejä paremmin. Tässä 
en kuitenkaan tätä tarkempaan analyysiin ryhdy.

![SEntimenttien jakauma](/images/sentimentti/jouko.png)

*Kuva 7. Sentimenttianalyysi ekonomistitwitteristä.*

Lopuksi
=====

Ennen budjettiriiheä twiitit olivat pääosin myönteisiä. 
Budjettiriiheä koskevat twiitin kääntyivät kuitenkin negatiivisiksi heti budjettiriihen jälkeen. 
Tähän lienee monia syitä, mutta päällimmäisenä nousee ehkä aito pettymys budjettiriihen päätöksiin ja velkaantumiseen.


