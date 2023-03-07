---
title: 'Voiko syntyvyyttä ennustaa?'
date: 2023-03-8
permalink: /posts/2023/02/syntyvyys/
image: /images/syntyvyys/teddybearphoto.png
largeimage: /images/syntyvyys/teddybearphoto.png
summary: 'Blogi | Jälkikäteinen arvio siitä, miten hyvin 2018 tehty syntyvyysennuste onnistui. Mukana myös uusi ennuste hedelmällisyysluvulle.'
tags:
  - syntyvyys
  - kokonaishedelmällisyysluku
---

Suomessa syntyvyys on pudonnut rajusti vuoden 2010 jälkeen: Syntyneiden lasten määrä on Suomessa laskenut 61 000 lapsesta vuonna 2010 noin 44 900:ään vuonna 2022. Hedelmällisyysluku on jäämässä vuoden 2022 alustavien tietojen mukaan 1,31:een, joka kaikkien aikojen matalin (Tilastokeskus, 2023). Laskeva trendi on jatkunut lähes koko aikavälin 2010-2023, joten satunnaisvaihtelusta ei ole kysymys (Kuva 1). 

# Ennustaminen

Syntyvyyden ennustaminen on vaikeaa, koska syntyvyyden muutokseen vaikuttavia tekijöitä ei kovin hyvin tunneta. Tein [marraskuussa 2018 ennusteen](https://ajtanskanen.github.io/posts/2018/11/Sosiaalisen-median-aktiivik%C3%A4ytt%C3%B6-ja-syntyvyys/) syntyvien lasten lukumäärän ja kokonaishedelmällisyysluvun kehityksestä. Nyt muutaman vuoden jälkeen on hyvä palata aiheeseen ja tarkastaa, osuiko ennuste kohdilleen. 
Osoittautui, että ennuste oli paljon paremmin kuin osasin edes odottaa. 

Tein analyysiä syntyvyyden ja hedelmällisyysluvun laskusta, missä käytin yksinkertaista regressiomallia. Sen avulla tein myös ennusteen vuosille 2018 - 2030. Kuva 1 näyttää ennusteen kokonaishedelmällisyysluvulle yhdessä vertailuaineiston kanssa. Kuvassa musta käyrä näyttää havaitut kokonaishedelmällisyysluvut vuosina 1990-2017 ja arvion vuoden 2018 kokonaishedelmällisyysluvuksi. Turkoosi käyrä näyttää sovitteen 1990-2017. 

### Kokonaishedelmällisyys

![IRR:t](/images/syntyvyys/ennuste2018.png)
_Kuva 1. Vertailu vuoden 2018 ennusteen (vihreä Ennuste) osuvuudesta. Punaisella on merkitty dataa, joka ei ollut saatavilla ennustetta tehtäessä._

Vuonna 2018 tehty ennuste vuosille 2018-2030 on kuvassa merkitty katkoviivalla. Kun ennustetta vertaa vuosien 2018-2022 havaintoihin, huomaa että ennuste on vuosina 2020 ja 2022 kohdallaan, mutta muina vuosina on eroa. Vuoden 2021 koronapiikkiä tuskin olisi voinut edes ennustaa.  

Kuvan 1 neljästä uudesta havainnosta kaksi on aivan kohdallaan. Erityisesti vuoden 2022 arvio on hyvä: toteutunut oli 1,31 ja ennuste 1,32. Onnistumisesta huolimatta on pettynyt olo: en olisi halunnut nähdä trendin jatkuvan näin hyvin. Mielummin olisin 

Vertailun vuoksi kuvaan 2 oli lisätty kokonaishedelmällisyysluku Tilastokeskuksen väestöennusteesta 2018 (Väestöennuste, pisteviiva) ja kokonaishedelmällisyysluvun trendin lineaarinen jatko. Kiinnostavasti lineaarinen jatko ennustee vuosien 2018 
ja 2019 kokonaishedelmällisyysluvut hyvin, mutta poikkeaa sen jälkeen rajusti toteutuneista luvuista. Näistä kolmesta ennusteesta faktorimalli on selvästi paras. 

### Syntyneiden määrä
![IRR:t](/images/syntyvyys/syntyneita2018.png)
_Kuva 2. Syntyneiden lukumäärä 2018 verrattuna toteutuneeseen._

Vastaava vertailu syntyneiden lukumäärille on kuvassa 2. Se kertoo samaa tarinaa. 

## Mistä lasku johtuu?

Osan syntyneiden lukumäärän laskusta selittää synnytysikäisten naisten lukumäärän pieneneminen, mutta ei kaikkea. Muiksi selityksiksi on tarjottu mm. työttömyyttä (Hiilamo, 2017) ja miesten heikkoa työsuhteeseen kiinnittymistä (Miettinen ja Jalovaara, 2015). Muissa maissa syntyvyyden laskun on arvioitu aiheutuvan mm. lapsikuolleisuuden vähenemisestä (Becker ja Barro, 1988), kaupungistumisesta (Martine et al., 2013) ja vanhuuseläkkeiden korkeammasta korvausasteesta (Boldrin et al., 2015). Sen lisäksi että työttömyys alentaisi syntyvyyttä, taloudellisten kriisien on myös havaittu lisänneen syntyvyyttä (Kohler ja Kohler, 2002). Suomessa Korona-kriisin aikana syntyvyys kasvoi vuosina 2020 ja 2021, mutta ei enää 2022.
Myös Väestöntutkimuslaitos on analysoinut syitä syntyvyyden laskulle, mutta selkeätä syytä ei ole löytynyt (Rotkirch et al, 2017).

Tässä tarkastellussa regressiomallissa tärkeimmät tekijät ovat kaupungistuminen, avioliittojen määrän lasku ja sosiaalisen median päivittäisen käytön lisääntyminen. Ennuste on tehty jatkamalla havaittuja trendeja avioituvuudelle, kaupungistumiselle ja aktiivisten somen käyttäjien osuudelle lineaarisesti ajassa eteenpäin. Muut tekijät pidetään vakiona. Tarkastellaan kolmea tärkeintä faktoria seuraavassa erikseen. 

### Kaupungistuminen
Kaupungistumista kuvaa sisemmässä kaupungissa, ulommassa kaupungissa ja kehyskaupungissa asuvien osuudet väestöstä. 
Kuva 3 näyttää ennusteissa käytetyt Tilastokeskuksen datat (Tilastokeskus, 2023b). Tasoero johtuu siitä, että uudemmassa Tilastokeskuksen aineistossa on tehty määritelmämuutos.

![IRR:t](/images/syntyvyys/sisempikaupunki.png)
_Kuva 3. Sisemmässä kaupungissa asuvien osuus väestöstä vuoden 2018 ennusteessa ja vuoden 2023 ennusteessa._

Sisempi kaupunkialue on kaupunkien tiivis yhtenäinen tehokkaasti rakennettu alue.
Ulompi kaupunkialue on sisemmän kaupunkialueen reunasta yhtenäisesti jatkuvan
taajamarakenteen reunalle ulottuva kaupunkimaisen tehokkuuden alue.
Kaupungin kehysalue on kaupunkiin välittömästi kytkeytyvä osa kaupungin ja maaseudun välivyöhykkeestä.
Maaseutualueet rajataan kaupunkien kehysalueiden ulkopuolelle.

Mallissa erityisesti sisemmässä kaupungissa asuvien osuus väestöstä vaikuttaa syntyvyyteen. Mitä suurempi osa
väestöstä asuu tiiviisti kaupunkien keskustoissa, sen alempi syntyvyys. Tämä osuus kasvaa edelleen, mikä regressiomallin mukaan
tulee jatkossakin alentamaan syntyvyyttä.

Ei ole täysin selvää, miksi kaupungistuminen alentaa syntyvyyttä. Kaupungistumiseen liittyy ainakin anekdotaalisen tiedon mukaan "ikisinkkuus", johon eivät mahdu pysyvät parisuhteet eivätkä lapset.
Kaupungistumisen vaikutus kytkeytyy siten osin parisuhteiden laadun muutokseen. Toinen syy, miksi sisempi kaupunki kytkeytyy 
syntyvyyteen, on se, että perheasuntojen hinnat ovat sisemmässä kaupungissa korkeita ja saattavat vähentää lasten hankintaa.

### Parisuhteet
Avioliittojen määrä on lähinnä proksi parisuhteiden määrälle. Syntyvyyden aleneminen liittyy väistämättä parisuhteiden määrään.
Ilmeisesti viime vuosina pysyvien parisuhteiden määrä on laskenut, vaikka parisuhteiden määrä ei niinkään ole laskenut (Tilastokeskus, 2023c).

![IRR:t](/images/syntyvyys/avioituvuus.png)
_Kuva 4. Avioituvuus_

Avioituvuus jatkaa tämän arvion mukaan laskua. Kulmakertoimen on kuitenkin arvioitu olevan aiempaa loivempi, jolloin
se ei vähennä yhtä paljon syntyvyyttä kuin kuin 2010 jälkeen.

### Sosiaalinen media
Verrattuna aiempiin harjoitelmiin, mukaan on otettu myös sosiaalisen median aktiivikäyttäjien osuus Tilastokeskuksen Viestintä- ja tietotekniikan käyttö-tutkimuksesta (“Seuraa jotain yhteisöpalvelua yleensä jatkuvasti kirjautuneena tai useasti päivässä”).

![IRR:t](/images/syntyvyys/some.png)
_Kuva 5. Sosiaalisen median päivittäinen käyttö_

Somen käyttöä kuvaa päivittäin sosiaalista mediaa käyttävien osuus (Tilastokeskus, 2023a). 
Sosiaalisen median käyttö kasvoi koronavuonna 2020 voimakkaasti. Se näyttää saturoituneen, ja tuskin enää jatkossa vaikuttaa
syntyvyyttä nykyisestä laskevasti. Kuva 6 näyttää vuoden 2018 ennusteessa käytetyn datan ja Tilastokeskuksen uuden datan (2023a). Katkoviivalla on näytetty ennuste sosiaalisen median käytön kehityksestä.

# Uusi ennuste
Päivitin datan siihen, mitä on saatavissa 1.3.2023. Kuvassa on päivitetty versio kokonaishedelmällisyysluvun ennusteesta.
Aiemmassa ennusteessa kokonaishedelmällisyysluku aleni 1,1:een vuonna 2030. Päivitetty ennuste menee vielä alemmas: vuonna 2030 kokonaishedelmällisyysluku on 1,0x.

Tuloksissa parhaana näkyy neljän faktorin ja vakiotermin malli, jossa faktoreina ovat 30-34 -vuotiaiden avioituvuus, sisäkaupungissa ja kehyskaupungissa asuvien osuus, sekä 35-44 -vuotiaiden sosiaalisen median aktiivikäyttäjien osuus. Näillä faktoreilla on mahdollista selittää noin 97 % kokonaishedelmällisyysluvun varianssista datassa.

Aineiston perusteella ei voi tehdä kausaalisia päätelmiä, ainostaan assosiatiivisuutta koskevia. Tämä tietenkin rajoittaa tulkintamahdollisuuksia.

![IRR:t](/images/syntyvyys/ennuste2023.png)
_Kuva 6. Uusi ennuste kokonaishedelmällisyysluvulle vuosina 2023-2030._

### Syntyneiden määrä
Syntyneiden määrässä näkyy samanlainen kehitys kuin kokonaishedelmällisyysluvussa. Syntyneiden määrään vaikuttaa kokonaishedelmällisyysluvun lisäksi synnytysikäisten naisten määrä, mistä johtuu pidempään kestänyt laskeva trendi.

![IRR:t](/images/syntyvyys/syntyneita2023.png)
_Kuva 7. Uusi ennuste syntyneiden määrälle vuosina 2023-2030._

### Vertailu aiempaan ennusteeseen
Uusi hedelmällisyyslukuennuste on hyvin samankaltainen kuin aiempi ennuste. Uusi ennuste on hieman alempi kuin aiempi (kuva 12).

![IRR:t](/images/syntyvyys/ennustevertailu.png)
_Kuva 8. Vuosien 2018 ja 2023 ennusteet kokonaishedelmällisyysluvulle._

Uuden ennusteen mukaan vuoden 2030 kokonaishedelmällisyysluku on 1,044, kun aiemman ennusteen mukaan se tulee olemaan 1,103.
Ennuste on vielä synkempi kuin aiempi huolimatta korona-ajan noususta. Tämän ennusteen mukaan se jää väliaikaiseksi. Toivottavasti ennuste on tällä kertaa väärässä, ja syntyvyys kääntyy nousuun.

### Regressiomalli

Taulukoissa 1-3 esitetään bayesilaisten regressiomallien yksityiskohtia. Ne ovat valitettavasti hieman vaikealukuisia.
sekä todennäköisin malli (HPM) että agregaatti 1024:stä todenäköisimmästä regressiomallista.
Kuvio ovat hieman hankalalukuisia, joten ne voi hyvinkin hypätä yli.

![IRR:t](/images/syntyvyys/posterior2023.png)
_Taulukko 1. Regression termit, todennäköisin malli_

![IRR:t](/images/syntyvyys/bmaposterior2023.png)
_Taulukko 2. Regression termit, aggregaatti_

![IRR:t](/images/syntyvyys/coef2023.png)
_Taulukko 3. Todennäköisyys että faktorin kerroin poikkeaa nollasta (P(B!=0)) kaikissa malleissa. Lisäksi näytetään kuuluvatko faktorit todennäköisimpiin malleihin. Rivi R2 kertoo kuinka suuren osuuden varianssista malli selittää._

Mallit 1-3 selittävät 97 - 97,9 % datan varianssista. Tällä mittarilla ne siis ovat selitysvoimaisia. 
Malleissa on 2-5 tekijää, jos vuoden 2021 poikkeavaa hedelmällisyyttä kuvaava dummy-muuttuja huomioidaan.
Uudessa ennusteessa on käytetty dummy-muuttujaa kuvaamaan vuoden 2021 poikkeuksellista kehitystä.

# Johtopäätökset
Vuonna 2018 tehty ennuste osui kohdalleen yllättävän hyvin. Koronan vaikutusta syntyvyyteen tuskin olisi ollut mahdollista ennustaa vuonna 2018. Ennusteessa kokonaishedelmällisyyslukuun vaikuttavat kaupungistuminen, avioituvuus ja päivittäinen some käyttö, joista erityisesti kaupungistuminen ja avioituminen vaikuttavat jatkossa. 

Pysyvien parisuhteiden määrään ei voi vaikuttaa etuuksilla, joten etuusmuutoksilla tuskin voi kovin paljon vaikuttaa syntyvyyteen. Kaupungistumista tuskin on mahdollista tai edes syytä hidastaa. On epäselvää, miksi kaupungistuminen alentaa syntyvyyttä. Mahdollisia selityksiä ovat esimerkiksi kaupunkilainen ikisinkkuus ja lapsiperheille pienet asunnot.

Joka tapauksessa tulevaisuus näyttää entistä vähälapsiselta.

# Viittaukset

Becker, G.S., Barro, R.J., Reformulation of the economic theory of fertility, The quarterly journal of economics, 1988

Boldrin, M., De Nardi, M., Jones, L.E. Fertility and social security, Journal of Demographic Economics 81, 261-299, https://doi.org/10.1017/dem.2014.14, 2015

Doepke, M., Child mortality and fertility decline: Does the Barro-Becker model fit the facts?

Hiilamo, H. T., Fertility Response to Economic Recessions in Finland 1991–2015 Finnish Yearbook of Population Research 52, 15-28 . DOI: 10.23979/fypr.65254, 2017

Kohler, H.-P., Kohler, I., Fertility Decline in Russia in the Early and Mid 1990s: The Role of Economic Uncertainty and Labour Market Crises, European Journal of Population 18, 233-262, https://doi.org/10.1023/A:1019701812709, 2002.

Martine, G., Alves, J.E., Cavenaghi, S., Urbanization and fertility decline: Cashing in on structural change, IIED Working paper, 2013

Miettinen, A., Miksi syntyvyys laskee? Suomalaisten lastensaantiin liittyviä toiveita ja odotuksia. Perhebarometri 2015. Väestöliitto, 2015.

Miettinen, A., Jalovaara, M. Stable employment – more babies? Life stage and educational differences in the effects of labour market attachment on first birth among Finnish men and women. Working Papers on Social and Economic Issues 15/2016, Turku Center for Welfare Research, 2016

Rotkirch, A., Tammisalo, K., Miettinen, A., Berg, V. Miksi vanhemmuutta lykätään? Perhebarometri, 2017.

Tanskanen, A.J. Sosiaalisen median aktiivikäyttö ja syntyvyys. https://ajtanskanen.github.io/posts/2018/11/Sosiaalisen-median-aktiivik%C3%A4ytt%C3%B6-ja-syntyvyys/, 2018

Tikanmäki, H., Huomisen aikuiset syntyvät nyt, Eläketurvakeskuksen blogi https://www.etk.fi/blogit/huomisen-aikuiset-syntyvat-nyt/, 2017

Tilastokeskus (2023a) Suomen virallinen tilasto (SVT): Väestön tieto- ja viestintätekniikan käyttö / 13ud -- Väestön tieto- ja viestintätekniikan käyttö sukupuolen ja ikäluokan mukaan, 2013-2022 sarja "Käyttänyt yhteisöpalvelua päivittäin tai lähes päivittäin, %" ISSN=1797-6413. Helsinki: Tilastokeskus [Viitattu: 7.3.2023]. Saantitapa: https://stat.fi/tilasto/sutivi

Tilastokeskus (2023b) Suomen virallinen tilasto (SVT): Väestörakenne [verkkojulkaisu]. Taulukko 11ra -- Tunnuslukuja väestöstä alueittain, 1990-2021. ISSN=1797-6413. Helsinki: Tilastokeskus [Viitattu: 7.3.2023]. Saantitapa: https://stat.fi/tilasto/vaerak

Tilastokeskus (2023c) Avioituvuus promillea, Suomen virallinen tilasto (SVT): Siviilisäädyn muutokset [verkkojulkaisu].
ISSN=1797-6413. Helsinki: Tilastokeskus [Viitattu: 7.3.2023]. Saantitapa: https://stat.fi/tilasto/ssaaty