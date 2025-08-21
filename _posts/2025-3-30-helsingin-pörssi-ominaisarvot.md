---
title: 'Montako faktoria ajaa tuottoja Helsingin pörssissä?'
date: 2025-08-20
permalink: /posts/2024/8/helsinginpörssi/
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

Tarkastellaan Helsingin pörssissä (Nasdaq OMXH) listattuja 97 osaketta, joista löytyy yhtenäinen aikasarja vuosille 2015-2025. Niistä on saatavissa päivädataa Yahoon palvelun kautta. Osakkeiden päivätuotot lasketaan yksinkertaisuuden vuoksi suoraan kursseista ilman osinkojen huomiointia. Kurssikehitys muutetaan logaritmisiksi tuotoiksi.

Yahoo Finance löytää päivänoteeraukset 97:ltä Helsingin pörssin osakkeelta periodilta, joka alkaa 2015-08-15 ja loppuu 2025-08-15. Nämä ovat tikkerit 
> ACG1V.HE, AFAGR.HE, AKTIA.HE, ALBAV.HE, ALBBV.HE, ALMA.HE',
       'APETIT.HE, ASPO.HE, ATRAV.HE, BIOBV.HE, BITTI.HE, BOREO.HE',
       'CAPMAN.HE, CTH1V.HE, CTY1S.HE, DIGIA.HE, DIGIGR.HE',
       'DOV1V.HE, ELEAV.HE, ELISA.HE, ENENTO.HE, EQV1V.HE, ETTE.HE',
       'EXL1V.HE, FORTUM.HE, FSKRS.HE, GLA1V.HE, HONBS.HE, HUH1V.HE',
       'ICP1V.HE, ILKKA2.HE, INVEST.HE, KCR.HE, KELAS.HE, KEMIRA.HE',
       'KESKOA.HE, KESKOB.HE, KNEBV.HE, LAT1V.HE, LINDEX.HE',
       'MARAS.HE, MEKKO.HE, METSA.HE, METSB.HE, METSO.HE, NESTE.HE',
       'NLG1V.HE, NOHO.HE, NOKIA.HE, OLVAS.HE, ORNAV.HE, ORNBV.HE',
       'OUT1V.HE, OVARO.HE, PIHLIS.HE, PNA1V.HE, PON1V.HE, QPR1V.HE',
       'RAIVV.HE, RAP1V.HE, RAUTE.HE, REBL.HE, REG1V.HE, REKA.HE',
       'ROBIT.HE, SAGCV.HE, SAMPO.HE, SANOMA.HE, SCANFL.HE',
       'SIILI.HE, SOLTEQ.HE, SOSI1.HE, SRV1V.HE, SSH1V.HE, STEAV.HE',
       'STERV.HE, SUY1V.HE, TAALA.HE, TELIA1.HE, TEM1V.HE, TIETO.HE',
       'TLT1V.HE, TNOM.HE, TRH1V.HE, TULAV.HE, TYRES.HE, UNITED.HE',
       'UPM.HE, VAIAS.HE, VALMT.HE, VERK.HE, VIK1V.HE, WETTERI.HE',
       'WITH.HE, WRT1V.HE, WUF1V.HE, YIT.HE

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

[Bouchaud ja Laloux](https://arxiv.org/pdf/0910.1205v1) sovelsivat Pastur-Marchenko -teoreemaa S&P 500:n korrelaationmatriisiin. 
Heidät havaintojensa mukaan noin 94 prosenttia ominaisarvoista jakautui Pastur-Marchenkon jakauman mukaan (Kuvio).
[Bouchaud ja Potters](https://arxiv.org/pdf/0910.1205v1) jatkoivat tutkimusta.

Mitä tämä sitten tarkoittaa? Sen voi tulkita tarkoittavan, että suurin osa korrelaatiomatriisista on kohinaa ja että vain muutama lineaarinen faktori ajaa osaketuottoja.
Tämä ei tarkoita, ettei tuottoja voisi ajaa jokin ei-lineaarinen tekijä, mutta PCA ei sellaista löytäisi. 

![Ominaisarvot](/images/eigen/HEX_eigen.png)<br>
_Kuvio 2. Analysoitujen osakkeiden tuottojen korrelaatiomatriisin ominaisarvojen jakauma. Suurin ominaisarvo kuvaa markkinaliikettä._

4 Montako faktoria ajaa Helsingin osakkeiden tuottoja? 
===

Pastur-Marchenko-teoreemassa ainoat parametrit ovat keskihajonta s ja osakkeiden lukumäärän ja havaintojen lukumäärän suhde N/M. Pastur-Marchenko kuitenkin olettaa, että havainnot ovat toisistaan riippumattomia ajallisesti. Näinhän ei ole. Siksi efektiivinen havaintojen lukumäärä T* on pienempi kuin havaintojen todellinen lukumäärä T. Tässä tutkimuksessa suhde oli luokkaa T* / T = 0,4.

Suurin ominaisarvo vastaa suurimman varianssi portfoliota (jossa painot kuten ominaisvektorin alkiot). Näin tulkittuna OMXH:ssa on neljä merkitsevää toisistaan riippumatonta faktoria,
muut varianssin lähteet ovat kohinaa. 

![Ominaisarvot](/images/eigen/pm_vs_data.png)<br>
_Kuvio 3. Pastur-Marchenko -jakauma verrattuna datan tiheyteen._


Suoralla PCA:llä nähdään, että tuottoaikasarjasta riittää poimia ensimmäiset 5 faktoria, niin osakekurssien heilunnasta selittyy yli 90 prosenttia. Samaa kertoo satunnaismatriisien teoria: muutama ominaisarvo on merkitsevä, loppuja on vaikea erottaa kohinasta. Tässä tarkastellaan lineaarisia faktoreita, ja voi olla, että muitakin on.

5 Mitä faktori kertovat?
===

Faktoreista ensimmäinen on markkinariski. Sen ominaisvektori on
> [0.07138418 0.06515197 0.14093996 0.05086095 0.10338822 0.08907242
  0.07145822 0.13225237 0.10770909 0.06869495 0.0900749  0.07313301
  0.14846975 0.05107834 0.13911678 0.09667943 0.03878185 0.07869674
  0.04777094 0.0871974  0.06203801 0.11186422 0.07862516 0.06094646
  0.1397037  0.12567481 0.10964379 0.07770072 0.14261453 0.0958137
  0.08425772 0.05963127 0.15723661 0.06664166 0.14520435 0.12220788
  0.11659927 0.11619177 0.12660305 0.09134456 0.07121193 0.11940853
  0.10811353 0.13971358 0.14530843 0.11554081 0.04881166 0.10046115
  0.12619158 0.10831876 0.08540562 0.08578323 0.14473747 0.08016548
  0.07308186 0.06878606 0.11733958 0.04316597 0.11146253 0.08164928
  0.0894419  0.02092943 0.10394233 0.05831768 0.06921687 0.05641445
  0.16811193 0.11345766 0.10093468 0.08057699 0.07038371 0.06401473
  0.0925772  0.06538574 0.11998576 0.1693524  0.07524399 0.1143523
  0.06771801 0.07524241 0.15230357 0.08301954 0.09307997 0.04777306
  0.0682913  0.13940379 0.04927089 0.16137764 0.11076194 0.15182701
  0.09191066 0.03328845 0.04101367 0.10165961 0.15138451 0.05470399
  0.13807004]

Toinen faktori onkin sitten epäselvempi.
> [-9.87624634e-02 -5.02852749e-02 -4.81837456e-02 -1.53289008e-01
  -1.49989488e-01 -5.62424059e-02 -1.17011204e-01 -1.00117796e-01
  -6.10230183e-02 -9.53434726e-02 -8.35771064e-02 -1.21439289e-01
  -8.39266903e-02 -7.40467339e-02  2.93325398e-02 -6.76032927e-02
  -8.55887156e-02 -1.09141615e-01 -1.00041724e-01  6.31656348e-02
  -3.82329203e-02 -1.16545486e-01 -1.33499856e-01 -6.70170611e-02
   3.61016090e-02 -2.31659398e-02 -9.74567014e-02 -1.11406578e-01
   1.75734237e-01 -7.08021364e-02 -8.58017521e-02 -9.53056278e-02
   1.29731230e-01 -6.39025280e-02  1.39416934e-01 -2.65042313e-04
   2.53976019e-02  1.65054213e-01  4.19601950e-04 -2.21605353e-02
  -8.10494439e-02 -7.41386930e-02  1.24951049e-01  2.61001489e-01
   1.30615502e-01  8.00201034e-02 -8.83546230e-02 -1.14680032e-01
   2.48009761e-02 -6.21298964e-02  2.19647512e-02  2.82661392e-02
   1.27532692e-01 -6.21108717e-02 -7.65797720e-02 -7.92099713e-02
  -6.34239656e-02 -3.93799719e-02 -1.66030421e-02 -1.25951014e-01
  -1.01232772e-01 -4.73239024e-02 -3.11402236e-02 -7.14978651e-02
  -1.12448846e-01 -1.25448703e-01  4.10069523e-02  3.19834779e-02
  -9.07293839e-02 -4.10515879e-02 -9.94496767e-02 -3.86931113e-02
  -6.62552138e-02 -8.39775278e-02  2.37343295e-01  2.84038969e-01
  -1.06575753e-01 -1.46939799e-01  2.72698388e-02 -7.45878092e-02
   1.05299837e-01 -3.92799796e-02 -4.70734758e-02 -8.33071059e-02
  -1.06349879e-01  6.60218823e-02 -4.29861826e-02  2.76294155e-01
  -2.34390306e-02  1.56106879e-01 -4.98269534e-02 -6.13148939e-02
  -2.57911168e-02  2.31257224e-02  1.33235641e-01 -1.17074570e-01
   8.07628761e-02]

Kolmas faktori onkin sitten epäselvempi.
> [3.83031599e-02 -8.86634024e-03  1.48878469e-02 -2.19760410e-03
   5.26798455e-03  3.39320551e-02  4.62159565e-02  6.39568502e-02
   2.91233774e-03  3.21862128e-02  3.65768469e-03  4.64085007e-02
  -2.70048452e-02  1.30996846e-02  1.59212842e-03  4.69898235e-02
   3.14604526e-02  6.32965694e-03  1.42584154e-02 -2.39011819e-01
   2.23242114e-02 -2.40159272e-02  4.47642911e-03  2.01527474e-02
   4.01240944e-03 -3.11853193e-02  5.94067705e-02  5.38221748e-02
  -1.53792632e-02  3.82593791e-02 -5.29390740e-02  6.40056318e-03
   6.17867118e-02  1.22123627e-02  2.29221332e-02 -2.97550667e-01
  -2.92540318e-01 -1.29452996e-01 -2.32425488e-03  1.36942124e-02
  -1.27957966e-02 -3.86070970e-03  8.17747492e-02  1.29495536e-01
   7.93577066e-02 -2.59131167e-04  4.74757967e-02  5.87612208e-02
   2.16119133e-03 -5.84446782e-02 -5.09304512e-01 -5.11751145e-01
   9.87670440e-02  5.18445511e-02 -5.48713599e-03  2.95985951e-02
   1.79438541e-02  2.14283344e-02 -4.65376298e-02  1.39097864e-02
   8.43014797e-02  5.77647830e-02 -1.00528427e-01  3.34932236e-03
   5.91577670e-02  7.44521692e-02  6.90707322e-03 -7.92865667e-02
   2.57855053e-02 -4.29411940e-04  3.00224845e-04  4.12371294e-02
   4.63543927e-02 -9.28043385e-03  1.32361842e-01  1.45163388e-01
  -5.58762126e-02  4.93481555e-02 -8.19186730e-02  1.55174917e-02
  -6.21810234e-02  1.10073712e-01 -5.93212581e-03  4.54054828e-02
   4.16300029e-02  4.49473612e-02  3.16187375e-02  1.08313284e-01
  -6.33273245e-02  2.68520902e-02  3.50290302e-02  1.42398918e-02
   4.49776946e-02 -4.21317965e-02  3.93235111e-02  3.49903611e-02
   3.68444047e-02]

Neljäs faktori onkin sitten epäselvempi.
> [-0.09981017 -0.04462578  0.06154008  0.01845842  0.00428544 -0.0843227
  -0.01340064  0.00872504 -0.02526232 -0.04675185 -0.0940226   0.06947079
  -0.00431647 -0.03919272  0.09540994 -0.09442172 -0.03392165  0.01649884
   0.0037517   0.02029941  0.04143361  0.01072872 -0.05524074 -0.00458357
   0.0986183   0.06439377 -0.04634434 -0.04289727  0.0192435   0.03123015
  -0.04332561 -0.00067602  0.08207861 -0.0544767   0.00897422  0.42752961
   0.43893907  0.10839916  0.03392737  0.05203797 -0.0301131   0.06905019
  -0.11901515 -0.09834386 -0.04977529  0.0758027   0.01945902 -0.05387228
   0.00860028  0.12755384 -0.38776878 -0.38838214 -0.03576092 -0.04969434
  -0.03212318 -0.05085499  0.00515191  0.02411178  0.0380187  -0.00488145
  -0.00252098 -0.05695847  0.0344187  -0.0574816  -0.04768121 -0.09181073
   0.0503662   0.05430248 -0.01678147 -0.10240153  0.03367337  0.00690569
  -0.05756993 -0.0670083  -0.14766118 -0.10940161 -0.04241134  0.01317474
  -0.02830229  0.02628058  0.05946969 -0.02079204  0.05600617 -0.04802417
  -0.01784036  0.10621355  0.02767594 -0.11891463  0.00255348  0.02067441
  -0.03890056 -0.05858377 -0.10583276 -0.09381429  0.0340984   0.01896043
   0.00654119]

   Viides faktori onkin sitten epäselvempi.
> [0.07900279 -0.08825045 -0.05046086  0.02376756 -0.00907841  0.01236585
   0.01090427  0.03986844  0.04182622  0.00591613 -0.07156413  0.15607712
  -0.08450016 -0.04476704 -0.0484111  -0.01923129  0.02930586  0.03564115
   0.11950687  0.05173885  0.01828875  0.03827116  0.03472039  0.06631641
  -0.09048332 -0.06905065 -0.02854425  0.03703055 -0.03861332 -0.0571746
  -0.02888924  0.07818817 -0.1850927  -0.00877014 -0.05175395  0.26780191
   0.27566077 -0.08411171 -0.01382937  0.00325778 -0.00272012  0.00335039
   0.34940318  0.30782277 -0.11819663 -0.18572729  0.11132105  0.00314863
  -0.08321566  0.05777339  0.00733027 -0.00152362 -0.09454869  0.10912753
  -0.03836899  0.07800698 -0.02026444 -0.07921568  0.04151247  0.08812862
   0.03089122  0.06252371 -0.13958187  0.00130697 -0.00592137  0.0242664
  -0.04497766 -0.0236357  -0.07231516  0.04609836 -0.07470178 -0.0928202
  -0.00574458  0.01578052  0.26002322  0.19562461  0.06101797  0.05165879
  -0.06392793 -0.05228445 -0.0566685   0.02576123 -0.00603358  0.05647212
   0.1493123  -0.09726085 -0.0228137   0.1498187  -0.06108896 -0.14681379
  -0.03201511  0.01506275  0.00221919 -0.08444986 -0.27375793  0.06986084
  -0.12661738]

  6 Yhteenveto
  ===

  Muutama faktori on vastuussa suurimmasta osasta tuottoja.