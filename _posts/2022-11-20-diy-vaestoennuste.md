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

Syntyvyyden aleneminen on tehnyt väestöennusteet vanhentuneiksi jo niiden julkaisuvuonna.
Väestöennusteen tekeminen ei kaavojen puolesta ole kovin hankalaa. Vaikeinta on saada malli
kalibroitua uskottavasti.

Suomessa väestöennusteita tekee mm. [Tilastokeskus](https://stat.fi/tilasto/vaenn), 
[Eläketurvakeskus](https://www.etk.fi/tutkimus-tilastot-ja-ennusteet/ennustelaskelmat/pitkan-aikavalin-laskelmat/), 
ja [MDI oy](https://www.mdi.fi/ennuste2040/). Laskelmat ovat sinänsä
luotettavia, mutta on hauska tehdä väestöennuste myös itse. 

Mistä on hyvä väestöennuste tehty?
=====

Väestöennuste tarvitsee alkutiedoiksi väestön lähtötilanteen. Riittäviä tietoja ovat
ikäluokittain ja sukupuolittain jaettu väestö. Kuvassa 1 on esimerkki 1-vuotisikäluokittain
jaotellusta väestöstä. Data on peräisin [Tilastokeskukselta](https://stat.fi/).

![Tuotot](/images/demog/stop2022.png)<br>
Kuvio 1. Esimerkki väestöennusteen alkutilanteesta. Kuvaan on lisätty myös tiedot työssäolevista,
työttömistä, opiskelijoista ja työelämän ulkopuolella olevista.

Toiseksi, tarvitaan tiedot siitä, miten väestörakenne ajan mukana muuttuu. Tätä varten 
tarvitaan tiedot syntyvyydestä, kuolleisuudesta, ja maahanmuutosta. 

![Tuotot](/images/demog/tfr.png)<br>
Kuvio 2. Kokonaishedelmällisyysluku Suomssa.

Kolmanneksi, pitää arvioida, miten syntyvyys, kuolleisuus ja maahanmuutto muuttuvat ajan mukana.
Tämä on se vaikein kohta. 

Valmis väestöennuste näyttää tältä. Laskelma on ajettu vuoteen 3000 asti, jotta siitä näkyy, millaiseen tasapainoon
ennuste asettuu. Ennuste vastaa melko hyvin Tilastokeskuksen vuoden 2021 väestöennustetta.

![Tuotot](/images/demog/baseline.png)<br>
Kuvio 3. Suomen väestöennuste vuoteen 2400 asti.

Väestöennuste tasapainottuu muutaman sadan vuoden päästä.
Tasapainossa väestörakenteen kehitys muuttuu tylsäksi, kun 
väestörakenne vakioituu. Voisi ajatella, että Suomi hiipuu pois. Näin ei kuitenkaan käy:
nettomaahanmuutto on laskelmassa niin suurta, että kantaväestön ja maahanmuuttajien saamien lasten määrä
riittää yhdessä maahanmuuton kanssa vakioimaan väestörakenteen. Tasapainon saavuttamiseen menee kuitenkin useita satoja vuosia.

Tämä antaa myös vastauksen siihen, miltä Suomen väestörakenne näyttää vuonna 3000. Jos parametrit pysyvät nykyisellään,
asuu Suomessa xx henkilöä vuonna 3000.

Vaikutukset
======

Sekä kokonaishedelmällisyys että nettomaahanmuutto vaikuttavat voimakkaasti väestön määrään.
Mutta miten ne vaikuttavat väestöön ja kuinka nopeasti?

Syntyvyys
-----

Ennuste tarvitsee tiedoiksi syntyvyyden ikäluokittain datassa. Käytetään tässäkin Tilastokeskuksen aineistoa.
Mutta miten syntyvyys kehittyy jatkossa? Tähän on mahdoton vastata. 

Vuonna 2010 kokonaishedelmällisyysluku oli Suomessa 1,87. Nyt kokonaishedelmällisyysluku on noin 1,37. Kuvio 5 näyttää, millaisia
vaikutuksia kokonaishedelmällisyysluvulla on väestöön pitkällä aikavälillä. Kuviossa 5 oletetaan, että vuodesta 2021 alkaen
tfr on annetun suuruinen.

![Tuotot](/images/demog/comp.png)<br>
Kuvio 5. Verrataan kokonaishedelmällisyyslukua 1,87 perusmalliin (kokonaishedelmällisyys 1,45). 

Tilastokeskus käyttää tuoreinta havaintoa. Eläketurvakeskus tekee tämän lisäksi matalan ja korkean syntyvyyden skenaarioita.
Näiden lisäksi voisi myös rakentaa stokastisia ennusteita. Oletetaan tässä yksinkertaisuuden vuoksi,
että syntyvyys säilyy samassa tasossa, mitä on oli vuonna 2021.

Hedelmällisyysluku kertoo iän funktiona, kuinka monta lasta nainen saa. Kokonaishedelmällisyysluku
on summa ikäluokittaisista hedelmällisyysluvuista ja kertoo, montako lasta nainen saa koko elämänsä aikana.

Nettomaahanmuutto
-----

Nettomaahanmuutto kasvattaa väestöä kahta kautta: maahanmuuttajat kasvattavat väestöä suoraan. Toisaalta he myös hankkivat
lapsia, usein kantaväestöä enemmän. Jos nettomaahanmuuttoa ei olisi, kutistuisi väestö matalan syntyvyyden seurauksena hitaasti kohden nollaa.

![Tuotot](/images/demog/compzero.png)<br>
Kuvio 6. Väestöennuste ilman maahanmuuttoa (Nolla) verrattunan perusmalliin (Perus).

Entä, jos nettomaahanmuutto nousisi 30 000 henkilöön vuodessa? Miltä väestörakenne silloin näyttäisi?

![Tuotot](/images/demog/comp2.png)<br>
Kuvio 7. Verrataan Nettomaahanmuuton vaikutusta väestörakenteeseen. Toisessa ennusteessa nettomaahanmuutto on 30 000 henkilöä vuodessa,
toisessa 15 000 henkilöä vuodessa.

Johtopäätökset
=====

Syntyvyyden lasku on alentanut ennustetta Suomen väestön kehityksestä. Väestön määrään
vaikuttaa, jos syntyvyys kasvaa tai laskee. Politiikan keinoin siihen taitaa kuitenkin olla vaikea vaikuttaa.
Oikeastaan ainoa, mitä voidaan tehdä, on pyrkiä tekemään ihmisille mahdolliseksi se lapsimäärä, jonka he haluavat.
Nettomaahanmuuttoon voi vaikuttaa yrittämällä lisätä maahanmuuttoa. Tämä vaatii aktiivista toimintaa, eikä suinkaan sekään ole
helppoa. Ongelma on kuitenkin niin merkittävä, että molempia keinoja on syytä tosissaan yrittää.
