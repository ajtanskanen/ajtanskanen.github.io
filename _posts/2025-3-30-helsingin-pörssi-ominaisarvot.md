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

Suoralla PCA:llä nähdään, että tuottoaikasarjasta riittää poimia ensimmäiset 5 faktoria, niin osakekurssien heilunnasta selittyy 24 prosenttia. 

Samaa kertoo satunnaismatriisien teoria: muutama ominaisarvo on merkitsevä, loppuja on vaikea erottaa kohinasta. Tässä tarkastellaan lineaarisia faktoreita, ja voi olla, että muitakin on.

Kiinnostavaa kyllä [Lettau ja Pelger (2018)](https://www.nber.org/system/files/working_papers/w24858/w24858.pdf) päätyivät siihen, että eri kriteereillä tarkasteltuna vain ensimmäiset viisi faktoria ovat merkitseviä tuottojen PCA-analyysissä. Heidän analyysinsä kohdistuu kuitenkin täysin eri aineistoon kuin tässä: Lettau ja Pelgar tarkastelevat S&P500-osaketuottoja vuosilta 1972-2014.

| Number of factors | Explanation of variance (%) |
|---:|---:|
| 1 | 16.7 |
| 2 | 19.2 |
| 3 | 21.2 |
| 4 | 22.8 |
| 5 | 24.3 |
| 6 | 25.7 |
| 7 | 27.0 |
| 8 | 28.3 |
| 9 | 29.6 |
| 10 | 30.8 |

_Taulukko 1. Varianssin selitysosuus faktorien lukumäärän funktiona._

5 Mitä faktori kertovat?
===

Faktoreista ensimmäinen on markkinariski. Ominaisvektorin arvot ovat jotakuinkin yhtä suuri kaikille osakkeille, joten faktori sijoittaa 
oleellisesti kaikkii kohteisiin yhtä paljon. Keskiarvo on noin 0.095 (Taulukko 2).

|    |         0 |        1 |       2 |         3 |        4 |         5 |         6 |        7 |        8 |         9 |        10 |       11 |      12 |        13 |       14 |        15 |        16 |        17 |        18 |        19 |       20 |       21 |        22 |        23 |       24 |       25 |       26 |        27 |       28 |        29 |        30 |        31 |       32 |        33 |       34 |       35 |       36 |       37 |       38 |        39 |        40 |       41 |       42 |       43 |       44 |       45 |        46 |       47 |       48 |       49 |        50 |        51 |       52 |        53 |        54 |       55 |      56 |       57 |       58 |        59 |        60 |        61 |       62 |        63 |        64 |        65 |       66 |       67 |       68 |       69 |        70 |        71 |        72 |        73 |       74 |       75 |       76 |       77 |       78 |        79 |       80 |        81 |      82 |       83 |        84 |       85 |        86 |       87 |       88 |       89 |        90 |        91 |        92 |      93 |       94 |       95 |      96 |
|---:|----------:|---------:|--------:|----------:|---------:|----------:|----------:|---------:|---------:|----------:|----------:|---------:|--------:|----------:|---------:|----------:|----------:|----------:|----------:|----------:|---------:|---------:|----------:|----------:|---------:|---------:|---------:|----------:|---------:|----------:|----------:|----------:|---------:|----------:|---------:|---------:|---------:|---------:|---------:|----------:|----------:|---------:|---------:|---------:|---------:|---------:|----------:|---------:|---------:|---------:|----------:|----------:|---------:|----------:|----------:|---------:|--------:|---------:|---------:|----------:|----------:|----------:|---------:|----------:|----------:|----------:|---------:|---------:|---------:|---------:|----------:|----------:|----------:|----------:|---------:|---------:|---------:|---------:|---------:|----------:|---------:|----------:|--------:|---------:|----------:|---------:|----------:|---------:|---------:|---------:|----------:|----------:|----------:|--------:|---------:|---------:|--------:|
|  Faktori 1 | 0.0713842 | 0.065152 | 0.14094 | 0.0508609 | 0.103388 | 0.0890724 | 0.0714583 | 0.132252 | 0.107709 | 0.0686949 | 0.0900749 | 0.073133 | 0.14847 | 0.0510784 | 0.139117 | 0.0966794 | 0.0387819 | 0.0786968 | 0.0477709 | 0.0871974 | 0.062038 | 0.111864 | 0.0786251 | 0.0609464 | 0.139704 | 0.125675 | 0.109644 | 0.0777007 | 0.142615 | 0.0958137 | 0.0842577 | 0.0596313 | 0.157237 | 0.0666416 | 0.145204 | 0.122208 | 0.116599 | 0.116192 | 0.126603 | 0.0913446 | 0.0712119 | 0.119409 | 0.108114 | 0.139714 | 0.145308 | 0.115541 | 0.0488117 | 0.100461 | 0.126192 | 0.108319 | 0.0854056 | 0.0857832 | 0.144737 | 0.0801655 | 0.0730819 | 0.068786 | 0.11734 | 0.043166 | 0.111463 | 0.0816493 | 0.0894419 | 0.0209294 | 0.103942 | 0.0583177 | 0.0692169 | 0.0564145 | 0.168112 | 0.113458 | 0.100935 | 0.080577 | 0.0703837 | 0.0640147 | 0.0925772 | 0.0653857 | 0.119986 | 0.169352 | 0.075244 | 0.114352 | 0.067718 | 0.0752424 | 0.152304 | 0.0830195 | 0.09308 | 0.047773 | 0.0682913 | 0.139404 | 0.0492709 | 0.161378 | 0.110762 | 0.151827 | 0.0919106 | 0.0332884 | 0.0410137 | 0.10166 | 0.151385 | 0.054704 | 0.13807 |

![Faktorien tulkinta sektorien mukaan](/images/eigen/factor1.png)<br>

Toinen faktori onkin sitten epäselvempi. Siinä painojen etumerki vaihtelee, joten kyse on jonkinlaisesta Long-Short -strategiasta.
Siinä keskipaino on noin -0.023 (Taulukko 2).

Toisessa faktorissa paino on negatiivinen suurammassa osassa osakkeista (Kuvio 4). Sektoreista kuitenkin yleishyödylliset palvelut (6510), pankit (4010), kemikaalit (5520) ovat ainoastaan positiivisia. Teknologia (1010) on valtaosin negatiivinen, samoin teollisuushyödykkeet ja -palvelut (5020). Kulutustuotteet ja -palvelu (4020) on ainoastaan negatiivinen.

|    |          0 |          1 |          2 |         3 |        4 |          5 |         6 |         7 |          8 |          9 |         10 |        11 |         12 |         13 |       14 |         15 |         16 |        17 |        18 |        19 |         20 |        21 |      22 |         23 |        24 |        25 |         26 |        27 |       28 |         29 |         30 |         31 |       32 |         33 |       34 |          35 |        36 |       37 |          38 |         39 |         40 |         41 |       42 |       43 |       44 |        45 |         46 |       47 |        48 |         49 |        50 |        51 |       52 |         53 |         54 |       55 |         56 |       57 |         58 |        59 |        60 |         61 |         62 |         63 |        64 |        65 |        66 |        67 |         68 |         69 |         70 |         71 |         72 |         73 |       74 |       75 |        76 |       77 |      78 |         79 |     80 |         81 |         82 |         83 |       84 |        85 |         86 |       87 |         88 |       89 |         90 |         91 |         92 |        93 |       94 |        95 |        96 |
|---:|-----------:|-----------:|-----------:|----------:|---------:|-----------:|----------:|----------:|-----------:|-----------:|-----------:|----------:|-----------:|-----------:|---------:|-----------:|-----------:|----------:|----------:|----------:|-----------:|----------:|--------:|-----------:|----------:|----------:|-----------:|----------:|---------:|-----------:|-----------:|-----------:|---------:|-----------:|---------:|------------:|----------:|---------:|------------:|-----------:|-----------:|-----------:|---------:|---------:|---------:|----------:|-----------:|---------:|----------:|-----------:|----------:|----------:|---------:|-----------:|-----------:|---------:|-----------:|---------:|-----------:|----------:|----------:|-----------:|-----------:|-----------:|----------:|----------:|----------:|----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|---------:|---------:|----------:|---------:|--------:|-----------:|-------:|-----------:|-----------:|-----------:|---------:|----------:|-----------:|---------:|-----------:|---------:|-----------:|-----------:|-----------:|----------:|---------:|----------:|----------:|
|  Faktori 2 | -0.0987624 | -0.0502853 | -0.0481837 | -0.153289 | -0.14999 | -0.0562425 | -0.117011 | -0.100118 | -0.0610231 | -0.0953434 | -0.0835772 | -0.121439 | -0.0839265 | -0.0740467 | 0.029333 | -0.0676031 | -0.0855886 | -0.109142 | -0.100042 | 0.0631662 | -0.0382328 | -0.116545 | -0.1335 | -0.0670171 | 0.0361017 | -0.023166 | -0.0974569 | -0.111407 | 0.175734 | -0.0708022 | -0.0858016 | -0.0953058 | 0.129731 | -0.0639025 | 0.139417 | -0.00026477 | 0.0253977 | 0.165055 | 0.000419409 | -0.0221606 | -0.0810495 | -0.0741386 | 0.124951 | 0.261001 | 0.130615 | 0.0800201 | -0.0883547 | -0.11468 | 0.0248014 | -0.0621301 | 0.0219651 | 0.0282665 | 0.127533 | -0.0621109 | -0.0765798 | -0.07921 | -0.0634239 | -0.03938 | -0.0166029 | -0.125951 | -0.101233 | -0.0473239 | -0.0311402 | -0.0714979 | -0.112449 | -0.125449 | 0.0410068 | 0.0319837 | -0.0907293 | -0.0410517 | -0.0994497 | -0.0386931 | -0.0662552 | -0.0839776 | 0.237343 | 0.284039 | -0.106576 | -0.14694 | 0.02727 | -0.0745879 | 0.1053 | -0.0392802 | -0.0470736 | -0.0833072 | -0.10635 | 0.0660218 | -0.0429861 | 0.276294 | -0.0234391 | 0.156107 | -0.0498271 | -0.0613148 | -0.0257913 | 0.0231258 | 0.133236 | -0.117075 | 0.0807628 |

![Faktorien tulkinta sektorien mukaan](/images/eigen/factor2.png)<br>

Kolmas faktori kuvaa Long-Short -strategiaa, jossa osaan kohteista sijoitetaan (long), osaa myydään (short).
Keskimääräinen paino on lähes nolla (Taulukko 2). Vastaavan tuloksen saivat 
[Lettau ja Pelger (2018)](https://www.nber.org/system/files/working_papers/w24858/w24858.pdf).

Entä mihin kohteisiin kolmas faktori sijoittaa? 

|    |         0 |           1 |         2 |           3 |          4 |        5 |         6 |         7 |          8 |         9 |         10 |        11 |        12 |        13 |         14 |        15 |        16 |         17 |        18 |        19 |       20 |         21 |         22 |        23 |         24 |         25 |        26 |        27 |         28 |        29 |         30 |         31 |       32 |        33 |        34 |        35 |        36 |        37 |          38 |        39 |         40 |          41 |        42 |       43 |        44 |           45 |       46 |        47 |         48 |         49 |        50 |        51 |        52 |        53 |          54 |        55 |        56 |        57 |         58 |        59 |        60 |        61 |        62 |         63 |        64 |       65 |         66 |        67 |        68 |           69 |          70 |       71 |        72 |          73 |       74 |       75 |         76 |       77 |        78 |        79 |         80 |       81 |          82 |        83 |        84 |        85 |        86 |       87 |         88 |        89 |        90 |        91 |        92 |         93 |        94 |        95 |        96 |
|---:|----------:|------------:|----------:|------------:|-----------:|---------:|----------:|----------:|-----------:|----------:|-----------:|----------:|----------:|----------:|-----------:|----------:|----------:|-----------:|----------:|----------:|---------:|-----------:|-----------:|----------:|-----------:|-----------:|----------:|----------:|-----------:|----------:|-----------:|-----------:|---------:|----------:|----------:|----------:|----------:|----------:|------------:|----------:|-----------:|------------:|----------:|---------:|----------:|-------------:|---------:|----------:|-----------:|-----------:|----------:|----------:|----------:|----------:|------------:|----------:|----------:|----------:|-----------:|----------:|----------:|----------:|----------:|-----------:|----------:|---------:|-----------:|----------:|----------:|-------------:|------------:|---------:|----------:|------------:|---------:|---------:|-----------:|---------:|----------:|----------:|-----------:|---------:|------------:|----------:|----------:|----------:|----------:|---------:|-----------:|----------:|----------:|----------:|----------:|-----------:|----------:|----------:|----------:|
|  Faktori 3 | 0.0383032 | -0.00886664 | 0.0148879 | -0.00219741 | 0.00526766 | 0.033932 | 0.0462158 | 0.0639568 | 0.00291229 | 0.0321859 | 0.00365783 | 0.0464083 | -0.027005 | 0.0130993 | 0.00159199 | 0.0469896 | 0.0314603 | 0.00632941 | 0.0142583 | -0.239012 | 0.022324 | -0.0240161 | 0.00447637 | 0.0201527 | 0.00401227 | -0.0311855 | 0.0594066 | 0.0538222 | -0.0153789 | 0.0382594 | -0.0529391 | 0.00640041 | 0.061787 | 0.0122126 | 0.0229221 | -0.297551 | -0.292541 | -0.129453 | -0.00232405 | 0.0136942 | -0.0127959 | -0.00386063 | 0.0817746 | 0.129496 | 0.0793578 | -0.000259022 | 0.047476 | 0.0587609 | 0.00216131 | -0.0584443 | -0.509304 | -0.511751 | 0.0987671 | 0.0518446 | -0.00548708 | 0.0295989 | 0.0179439 | 0.0214282 | -0.0465378 | 0.0139097 | 0.0843017 | 0.0577647 | -0.100528 | 0.00334922 | 0.0591576 | 0.074452 | 0.00690699 | -0.079287 | 0.0257852 | -0.000429284 | 0.000300366 | 0.041237 | 0.0463542 | -0.00928066 | 0.132362 | 0.145164 | -0.0558764 | 0.049348 | -0.081919 | 0.0155175 | -0.0621808 | 0.110073 | -0.00593215 | 0.0454056 | 0.0416298 | 0.0449474 | 0.0316188 | 0.108314 | -0.0633271 | 0.0268522 | 0.0350287 | 0.0142398 | 0.0449774 | -0.0421315 | 0.0393237 | 0.0349904 | 0.0368445 |

![Faktorien tulkinta sektorien mukaan](/images/eigen/factor3.png)<br>

Neljäs faktori onkin sitten epäselvempi.

|    |          0 |          1 |         2 |         3 |          4 |          5 |          6 |          7 |          8 |          9 |         10 |        11 |          12 |         13 |        14 |         15 |         16 |        17 |         18 |       19 |        20 |        21 |         22 |          23 |        24 |        25 |         26 |        27 |        28 |        29 |         30 |           31 |        32 |         33 |         34 |       35 |       36 |       37 |        38 |        39 |         40 |        41 |        42 |        43 |         44 |       45 |        46 |         47 |         48 |       49 |        50 |        51 |         52 |         53 |         54 |        55 |         56 |        57 |        58 |          59 |          60 |         61 |        62 |         63 |         64 |         65 |        66 |        67 |         68 |        69 |        70 |         71 |         72 |         73 |        74 |        75 |         76 |        77 |         78 |        79 |        80 |         81 |        82 |         83 |         84 |       85 |        86 |        87 |         88 |        89 |         90 |         91 |        92 |         93 |        94 |        95 |         96 |
|---:|-----------:|-----------:|----------:|----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|----------:|------------:|-----------:|----------:|-----------:|-----------:|----------:|-----------:|---------:|----------:|----------:|-----------:|------------:|----------:|----------:|-----------:|----------:|----------:|----------:|-----------:|-------------:|----------:|-----------:|-----------:|---------:|---------:|---------:|----------:|----------:|-----------:|----------:|----------:|----------:|-----------:|---------:|----------:|-----------:|-----------:|---------:|----------:|----------:|-----------:|-----------:|-----------:|----------:|-----------:|----------:|----------:|------------:|------------:|-----------:|----------:|-----------:|-----------:|-----------:|----------:|----------:|-----------:|----------:|----------:|-----------:|-----------:|-----------:|----------:|----------:|-----------:|----------:|-----------:|----------:|----------:|-----------:|----------:|-----------:|-----------:|---------:|----------:|----------:|-----------:|----------:|-----------:|-----------:|----------:|-----------:|----------:|----------:|-----------:|
|  Faktori 4 | -0.0998106 | -0.0446252 | 0.0615402 | 0.0184584 | 0.00428632 | -0.0843223 | -0.0134014 | 0.00872459 | -0.0252623 | -0.0467516 | -0.0940223 | 0.0694705 | -0.00431648 | -0.0391921 | 0.0954103 | -0.0944217 | -0.0339217 | 0.0164986 | 0.00375207 | 0.020299 | 0.0414336 | 0.0107286 | -0.0552413 | -0.00458413 | 0.0986191 | 0.0643935 | -0.0463447 | -0.042897 | 0.0192432 | 0.0312305 | -0.0433251 | -0.000675563 | 0.0820787 | -0.0544771 | 0.00897412 | 0.427529 | 0.438939 | 0.108399 | 0.0339271 | 0.0520375 | -0.0301137 | 0.0690498 | -0.119016 | -0.098344 | -0.0497751 | 0.075803 | 0.0194581 | -0.0538717 | 0.00860067 | 0.127554 | -0.387769 | -0.388383 | -0.0357605 | -0.0496947 | -0.0321234 | -0.050855 | 0.00515158 | 0.0241119 | 0.0380187 | -0.00488167 | -0.00252104 | -0.0569579 | 0.0344185 | -0.0574819 | -0.0476811 | -0.0918105 | 0.0503666 | 0.0543022 | -0.0167812 | -0.102402 | 0.0336735 | 0.00690586 | -0.0575701 | -0.0670082 | -0.147661 | -0.109402 | -0.0424107 | 0.0131749 | -0.0283011 | 0.0262806 | 0.0594698 | -0.0207924 | 0.0560062 | -0.0480243 | -0.0178403 | 0.106214 | 0.0276758 | -0.118915 | 0.00255351 | 0.0206749 | -0.0389004 | -0.0585835 | -0.105833 | -0.0938143 | 0.0340986 | 0.0189602 | 0.00654115 |

![Faktorien tulkinta sektorien mukaan](/images/eigen/factor4.png)<br>

Viides faktori onkin sitten epäselvempi.

|    |         0 |          1 |          2 |         3 |           4 |         5 |         6 |         7 |         8 |          9 |         10 |       11 |         12 |         13 |         14 |         15 |        16 |        17 |       18 |        19 |        20 |        21 |        22 |        23 |         24 |         25 |         26 |        27 |        28 |         29 |         30 |       31 |        32 |          33 |        34 |       35 |       36 |         37 |       38 |        39 |          40 |         41 |       42 |       43 |        44 |        45 |      46 |         47 |         48 |        49 |         50 |         51 |         52 |       53 |        54 |        55 |         56 |         57 |        58 |        59 |       60 |        61 |        62 |        63 |         64 |        65 |         66 |         67 |         68 |        69 |        70 |         71 |          72 |      73 |       74 |       75 |        76 |        77 |         78 |        79 |        80 |        81 |          82 |        83 |       84 |         85 |         86 |       87 |         88 |        89 |         90 |        91 |         92 |         93 |        94 |      95 |        96 |
|---:|----------:|-----------:|-----------:|----------:|------------:|----------:|----------:|----------:|----------:|-----------:|-----------:|---------:|-----------:|-----------:|-----------:|-----------:|----------:|----------:|---------:|----------:|----------:|----------:|----------:|----------:|-----------:|-----------:|-----------:|----------:|----------:|-----------:|-----------:|---------:|----------:|------------:|----------:|---------:|---------:|-----------:|---------:|----------:|------------:|-----------:|---------:|---------:|----------:|----------:|--------:|-----------:|-----------:|----------:|-----------:|-----------:|-----------:|---------:|----------:|----------:|-----------:|-----------:|----------:|----------:|---------:|----------:|----------:|----------:|-----------:|----------:|-----------:|-----------:|-----------:|----------:|----------:|-----------:|------------:|--------:|---------:|---------:|----------:|----------:|-----------:|----------:|----------:|----------:|------------:|----------:|---------:|-----------:|-----------:|---------:|-----------:|----------:|-----------:|----------:|-----------:|-----------:|----------:|--------:|----------:|
|  Faktori 5 | 0.0790022 | -0.0882495 | -0.0504608 | 0.0237683 | -0.00907747 | 0.0123653 | 0.0109041 | 0.0398683 | 0.0418264 | 0.00591652 | -0.0715646 | 0.156077 | -0.0845007 | -0.0447667 | -0.0484104 | -0.0192313 | 0.0293059 | 0.0356413 | 0.119507 | 0.0517396 | 0.0182892 | 0.0382712 | 0.0347205 | 0.0663156 | -0.0904822 | -0.0690511 | -0.0285441 | 0.0370308 | -0.038613 | -0.0571747 | -0.0288894 | 0.078189 | -0.185093 | -0.00877028 | -0.051754 | 0.267802 | 0.275661 | -0.0841113 | -0.01383 | 0.0032576 | -0.00272046 | 0.00335009 | 0.349403 | 0.307823 | -0.118197 | -0.185727 | 0.11132 | 0.00314863 | -0.0832148 | 0.0577737 | 0.00732941 | -0.0015242 | -0.0945485 | 0.109128 | -0.038369 | 0.0780073 | -0.0202643 | -0.0792158 | 0.0415123 | 0.0881285 | 0.030891 | 0.0625239 | -0.139582 | 0.0013066 | -0.0059215 | 0.0242666 | -0.0449767 | -0.0236362 | -0.0723152 | 0.0460974 | -0.074702 | -0.0928199 | -0.00574434 | 0.01578 | 0.260023 | 0.195625 | 0.0610182 | 0.0516594 | -0.0639264 | -0.052284 | -0.056669 | 0.0257612 | -0.00603358 | 0.0564721 | 0.149313 | -0.0972607 | -0.0228145 | 0.149819 | -0.0610897 | -0.146814 | -0.0320156 | 0.0150621 | 0.00221875 | -0.0844506 | -0.273758 | 0.06986 | -0.126617 |

![Faktorien tulkinta sektorien mukaan](/images/eigen/factor5.png)<br>
_Kuvio 4. Viiden ensimmäisen faktori tulkinta sektoreittain. Siniset positiivisia, oranssit negatiivia._

Kuvio 4 näyttää, että ensimmäinen faktorin paino on positiivinen kaikille osakkeille. 


| Faktori | Keskiarvo | Keskihajonta |
-----------------------
1 | 0.09548300617702303 | 0.03452931916377785 |
2 | -0.023428722795141223 | 0.09879460156660337 |
3 | -0.0006403110756748557 | 0.10153259748593965 |
4 | -0.008493130553508857 | 0.10117877783367679 |
5 | 0.006394760285126634 | 0.10133304195281624 |
-----------------------
_Taulukko 2. Faktorien tunnusluvut._

Ensimmäinen faktori 

  6 Yhteenveto
  ===

  Muutama faktori on vastuussa suuresta osasta osakeindeksin tuottoa. Tämän tutkimuksen mukaan Helsingin Pörssin NASDAQ Helsinki -indeksin tuottoja ajaa vain viisi faktoria.
  