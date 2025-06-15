---
title: 'Haittaluokkien yhteenlasku eli miten juristeilta sujuu kertolasku?'
date: 2025-6-30
permalink: /posts/2025/6/haittaluokat/
summary: 'Blogi | Työtapaturmajärjestelmässä haittaluokituksen perusteella maksetaan haittarahaa. Jos haittoja on useampi, lasketaan niiden haittaluokat yhteen. Juristien käsissä reaalilukujen kertolaskun vaihdannaisuus voi hävitä.'
tags:
  - kertolasku
  - juridiikka
---

Juristeista kerrotaan monenlaisia vitsejä, joista jotkin ovat ihan osuvia. Mutta ei mennä tässä niihin, vaan mietitään, millaista on juristimatematiikka. Innoitus tähän tulee työtapaturmalainsäädännöstä, jossa on oma sääntönsä siihen, missä järjestyksessä kertolasku pitää tehdä.

Matematiikassa kertolasku voi olla vaihdannasta tai ei-vaihdannaista. Reaaliluvuille tavanomainen kertolasku on vaihdannaista, eikä ole väliä kummassa järjestyksessä kahden luvun kertolasku tehdään. Aina näin ei ole, ei ainakaan työtapaturman haittaluokka-asetuksen mukaan. Siinä on kokonaislukujen kertolaskusta versio, joka vaatii järjestyssäännön toimiakseen. Käydään läpi, mistä on kyse.

1 Työtapaturmalainsäädäntö
===

Suomessa on yksi maailman parhaista työtapaturmajärjestelmistä. Jos työssä sattuu tapaturma, korvataan tapaturman aiheuttaman työkyvyttömyyden ajalta täyden palkan verran jopa vuoden ajan. Jos työnteko tämänkin jälkeen estyy, jatketaan korvausta 70 prosentin tasolla aiemmista tuloista tästä eteenpäinkin. Korvaustaso on korkea verrattuna oikeastaan mihin tahansa muuhun suomalaiseen lakisääteiseen sosiaalivakuutukseen.

Jos tapaturma aiheuttaa pysyvän yleisen haitan, maksetaan korvauksena haittarahaa. Pysyvä yleinen haitta tarkoittaa tapaturman aiheuttamaan toimintakyvyn alentumista.
Haittaraha määräytyy haittaluokan mukaan. Haittaluokkien laskentasäännöstä juristit ovat matemaatikon näkökulmasta tehneet hieman erikoisen.

Pysyvä haitta määritellään asteikolla 0-20. Korvaukseen oikeuttavat haittaluokat 1-20, korvaustaso kasvaa joka luokan mukaan. Esimerkiksi haittaluokka 10 oikeuttaa 13 % * 12 440 euroa/kuukaudessa haittarahaan vuonna 2025. (Tsekkaa)

2 Haittaluokkien yhteenlasku
===

Jos henkilöllä on useampi haittarahaan oikeuttava haitta, lasketaan haittojen haittaluokat yhteen. Eri raajoihin kohdistuvat vammat lasketaan yhteen kaavalla
\[
    H_{A+B} = H_A + H_B – H_A * H_B / 20        (1)
\]

Tämähän näyttää samalta kuin riippumattomien todennäköisyyksien yhteenlasku. Ja kyllä, sitä se onkin, mutta siinä on huomioitu skaala 0-20 tavanomaisen 0-1 skaalan sijaan.

Jos haitat kohdistuvat samanaikaisesti toisiaan korvaaviin parillisiin elimiin tai sekä näkö- että kuuloaistiin, lasketaan haitat suoraan yhteen. Esimerkiksi molempiin käsiin kohdistuvat vammat lasketaan suoraan yhteen. Tämä taas on täysin korreloituneiden erillisten todennäköisyyksien summaukselta. 

Haittaluokkien yhteenlaskussa on siis kyse todennäköisyyksien yhteenlaskusta. Ikäänkuin haittaluokka 20 vastaisi tilannetta, jossa kaikki toimintakyky on hävinnyt. Alemmat haittaluokat kuvaavat lineaarisesti kasvavaa osuutta täydestä toimintakyvyn menetyksestä. 

Ongelma
===

Tähän asti kaikki selvää. Kuitenkin kolmeen tai useampaan haittaan sovellettaessa, on lainsäädännössä määritelty, että yhdistettäessä kolme haittaluokkaa lähdetään yhdistämään suurimmasta alkaen. Sääntö on vastaus siihen, että riippuen yhdistämisjärjestyksestä tulos voi olla. Mutta .. eihän tämä voi olla totta!? Reaalilukujen kertolasku on vaihdannaista, järjestyksellä ei ole väliä. 

Erikoinen ongelma johtuu pyöristyksestä. Haittaluokat pyöristetään kokonaislukuun kesken laskutoimituksen. Jos esimerkiksi yhdistetään haittaluokat 1,2 ja 5 kaavalla (1), saadaan 7,175, joka pyöristyy haittaluokkaan 7. 

Jos taas lähdetään suurimmasta liikkeelle ja yhdistetään siihen haittalaluokka 2, saadaan haittaluokka 6,5. Pyöristetään se seitsemään ja yhdistetään siihen haittaluokka 1, jolloin tulos on 7,65. Tämä pyöristyy haittaluokkaan 8. Matematiikan kannalta tämä on väärä tulos.

Matematiikassa reaalilukujen kertolasku on vaihdannaista. Jos kesken laskutoimituksen kuitenkin pyöristetään, voi vaihdannaisuus kadota. Otetaanpa esimerkki. Kerrotaan luvut 1,5; 3 ja 4. Tulo luvuista 1,5 ja 3 on 4,5. Jos tässä vaiheessa pyöristetään, on tulos 5. Tulo luvuista 5 ja 4 on 20. Eli matkan varrella pyöristämällä kertolasku

\[
1,5 * 3 * 4 \sim 20 \text{pyöristämällä}
4 * 3 * 1,5 \sim 18 \text{pyöristämättä}
\]

Toisessa järjestyksessä: tulo luvuista 4 ja 3 on 12. Kerrotaan tämä 1,5:llä ja saadaan 18, joka tulee myös pyöristämättä. Ongelma haittaluokkien yhteenlaskussa tulee  pyöristämisestä. Tästä syystä peruskoulussa opetettiin, ettei lukuja ole fiksua pyöristää kesken laskutoimituksen.

4 Lopuksi
===

Tavoitteena matemaattisten laskusääntöjen rusikoinnilla tapaturmalainsäädässä on ollut yhdenmukaistaa soveltamiskäytäntö ja varmistaa, että kaikkia vakuutettuja kohdellaan yhdenmukaisesti. Tämä on hyvä ja perusteltu tavoite. Lopputulos on kuitenkin sattumanvarainen, ja heikentää laskennan teoriapohjaa ja tulkintaa. On olemassa matematiikkaa ja juristimatematiikkaa, eikä niillä ole kovin paljoa tekemistä keskenään.

