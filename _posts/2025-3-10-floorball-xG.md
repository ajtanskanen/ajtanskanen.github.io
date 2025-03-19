---
title: 'Salibandyn xG ja maalit - Salibandy osa 3'
date: 2025-03-16
permalink: /posts/2025/3/salibandy_xG/
image: /images/floorball/xG/miehet_goals_xG.png
largeimage: /images/floorball/xG/miehet_goals_xG.png
summary: 'Blogi | Analysoidaan odotettujen maalien määrää, siis xG:tä, F-Liigassa.'
tags:
  - salibandy
  - tilastot
  - maalit
---

Maaliodottama xG kertoo, kuinka monta maalia ottelussa esiintyneistä tilanteista yleensä olisi tehty. Mutta miten lasketaan maaliodottama xG salibandyn datasta? Entä millaisia eroja joukkueiden välillä on xG:ssä? Tämä blogi vastaa näihin kysymyksiin.

1 Maaliodottama xG
===

Maaliodottama xG tarkoittaa odotettua maalien määrää, kun otetaan ottelussa esiintyneet maalintekotilanteet annettuna. Maaliodottaman voi laskea usealla eri menetelmällä. Tässä on käytetty kaikkein helpointa tapaa, jossa huomioidaan yksinkertaisella tavalla vain maalitekotilanteen sijainti kentällä. 

Tässä xG lasketaan pelkästään laukaisujen määrän ja paikan perusteella. Kenttä jaetaan ensin ruudukoihin, joista jokaiselle lasketaan montako laukausta ja maalia on tehty ko. ruudusta. Tämä suhde kertoo estimaatin todennäköisyydelle ruudusta laukaistulle vedolle mennä maaliin. Näin saadaan todennäköisyysjakauma vedoille.

Kun lasketaan odotettujen maalien määrää xG ottelussa, lasketaan jokaiselle ruudulle joukkueen siitä ampumien vetojen määrä ja kerrotaan yllä lasketulla todennäköisyydellä. Näiden tulojen summa on sitten joukkueen xG ottelussa.

xG-ero kertoo tehtyjen maalien ja xG:n erotuksen. Mitä korkeampi se on, sitä laadukkaampaa on joukkueen viimeistely. Osaltaan se kertoo myös sen, että xG ei suinkaan ole koko tarina. Tässä käytetty maaliodottama xG ei mm. kerro, miten muut pelaajat ovat sijoittuneet vetotilanteessa.

Mitä korkeampi on joukkueen xG, sitä laadukkaampaa on sen peli. 
Samalla tavalla myös xG-ero, siis tehtyjen maalien ja xG:n ero kertoo joukkueen pelin tasosta. Jos joukkue pystyy toistuvasti ylittämään xG:n, on sen pystyttävä luomaan laadukkaampia vetoja kuin mitä xG ennustaa.

Vastinpari xG:lle on joukkuetta vastaan tehty xG, jota merkitään xGA:lla. Se kertoo siitä, miten laadukkaita maalintekopaikkoja joukkueen puolustus salliin. Mitä korkeampi xGA, sitä heikompi puolustus. Jos joukkuetta vastaan on tehty maaleja vähemmän kuin xGA antaa odottaa, on joukkueen puolustus ollut hyvää.

Aineistona analyysissä on kauden 2024-2025 runkosarjan data.

2 Joukkueiden xG
===

2.1 Miehet
===

Taulukko 1 näyttä, millaisia odotettuja maalimääriä eri joukkueet ovat saaneet. Erot xG:n ja tehtyjen maalien välillä ovat eri suuria. Oleellisesti xG kertoo, miten hyviä vetopaikkoja joukkueiden peli tuottaa. KrP:llä ero on hurja, jopa 51 maalia. Kiinnostavasti Classic kuitenkin johtaa sarjaa, vaikka sen xG-ero on paljon pienempi, 37,2 maalia. 

Classicin ja SPV:n xG:t ovat lähes samat, mutta SPV:n xG-ero on -4,1. Peli tuottaa yhtä hyviin paikkoihin vetopaikkoja, mutta SPV saa niistä selvästi Classicia vähemmän tehtyä maaleja. SPV:n xG on korkeampi kuin Indiansin, mutta Indians on kyennyt tekemään selvästi enemmän maaleja.

Oilersin xG on selvästi korkein kaikista joukkueista. Sen peli on tällä mittarilla kaikkein laadukkainta. Maaleja se ei kuitenkaan ole pystynyt niistä tekemään yhtä tehokkaasti kuin KrP, Classic tai Indians. 

![Maalien jakauma](/images/floorball/xG/xG_laaja_miehet.png)<br>
_Taulukko 1. xG joukkueille miesten F-Liigassa._

Maalidottamalla mitattuna heikoin joukkue miesten F-Liigassa on LASB. Sen peli ei tuota hyvin vetopaikkoja (matala xG). Heikoin konvertoimaan vetopaikat maaleiksi on kuitenkin OLS, joka on onnistunut saaman vetoja hyviltä paikoilta, mutta xG-ero on jopa -35,1 maalia. 

Oilers on onnistunut tekemään enemmän maaleja kuin odottaman xG verran. Tämän lisäksi Oilersin puolustus on ollut niin tiivis, että maaleja sitä vastaan on tehty jopa vähemmän sitä vastaantehtyjen maaliodottaman XGA:n verran.

![Maalien jakauma](/images/floorball/xG/miehet_xGA_xG.png)<br>
_Kuvio 1. xGA/maalit vastaan vs xG/maalit joukkueille miesten F-Liigassa. Oranssit pisteet toteuma, siniset xG._

Heikoin XGA on Jymyllä ja LASBilla. Molemmille on vieläpä tehty enemmän maaleja kuin sarjan heikoin XGA antaa odottaa. EräViikingit on tehnyt vähemmän maaleja kuin xG antaa odottaa, mutta puolustanut tiiviisti, jolloin sitä vastaa on tehty vähemmän maaleja kuin xGA antaa odottaa.

![Maalien jakauma](/images/floorball/xG/miehet_goals_xG.png)<br>
_Kuvio 2. xG vastaa melko hyvin tehtyjen maalien määrää eri joukkueilla. Oranssi katkoviiva kuvaa tilannetta, jossa xG on sama kuin tehtyjen maalien määrä._

Ainoastaan F-Liigan neljän sarjakärki on pystynyt ylittämään maaliodottaman. SPV on lähellä rajaa ja kaikki muut alapuolella. Regressioviiva (sininen käyrä kuviossa 2) kertoo, että mitä korkeampi xG sitä enemmän toteuma ylittää xG:n. Tämä tarkoittaa, että tässä käytetty tapa laskea xG ei sisällä riittävästi tietoja.

2.2 Naiset
===

Naisten F-Liigassa erot kärjen ja häntäpään välillä ovat valtavat kaikilla mittareilla mitattuna: niin xG:llä, xGA:lla kuin tehtyjen maalien perusteella mitattuna.
Kärki on suorittanut hyvin xG:llä mitattuna mutta myös ylittänyt xG:n. Samoin kärjen puolustus on ollut hyvää xGA:lla mitattuna.

Naisten F-Liigassa TPS on aivan omilla lukemillaan xG:ssä. Se on jauhanut xG:tä 35 maalia enemmän kuin seuraavana oleva Classic. Tämä näkyy myös sarjataulukossa, jossa TPS johtaa ja Classic on toinen. Karkeasti xG kertoo sijoituksen sarjataulukossa.

![Maalien jakauma](/images/floorball/xG/xG_laaja_naiset.png)<br>
_Taulukko 2. xG joukkueille naisten F-Liigassa._

Taulukosta 2 näkyy, että TPS sekä tekee tehokkaasti maaleja että myös puolustaa vahvasti. Sitä vastaan on tehty maaleja vähän ja myös xGA TPS:ää vastaan on F-Liigan toiseksi matalin 57,9 maalia. Kuitenkin toteuma 39 maalia in tätäkin matalampi. Hajonta on naisten F-Liigassa suurta.

Vastaavasti Erä-Viikingit tekee maaleja odotettuun tahtiin, mutta puolustaa hyvin. Sitä vastaan on tehty vähän maaleja ja myös xGA sitä vastaan on matala. Tämä näkyy myös kuviosta 3, joka osoittaa, että korkea xG yhdistyy matalaan xGA:han. Tämän voi myös sanoa, että hyvin puolustavat joukkueet ovat sekä antaneet vain vähän maalintekotilanteita vastustajalle että päässeet itse paljon hyviin maalintekotilanteita. 

![Maalien jakauma](/images/floorball/xG/naiset_xGA_xG.png)<br>
_Kuvio 3. xGA/maalit vastaan vs xG/maalit joukkueille naisten F-Liigassa. Oranssit pisteet toteuma, siniset xG._

![Maalien jakauma](/images/floorball/xG/naiset_goals_xG.png)<br>
_Kuvio 4. xG vastaa melko hyvin tehtyjen maalien määrää eri joukkueilla. Oranssi katkoviiva kuvaa tilannetta, jossa xG on sama kuin tehtyjen maalien määrä._

Naisten F-Liigan kuudesta kärkijoukkueesta viisi on pystynyt ylittämään maaliodottaman. Kuusikosta vain EräViikingit on alittanut odottaman. Kaikki muut joukkueet ovat odottaman alapuolella. Regressioviiva (sininen käyrä kuviossa 4) kertoo, että mitä korkeampi xG sitä enemmän toteuma keskimäärin ylittää xG:n.

3 Pelaajien xG
===

3.1 Miehet
----

Justus Kainulainen on kuuluisa hurjasta vedostaan. Hän onkin xG-erolla:llä mitattuna toiseksi paras miesten F-Liigassa. Paras on kuitenkin Tiitus Salokangas, joka on onnistunut taikomaan yli kaksinkertaisen määrän maaleja xG:hen verrattuna. Hän on vastannut yksinään lähes puolesta Classicin xG-erosta.

![Maalien jakauma](/images/floorball/xG/xG_players_men.png)<br>
_Taulukko 3. xG pelaajille miesten F-Liigassa._

Kaikkiaan 281 pelaajaa on tehnyt F-Liigassa maaleja. Pelaajista 110:llä on positiivinen xG. Yli 10 maalia tehneitä pelaajia on 70 ja heistä 46:lla on positiivinen xG.
Toisin sanoen, paljon maaleja tehneillä on pääsääntöisesti keskimääräistä korkeampi xG.

3.2 Naiset
---

Naisissa Miisa Turunen on omilla lukemillaan: kun xG on 17, on hän tehnyt maaleja 29. Tästä huolimatta SaiPan xG-ero on negatiivinen.

![Maalien jakauma](/images/floorball/xG/xG_players_women.png)<br>
_Taulukko 4. xG pelaajille naisten F-Liigassa._

Kaikkiaan 275 pelaajaa on tehnyt F-Liigassa maaleja. Pelaajista 101:llä on positiivinen xG. Jos rajoitutaan yli 10 maalia tehneisiin, on pelaajia 33 kappaletta, ja heistä 31:llä on positiivinen xG.


4 Kehityskohteita ja rajoituksia
===

Tässä on tehty xG:n laskentaa yksinkertaistetusti. Osin se johtuu saatavilla olevasta datasta. 

Tulosten mukaan tässä käytetty tapa laskea xG ei sisällä riittävästi tietoja. Se näkyi siinä, että xG systemaattisesti aliarvioi tehtyjen maalien lukumäärää kärkijoukkueilla ja yliarvioi tehtyjen maalien määrää häntäpään joukkueilla. Sama ilmiö oli havaittavissa sekä naisten että miesten F-Liigassa. 

Tarkempaa laskentaa olisi mahdollista tehdä, jos tarkempaa dataa vetoihin annetuista syötöistä ja vastustajan sijoittumisesta vetotilanteessa olisi saatavilla. Tällöin laskenta edellyttäisi koneoppimismenetelmien käyttöä, mutta se olisi lähinnä kiinnostava harjoitus. Data kuitenkin puuttuu.