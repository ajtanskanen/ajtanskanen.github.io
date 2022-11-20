---
title: 'Miltä Suomen väestö näyttää vuonna 3000?'
date: 2022-11-17
permalink: /posts/2022/11/vaestoennuste/
image: /images/pts/2men.png
largeimage: /images/pts/2men.png
summary: 'Miten Suomen väestörakenteeseen ja määrän vaikuttaa syntyvyys? Entä maahanmuutto? Ja millainen väestörakenne Suomessa on vuonna 3000?'
tags:
  - väestöennuste
---

Syntyvyys on alentunut niin nopeasti, että se uhkaa tehdä väestöennusteet vanhentuneiksi jo niiden julkaisuvuonna.
Väestöennusteet ovat silti arvokkaita välineitä tulevaisuuden haasteiden arviointiin. Niiden avulla mm. voidaan
suunnitella tulevia resurssitarpeita. Myös erilaisten pitkän aikavälin laskelmien perusta on usein väestöennuste.

Suomessa väestöennusteita tekee mm. [Tilastokeskus](https://stat.fi/tilasto/vaenn), 
[Eläketurvakeskus](https://www.etk.fi/tutkimus-tilastot-ja-ennusteet/ennustelaskelmat/pitkan-aikavalin-laskelmat/), 
ja [MDI oy](https://www.mdi.fi/ennuste2040/). Laskelmat ovat sinänsä
luotettavia, mutta on hauska tehdä väestöennuste myös itse. 
Väestöennusteen tekeminen ei kaavojen puolesta ole kovin hankalaa. Vaikeinta on saada malli
kalibroitua uskottavasti.

![Tuotot](/images/demog/tfr.png)<br>
Kuvio 1. Kokonaishedelmällisyysluku Suomssa.

Ajankohtaiseksi väestöennusteet tekee syntyvyyden lasku (Kuvio 1). Syntyvyys on Suomessa ennenkin aaltoillut.
Vuodesta 2010 alkanut hedelmällisyysluvun jyrkkä lasku (Kuvio 1) on kuitenkin poikkeuksellisen suuri, eikä
se alustavien tietojen mukaan edes ole kääntymässä, vaikka Kuvio 1 niin kertookin. Erikoista tilanteessa on 
myös se, että syntyvyyden laskua uskottavasti selittäviä tekijöitä ei oikein ole löydetty.

Mistä on hyvä väestöennuste tehty?
=====

Väestöennuste tarvitsee alkutiedoiksi väestön lähtötilanteen. Riittäviä tietoja ovat
ikäluokittain ja sukupuolittain jaettu väestö. Kuvassa 1 on esimerkki 1-vuotisikäluokittain
jaotellusta väestöstä. Alkudata on peräisin [Tilastokeskukselta](https://stat.fi/).
tässä esitetyt laskelmat on tehty itse.

![Tuotot](/images/demog/baseline_stop2022.png)<br>
Kuvio 2. Esimerkki väestöennusteen alkutilanteesta.

Toiseksi, tarvitaan tiedot siitä, miten väestörakenne ajan mukana muuttuu. Tätä varten 
tarvitaan tiedot syntyvyydestä, kuolleisuudesta, ja maahanmuutosta. 

Kolmanneksi, pitää arvioida, miten syntyvyys, kuolleisuus ja maahanmuutto muuttuvat ajan mukana.
Tämä on se vaikein kohta. Mallissa on oletettu, että sekä nettomaahanmuutto että syntyvyys 
ovat vakioita ennusteperiodin ajan, mutta kuolleisuuden oletetaan alenevan samalla vauhdilla koko periodin.

Valmis väestöennuste näyttää tältä. Laskelma on ajettu vuoteen 3000 asti, jotta siitä näkyy, millaiseen tasapainoon
ennuste asettuu. Ennuste vastaa periodilta 2021-2070 melko hyvin Tilastokeskuksen vuoden 2021 väestöennustetta.

![Tuotot](/images/demog/baseline.png)<br>
Kuvio 3. Perusversio väestöennusteesta.

Väestöennuste tasapainottuu muutaman sadan vuoden päästä. Tasapainossa väestörakenteen kehitys muuttuu tylsäksi, kun 
väestörakenne vakioituu. Voisi ajatella, että Suomi hiipuu pois. Näin ei kuitenkaan käy:
nettomaahanmuutto on laskelmassa niin suurta, että kantaväestön ja maahanmuuttajien saamien lasten määrä
riittää yhdessä maahanmuuton kanssa vakioimaan väestörakenteen. Tasapainon saavuttamiseen menee kuitenkin useita satoja vuosia.

![Tuotot](/images/demog/baselinepop.png)<br>
Kuvio 4. Väestön määrä Perusversiossa väestöennusteesta.

Tämä antaa myös vastauksen siihen, miltä Suomen väestörakenne näyttää vuonna 3000. Jos parametrit pysyvät nykyisellään,
asuu Suomessa vuonna 3000 selvästi nykyistä vähemmän väkeä, noin 3,6 miljoonaa henkilöä (Kuvio 4). Alin väestömäärä saavutetaan
vuonna 2500, minkä jälkeen kuolleisuuden aleneminen kasvattaa hitaasti erittäin ikääntyneen väestön määrää.


Entä jos
======

Sekä kokonaishedelmällisyys että nettomaahanmuutto vaikuttavat voimakkaasti väestön määrään.
Mutta miten ne vaikuttavat väestöön ja kuinka nopeasti?

Syntyvyys
-----

Ennuste tarvitsee tiedoiksi syntyvyyden ikäluokittain datassa. Käytetään tässäkin Tilastokeskuksen aineistoa.
Mutta miten syntyvyys kehittyy jatkossa? Tähän on mahdoton vastata. 

Tilastokeskus käyttää hedelmällisyysluvun tuoreinta havaintoa koko ennusteperiodille.
Eläketurvakeskus tekee tämän lisäksi matalan ja korkean syntyvyyden skenaarioita.
Näiden lisäksi voisi myös rakentaa stokastisia ennusteita. 

Vuonna 2010 kokonaishedelmällisyysluku oli Suomessa 1,87. Nyt kokonaishedelmällisyysluku on noin 1,37. Kuvio 5 näyttää, millaisia
vaikutuksia kokonaishedelmällisyysluvulla on väestöön pitkällä aikavälillä. Kuviossa 5 oletetaan, että vuodesta 2021 alkaen
tfr on annetun suuruinen.

![Tuotot](/images/demog/comp.png)<br>
Kuvio 5. Verrataan korkeaa syntyvyyttä (kokonaishedelmällisyys 1,87) perusmalliin (kokonaishedelmällisyys 1,45). 

Hedelmällisyysluku kertoo montako lasta hedelmällisyysikäinen ikäinen nainen vuoden aikana saa.
Kokonaishedelmällisyysluku on summa ikäluokittaisista hedelmällisyysluvuista ja kertoo, montako lasta 
nainen saa elämänsä aikana.

Nettomaahanmuutto
-----

Nettomaahanmuutto kasvattaa väestöä kahta kautta: maahanmuuttajat kasvattavat väestöä suoraan. Toisaalta he myös hankkivat
lapsia, usein kantaväestöä enemmän. Jos nettomaahanmuuttoa ei olisi, kutistuisi väestö matalan 
syntyvyyden seurauksena hitaasti kohden nollaa.

![Tuotot](/images/demog/compzero.png)<br>
Kuvio 6. Väestöennuste ilman maahanmuuttoa (Nolla) verrattuna perusmalliin (Perus).

Entä, jos nettomaahanmuutto nousisi 30 000 henkilöön vuodessa? Tai 50 000:een? Miltä väestörakenne silloin näyttäisi?
Nettomaahanmuuton suuruutta voi verrata ikäluokan kokoon. Aiemmin ikäluokan koko oli Suomessa lähempänä 60 000 henkilöä, suuret ikäluokat
jopa 108 000 henkilöä, kun taas nuorimmat ikäluokat ovat hieman vajaat 50 000 henkilöä.
Hieman yksinkertaistaen voi sanoa, että 50 000 hengen nettomaahanmuutto tarkoittaisi efektiivisesti
suurten ikäluokkien paluuta.

![Tuotot](/images/demog/comp2.png)<br>
Kuvio 7. Verrataan nettomaahanmuuton vaikutusta väestörakenteeseen, kun vuosittainen nettomaahanmuutto on 15 000, 30 000 ja 50 000 henkilöä.

Suomen väkiluku kasvaisi reippaasti, jos nettomaahanmuutto nousisi 50 000 henkeen vuodessa. 
Myös 30 000 henkilön vuosittainen nettomaahanmuutto kasvattaisi väestöä, toisin kuin nykytasoinen nettomaahanmuutto.

Väestö
------

Katsotaan sitten vielä, millä tavalla väestön kokonaismäärä muuttuu eri vaihtoehtoissa.
Ilman maahanmuuttoa ja syntyvyyden kasvua Suomen väkiluku hiipuu (Kuvio 8). Vuoden 2010 kaltaisella
syntyvyydellä väestö kasvaisi pitkään. Jos väestön määrä halutaan säilyttää nykytasolla, pitäisi
syntyvyyden kasvaa tasolle 1,65 tai nettomaahanmuuton 24 000 henkilöön vuodessa.

![Tuotot](/images/demog/popcomp.png)<br>
Kuvio 8. Väestöennusteiden kokonaisväkimäärät verrattuna. 

Jos halutaan, että väestön määrä olisi karkeasti samalla uralla kuin se olisi ollut 2010 syntyvyyden seurauksena, 
pitäisi nettomaahanmuutto kasvattaa 30 000 henkilöön vuodessa.
Jos nettomaahanmuutto olisi 50 000 henkilöä vuodessa, kasvaisi Suomen väkiluku yli 10 miljoonan pitkällä aikavälillä.
Jos taas kokonaishedelmällisyysluku olisi 1,87 jatkossa, kasvaisi väkiluku yli 8 miljoonan.

Johtopäätökset
=====

Syntyvyyden lasku on alentanut ennustetta Suomen väestön tulevasta määrästä. Väestön määrään
vaikuttaa syntyvyys, kuolleisuus ja maahanmuutto. Erityisesti muutos on tapahtunut viime aikoina syntyvyydessä. 
Politiikan keinoin siihen taitaa kuitenkin olla vaikea vaikuttaa. On kuitenkin mahdollista 
pyrkiä tekemään ihmisille mahdolliseksi se lapsimäärä, jonka he haluavat.
Maahanmuuttoon voi vaikuttaa todennäköisesti helpommin, mutta on turha elätellä kuvitelmaa, että tämä olisi helppoa.
Se on tehtävissä, mutta vaatii aktiivista toimintaa. Vähenevä väestö tarkoittaa pienempää työvoimaa ja pienempiä
taloudellisia mahdollisuuksia ylläpitää hyvinvointivaltiota.
Ongelma on niin merkittävä, että on tarpeen sekä syntyvyyteen että maahanmuuttoon vaikuttavia toimenpiteitä
on tarpeen tehdä.
