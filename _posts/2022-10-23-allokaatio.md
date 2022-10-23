---
title: 'Miten työeläkeyhtiöt ovat sijoittaneet?'
date: 2022-10-23
permalink: /posts/2022/10/allokaatio/
image: /images/pts/2men.png
largeimage: /images/pts/2men.png
summary: 'Sijoittavatko työeläkeyhtiöt myötäsyklisesti, vastasyklisesti vai neutraalisti?'
tags:
  - työeläke
  - sijoittaminen
  - allokaatio
---

Työeläkejärjestelmä sijoittaa varat tuottavasti ja turvaavasti. Paino on perinteisesti ollut turvaavuuden puolella, mutta viimeisten 5 vuoden aikana
osakeriskin osuutta on kasvatettu ja tuotot ovat olleet hyviä. Mutta minkälaista sijoittaminen on ollut?

![Reaalituotot](/images/pts/tuotot_toteuma.png)
Kuvio 1. Reaaliset vuosituotot TyELissä vuosina 2006 - 2021. Vuoden 2022 tuotot ovat alkuvuoden tuotot.

Viime vuosina sijoitustuotot ovat olleet hyviä (Kuvio 2). 
Korkean inflaation vuoksi vuoden 2022 heinäkuun alkuun mennessä tulleet tuotot ovat reaalisesti erittäin heikot.

Sijoitustuotot riippuvat sijoitusjakaumasta: mitä riskipitoisempi sijoitusjakauma, sitä parempia ovat tuotot.
Sijoitusjakauman riskipitoisuutta taas säädetään markkinanäkemyksen ja riskinkantokyvyn perusteella. Laitoksen vakavaraisuus
taas määrittää riskinkantokykyä. 

Vuoden 2017 eläkeuudistuksessa sovittiin sijoitusriskin lisäämisestä, kun osaketuottosidonnaista vastuuta 
OLVia nostettiin 10 prosentista 20 prosenttiin. Osin sen ansiosta
työeläkelaitokset ovat saaneet parempia tuottoja. 

![Tuotot](/images/tuotot/allo.png)
Kuvio 2. Reaaliset vuosituotot TyELissä vuosina 2006 - 2021. Vuoden 2022 tuotot ovat alkuvuoden tuotot.

Kuviosta 2 näkyy, miten osakesijoitusten osuus työeläkelaitosten salkuissa on kasvanut. Samaan aikaan
korkosijoitusten osuus on laskenut. Kiinteistöjen osuus on pysynyt ennallaan, mutta muiden sijoitusten 
osuus on kasvanut. Muut sijoitukset pitävät sisällään mm. Hedge fund-sijoitukset. Tiedetään, että HF-sijoitukset
ovat usein korreloituneet voimakkaasti osakkeiden kanssa. 

Sijoittaminen
=====

Tarkastellaan yksinkertaista sijoitusmalli, jossa sijoituslajeina on joukkovelkakirjat, osakkeet, kiinteistöt ja muut. 
Muut sisältää mm. Hedge Fund-rahastot. Näiden sijoituslajien tuotot saa (Telan tuottotietokannasta)[https://].



Sijoitusstrategia
=====

Paljonko ja miten työeläkelaitokset sitten sijoittavat osakkeisiin tai osakeriskiin? Katsotaan ensin, miltä vuosituottojen
korrelaatiot näyttävät

![Korrelaatiot](/images/tuotot/korrelaatio.png)

Taulukko 1. Korrelaatiot TyEL-vuosituottojen välillä

Korrelaatiot eri tuottojen välillä ovat korkeita (Taulukko 1). Erityisesti Muut-Osake -korrelaatio on korkea, noin 75 prosenttia.
Tämä tarkoittaa, että Muut -luokan kautta otetaan merkittävässä määrin osakeriskiä. Vielä yllättävämpi on aineiston korko- ja
osaketuottojen välinen korrelaatio 58 prosenttia.  

Oletaanpa sitten argumentin vuoksi, että työeläkelaitokset sijoittaisivat samalla sijoitusjakaumalla
koko välin 2006-2022. Miten hyvin tällainen approksimaatio toistaisi havaitut tuotot?

![](/images/tuotot/alloennuste.png)

Kuvio 3. Todellinen keskimääräinen TyEL-yhtiöiden sijoitusjakauma verrattuna regressiolla löydettyyn jakaumaan vuosina 2005-2022.

Vakioallokaatio
-----

Vakioallokaatio on vastasyklinen sijoitusstrategia, jossa pidetään sama sijoitusten jakauma
koko tarkasteluajan. Siinä osakkeita myydään, kun osakkeiden arvo nousee, ja ostetaan, kun osakkeiden
arvo laskee. Simulaatioissa vakioallokaatio on vakuutusyhtiölle hyvä tapa joutua konkurssiin nopealla aikataululla,
mutta se antaa myös usein hyviä tuottoja.

![](/images/tuotot/vakioallo.png)

Kuvio 4. TyElin kokonaistuotto verrattuna kiinteällä allokaatiolla saatuun tuottoon.

![](/images/tuotot/vakioallo_ero.png)

Kuvio 5. TyElin kokonaistuotto verrattuna kiinteällä allokaatiolla saatuun tuottoon.

Vakioallokaatio on $[0.50591377 0.27680256 0.15373537 0.06354831]$

Vakioallokaatiolla päästään hyvin lähelle todellista tyel-yhtiöiden sijoitustuottoa.

Osakepaino on regressiossa 56 prosenttia vuodesta 2015 alkaen. [ETK:n arvio PTS-2022:ssa]()
on 59,7 prosenttia osakkeet ja muut sijoitukset.

Miten hyvin vakioallokaatio toistaa tuotot ajan yli? Lähdetään liikkeelle 100 yksikön sijoituksesta 2005 ja
annetaan varojen kehittyä vakioallokaatioiden mukaan.

![](/images/tuotot/kumulaatio.png)

Kuvio 6. 

![](/images/tuotot/vakioallo_osake.png)

Kuvio 6. 


Keskivirhe PI-mallissa on 0,49 %-yksikköä sijoitustuotoissa. Tätä voi pitää kohtalaisena ottaen huomioon,
että laskelmat on tehty TyEL-järjestelmän keskiarvoista, ei laitoskohtaisista tunnusluvuista.


Portfolio insurance
-----

Portfolio insurance (PI) on sijoitustrategia, jossa osakepaino määräytyy vakavaraisuuden mukaan.
Tässä tarkastellaan mallia, jossa osakepaino on vakio kertaa vakavaraisuuspääoma suhteessa vastuisiin.
PI on myötäsyklinen sijoitusstrategia, jossa osakkeita ostetaan, kun vakavaraisuus on korkealla, mikä tapahtuu
kun osakkeet ovat tuottaneet hyvin. Osakkeita taas myydään, kun niiden arvo laskee.

PI suojaa konkurssia vastaan, jos transaktiokustannukset ovat pienet ja toiminta markkinoilla on välitöntä.

Keskivirhe PI-mallissa on 0,24 %-yksikköä sijoitustuotoissa. Tätä voi pitää pienenä ottaen huomioon,
että laskelmat on tehty TyEL-järjestelmän keskiarvoista, ei laitoskohtaisista tunnusluvuista.

![](/images/tuotot/PI.png)

Kuvio 6. 

![](/images/tuotot/PI_virhe.png)

Kuvio 6. 


Buy-and-Hold
-----

Buy-and-Hold (BH) on sijoitusstrategia, jossa annetaan salkun liikkua markkinoiden mukana.
Siinä ei osakkeita osteta tai myydä markkinaliikkeiden mukaan. Se on siis suhdanteiden osalta neutraali 
sijoitusstrategia.


Myötäsyklisyys
=====

Yllä olevat laskelmat antavat ymmärtää, että sijoitustoiminta on ollut myötäsyklistä. Olisi yllättävää, jos
sijoittaminen olisi ollut vastasyklistä.


Lopuksi
=====

Osake
