---
title: 'Helsingin sanomien pääkirjoitusten poliittisuus ja arvot'
date: 2025-06-30
permalink: /posts/2025/6/paakirjoitukset/
summary: 'Blogi | Helsingin Sanomien pääkirjoituksissa otetaan usein kantaa ajankohtaisiin asioihin. Uutisoinnin neutraaliutta voi analysoida suurilla kielimalleilla. Tässä käytämme Anthropicin Claudea, jonka mukaan HS:n pääkirjoitukset painottuvat vahvasti arvoliberalismia kannattaviksi ja maltillisen vasemmistolaisiksi.'
tags:
  - pääkirjoitukset
  - poliittisuus
  - arvot
---

Helsingin Sanomat on arvostettu suomalainen instituutio, joka ei ole vain passiivinen asioiden seuraaja, vaan ottaa lehtenä kantaa ajankohtaisiin asioihin. Linjaa esitellään pääkirjoituksissa. Tässä blogissa analysoidaan, mihin kohtaan arvokarttaa pääkirjoitukset sijoittuvat. Tulosten mukaan HS on vahvasti arvoliberaali ja lievästi vasemmistolainen lehti.

Alun perin Helsingin Sanomat perustettiin nuorsuomalaisen Päivälehden jatkajaksi. Se aatemaailma tulee siis porvarillis-liberaalista, sosiaalisia asioita korostaneesta nuorsuomalaisesta liikkeestä.

![HS:n uutisten poliittisuuden jakauma](/images/HS/jakauma.png)<br>
_Kuvio 1. HS:n uutisjuttujen poliittisen näkökulman (vaaka-akseli) ja arvojen (pystyakseli) yhteisjakauma._

1 Aineisto
===

Helsingin Sanomat kuvaava itse [pääkirjoitusten](https://www.hs.fi/info/art-2000010221266.html) linjaa näin:
> Pääkirjoituksissa määritellään lehden kanta eri asioihin, mutta uutistoimituksen työtä pääkirjoitukset eivät määritä. Niiden linjaukset eivät myöskään poista objektiivisuuden tai tasapuolisuuden vaadetta uutissisällöissä.

Blogin analyysin ei ole tarkoitus olla kattava. Aineistossa oli vain 39 pääkirjoitusta, jotka on kerätty 31.5.2025-20.6.2025 väliltä. Laajempi tutkimus kertoisia paremmin, miten HS sijoittuu arvokartalle. 

2 Menetelmä
===

Suurella kielimallilla voi luokitella kirjoituksia erilaisilla perusteilla. Tässä käytetään Anthropicin Claude Opus 4 -mallia.
Tarkastelen 83 uutisjuttua YLEn verkkosivuilla. Juttujen teksti haettiin scraperilla analyysiä varten. Tästä aineistosta on poistettu 7 uutista, joita scraper ei onnistunut keräämään kunnolla koska vain otsikko tuli mukaan ja varsinainen teksti jäi pois. Lisäksi yhdessä tapauksessa Claude ei osannut tuottaa numeerista arviota. Lista jutuista ja tulokset löytyy tiiviissä muodossa blogin lopussa.

Promptit, joita analyysissä on käytetty, ovat yksinkertaisia. Mitään muita prompteja ei analyysissä käytetä.

Systeemi-prompti:
> You are an AI assistant tasked with analyzing political biases in works. Your goal is to provide insightful commentary on polical leaning, and liberal/conservative leaning. output in JSON format with keys: \“arvot\” (asteikko (-10,10)), \"poliittinen suuntaus\" (asteikko (-10,10)), \"perustelut arvot\", and \"perustelut poliittinen suuntaus\".\n

Analyysi-prompti:
> Analysoi kirjoitus. Onko se kirjoitettu arvoliberaalista vai arvokonservatiivisesta näkökulmasta? arvioi asteikolla (-10,10). Arvo -10 tarkoittaa hyvin arvoliberaalia, arvo 10 hyvin arvokonservatiivista. Entä onko se kirjoitettu vasemmistolaisesta vai oikeistolaisesta näkökulmasta? arvioi asteikolla (-10,10). Arvo -10 tarkoittaa hyvin vasemmistolaista, arvo 10 hyvin oikeistolaista. Vastaa JSON muodossa. (encode special chars properly)

Promptien tarkoituksena on tuottaa numeerinen arvio kirjoituksen poliittisesta näkökulmasta ja siitä, mitä arvonäkökulmasta juttu on kirjoitettu. Poliittinen näkökulma arvioidaan vasemmisto-oikeisto -akselilla, kun taas kirjoituksen arvot arvioidaan arvoliberaali-konservatiivi -akselilla. Näiden pitäisi vastata esimerkiksi Helsingin Sanomien tekemien arvokarttojen asteikkoja, vaikka metodologia on erilainen.

Jokaista tekstiä varten keskustelu Clauden kanssa avataan uudestaan, jotta aiemmat vastaukset eivät sotke tuloksia. Lämpötila on mallinnuksessa 1.0, jotta tulokset olisivat mahdollisimman toistettavissa. Clauden vastaukset muuttuvat eri ajokerroilla hieman, vaikka promptit ja aineistot pysyvät samoina. Vaihtelu ei kuitenkaan vaikuta olevan kovin suurta.


3 Arvot
===

Pääkirjoitukset ovat selvästi arvoliberaaleja: keskiarvo on -2,3 asteikolla (-10; 10). Tyypillinen pääkirjoitus on sekin selvästi arvoliberaali, sillä mediaani on -2.
Tämä lienee odotettua, koska HS perustettiin kannattamaan liberaaleja arvoja.

![YLEn uutisten arvojen jakauma](/images/HS/arvot.png)<br>
_Kuvio 2. YLEn uutisjuttujen arvojen jakauma._

Vaikka arvojen jakauma painottuu vahvasti arvoliberaaliin suuntaan, on pääkirjoitusten joukossa myös arvokonservatiivisesta näkökulmia.

4 Poliittisuus
===

Kirjoitusten näkökulmien on hyvin lievästi vasemmistolainen: keskiarvo on -0,5 asteikolla (-10; 10). Tyypillinen pääkirjoitus taas on maltillisen vasemmistolainen, sillä mediaani on -2. Tämä siis tarkoittaa, että myös pääkirjoitusten joukossa on selvästi oikeistolaisia pääkirjoituksia. Tämä näkyy kuviosta 3.

![YLEn uutisten poliittisuuden jakauma](/images/HS/poliittinen.png)<br>
_Kuvio 3. YLEn uutisjuttujen poliittisuuden jakauma._

Arvojen ja polittiisen näkökulman yhteisjakauma (Kuvio 1) osoittaa että suurin osa uutisjutuista on vasemmisto/arvoliberaali - oikeisto/arvokonservatismi -akselilla. Yhteisjakaumassa on vähän havaintoja oikeisto/arvoliberaali -neljänneksestä tai vasemmisto/arvokonservatiivi -neljänneksestä. Tämä sama ilmiö näkyy vaalien yhteydessä tehdyissä ehdokkaiden arvokartoissa. Myös yhteisjakauma näyttää, että juttujen paino on hyvin neutraali.

5 Esimerkkejä tuloksista
===

Seuraavaksi käyn hieman yksityiskohtaisemmin läpi muutaman jutun. Arvion jälkeen esitetään Clauden perustelut arvostelulle.

5.1 Myllypuro uudistui ja kaikki voittivat – paitsi ennakkoluulot
==

[Myllypuron uudistamisesta kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011292427.html) arvioidaan selvästi arvoliberaaliksi (-6) ja vasemmistolaiseksi (-4).

> Kirjoitus on vasemmistolaisesti painottunut. Se näkee valtion tukemat ara-asunnot positiivisena asiana, korostaa julkisten palveluiden (terveyskeskus, koulut) merkitystä alueen kehityksessä, ja pitää hyvänä että alkuperäiset asukkaat eivät joudu muuttamaan pois gentrifioitumisen vuoksi. Kirjoitus kritisoi markkinaehtoista asumispolitiikkaa epäsuorasti ja puolustaa valtion roolia kaupunkikehityksessä.

> Kirjoitus on vahvasti arvoliberaali. Se vastustaa maahanmuuttoon liittyviä ennakkoluuloja ja stereotypioita, korostaa monimuotoisuuden arvoa, kritisoi perussuomalaisten näkemyksiä islamista ja maahanmuutosta, sekä näkee positiivisena alueen kehittymisen ja asukasrakenteen monipuolistumisen. Kirjoittaja puolustaa suvaitsevaisuutta ja avoimuutta.

5.2 Ilmailun työtaistelu
==
[Ilmailun työtaistelusta kertova pääkirjoitus](https://yle.fi/a/74-20167070) arvioidaan lievästi arvokonservatiiviseksi (+2) ja selvästi oikeistolaisesta näkökulmasta kirjoitetuksi (+5).

> Kirjoitus ei käsittele arvoliberaaleja tai -konservatiivisia teemoja kuten perhearvoja, seksuaalivähemmistöjä, maahanmuuttoa tai muita sosiokulttuurisia kysymyksiä. Teksti keskittyy puhtaasti työmarkkinapolitiikkaan ja talouteen, joten arvoulottuvuuden arviointi on neutraali hieman konservatiivisen sävyisellä tavalla korostaen järjestelmän vakautta.

> Kirjoitus on selkeästi oikeistolaisesta näkökulmasta kirjoitettu. Se: 1) Puolustaa vientimallia ja yleistä linjaa työmarkkinoilla, 2) Kritisoi lakkoja ja niiden aiheuttamia taloudellisia menetyksiä, 3) Korostaa Finnairin tuloksentekoa ja osinkojen maksamista valtiolle, 4) Pitää työntekijöiden vaatimuksia kohtuuttomina ja 'päättöminä', 5) Asettuu työnantajapuolen kannalle korostaen taloudellista vastuullisuutta ja kilpailukykyä.

5.3 Piispat tekivät ison linjauksen samaa sukupuolta olevien vihkimisestä 
==

[Kirkolliskokouksen päätöstä arvioiva pääkirjoitus](https://yle.fi/a/74-20167408) on selvästi arvoliberaali (-6) ja poliittiselta näkökulmaltaan neutraali (0).

> Kirjoitus on kirjoitettu selkeästi arvoliberaalista näkökulmasta. Teksti kuvaa positiivisena kehityksenä piispojen linjauksen olla rankaisematta samaa sukupuolta olevien parien vihkiviä pappeja. Kirjoittaja kutsuu tilannetta 'merkittäväksi askeleeksi' ja pitää ratkaisua 'parhaana tapana' selvittää asia. Hän ei kritisoi yhteiskunnallista muutosta tasa-arvoisen avioliittolain suuntaan, vaan päinvastoin esittää kirkon perinteisen avioliittokäsityksen ja nykytilanteen välisen ristiriidan ongelmallisena ja kirkkoa 'repivänä'. Kirjoittaja rinnastaa myös samaa sukupuolta olevien vihkimisen eronneiden vihkimiseen, vihjaten että kyse on samanlaisesta luonnollisesta kehityksestä.

> Kirjoituksessa ei oteta kantaa taloudellisiin tai muihin perinteisiin vasemmisto-oikeisto -jakolinjoihin. Teksti keskittyy puhtaasti kirkon sisäiseen arvomaailmaan ja avioliittokäsitykseen liittyviin kysymyksiin. Kirjoittaja ei ota kantaa esimerkiksi kirkon ja valtion suhteeseen, kirkon rahoitukseen, työntekijöiden asemaan tai muihin poliittisen vasemmisto-oikeisto -akselin teemoihin. Näkökulma on neutraali suhteessa poliittiseen suuntaukseen.

5.4 Raja railona aukeaa Suomen sisällä
==

[Väestöllisestä painopisteestä kertova pääkirjoitus](https://yle.fi/a/74-20163230) on arvoliberaali (-3) ja maltillisen oikeistolainen (+3).

> Pääkirjoitus vaikuttaa arvoliberaalin näkökulman suuntaan kallistuvan. Siinä hyväksytään Suomen rakennemuutos, globalisaatio ja kansainvälistyminen luonnollisina kehityssuuntina. Vihreä siirtymä mainitaan myönteisenä talouden moottoriena. Perinteinen 'koko Suomi pidettävä asuttuna' -ajatus kyseenalaistetaan rationaalisesti ilman nostalgista kaipuuta.

> Kirjoitus kallistuu hieman oikealle keskiviivasta. Markkinavetoinen kehitys hyväksytään ilman kritiikkiä, ja julkiseen menotalouteen viitataan skeptisesti ('rahaa ei ole'). Aluetukia pidetään tehottomina. Toisaalta kirjoitus ei myöskään tuomitse valtiollista roolia aluepolitiikassa, vaan toteaa realistisesti sen rajoitteet. Näkökulma on lähellä pragmaattista markkinatalouskeskeistä liberalismia.

5.5 Telakka tuo rahaa ja työtä Suomeen
==

Mika Poutalasta kertova [juttu](https://yle.fi/a/74-20162150) arvioidaan arvoneutraaliksi (0) ja poliittisesti neutraaliksi (0).

> Teksti ei käsittele varsinaisia arvopohjaan liittyviä kysymyksiä. Se keskittyy käytännön talousteemoihin kuten työllisyyteen, vientiin ja jalostusarvoon. Maininta Ruotsista viittaa konservatiiviseen argumenttiin asevelvollisuuden ja teollisuuden säilyttämisen puolesta. Kansallisen edun korostaminen viittaa lievästi konservatiiviseen ajatteluun.

> Kirjoitus on selvästi talousnäkökulmasta positiivinen suuryrityksen toimintaa kohtaan. Se kritisoi vihreän siirtymän investointeja tuottavuuden näkökulmasta, mikä on tyypillinen oikeistoargumentti. Valtion tukitoimien kannattaminen työllisyyden edistämiseksi tekee kannanotosta kuitenkin hieman maltillisemman.

6 Yhteenveto
===

Tulosten mukaan HS tunnustaa arvokysymyksissä selvästi väriä: pääkirjoitukset on kirjoitettu vahvasti arvoliberaalista näkökulmasta. Poliittisesti tulos ei ole yhtä selvä, vaikka pääkirjoituksissa painottuu vahvasti maltillinen vasemmistolaisuus. Ehkä Björn Wahlroos oli oikeassa, kun hän haastattelussa kertoi pitävänsä Helsingin Sanomia oikeistodemokraattina.


Liite
===

|    | otsikko                                                                                     | linkki                                                   |   arvot |   poliittinen suuntaus |
|---:|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------|--------:|-----------------------:|
|  0 | Valtio voisi ottaa mallia arkkipiispan anteeksipyynnöstä saamelaisilta                      | https://www.hs.fi/paakirjoitukset/art-2000011303517.html |    -6   |                   -5   |
|  1 | Helsingin uusi silta on veronmaksajalle ilonaihe                                            | https://www.hs.fi/paakirjoitukset/art-2000011309509.html |     0   |                   -2   |
|  2 | Suomalaisten kielitaitoon kuuluvat myös farsi ja tagalog                                    | https://www.hs.fi/paakirjoitukset/art-2000011275924.html |    -6   |                   -3   |
|  3 | Eurooppa seuraa Iranin ja Israelin konfliktia katsomosta                                    | https://www.hs.fi/paakirjoitukset/art-2000011310634.html |     3   |                    0   |
|  4 | Pelttarin tapaus ajaa muuttamaan virkarikoksia koskevia pykäliä                             | https://www.hs.fi/paakirjoitukset/art-2000011307176.html |    -2   |                    0   |
|  5 | Valtiovarainministeriö taloudesta: paremmalta näyttää jo, kunhan ei katso kovin kauas       | https://www.hs.fi/paakirjoitukset/art-2000011304178.html |     0   |                   -3   |
|  6 | Osuuskuntien omistajien kannattaisi terävöityä                                              | https://www.hs.fi/paakirjoitukset/art-2000011303530.html |     0   |                   -2   |
|  7 | Kultarannassa nähtiin, että hopealuodit maailman ongelmiin ovat vähissä                     | https://www.hs.fi/paakirjoitukset/art-2000011304824.html |    -1   |                    1   |
|  8 | Eduskunnan on hyväksyttävä uusi saamelaiskäräjälaki                                         | https://www.hs.fi/paakirjoitukset/art-2000011299499.html |    -5   |                   -3   |
|  9 | Helsingin ydinkeskustasta pitää tehdä viihtyisämpi                                          | https://www.hs.fi/paakirjoitukset/art-2000011298342.html |     1   |                    2   |
| 10 | Myllypuro uudistui ja kaikki voittivat – paitsi ennakkoluulot                               | https://www.hs.fi/paakirjoitukset/art-2000011292427.html |    -6   |                   -4   |
| 11 | Kala olisi kiva ostaa suoraan kalastajalta                                                  | https://www.hs.fi/paakirjoitukset/art-2000011295902.html |   nan   |                  nan   |
| 12 | Talousennustajien tähtäin oli säädetty liian ylös                                           | https://www.hs.fi/paakirjoitukset/art-2000011295704.html |     0   |                    1   |
| 13 | Nyt tai ei koskaan – Israel yrittää estää Iranin ydinaseen                                  | https://www.hs.fi/paakirjoitukset/art-2000011299143.html |    -3   |                   -2   |
| 14 | Perussuomalaiset alkaa valmistautua Purran jälkeiseen aikaan                                | https://www.hs.fi/paakirjoitukset/art-2000011296551.html |    -4   |                   -5   |
| 15 | Lentäjien sopimuksen viivästyminen tuli kalliiksi                                           | https://www.hs.fi/paakirjoitukset/art-2000011295176.html |     2   |                    5   |
| 16 | Veneilijänkin pitää nyt varautua Venäjän häirintään                                         | https://www.hs.fi/paakirjoitukset/art-2000011293354.html |    -2   |                   -2   |
| 17 | Kesäloman juhlat eivät kuulu työnantajalle                                                  | https://www.hs.fi/paakirjoitukset/art-2000011292933.html |    -4   |                   -3   |
| 18 | Suomessa konkurssia hävetään turhaan                                                        | https://www.hs.fi/paakirjoitukset/art-2000011289952.html |    -2   |                    5   |
| 19 | Ääniveturit vetivät yllätysehdokkaita kuntien valtuustoihin                                 | https://www.hs.fi/paakirjoitukset/art-2000011290503.html |     2   |                   -2   |
| 20 | Trump haastaa riitaa Kalifornian kanssa                                                     | https://www.hs.fi/paakirjoitukset/art-2000011288471.html |    -6.5 |                   -4.5 |
| 21 | Suomalaisten ylipaino maksaa ja koskee                                                      | https://www.hs.fi/paakirjoitukset/art-2000011264522.html |    -2   |                    1   |
| 22 | Perusäänestäjä muistuttaa perusehdokasta                                                    | https://www.hs.fi/paakirjoitukset/art-2000011282959.html |    -5   |                   -4   |
| 23 | Hyviä uutisia taloudesta                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011280206.html |    -1   |                    1   |
| 24 | Raja railona aukeaa Suomen sisällä                                                          | https://www.hs.fi/paakirjoitukset/art-2000011279927.html |    -3   |                    3   |
| 25 | Maanpuolustus kuuluu niin naisille kuin miehillekin                                         | https://www.hs.fi/paakirjoitukset/art-2000011283601.html |    -5   |                   -2   |
| 26 | Yliopistojen valintakokeiden hiominen alkaa nyt                                             | https://www.hs.fi/paakirjoitukset/art-2000011281362.html |    -1   |                   -2   |
| 27 | Venäjä valmistelee vielä kostoaan                                                           | https://www.hs.fi/paakirjoitukset/art-2000011283508.html |    -3   |                   -2   |
| 28 | Petteri Orpo on tehnyt sen, mitä kokoomus on pitkään halunnut                               | https://www.hs.fi/paakirjoitukset/art-2000011267971.html |    -3   |                   -2   |
| 29 | Piispat tekivät ison linjauksen samaa sukupuolta olevien vihkimisestä                       | https://www.hs.fi/paakirjoitukset/art-2000011278250.html |    -6   |                    0   |
| 30 | Rajalaissa poikkeuksesta tehtiin uusi normaali                                              | https://www.hs.fi/paakirjoitukset/art-2000011278329.html |    -2.5 |                    1.5 |
| 31 | Suomi sai EU:lta armoviitosen ja välttyi tarkkailuluokalle joutumiselta                     | https://www.hs.fi/paakirjoitukset/art-2000011278493.html |    -1   |                    3   |
| 32 | Ilmailun työtaisteluissa kamppaillaan palkkojen ohella Finnairin ja vientimallin kohtalosta | https://www.hs.fi/paakirjoitukset/art-2000011274686.html |     2   |                    5   |
| 33 | Trumpin uhkaukset ovat muuttuneet pelottavista huvittaviksi                                 | https://www.hs.fi/paakirjoitukset/art-2000011275091.html |    -6   |                   -5   |
| 34 | Telakka tuo rahaa ja työtä Suomeen                                                          | https://www.hs.fi/paakirjoitukset/art-2000011272057.html |     2   |                    4   |
| 35 | Ukrainan iskut pääsevät vielä sotataidon oppikirjoihin                                      | https://www.hs.fi/paakirjoitukset/art-2000011272652.html |     0   |                    3   |
| 36 | Vihreät tyytyvät puolueen kutistumiseen                                                     | https://www.hs.fi/paakirjoitukset/art-2000011263892.html |    -3   |                    2   |
| 37 | Ilman maahanmuuttoa Suomi joutuu kriisiin pitkällä aikavälillä                              | https://www.hs.fi/paakirjoitukset/art-2000011266091.html |    -6   |                   -1   |
| 38 | Puolalla on taas valinnan paikka                                                            | https://www.hs.fi/paakirjoitukset/art-2000011267641.html |    -6   |                   -3   |
| 39 | Suomen on päästävä takaisin jatkuvan kasvun oravanpyörään                                   | https://www.hs.fi/paakirjoitukset/art-2000011267513.html |    -2   |                    4   |