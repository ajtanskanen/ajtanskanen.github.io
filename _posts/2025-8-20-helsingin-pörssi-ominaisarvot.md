---
title: 'Montako faktoria ajaa tuottoja Helsingin pörssissä?'
date: 2025-03-30
permalink: /posts/2024/5/helsinginpörssi/
summary: 'Blogi | Bouchard ja Laloux, Potters näyttivät, että S&P 500 -indeksin osakkeiden korrelaatiomatriisissa on suuri satunnainen komponentti. Onko näin myös Helsingin Pörssin osakkeiden korrelaatiomatriisille? Blogissa tarkastellaan, montako lineaarista, kohinasta erottuvaa faktoria Helsingin Pörssistä erottuu. Tulosten mukaan viimeisen kymmenen vuoden tuottoja on ajanut 5 faktoria.'
tags:
  - osaketuotot
  - korrelaatio
  - sijoittaminen
---

Tuottoja ajavien faktorien lukumäärä vaihtelee suhdannetilanteen mukaan -- näin ainakin uskotaan. Voiko sitä mitata? Blogissa käytetään satunnaismatriisien teoriaa
arvioimaan, montako riippumatonta faktoria ajaa tuottojen korrelaatioita eri vuosina.

1 Helsingin Pörssissä listatut osakkeet
===

Tarkastellaan Helsingin pörssissä (Nasdaq OMXH) listattuja 140 osaketta, joista löytyy yhtenäinen aikasarja vuosille 2015-2025. Niistä on saatavissa päivädataa Yahoon palvelun kautta. Osakkeiden päivätuotot lasketaan yksinkertaisuuden vuoksi suoraan kursseista ilman osinkojen huomiointia. Kurssikehitys muutetaan logaritmisiksi tuotoiksi.

Yahoo Finance löytää päivänoteeraukset 97:ltä Helsingin pörssin osakkeelta periodilta, joka alkaa 2015-08-15 ja loppuu 2025-08-15. Nämä ovat tikkerit 
> AFAGR.he, AKTIA.he, ALISA.he, ALMA.he, ANORA.he, APETIT.he, TALLINK.he, ASPO.he, ACG1V.he, ATRAV.he, ALBAV.he, ALBBV.he, BIOBV.he, BITTI.he, BOREO.he, CAPMAN.he, CGCBV.he, CTY1S.he, CTH1V.he, CONSTI.he, DIGIA.he, DIGIGR.he, DOV1V.he, EEZY.he, ELEAV.he, ELISA.he, PAMPALO.he, ENENTO.he, ESENSE.he, EQV1V.he, ETTE.he, EVLI.he, EXL1V.he, FSECURE.he, FIA1S.he, FSKRS.he, FORTUM.he, GLA1V.he, GOFORE.he, HARVIA.he, HKSAV.he, HONBS.he, HUH1V.he, ILKKA2.he, ICP1V.he, INVEST.he, KALMAR.he, KAMUX.he, KEMIRA.he, KEMPOWR.he, KSL.he, KESKOA.he, KESKOB.he, KELAS.he, KHG.he, KOJAMO.he, KNEBV.he, KCR.he, KOSKI.he, KREATE.he, LAMOR.he, LAT1V.he, LEHTO.he, LINDEX.he, MANTA.he, MEKKO.he, MARAS.he, METSO.he, METSA.he, METSB.he, MUSTI.he, NESTE.he, NOHO.he, NOKIA.he, TYRES.he, NDA FI.he, NLG1V.he, OLVAS.he, OMASP.he, OPTOMED.he, OKDAV.he, OKDBV.he, ORNAV.he, ORNBV.he, ORTHEX.he, OUT1V.he, OVARO.he, PNA1V.he, PIHLIS.he, PON1V.he, PUUILO.he, QPR1V.he, QTCOM.he, RAIVV.he, RAP1V.he, RAUTE.he, REBL.he, REKA.he, RELAIS.he, REMEDY.he, REG1V.he, ROBIT.he, SAGCV.he, SAMPO.he, SANOMA.he, SCANFL.he, SIILI.he, SITOWS.he, SOLTEQ.he, SOSI1.he, SRV1V.he, SSABAH.he, SSABBH.he, SSH1V.he, STEAV.he, STERV.he, SUY1V.he, TAALA.he, TNOM.he, TEM1V.he, TLT1V.he, TELIA1.he, TTALO.he, TIETO.he, TOKMAN.he, TRH1V.he, TULAV.he, UNITED.he, UPM.he, VAIAS.he, VALMT.he, VALOE.he, VERK.he, VIK1V.he, WETTERI.he, WITH.he, WUF1V.he, WRT1V.he, YIT.he

![nettomaahanmuutto](/images/eigen/replication.png)<br>
_Kuvio 1. Tuottojen replikointi neljällä faktorilla._

2 Satunnaismatriisit
===
[Satunnaismatriisit](https://en.wikipedia.org/wiki/Random_matrix) ovat satunnaislukujen yleistys. Todennäköisyysjakautuneen satunnaisluvun sijaan tarkastellaan matriiseita, joiden alkiot ovat satunnaislukuja ja lisäksi alkioiden väillä voi olla keskinäisiä riippuvuuksia. Voidaan ajatella, että tuottojen korrelaatiomatriisi on ortogonaalisten matriisien ensemblen jäsen. 
Todennäköisyyslaskennalla voidaan arvioida satunnaismatriisien ominaisuuksia.

Esimerkki satunnaismatriisien joukosta on kaikkien korrelaatiomatriisien joukko varustettuna todennäköisyys mitalla. 
Olkoon $X$ reaalinen $m\times n$ satunnaismatriisi, jonka alkiot ovat toisistaan riippumattomia ja samalla tavalla jakautuneita satunnaislukuja, joiden keskiarvo on 0 ja varianssi 
$\sigma ^{2}<\infty$. Tällöin $Y_{n}={\frac {1}{n}}XX^{T}$ on korrelaatiosatunnaismatriisi.

3 Korrelaatiomatriisin ominaisarvojen jakauma
===

Pääarvomenetelmällä voi etsiä tuottoja selittäviä tekijöitä. Menetelmä toimii korrelaatiomatriisin ominaisarvojen avulla. Suurin ominaisarvo kuvaa markkinan liikettä ja sen suuruus tyypillisesti poikkeaa kaikista muista (Kuvio 1). 

Korrelaatio kuvaa tuottojen keskinäistä lineaarista riippuvuutta. Tuottoaikasarjoille $X_k,Y_k$ se määritellään

Satunnaismatriisien teoriasta tiedetään, että tällaisten korrelaatiomatriisien ominaisarvot noudattavat todennäköisyysjakaumaa. 
[Pastur-Marchenko-teoreeman](https://en.wikipedia.org/wiki/Marchenko%E2%80%93Pastur_distribution) mukaan satunnaismatriisin ominaisarvot jakautuvat

$$
  p(x) = \frac{1}{2\pi\sigma^2}\frac{\sqrt{(\lambda_+-x)(x-\lambda_-)}}{\lambda x},
$$

missä $x\in(\lambda_-,\lambda_+)$ ja $\lambda_-=..$ ja $\lambda_+=..$. Kaava pätee, kun  suurten neliömatriisien rajalla $n\to\infty$.

kertoo. 

[Bouchaud ja Laloux]() sovelsivat Pastur-Marchenko -teoreemaa S&P 500:n korrelaationmatriisiin. 
Heidät havaintojensa mukaan noin 94 prosenttia ominaisarvoista jakautui Pastur-Marchenkon jakauman mukaan (Kuvio).

Mitä tämä sitten tarkoittaa? Sen voi tulkita tarkoittavan, että suurin osa korrelaatiomatriisista on kohinaa ja että vain muutama lineaarinen faktori ajaa osaketuottoja.
Tämä ei tarkoita, ettei tuottoja voisi ajaa jokin ei-lineaarinen tekijä, mutta PCA ei sellaista löytäisi. 

![Ominaisarvot](/images/eigen/eigen.png)<br>
_Kuvio 2. Analysoitujen osakkeiden tuottojen korrelaatiomatriisin ominaisarvojen jakauma. Suurin ominaisarvo kuvaa markkinaliikettä._


4 Montako faktoria ajaa Helsingin osakkeiden tuottoja? 
===

Pastur-Marchenko-teoreemassa ainoat parametrit ovat keskihajonta s ja osakkeiden lukumäärän ja havaintojen lukumäärän suhde N/M. Pastur-Marchenko kuitenkin olettaa, että havainnot ovat toisistaan riippumattomia ajallisesti. Näinhän ei ole. Siksi efektiivinen havaintojen lukumäärä T* on pienempi kuin havaintojen todellinen lukumäärä T. Tässä tutkimuksessa suhde oli luokkaa T* / T = 0,4.

Suurin ominaisarvo vastaa suurimman varianssi portfoliota (jossa painot kuten ominaisvektorin alkiot). Näin tulkittuna OMXH:ssa on neljä merkitsevää toisistaan riippumatonta faktoria,
muut varianssin lähteet ovat kohinaa. 

Suoralla PCA:llä nähdään, että tuottoaikasarjasta riittää poimia ensimmäiset 5 faktoria, niin osakekurssien heilunnasta selittyy yli 90 prosenttia. Samaa kertoo satunnaismatriisien teoria: muutama ominaisarvo on merkitsevä, loppuja on vaikea erottaa kohinasta. Tässä tarkastellaan lineaarisia faktoreita, ja voi olla, että muitakin on.

5 Mitä faktori kertovat?
===

Faktoreista ensimmäinen on markkinariski. Sen ominaisvektori on
> []

Toinen faktori onkin sitten epäselvempi.
> []

