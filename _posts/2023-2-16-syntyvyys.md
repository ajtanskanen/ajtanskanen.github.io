---
title: 'Menikö syntyvyysennuste kohdilleen?'
date: 2023-03-1
permalink: /posts/2023/02/syntyvyys/
image: /images/syntyvyys/teddybearphoto.png
largeimage: /images/syntyvyys/teddybearphoto.png
summary: 'Blogi | Jälkikäteinen arvio siitä, miten 2018 tehty syntyvyysennuste onnistui.'
tags:
  - syntyvyys
---

Suomessa syntyvyys on pudonnut rajusti vuoden 2010 jälkeen. Syntyvyyden ennustaminen on vaikeaa, koska syntyvyyden muutokseen vaikuttavia tekijöitä ei kovin hyvin tunneta. Tein [marraskuussa 2018 ennusteen](https://ajtanskanen.github.io/posts/2018/11/Sosiaalisen-median-aktiivik%C3%A4ytt%C3%B6-ja-syntyvyys/) syntyvien lasten lukumäärän ja kokonaishedelmällisyysluvun kehityksestä. Nyt muutaman vuoden jälkeen on hyvä palata aiheeseen ja tarkastaa, osuiko ennuste kohdilleen. 
Osoittautuu, että paljon paremmin kuin osasin edes odottaa. Lopuksi päivitän
datan ja teen uuden ennusteen. Toivottavasti tällä kertaa menee vihdoin pieleen.

![IRR:t](/images/syntyvyys/tfr.png)
Kuva 1. Alkuperäinen, vuoden 2018 ennuste kokonaishedelmällisyysluvulle.

Johdanto
---

Syntyneiden lasten määrä on Suomessa laskenut 61 000 lapsesta vuonna 2010 noin 44 900:ään vuonna 2022 (Tilastokeskus, 2023). Hedelmällisyysluku on jäämässä vuoden 2022 alustavien tietojen mukaan 1,31:een, joka kaikkien aikojen matalin (Tilastokeskus, 2023). Laskeva trendi on jatkunut lähes koko aikavälin 2010-2023, joten satunnaisvaihtelusta ei ole kysymys. 

Tein vuonna 2018 analyysiä syntyvyyden ja hedelmällisyysluvun laskusta. Käytin yksinkertaista regressiomallia, jonka avulla tein myös ennusteen vuosille 2018 - 2030. Kuva 1 ennusteen. Kuvassa punainen käyrä näyttää havaitut kokonaishedelmällisyysluvut vuosina 1990-2017 ja arvion vuoden 2018 kokonaishedelmällisyysluvuksi. Turkoosi käyrä näyttää sovitteen 1990-2017 ja ennusteen vuosille 2018-2030.

Lukuunottamatta koronapiikkiä vuonna 2021, ennuste osui hyvin (Kuva 2). 

![IRR:t](/images/syntyvyys/ennuste2018.png)
Kuva 2. Vertailu vuoden 2018 ennusteen (vihreä Ennuste) osuvuudesta. Punaisella on merkitty dataa, joka ei ollut saatavilla ennustetta tehtäessä.

Kuvan 1 neljästä havainnosta kaksi on aivan kohdallaan. Erityisesti vuoden 2022 arvio on hyvä: toteutunut oli 1,31 ja ennuste 1,32. Onnistumisesta huolimatta on pettynyt olo: en olisi halunnut nähdä trendin jatkuvan näin hyvin. Mielummin olisin 

Ennuste on tehty jatkamalla havaittuja trendeja avioituvuudelle, kaupungistumiselle ja aktiivisten somen käyttäjien osuudelle lineaarisesti ajassa eteenpäin. 
Muut tekijät pidetään vakiona. 

![IRR:t](/images/syntyvyys/syntyneita2018.png)
Kuva 3. Syntyneiden lukumäärä 2018 verrattuna toteutuneeseen.

Mistä lasku johtuu?
---

Osan syntyneiden lukumäärän laskusta selittää synnytysikäisten naisten lukumäärän pieneneminen, mutta ei kaikkea. Muiksi selityksiksi on tarjottu mm. työttömyyttä (Hiilamo, 2017) ja miesten heikkoa työsuhteeseen kiinnittymistä (Miettinen ja Jalovaara, 2015). Muissa maissa syntyvyyden laskun on arvioitu aiheutuvan mm. lapsikuolleisuuden vähenemisestä (Becker ja Barro, 1988), kaupungistumisesta (Martine et al., 2013) ja vanhuuseläkkeiden korkeammasta korvausasteesta (Boldrin et al., 2015). Sen lisäksi että työttömyys alentaisi syntyvyyttä, taloudellisten kriisien on myös havaittu lisänneen syntyvyyttä (Kohler ja Kohler, 2002). Suomessa Korona-kriisin aikana syntyvyys kasvoi vuosina 2020 ja 2021.
Myös Väestöntutkimuslaitos on analysoinut syitä syntyvyyden laskulle, mutta selkeätä syytä ei ole löytynyt (Rotkirch et al, 2017).

Tässä tarkastellussa regressiomallissa tärkeimmät tekijät ovat kaupungistuminen, avioliittojen määrän lasku ja sosiaalisen median käytön lisääntyminen. Sosiaalisen median päivittäinen käyttö

### Kaupungistuminen
Kaupungistumista kuvaa sisemmässä kaupungissa, ulommassa kaupungissa ja kehyskaupungissa asuvien osuudet väestöstä. 

![IRR:t](/images/syntyvyys/sisempikaupunki.png)
Kuva 4. Sisemmässä kaupungissa asuvien osuus väestöstä.

Sisempi kaupunkialue on kaupunkien tiivis yhtenäinen tehokkaasti rakennettu alue.
Ulompi kaupunkialue on sisemmän kaupunkialueen reunasta yhtenäisesti jatkuvan
taajamarakenteen reunalle ulottuva kaupunkimaisen tehokkuuden alue.
Kaupungin kehysalue on kaupunkiin välittömästi kytkeytyvä osa kaupungin ja maaseudun välivyöhykkeestä.
Maaseutualueet rajataan kaupunkien kehysalueiden ulkopuolelle.

Mallissa erityisesti sisemmässä kaupungissa asuvien osuus väestöstä vaikuttaa syntyvyyteen. Mitä suurempi osa
väestöstä asuu tiiviisti kaupunkien keskustoissa, sen alempi syntyvyys. Tämä osuus kasvaa edelleen, mikä regressiomallin mukaan
tulee jatkossakin alentamaan syntyvyyttä.

Ei ole täysin selvää, miksi kaupungistuminen alentaa syntyvyyttä. Kaupungistumiseen liittyy ainakin anekdotaalisen tiedon mukaan "ikisinkkuus", johon ei mahdu pysyvät parisuhteet eivätkä lapset.
Kaupungistumisen vaikutus kytkeytyy siten osin parisuhteiden laadun muutokseen. Toinen syy, miksi sisempi kaupunki kytkeytyy 
syntyvyyteen, on se, että perheasuntojen hinnat ovat sisemmässä kaupungissa korkeita ja saattavat vähentää lasten hankintaa.

### Parisuhteet
Avioliittojen määrä on lähinnä proksi parisuhteiden määrälle. Syntyvyyden aleneminen liittyy väistämättä parisuhteiden määrään.
Ilmeisesti viime vuosina pysyvien parisuhteiden määrä on laskenut, vaikka parisuhteiden määrä ei niinkään ole laskenut (VIITTAUS).

![IRR:t](/images/syntyvyys/avioituvuus.png)
Kuva 5. Avioituvuus

Avioituvuus jatkaa tämän arvion mukaan laskua. Kulmakertoimen on kuitenkin arvioitu olevan aiempaa loivempi, jolloin
se ei vähennä yhtä paljon syntyvyyttä kuin kuin 2010 jälkeen.

### Sosiaalinen media
Verrattuna aiempiin harjoitelmiin, mukaan on otettu myös sosiaalisen median aktiivikäyttäjien osuus Tilastokeskuksen Viestintä- ja tietotekniikan käyttö-tutkimuksesta (“Seuraa jotain yhteisöpalvelua yleensä jatkuvasti kirjautuneena tai useasti päivässä”).

![IRR:t](/images/syntyvyys/some.png)
Kuva 6. Sosiaalisen median päivittäinen käyttö

Somen käyttöä kuvaa Tilastokeskuksen tietokannoista / StatFin / Väestön tieto- ja viestintätekniikan käyttö / 13ud -- Väestön tieto- ja viestintätekniikan käyttö sukupuolen ja ikäluokan mukaan, 2013-2022 sarja "Käyttänyt yhteisöpalvelua päivittäin tai lähes päivittäin, %"

Sosiaalisen median käyttö kasvoi koronavuonna 2020 voimakkaasti. Se näyttää saturoituneen, ja tuskin enää jatkossa vaikuttaa
syntyvyyttä nykyisestä laskevasti.

Uusi ennuste
---
Päivitin datan siihen, mitä on saatavissa 1.3.2023. Kuvassa on päivitetty versio kokonaishedelmällisyysluvun ennusteesta.
Aiemmassa ennusteessa kokonaishedelmällisyysluku aleni 1,1:een vuonna 2030. Päivitetty ennuste menee vielä alemmas: vuonna 2030 kokonaishedelmällisyysluku on 1,0x.

Tuloksissa parhaana näkyy neljän faktorin ja vakiotermin malli, jossa faktoreina ovat 30-34 -vuotiaiden avioituvuus, sisäkaupungissa ja kehyskaupungissa asuvien osuus, sekä 35-44 -vuotiaiden sosiaalisen median aktiivikäyttäjien osuus. Näillä faktoreilla on mahdollista selittää noin 97 % kokonaishedelmällisyysluvun varianssista datassa.

Aineiston perusteella ei voi tehdä kausaalisia päätelmiä, ainostaan assosiatiivisuutta koskevia. Tämä tietenkin rajoittaa tulkintamahdollisuuksia.

![IRR:t](/images/syntyvyys/ennuste2023.png)
Kuva 7. Uusi ennuste kokonaishedelmällisyysluvulle vuosina 2023-2030.

Ennuste on vielä synkempi kuin aiempi huolimatta korona-ajan noususta. Tämän ennusteen mukaan se jää väliaikaiseksi. Toivottavasti ennuste on tällä kertaa väärässä, ja syntyvyys kääntyy nousuun.

![IRR:t](/images/syntyvyys/syntyneet2023.png)
Kuva 8. Uusi ennuste syntyneiden määrälle vuosina 2023-2030.

### Regressiomalli

Kuvissa 9-11 esitetään sekä todennäköisin malli (HPM) että agregaatti 1024:stä todenäköisimmästä regressiomallista.
Kuvio ovat hieman hankalalukuisia, joten ne voi hyvinkin hypätä yli.

![IRR:t](/images/syntyvyys/posterior2023.png)
Kuva 9. Regression termit, todennäköisin malli

![IRR:t](/images/syntyvyys/bmaposterior2023.png)
Kuva 10. Regression termit, aggregaatti

![IRR:t](/images/syntyvyys/coef2023.png)
Kuva 11. Todennäköisyys että faktorin kerroin poikkeaa nollasta (P(B!=0)) kaikissa malleissa. Lisäksi näytetään kuuluvatko faktorit todennäköisimpiin malleihin. Rivi R2 kertoo kuinka suuren osuuden varianssista malli selittää.

Mallit 1-3 selittävät 97 - 97,9 % datan varianssista. Tällä mittarilla ne siis ovat selitysvoimaisia. 
Uudessa ennusteessa on käytetty dummy-muuttujaa kuvaamaan vuoden 2021 poikkeuksellista kehitystä. Dummyä tarvitaan 

Johtopäätökset
---
Vuonna 2018 tehty ennuste oli hyvä. Koronan vaikutusta syntyvyyteen tuskin olisi ollut mahdollista ennustaa vuonna 2018. Mielummin olisin nähnyt, että syntyvyys lähtee nousuun.

Regressiomalli kuvaa syntyvyyttä kaupungistumisen, avioituvuuden, some käytön avulla. Keskeiset syntyvyyteen vaikuttavat tekijät
ovat jatkossa mallin mukaan kaupungistuminen ja avioituminen. Pysyvien parisuhteiden määrään ei voi vaikuttaa etuuksilla, joten 
niillä tuskin voi vaikuttaa syntyvyyteen. Sitä vastoin syntyvyyttä voi edistää mahdollistamalla lasten hankinta niille, joille se ei muuten ehkä olisi ollut mahdollista. 

On epäselvää, miksi kaupungistuminen alentaa syntyvyyttä. Mahdollisia selityksiä ovat esimerkiksi kaupunkilainen ikisinkkuus ja 
lapsiperheille pienet asunnot. Kaupungistumista tuskin on mahdollista tai edes syytä pienentää. Sitä vastoin kaupungeissakin pitää olla mahdollista hankkia lapsia.

Kaikesta huolimatta tulevaisuus näyttää entistä vähälapsiselta. Toivottavasti olen tällä kertaa väärässä.