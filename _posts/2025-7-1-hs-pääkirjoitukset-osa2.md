---
title: 'Helsingin Sanomien pääkirjoitusten poliittisuus ja arvot laajemman datan näkökulmasta'
date: 2025-07-01
permalink: /posts/2025/7/paakirjoitukset/
summary: 'Blogi | Helsingin Sanomien pääkirjoituksissa otetaan usein kantaa ajankohtaisiin asioihin. Uutisoinnin neutraaliutta voi analysoida suurilla kielimalleilla. Tässä käytämme Anthropicin Claudea, jonka mukaan HS:n pääkirjoitukset painottuvat vahvasti arvoliberalismia kannattaviksi ja maltillisen vasemmistolaisiksi. Osassa 2 aineistoa on laajennettu ja tarkastuksia lisätty.'
tags:
  - pääkirjoitukset
  - poliittisuus
  - arvot
---

Helsingin Sanomat on arvostettu suomalainen lehti, joka on suorastaan instituutio. Hesari ei ole pelkkää passiivinen asioiden seuraaja, vaan ottaa lehtenä kantaa ajankohtaisiin asioihin. Lehden linjaa esitellään pääkirjoituksissa. [Edellisen blogin](/posts/2025/6/paakirjoitukset/) analysissä arvioitiin, että HS on vahvasti arvoliberaali ja maltillisen vasemmistolainen lehti. Tässä blogissa tarkastellaan tuloksia laajemman aineiston valossa ja uusilla menetelmillä.

![HS:n uutisten poliittisuuden jakauma](/images/HS/jakauma2.png)<br>
_Kuvio 1. HS:n uutisjuttujen poliittisen näkökulman (vaaka-akseli) ja arvojen (pystyakseli) yhteisjakauma. Pystyakselilla alhaalla arvoliberaalius, ylhäällä arvokonservatismi. Vaaka-akselilla vasemmalla vasemmmisto, oikealla oikeisto._

1 Aineisto
===

Helsingin Sanomat kuvaava itse [pääkirjoitusten](https://www.hs.fi/info/art-2000010221266.html) linjaa näin:
> Pääkirjoituksissa määritellään lehden kanta eri asioihin, mutta uutistoimituksen työtä pääkirjoitukset eivät määritä. Niiden linjaukset eivät myöskään poista objektiivisuuden tai tasapuolisuuden vaadetta uutissisällöissä.

Blogin analyysin ei ole tarkoitus olla kattava. Aiemmassa aineistossa oli vain 40 pääkirjoitusta, jotka on kerätty 31.5.2025-20.6.2025 väliltä. Nyt aineistoa on laajennettu 1.1.2025 alkavaksi. Nyt aineistossa on 318 pääkirjoitusta.

Tätäkin laajempi tutkimus pystyisi arvioimaan tätä tutkimusta paremmin, miten HS sijoittuu arvokartalle. Olisi myös kiinnostavaa nähdä, onko HS:n sijainti arvokartalla muuttunut ajan kuluessa.

2 Menetelmä
===

Suurella kielimallilla voi luokitella kirjoituksia erilaisilla perusteilla. Tässä käytetään Anthropicin Claude Opus 4 -mallia.
Lista jutuista ja tulokset löytyy tiiviissä muodossa blogin lopussa.
Promptit, joita analyysissä on käytetty, ovat yksinkertaisia. Mitään muita prompteja ei analyysissä käytetä.

Systeemi-prompti:
> You are an AI assistant tasked with analyzing political biases in works. Your goal is to provide insightful commentary on polical leaning, and liberal/conservative leaning. output in JSON format with keys: \“arvot\” (asteikko (-10,10)), \"poliittinen suuntaus\" (asteikko (-10,10)), \"perustelut arvot\", and \"perustelut poliittinen suuntaus\".\n

Analyysi-prompti:
> Analysoi kirjoitus. Onko se kirjoitettu arvoliberaalista vai arvokonservatiivisesta näkökulmasta? arvioi asteikolla (-10,10). Arvo -10 tarkoittaa hyvin arvoliberaalia, arvo 10 hyvin arvokonservatiivista. Entä onko se kirjoitettu vasemmistolaisesta vai oikeistolaisesta näkökulmasta? arvioi asteikolla (-10,10). Arvo -10 tarkoittaa hyvin vasemmistolaista, arvo 10 hyvin oikeistolaista. Vastaa JSON muodossa. (encode special chars properly)

Promptien tarkoituksena on tuottaa numeerinen arvio kirjoituksen poliittisesta näkökulmasta ja siitä, mitä arvonäkökulmasta juttu on kirjoitettu. Poliittinen näkökulma arvioidaan vasemmisto-oikeisto -akselilla, kun taas kirjoituksen arvot arvioidaan arvoliberaali-konservatiivi -akselilla. Näiden pitäisi vastata esimerkiksi Helsingin Sanomien tekemien arvokarttojen asteikkoja, vaikka metodologia on erilainen.

Jokaista tekstiä varten keskustelu Clauden kanssa avataan uudestaan, jotta aiemmat vastaukset eivät sotke tuloksia. Lämpötila on mallinnuksessa 0, jotta tulokset olisivat mahdollisimman toistettavissa. Clauden vastaukset muuttuvat eri ajokerroilla hieman, vaikka promptit ja aineistot pysyvät samoina. Vaihtelu ei kuitenkaan vaikuta olevan kovin suurta.

3 Arvot
===

Pääkirjoitukset ovat selvästi arvoliberaaleja: keskiarvo on -2,29 (aiemmin -2,4) asteikolla (-10; 10). Tyypillinen pääkirjoitus on sekin selvästi arvoliberaali, sillä mediaani on -2 (aiemmin -2).
Tämä lienee odotettua, koska HS on jo aikoinaan perustettu kannattamaan liberaaleja arvoja.

![HS:n pääkirjoitusten arvojen jakauma](/images/HS/arvot2.png)<br>
_Kuvio 2. HS:n pääkirjoitusten arvojen jakauma._

Tulokset eivät juuri muuttuneet, vaikka aineisto kasvoi 40:stä pääkirjoituksesta 318:sta.

![HS:n pääkirjoitusten arvojen aikajakauma](/images/HS/arvot_ts.png)<br>
_Kuvio 3. HS:n pääkirjoitusten arvojen aikajakauma._

Vaikka arvojen jakauma painottuu vahvasti arvoliberaaliin suuntaan, on pääkirjoitusten joukossa myös arvokonservatiivisesta näkökulmia.

4 Poliittisuus
===

Kirjoitusten näkökulmien on hyvin lievästi vasemmistolainen: keskiarvo on -1,11 (aiemmin -0,23) asteikolla (-10; 10). Tyypillinen pääkirjoitus taas on maltillisen vasemmistolainen, sillä mediaani on -2 (aiemmin -1). Ero mediaanin ja keskiarvon välillä selittyy sillä, että pääkirjoitusten joukossa on myös selvästi oikeistolaisia pääkirjoituksia. Tämä näkyy kuviosta 3.

![HS:n pääkirjoitusten poliittisuuden jakauma](/images/HS/poliittinen2.png)<br>
_Kuvio 4. HS:n pääkirjoitusten poliittisen näkökulman jakauma._

![HS:n pääkirjoitusten arvojen aikajakauma](/images/HS/poliittinen_ts.png)<br>
_Kuvio 5. HS:n pääkirjoitusten poliittisen näkökulman aikajakauma._

Arvojen ja polittiisen näkökulman yhteisjakauma (Kuvio 1) osoittaa että suuri huippu uutisjuttuille on arvoliberaalissa vasemmistossa. 
Kiinnostavasti jakaumalla on kaksi huippu, joista toinen sijoittuu "arvoneutraaliin" oikeistoon. Jakauman paino on selvästi arvolilberaalissa vasemmistossa.

Jos vertaa yhteisjakaumaa [Hesarin puolueiden arvokarttaan](https://www.hs.fi/politiikka/art-2000010457779.html), näkee, että yhteisjakauman kaksi huippua vastaavat
parhaiten SDP:tä ja Keskustaa. Myös Kokoomus on lähellä oikeisto-huippua.

5 Esimerkkejä tuloksista
===

Seuraavaksi käyn hieman yksityiskohtaisemmin läpi Clauden arviot muutamasta pääkirjoituksesta. Mukana on myös vertailu aiempaan arvioon, joka näyttää, missä määrin tulokset muuttuvat eri ajokerroilla. Muutokset vaikuttavat olevan suurempi arvonäkökulmassa kuin poliittisessa katsantokannassa.

5.1 Myllypuro uudistui ja kaikki voittivat – paitsi ennakkoluulot
==

[Myllypuron uudistamisesta kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011292427.html) arvioidaan selvästi arvoliberaaliksi -6 (aiemmin -6) ja vasemmistolaiseksi -4 (aiemmin -4).

> Kirjoituksessa on maltillisia vasemmistolaisia piirteitä. Se puolustaa valtion tukemaa asuntorakentamista (ARA-järjestelmä) ja näkee sen positiivisena tekijänä alueen kehityksessä. Vuokrasäännöstely esitetään hyvänä asiana, joka suojeli alkuperäisiä asukkaita. Kirjoitus kritisoi markkinaehtoista asumispolitiikkaa epäsuorasti ja korostaa julkisen sektorin roolia aluekehityksessä.

> Kirjoitus on selkeästi arvoliberaali. Se kritisoi maahanmuuttovastaisuutta ja stereotypioita, puolustaa monimuotoisuutta ja monikulttuurisuutta positiivisena asiana. Erityisesti perussuomalaisten edustajan kommentti 'minareeteista ja sharia-laista' esitetään negatiivisessa valossa. Kirjoitus korostaa Itä-Helsingin monimuotoisuutta ja torjuu ennakkoluuloja.

5.2 Ilmailun työtaistelu
==
[Ilmailun työtaistelusta kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011274686.html) arvioidaan lievästi arvokonservatiiviseksi +3 (aiemmin +2) ja selvästi oikeistolaisesta näkökulmasta kirjoitetuksi +6 (aiemmin +5).

> Kirjoitus ei käsittele varsinaisia arvokonservatiivisia tai -liberaaleja teemoja kuten perhearvojen, uskonnon, seksuaalivähemmistöjen oikeuksien tai maahanmuuton kysymyksiä. Se keskittyy työmarkkinapolitiikkaan ja taloudellisiin kysymyksiin. Lievä konservatiivinen sävy tulee esiin siinä, että kirjoittaja puolustaa olemassa olevia rakenteita (vientimalli, sovittelujärjestelmä) ja vastustaa niiden muuttamista.

> Kirjoitus on selvästi oikeistolainen. Se puolustaa työnantajien näkökulmaa, kritisoi ammattiliittojen lakkoja ja korostaa yrityksen (Finnair) taloudellisia menetyksiä. Kirjoittaja pitää työntekijöiden palkankorotusvaatimuksia kohtuuttomina ja 'päättöminä'. Vientimallin puolustaminen on myös tyypillisesti oikeistolainen kanta. Kirjoitus korostaa taloudellista vastuullisuutta ja kilpailukykyä työntekijöiden oikeuksien sijaan.

5.3 Piispat tekivät ison linjauksen samaa sukupuolta olevien vihkimisestä 
==

[Kirkolliskokouksen päätöstä arvioiva pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011278250.html) on selvästi arvoliberaali -6 (aiemmin -6) ja poliittiselta lievästi vasemmistolainen -2 (aiemmin -2).

> Kirjoitus on kirjoitettu selkeästi arvoliberaalista näkökulmasta. Teksti kuvaa positiivisena kehityksenä piispojen linjauksen olla rankaisematta samaa sukupuolta olevien parien vihkiviä pappeja. Kirjoittaja kutsuu tilannetta 'merkittäväksi askeleeksi' ja pitää ratkaisua 'parhaana tapana' selvittää asia. Hän ei kritisoi yhteiskunnallista muutosta tasa-arvoisen avioliittolain suuntaan, vaan päinvastoin esittää kirkon perinteisen avioliittokäsityksen ja nykytilanteen välisen ristiriidan ongelmallisena ja kirkkoa 'repivänä'. Kirjoittaja rinnastaa myös samaa sukupuolta olevien vihkimisen eronneiden vihkimiseen, vihjaten että kyse on samanlaisesta luonnollisesta kehityksestä.

> Kirjoituksessa ei oteta kantaa taloudellisiin tai muihin perinteisiin vasemmisto-oikeisto -jakolinjoihin. Teksti keskittyy puhtaasti kirkon sisäiseen arvomaailmaan ja avioliittokäsitykseen liittyviin kysymyksiin. Kirjoittaja ei ota kantaa esimerkiksi kirkon ja valtion suhteeseen, kirkon rahoitukseen, työntekijöiden asemaan tai muihin poliittisen vasemmisto-oikeisto -akselin teemoihin. Näkökulma on neutraali suhteessa poliittiseen suuntaukseen.

5.4 Raja railona aukeaa Suomen sisällä
==

[Väestöllisestä painopisteestä kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011279927.html) on maltillisen arvoliberaali -2(aiemmin maltillisen arvokonservatiivinen +2) ja maltillisen oikeistolainen +3 (aiemmin +4).

> Kirjoitus on lievästi arvokonservatiivinen. Se hyväksyy väestön keskittymisen ja alueellisen eriarvoisuuden luonnollisena kehityksenä, eikä kyseenalaista markkinavetoista kehitystä. Toisaalta se ei sisällä vahvoja arvokonservatiivisia teemoja kuten perinteiden tai yhteisöllisyyden korostamista.

> Kirjoitus on selkeästi oikeistolainen. Se kritisoi aluepolitiikkaa ja julkisten varojen käyttöä alueellisten erojen tasaamiseen, korostaa taloudellista realismia ja markkinoiden roolia. Erityisen paljastava on lause 'Eikä Weberin pistettä saa edes nykymaailmassa peruuttamaan rahalla työntämällä', joka viittaa markkinatalouden ylivoimaan valtiolliseen ohjaukseen nähden.

5.5 Telakka tuo rahaa ja työtä Suomeen
==
[Telakasta kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011272057.html) arvioidaan arvokonservatiiviseksi +3 (aiemmin arvoneutraali 0) ja poliittisesti oikeistolaiseksi +3 (aiemmin +3).

> Kirjoitus ei käsittele arvoliberaaleja tai arvokonservatiivisia teemoja kuten ihmisoikeuksia, tasa-arvoa, perinteisiä arvoja tai yhteiskunnallisia normeja. Se keskittyy puhtaasti taloudellisiin ja elinkeinopoliittisiin kysymyksiin, joten arvoulottuvuudella ei ole merkitystä tässä tekstissä.

> Kirjoitus kallistuu lievästi oikealle useista syistä: 1) Se korostaa yksityisen sektorin investointien ja viennin merkitystä talouskasvulle, 2) Kritisoi implisiittisesti vihreän siirtymän investointeja niiden vähäisen työllistävyyden vuoksi, 3) Kehuu telakkateollisuuden säilyttämistä markkinatalouden näkökulmasta, 4) Mainitsee valtion takausvastuut myönteisessä valossa nimenomaan siksi, että ne tukevat yksityistä liiketoimintaa. Toisaalta kirjoitus ei ole voimakkaan oikeistolainen, sillä se hyväksyy valtion roolin talouden tukijana.


6 Yhteenveto
===

Tulosten mukaan Helsingin Sanomat tunnustaa arvokysymyksissä selvästi väriä: pääkirjoitukset on kirjoitettu vahvasti arvoliberaalista näkökulmasta. Tätä ei ehkä voi pitää yllättävänä, koska Hesarin tausta on liberaalissa nuorsuomalaisessa liikkeessä.

Poliittisesti tulos ei ole yhtä selvä, vaikka pääkirjoituksissa painottuu lievä vasemmistolaisuus. Tyypillisin näkökulma on maltillinen vasemmmistolaisuus, mutta mukana on myös oikeistolaisia näkökulmia. Jyrkkää oikeistolaista tai jyrkkää vasemmistolaista näkökulmaa pääkirjoituksissa ei oteta.
Ehkä tulokset voi summata niin, että Hesari on jonkinlainen arvoliberaali oikeistososialidemokraatti. 


Liite
===

|     | otsikko                                                                                                        | linkki                                                   |   arvot |   poliittinen suuntaus |
|----:|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|--------:|-----------------------:|
|   0 | Helsinkiin valitaan tuomio­rovastia riitaisasti                                                                | https://www.hs.fi/paakirjoitukset/art-2000011317782.html |      -2 |                      0 |
|   1 | Naton uusi puolustus­meno­tavoite syntyi painekattilassa                                                       | https://www.hs.fi/paakirjoitukset/art-2000011316598.html |      -2 |                      0 |
|   2 | Lähi-itään ei viedä varmuutta ja vakautta pommikoneilla                                                        | https://www.hs.fi/paakirjoitukset/art-2000011317016.html |      -3 |                     -4 |
|   3 | Trumpin isku Iraniin käänsi sivua maailmanpolitiikassa                                                         | https://www.hs.fi/paakirjoitukset/art-2000011315938.html |      -2 |                     -3 |
|   4 | EU:n tulee katkoa energiasidoksiaan Venäjään                                                                   | https://www.hs.fi/paakirjoitukset/art-2000011306713.html |      -3 |                      0 |
|   5 | Trump teki uransa tärkeimmän päätöksen                                                                         | https://www.hs.fi/paakirjoitukset/art-2000011315894.html |      -2 |                     -3 |
|   6 | Teknologiayhtiöt juoksevat yliopistoihin kilpaa                                                                | https://www.hs.fi/paakirjoitukset/art-2000011306511.html |      -2 |                     -3 |
|   7 | Valtio voisi ottaa mallia arkkipiispan anteeksipyynnöstä saamelaisilta                                         | https://www.hs.fi/paakirjoitukset/art-2000011303517.html |      -6 |                     -5 |
|   8 | Suomalaisten kielitaitoon kuuluvat myös farsi ja tagalog                                                       | https://www.hs.fi/paakirjoitukset/art-2000011275924.html |      -4 |                     -2 |
|   9 | Eurooppa seuraa Iranin ja Israelin konfliktia katsomosta                                                       | https://www.hs.fi/paakirjoitukset/art-2000011310634.html |      -2 |                      1 |
|  10 | Pelttarin tapaus ajaa muuttamaan virkarikoksia koskevia pykäliä                                                | https://www.hs.fi/paakirjoitukset/art-2000011307176.html |      -2 |                      0 |
|  11 | Valtiovarainministeriö taloudesta: paremmalta näyttää jo, kunhan ei katso kovin kauas                          | https://www.hs.fi/paakirjoitukset/art-2000011304178.html |       0 |                     -3 |
|  12 | Osuuskuntien omistajien kannattaisi terävöityä                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011303530.html |       0 |                      2 |
|  13 | Kultarannassa nähtiin, että hopealuodit maailman ongelmiin ovat vähissä                                        | https://www.hs.fi/paakirjoitukset/art-2000011304824.html |      -2 |                      1 |
|  14 | Eduskunnan on hyväksyttävä uusi saamelaiskäräjälaki                                                            | https://www.hs.fi/paakirjoitukset/art-2000011299499.html |      -6 |                     -3 |
|  15 | Helsingin ydinkeskustasta pitää tehdä viihtyisämpi                                                             | https://www.hs.fi/paakirjoitukset/art-2000011298342.html |      -2 |                      3 |
|  16 | Myllypuro uudistui ja kaikki voittivat – paitsi ennakkoluulot                                                  | https://www.hs.fi/paakirjoitukset/art-2000011292427.html |      -6 |                     -4 |
|  17 | Kala olisi kiva ostaa suoraan kalastajalta                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011295902.html |      -2 |                     -1 |
|  18 | Talousennustajien tähtäin oli säädetty liian ylös                                                              | https://www.hs.fi/paakirjoitukset/art-2000011295704.html |       0 |                      2 |
|  19 | Nyt tai ei koskaan – Israel yrittää estää Iranin ydinaseen                                                     | https://www.hs.fi/paakirjoitukset/art-2000011299143.html |       2 |                      3 |
|  20 | Perussuomalaiset alkaa valmistautua Purran jälkeiseen aikaan                                                   | https://www.hs.fi/paakirjoitukset/art-2000011296551.html |      -3 |                     -4 |
|  21 | Lentäjien sopimuksen viivästyminen tuli kalliiksi                                                              | https://www.hs.fi/paakirjoitukset/art-2000011295176.html |       0 |                      5 |
|  22 | Veneilijänkin pitää nyt varautua Venäjän häirintään                                                            | https://www.hs.fi/paakirjoitukset/art-2000011293354.html |      -2 |                     -1 |
|  23 | Kesäloman juhlat eivät kuulu työnantajalle                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011292933.html |      -5 |                     -4 |
|  24 | Suomessa konkurssia hävetään turhaan                                                                           | https://www.hs.fi/paakirjoitukset/art-2000011289952.html |       2 |                      7 |
|  25 | Ääniveturit vetivät yllätysehdokkaita kuntien valtuustoihin                                                    | https://www.hs.fi/paakirjoitukset/art-2000011290503.html |      -2 |                      0 |
|  26 | Trump haastaa riitaa Kalifornian kanssa                                                                        | https://www.hs.fi/paakirjoitukset/art-2000011288471.html |      -6 |                     -5 |
|  27 | Suomalaisten ylipaino maksaa ja koskee                                                                         | https://www.hs.fi/paakirjoitukset/art-2000011264522.html |      -2 |                      2 |
|  28 | Perusäänestäjä muistuttaa perusehdokasta                                                                       | https://www.hs.fi/paakirjoitukset/art-2000011282959.html |      -4 |                     -3 |
|  29 | Raja railona aukeaa Suomen sisällä                                                                             | https://www.hs.fi/paakirjoitukset/art-2000011279927.html |      -2 |                      3 |
|  30 | Maanpuolustus kuuluu niin naisille kuin miehillekin                                                            | https://www.hs.fi/paakirjoitukset/art-2000011283601.html |      -2 |                      3 |
|  31 | Yliopistojen valintakokeiden hiominen alkaa nyt                                                                | https://www.hs.fi/paakirjoitukset/art-2000011281362.html |      -3 |                     -2 |
|  32 | Venäjä valmistelee vielä kostoaan                                                                              | https://www.hs.fi/paakirjoitukset/art-2000011283508.html |      -3 |                     -2 |
|  33 | Petteri Orpo on tehnyt sen, mitä kokoomus on pitkään halunnut                                                  | https://www.hs.fi/paakirjoitukset/art-2000011267971.html |      -3 |                     -4 |
|  34 | Piispat tekivät ison linjauksen samaa sukupuolta olevien vihkimisestä                                          | https://www.hs.fi/paakirjoitukset/art-2000011278250.html |      -6 |                     -2 |
|  35 | Rajalaissa poikkeuksesta tehtiin uusi normaali                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011278329.html |      -3 |                     -2 |
|  36 | Suomi sai EU:lta armoviitosen ja välttyi tarkkailuluokalle joutumiselta                                        | https://www.hs.fi/paakirjoitukset/art-2000011278493.html |       2 |                      4 |
|  37 | Ilmailun työtaisteluissa kamppaillaan palkkojen ohella Finnairin ja vientimallin kohtalosta                    | https://www.hs.fi/paakirjoitukset/art-2000011274686.html |       3 |                      6 |
|  38 | Trumpin uhkaukset ovat muuttuneet pelottavista huvittaviksi                                                    | https://www.hs.fi/paakirjoitukset/art-2000011275091.html |      -3 |                     -2 |
|  39 | Telakka tuo rahaa ja työtä Suomeen                                                                             | https://www.hs.fi/paakirjoitukset/art-2000011272057.html |       3 |                      5 |
|  40 | Ukrainan iskut pääsevät vielä sotataidon oppikirjoihin                                                         | https://www.hs.fi/paakirjoitukset/art-2000011272652.html |      -2 |                      1 |
|  41 | Vihreät tyytyvät puolueen kutistumiseen                                                                        | https://www.hs.fi/paakirjoitukset/art-2000011263892.html |      -3 |                      2 |
|  42 | Ilman maahanmuuttoa Suomi joutuu kriisiin pitkällä aikavälillä                                                 | https://www.hs.fi/paakirjoitukset/art-2000011266091.html |      -6 |                     -3 |
|  43 | Puolalla on taas valinnan paikka                                                                               | https://www.hs.fi/paakirjoitukset/art-2000011267641.html |      -5 |                     -3 |
|  44 | Suomen on päästävä takaisin jatkuvan kasvun oravanpyörään                                                      | https://www.hs.fi/paakirjoitukset/art-2000011267513.html |       2 |                      6 |
|  45 | Upea Sibelius-kilpailu vältti boikottikohun                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011267046.html |      -2 |                      0 |
|  46 | Trumpin tullipäätökset ovat ymmärrettäviä – jos haluaa maksimitehon minimiesteillä                             | https://www.hs.fi/paakirjoitukset/art-2000011263587.html |      -5 |                     -3 |
|  47 | Finnairia suojelee sen poikkeuksellinen asema tuulisina aikoina                                                | https://www.hs.fi/paakirjoitukset/art-2000011261940.html |       2 |                      4 |
|  48 | Sormen heristys Unkarille ei enää riitä                                                                        | https://www.hs.fi/paakirjoitukset/art-2000011261613.html |      -8 |                     -3 |
|  49 | Myös ammattikoululaiset tarvitsevat sivistystä                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011258662.html |      -3 |                     -4 |
|  50 | Merzin Saksa ei välttämättä yllätä vain positiivisesti                                                         | https://www.hs.fi/paakirjoitukset/art-2000011258174.html |       2 |                      3 |
|  51 | Poliisin valta kasvaa, mutta julkinen kontrolli vähenee                                                        | https://www.hs.fi/paakirjoitukset/art-2000011253334.html |      -6 |                     -4 |
|  52 | Yhteisvelka nosti Suomessa heti syljen suuhun                                                                  | https://www.hs.fi/paakirjoitukset/art-2000011250543.html |      -2 |                     -3 |
|  53 | Raha tulee armeijan luokse                                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011246476.html |       0 |                      2 |
|  54 | Juomatavat muuttuvat, alkoholipolitiikka ei                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011250467.html |      -6 |                      5 |
|  55 | Israelin tukijoilta loppuu ymmärrys Gazan tuhoamiselle                                                         | https://www.hs.fi/paakirjoitukset/art-2000011250695.html |      -6 |                     -5 |
|  56 | Rovaniemen hävittäjä­onnettomuus paljasti karusti Ilma­voimien Hornet-viestinnän riskit                        | https://www.hs.fi/paakirjoitukset/art-2000011245329.html |      -2 |                     -1 |
|  57 | Antti Pelttarin tulee siirtyä sivuun                                                                           | https://www.hs.fi/paakirjoitukset/art-2000011252442.html |       3 |                      0 |
|  58 | Jos isoa virhettä pienentää, se ei ole suuren suuri voitto                                                     | https://www.hs.fi/paakirjoitukset/art-2000011248169.html |      -3 |                     -4 |
|  59 | Hallituspuolueiden Gaza-kiista tuo arvoerot pintaan                                                            | https://www.hs.fi/paakirjoitukset/art-2000011248479.html |      -4 |                     -2 |
|  60 | Hallituksen talouspäätökset olivat taivaan lahja oppositiolle                                                  | https://www.hs.fi/paakirjoitukset/art-2000011246780.html |       0 |                     -3 |
|  61 | Itä-Euroopan EU-vastainen aalto laskee                                                                         | https://www.hs.fi/paakirjoitukset/art-2000011245749.html |      -6 |                     -4 |
|  62 | Pikajuna Eurooppaan kulkisi Tornion eikä Turun kautta                                                          | https://www.hs.fi/paakirjoitukset/art-2000011242831.html |      -2 |                     -3 |
|  63 | Trump raivostui rocktähden kriittisistä puheista                                                               | https://www.hs.fi/paakirjoitukset/art-2000011243364.html |      -5 |                     -4 |
|  64 | Nuoret täytyy vapauttaa eläintarhasta yhteiskuntaan                                                            | https://www.hs.fi/paakirjoitukset/art-2000011234534.html |      -6 |                     -4 |
|  65 | Eläkeraha muuttaa pois suomalaisista kiinteistöistä                                                            | https://www.hs.fi/paakirjoitukset/art-2000011237604.html |       0 |                      3 |
|  66 | Pääkaupunkiseudun ja maisterien työllisyysetu hiipuu                                                           | https://www.hs.fi/paakirjoitukset/art-2000011232250.html |       0 |                     -2 |
|  67 | Ammattiliitot voivat joutua ”palavalle lautalle”                                                               | https://www.hs.fi/paakirjoitukset/art-2000011234604.html |      -2 |                     -6 |
|  68 | Eurooppa tanssii nyt suomalaisten tahdissa                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011237641.html |      -3 |                      0 |
|  69 | Valtionhoitaja Lipponen ei hymysuin hyreksi                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011235441.html |      -2 |                      1 |
|  70 | Putin ei usko, että Trumpin pokka pitää                                                                        | https://www.hs.fi/paakirjoitukset/art-2000011234483.html |      -3 |                     -2 |
|  71 | Veronkevennysten dynaaminen vaikutus jäi viimeksi tulematta – onko kaikki tällä kertaa toisin?                 | https://www.hs.fi/paakirjoitukset/art-2000011229524.html |      -2 |                     -4 |
|  72 | Trump saa Nato-mailta ylävitosen                                                                               | https://www.hs.fi/paakirjoitukset/art-2000011231912.html |       2 |                      4 |
|  73 | Jo riittää, Israel!                                                                                            | https://www.hs.fi/paakirjoitukset/art-2000011228661.html |      -6 |                     -5 |
|  74 | Datakeskuksille tarvitaan selvät ja avoimet pelisäännöt                                                        | https://www.hs.fi/paakirjoitukset/art-2000011226480.html |      -2 |                      1 |
|  75 | Ei sähköpyörä tapa, vaan vauhti                                                                                | https://www.hs.fi/paakirjoitukset/art-2000011226811.html |      -3 |                     -2 |
|  76 | Sosiaaliturvan uudistus alkaa työttömien tuista                                                                | https://www.hs.fi/paakirjoitukset/art-2000011222882.html |      -2 |                     -3 |
|  77 | Lentäjille tuli sopu, joka ei ole sopu                                                                         | https://www.hs.fi/paakirjoitukset/art-2000011221559.html |       3 |                      6 |
|  78 | Kriisialueiden äidit maksavat kehitysavun alasajon                                                             | https://www.hs.fi/paakirjoitukset/art-2000011221577.html |      -7 |                     -6 |
|  79 | Suomalainen ei uskalla kuluttaa, koska maailma pelottaa                                                        | https://www.hs.fi/paakirjoitukset/art-2000011213744.html |      -2 |                     -3 |
|  80 | Paavi Leon pitäisi löytää kirkolleen polku eteenpäin                                                           | https://www.hs.fi/paakirjoitukset/art-2000011222058.html |      -3 |                     -4 |
|  81 | Perussuomalaisten nahka paloi kokoomuksen löylyissä                                                            | https://www.hs.fi/paakirjoitukset/art-2000011222633.html |      -3 |                     -4 |
|  82 | Eurooppa voisi uskoa enemmän itseensä                                                                          | https://www.hs.fi/paakirjoitukset/art-2000011212207.html |      -4 |                     -2 |
|  83 | Trump tukee amerikkalaista yritystä kuin köysi hirtettyä                                                       | https://www.hs.fi/paakirjoitukset/art-2000011217828.html |      -2 |                     -3 |
|  84 | Intia ja Pakistan näyttävät, mistä tulevaisuudessa soditaan                                                    | https://www.hs.fi/paakirjoitukset/art-2000011216205.html |      -2 |                      0 |
|  85 | Hajautettua mallia haettiin, keskitetty saatiin                                                                | https://www.hs.fi/paakirjoitukset/art-2000011216302.html |      -2 |                     -6 |
|  86 | Jauhelihapula on monen tekijän summa, eikä ongelma ratkea nopeasti                                             | https://www.hs.fi/paakirjoitukset/art-2000011212146.html |       0 |                      3 |
|  87 | Talouskuri joustaa, kun EU nostaa puolustusmenoja                                                              | https://www.hs.fi/paakirjoitukset/art-2000011214726.html |       0 |                      3 |
|  88 | Äärioikeistolainen AfD on Saksan uudelle hallitukselle myös ulkopoliittinen ongelma                            | https://www.hs.fi/paakirjoitukset/art-2000011210861.html |      -3 |                     -2 |
|  89 | Yleinen linja kelpasi – paitsi siellä, missä siihen ei ole varaa                                               | https://www.hs.fi/paakirjoitukset/art-2000011211358.html |       0 |                      4 |
|  90 | Trump sysäsi liikkeelle puheet Euroopan omasta ydinpelotteesta                                                 | https://www.hs.fi/paakirjoitukset/art-2000011197184.html |       2 |                      3 |
|  91 | Valtionhallinnon laihdutuskuuri sai jatkoa kehysriihessä                                                       | https://www.hs.fi/paakirjoitukset/art-2000011206662.html |      -2 |                     -3 |
|  92 | Trumpille alkaa nousta vastavoima                                                                              | https://www.hs.fi/paakirjoitukset/art-2000011200364.html |      -7 |                     -4 |
|  93 | Elon Musk ryvetti Teslan brändin – raikas muuttui tunkkaiseksi                                                 | https://www.hs.fi/paakirjoitukset/art-2000011205781.html |      -3 |                     -2 |
|  94 | Työeläkkeisiin kertyy satoja miljardeja, mutta nuoret eivät usko niiden olevan heitä varten                    | https://www.hs.fi/paakirjoitukset/art-2000011202395.html |      -3 |                     -2 |
|  95 | Kreml aliarvioi Ukrainan jälleen kerran                                                                        | https://www.hs.fi/paakirjoitukset/art-2000011205686.html |      -3 |                      3 |
|  96 | Viinien tulo ruokakauppaan lähenee askel kerrallaan                                                            | https://www.hs.fi/paakirjoitukset/art-2000011202665.html |       3 |                      4 |
|  97 | Työmarkkinoiden vappu sujuu riitelyn merkeissä                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011202578.html |       0 |                     -3 |
|  98 | Veroale velkaannuttaa varmasti, kasvu tulee myöhemmin – jos tulee                                              | https://www.hs.fi/paakirjoitukset/art-2000011202635.html |       0 |                     -3 |
|  99 | Espanjan sähkökatko antoi arvokkaan opetuksen                                                                  | https://www.hs.fi/paakirjoitukset/art-2000011199637.html |       2 |                      3 |
| 100 | Kansa kaipaa majakkaa, ja presidentti Stubb vastaa toiveeseen melko hyvin                                      | https://www.hs.fi/paakirjoitukset/art-2000011199728.html |       0 |                      1 |
| 101 | Keskustan virkoaminen avasi pohdinnat hallituspohjasta                                                         | https://www.hs.fi/paakirjoitukset/art-2000011197789.html |       0 |                      1 |
| 102 | Keltamustassa kiekkokeväässä purkautuvat suuret tunteet                                                        | https://www.hs.fi/paakirjoitukset/art-2000011197722.html |      -2 |                     -1 |
| 103 | Donald Trump taistelee kelloa vastaan, kun suosio hiipuu jo                                                    | https://www.hs.fi/paakirjoitukset/art-2000011191787.html |      -5 |                     -3 |
| 104 | Iranin ydinasetta yritetään estää uudella sopimuksella                                                         | https://www.hs.fi/paakirjoitukset/art-2000011186020.html |      -2 |                      1 |
| 105 | Hallitus on joko rohkea tai tyhmänrohkea                                                                       | https://www.hs.fi/paakirjoitukset/art-2000011189942.html |       0 |                      2 |
| 106 | Vaatteet eivät olekaan enää käytettyjä vaan ennalta rakastettuja                                               | https://www.hs.fi/paakirjoitukset/art-2000011191521.html |      -3 |                     -2 |
| 107 | Trump nielaisi Putinin Krim-syötin                                                                             | https://www.hs.fi/paakirjoitukset/art-2000011191456.html |      -5 |                     -3 |
| 108 | Hyvätuloista on helpompi auttaa kuin maahan tulevaa                                                            | https://www.hs.fi/paakirjoitukset/art-2000011191240.html |      -5 |                     -4 |
| 109 | Hallitus teki äkkikäännöksen talouspolitiikassaan                                                              | https://www.hs.fi/paakirjoitukset/art-2000011189440.html |       0 |                     -4 |
| 110 | Suomalaiset eivät luota Trumpiin eivätkä omien päättäjien viisauteen                                           | https://www.hs.fi/paakirjoitukset/art-2000011189321.html |      -3 |                     -2 |
| 111 | Trump huiskii rahapolitiikkaa kirveellä – isku lipeää dollarin kylkeen                                         | https://www.hs.fi/paakirjoitukset/art-2000011187326.html |      -3 |                     -2 |
| 112 | Trump pesee käsiään Ukrainan rauhanneuvotteluista                                                              | https://www.hs.fi/paakirjoitukset/art-2000011186003.html |      -3 |                     -2 |
| 113 | Oikeusvaltion vahvistaminen koskee myös Suomea                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011184312.html |      -6 |                     -3 |
| 114 | Paavi Franciscus oli hengen vallankumouksellinen                                                               | https://www.hs.fi/paakirjoitukset/art-2000011184621.html |      -3 |                     -5 |
| 115 | Suomi tarvitsee lisää softaa rajalle                                                                           | https://www.hs.fi/paakirjoitukset/art-2000011153542.html |      -2 |                      4 |
| 116 | Trumpin tullit toivat sumun hallituksen kehysriiheen                                                           | https://www.hs.fi/paakirjoitukset/art-2000011177019.html |      -1 |                     -2 |
| 117 | Murron raportilta odotettiin paljon, mutta politiikka tuli väliin                                              | https://www.hs.fi/paakirjoitukset/art-2000011159765.html |      -3 |                     -2 |
| 118 | Onko Darth Vader Yhdysvaltojen uusi esikuva?                                                                   | https://www.hs.fi/paakirjoitukset/art-2000011174736.html |      -6 |                     -4 |
| 119 | Suomi on lähimpänä maanpäällistä taivasta                                                                      | https://www.hs.fi/paakirjoitukset/art-2000011162757.html |       2 |                     -2 |
| 120 | Pääsiäisen tulitauko vaihtui Venäjän sotauhoon                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011176477.html |       0 |                      2 |
| 121 | Tarjouskahvin metsästyksestä tuli pääsiäisen kansanhuvi                                                        | https://www.hs.fi/paakirjoitukset/art-2000011175190.html |      -1 |                      0 |
| 122 | Kaksoisvaalien ideaa ei pidä pilata huonoilla järjestelyillä                                                   | https://www.hs.fi/paakirjoitukset/art-2000011175169.html |      -2 |                     -1 |
| 123 | Perussuomalaiset hakevat riitaa ilmastolaista paikatakseen vaalitappiota                                       | https://www.hs.fi/paakirjoitukset/art-2000011174935.html |      -5 |                     -3 |
| 124 | Trumpin hyökkäys kuristaa Yhdysvaltojen yliopistoja                                                            | https://www.hs.fi/paakirjoitukset/art-2000011169915.html |      -7 |                     -5 |
| 125 | Uuteen komentoon siirtyvä Saksa muuttaa suhdettaan niin velkaan kuin sotaankin                                 | https://www.hs.fi/paakirjoitukset/art-2000011168073.html |       2 |                      3 |
| 126 | Sdp:n menestys nosti maahanmuuttajia valtuustoihin                                                             | https://www.hs.fi/paakirjoitukset/art-2000011172257.html |      -5 |                     -3 |
| 127 | Asunnottomuuden piti olla historiaa, mutta nyt sen riski kasvaa myös työssä käyvillä                           | https://www.hs.fi/paakirjoitukset/art-2000011168252.html |      -5 |                     -7 |
| 128 | Vaalitulos tietää hallitukselle vaikeaa loppukautta                                                            | https://www.hs.fi/paakirjoitukset/art-2000011169424.html |      -2 |                     -3 |
| 129 | Sdp:n nousu sähköisti Helsingin kuntavaalit                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011163035.html |      -3 |                     -4 |
| 130 | Vaisuista vaaleista lähti tylyt terveiset hallituspuolueille                                                   | https://www.hs.fi/paakirjoitukset/art-2000011166467.html |      -2 |                     -3 |
| 131 | Vaaleissa äänestetään myös paremman politiikan puolesta – tässä muutama ehdotus, miten se onnistuu             | https://www.hs.fi/paakirjoitukset/art-2000011156392.html |      -3 |                     -2 |
| 132 | Ukraina voi jäädä hyvin nopeasti Euroopan tuen varaan                                                          | https://www.hs.fi/paakirjoitukset/art-2000011159284.html |      -3 |                     -2 |
| 133 | Vaalien alla puolueet yrittävät silmän­kääntö­temppuja                                                         | https://www.hs.fi/paakirjoitukset/art-2000011161871.html |      -2 |                     -3 |
| 134 | Ihminen onkin äkkiä liian vanha työelämään, kallispalkkainen ja muutenkin hankala                              | https://www.hs.fi/paakirjoitukset/art-2000011159388.html |      -3 |                     -4 |
| 135 | Hyvien oppilaiden pako ei ole ratkaisu koulutyön ongelmiin                                                     | https://www.hs.fi/paakirjoitukset/art-2000011159145.html |      -3 |                     -4 |
| 136 | Espoo haluaa kasvaa puolen miljoonan kaupungiksi                                                               | https://www.hs.fi/paakirjoitukset/art-2000011156796.html |      -3 |                     -2 |
| 137 | Trumpin älyttömyyteen on vastattava älykkäästi yhdessä                                                         | https://www.hs.fi/paakirjoitukset/art-2000011157481.html |      -3 |                     -2 |
| 138 | Friedrich Merz aloittaa Saksan johdossa siipirikkona                                                           | https://www.hs.fi/paakirjoitukset/art-2000011156284.html |      -2 |                      2 |
| 139 | Eduskunta hyväksyi nuorille hengenvaarallisen lain                                                             | https://www.hs.fi/paakirjoitukset/art-2000011154496.html |       5 |                      0 |
| 140 | Vaalien loppusuora ennakoi vasemmiston nousua                                                                  | https://www.hs.fi/paakirjoitukset/art-2000011153757.html |      -2 |                     -3 |
| 141 | Trump sai suomalaiset menettämään uskonsa Yhdysvaltoihin                                                       | https://www.hs.fi/paakirjoitukset/art-2000011150872.html |      -3 |                     -2 |
| 142 | Maailmaa johdetaan harhaisilla päähänpinttymillä                                                               | https://www.hs.fi/paakirjoitukset/art-2000011151294.html |      -3 |                     -2 |
| 143 | Syrjäseutujen suomalaisten kodit hajoavat käsiin                                                               | https://www.hs.fi/paakirjoitukset/art-2000011145294.html |      -2 |                     -3 |
| 144 | Alueiden kautta maksettavaan puoluetukeen oli korkea aika puuttua                                              | https://www.hs.fi/paakirjoitukset/art-2000011146348.html |      -2 |                      3 |
| 145 | Donald Trump köyhdyttää amerikkalaista ja suomalaista                                                          | https://www.hs.fi/paakirjoitukset/art-2000011145293.html |      -3 |                     -4 |
| 146 | Vantaalla maahanmuutto ei ole mörkö vaan arkista työtä                                                         | https://www.hs.fi/paakirjoitukset/art-2000011146795.html |      -6 |                     -3 |
| 147 | Alueilla menee jo paremmin, mutta kaikki on vielä kesken                                                       | https://www.hs.fi/paakirjoitukset/art-2000011144447.html |      -1 |                      2 |
| 148 | Kaisa Juuso epäonnistui sadan miljoonan mysteerisäästöjen selittämisessä                                       | https://www.hs.fi/paakirjoitukset/art-2000011144171.html |      -2 |                     -4 |
| 149 | Kiina pohtii vastausta Trumpin taisteluhaasteeseen                                                             | https://www.hs.fi/paakirjoitukset/art-2000011134885.html |      -3 |                     -2 |
| 150 | Wille Rydman astui Donald Trumpin virittämään ansaan                                                           | https://www.hs.fi/paakirjoitukset/art-2000011144131.html |      -3 |                     -2 |
| 151 | Eurooppa opettelee elämää Trumpin maailmassa                                                                   | https://www.hs.fi/paakirjoitukset/art-2000011139124.html |       0 |                      2 |
| 152 | Ay-liike taistelee kohta kokoomuksen ruiskukka napinlävessä                                                    | https://www.hs.fi/paakirjoitukset/art-2000011137387.html |       2 |                      5 |
| 153 | Kokoomus ja Sdp taistelevat Helsingin herruudesta – elpyykö aseveliakseli vai löytävätkö punavihreät toisensa? | https://www.hs.fi/paakirjoitukset/art-2000011137688.html |      -2 |                      0 |
| 154 | Miinapäätökselle oli kova poliittinen tarve                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011138194.html |      -3 |                     -2 |
| 155 | Hallituksen talouspolitiikalta putoaa pohja                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011129097.html |      -2 |                     -5 |
| 156 | Vasta lähipäivät näyttävät Stubbin golfkierroksen tuloksen                                                     | https://www.hs.fi/paakirjoitukset/art-2000011134726.html |      -2 |                      0 |
| 157 | Stubbin golfdiplomatia vei Trumpille Euroopan viestiä                                                          | https://www.hs.fi/paakirjoitukset/art-2000011133613.html |      -2 |                      1 |
| 158 | Tuhkarokko palaa, jos rokotuskattavuus laskee                                                                  | https://www.hs.fi/paakirjoitukset/art-2000011130101.html |      -3 |                     -2 |
| 159 | EU haluaa Suomesta apua vihreään talouteen                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011126729.html |      -3 |                     -2 |
| 160 | Tuomioistuin linjaa Pariisissa Ranskan ja koko Euroopan tietä                                                  | https://www.hs.fi/paakirjoitukset/art-2000011130070.html |      -3 |                     -2 |
| 161 | Hallitus teki sosiaalihuollon säästöistä oppositiolle vaaliaseen ihan itse                                     | https://www.hs.fi/paakirjoitukset/art-2000011130586.html |      -3 |                     -4 |
| 162 | Trumpille tulli on monitoimityökalu                                                                            | https://www.hs.fi/paakirjoitukset/art-2000011127924.html |      -2 |                     -3 |
| 163 | Maanpuolustajat muistuttavat, että maahanmuutto on Suomen etu                                                  | https://www.hs.fi/paakirjoitukset/art-2000011123595.html |      -6 |                     -2 |
| 164 | Palkkiovirkojen aika on ohi – Kelassa on edessä ratkaiseva valinta                                             | https://www.hs.fi/paakirjoitukset/art-2000011122871.html |      -3 |                     -2 |
| 165 | Ikääntyneille aukeaa pikakaista lääkäriin – kokeilu antaa tietoa, onko siinä järkeä                            | https://www.hs.fi/paakirjoitukset/art-2000011125028.html |      -2 |                     -3 |
| 166 | Taksiuudistus kaipaa uudistusta, mutta ei turhia kilpailun esteitä                                             | https://www.hs.fi/paakirjoitukset/art-2000011124398.html |      -3 |                      4 |
| 167 | Kansalaisaloitteet tarttuvat aiheisiin, joita poliitikot empivät nostaa keskusteluun                           | https://www.hs.fi/paakirjoitukset/art-2000011120208.html |      -4 |                     -2 |
| 168 | Lisäydinvoimaa ei pidä rakentaa tukien varaan                                                                  | https://www.hs.fi/paakirjoitukset/art-2000011121595.html |      -2 |                      6 |
| 169 | Työnantajat valavat nyt uskoa tulevaisuuteen, kun hallitukselle tehdyt tilaukset on saatu                      | https://www.hs.fi/paakirjoitukset/art-2000011118961.html |      -3 |                     -4 |
| 170 | Turkissa on rikos olla suositumpi kuin Erdo?an                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011120642.html |      -6 |                     -3 |
| 171 | Lyhytvuokrauksen hyödyt ylittävät edelleen haitat                                                              | https://www.hs.fi/paakirjoitukset/art-2000011111814.html |       2 |                      4 |
| 172 | Rahapeliuudistus on tasapainoilua houkutusten ja haittojen välillä                                             | https://www.hs.fi/paakirjoitukset/art-2000011113071.html |       0 |                      0 |
| 173 | Nuuka armeija marssii uuteen aikaan                                                                            | https://www.hs.fi/paakirjoitukset/art-2000011103839.html |       3 |                      4 |
| 174 | Tampere ottaa pormestari­vaalista ilon irti – asetelma on jälleen jännittävä                                   | https://www.hs.fi/paakirjoitukset/art-2000011106854.html |       0 |                      1 |
| 175 | EU:n hyvät aikeet muuttuvat hitaasti teoiksi                                                                   | https://www.hs.fi/paakirjoitukset/art-2000011115090.html |      -2 |                      2 |
| 176 | Todellinen mestarikokki ei mausta annosta kyynelillä                                                           | https://www.hs.fi/paakirjoitukset/art-2000011114596.html |      -6 |                     -4 |
| 177 | Perinteiset poliitikot epäonnistuivat, mutta Trumpin kova linja tilkitsi Yhdysvaltojen rajan                   | https://www.hs.fi/paakirjoitukset/art-2000011109210.html |      -2 |                      1 |
| 178 | Etätyö voi lisätä tuottavuutta, jos johtaminen on kunnossa                                                     | https://www.hs.fi/paakirjoitukset/art-2000011111418.html |      -2 |                      1 |
| 179 | Länsisataman tunneliratkaisuksi kannattaa valita halvempi, varmempi ja nopeammin valmistuva vaihtoehto         | https://www.hs.fi/paakirjoitukset/art-2000011108331.html |       2 |                      3 |
| 180 | Zelenskyi sai Stubbilta tukea hermopeliin Trumpin kanssa                                                       | https://www.hs.fi/paakirjoitukset/art-2000011108332.html |      -3 |                     -2 |
| 181 | Eurooppa kasvaa takomalla auroja aseiksi                                                                       | https://www.hs.fi/paakirjoitukset/art-2000011105593.html |       0 |                      5 |
| 182 | Zelenskyi ei halua olla Trumpin ja Putinin pelinappula                                                         | https://www.hs.fi/paakirjoitukset/art-2000011105787.html |      -6 |                     -3 |
| 183 | Hallitus hakee ay-liikkeestä vielä yhtä voittoa                                                                | https://www.hs.fi/paakirjoitukset/art-2000011103643.html |      -2 |                     -3 |
| 184 | Yhdysvaltojen loukkaukset herättivät Saksassa raivon ja saivat aikaan historiallisen käänteen                  | https://www.hs.fi/paakirjoitukset/art-2000011103052.html |      -3 |                     -2 |
| 185 | EU:ssa haetaan tiukempaa linjaa – vain viidennes kielteisen turva­paikka­päätöksen saaneista lähtee maasta     | https://www.hs.fi/paakirjoitukset/art-2000011097048.html |       3 |                      2 |
| 186 | Varallisuus Suomessa kasautuu, mutta sille ei tehdä mitään                                                     | https://www.hs.fi/paakirjoitukset/art-2000011097856.html |      -2 |                      2 |
| 187 | Koronapandemia oli outo painajainen, joka voi toistua                                                          | https://www.hs.fi/paakirjoitukset/art-2000011095265.html |      -2 |                     -1 |
| 188 | Duterten saaminen Haagiin valaa uskoa kansainväliseen oikeuteen                                                | https://www.hs.fi/paakirjoitukset/art-2000011093243.html |      -6 |                     -3 |
| 189 | Työeläkejärjestelmä on hyvässä kunnossa                                                                        | https://www.hs.fi/paakirjoitukset/art-2000011098414.html |       0 |                      3 |
| 190 | Euroopan on varauduttava sodan jatkumiseen                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011098062.html |      -3 |                      1 |
| 191 | Yleinen linja ei ole yleinen julkisella sektorilla                                                             | https://www.hs.fi/paakirjoitukset/art-2000011095273.html |       0 |                      3 |
| 192 | Yhdysvallat heitti pallon Ukrainasta Venäjälle                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011093386.html |      -3 |                      2 |
| 193 | Synkältä näyttää, sanoo suomalainen tulevaisuudesta                                                            | https://www.hs.fi/paakirjoitukset/art-2000011088361.html |      -2 |                     -1 |
| 194 | Hedelmöityshoidon korvauksia ei pidä rajata                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011093292.html |      -7 |                     -4 |
| 195 | Sotessa näkyy valoa, mutta alueet ovat eri tahdissa                                                            | https://www.hs.fi/paakirjoitukset/art-2000011088701.html |      -2 |                     -3 |
| 196 | Yhdysvaltojen talouden näkymät muuttuivat yllättäen huonommiksi                                                | https://www.hs.fi/paakirjoitukset/art-2000011090225.html |      -3 |                     -2 |
| 197 | Ranskalle aukeni tie Euroopan johtovaltioksi                                                                   | https://www.hs.fi/paakirjoitukset/art-2000011087243.html |       3 |                      2 |
| 198 | Suomi ja Ruotsi kulkevat käsi kädessä niin Natossa kuin Euroviisuissakin                                       | https://www.hs.fi/paakirjoitukset/art-2000011087406.html |      -3 |                     -2 |
| 199 | Kotona ei pidä joutua pelkäämään naapuria                                                                      | https://www.hs.fi/paakirjoitukset/art-2000011080936.html |       2 |                      1 |
| 200 | Paikallinen päätöksenteko ei vedä puoleensa                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011079875.html |      -3 |                     -1 |
| 201 | Trump vei Ukrainalta tiedustelutuen ja heikensi Euroopan luottamusta Yhdysvaltoihin                            | https://www.hs.fi/paakirjoitukset/art-2000011076668.html |      -6 |                     -4 |
| 202 | Raitiotieliikenne laajentaa kaupunkien henkistä keskustaa                                                      | https://www.hs.fi/paakirjoitukset/art-2000011079056.html |      -3 |                     -2 |
| 203 | Uhkailut tulleilla heikentävät jo Yhdysvaltojen taloutta                                                       | https://www.hs.fi/paakirjoitukset/art-2000011082083.html |      -3 |                     -4 |
| 204 | Saksa ja Ranska alkoivat taas johtaa EU:ta                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011082477.html |      -3 |                      2 |
| 205 | Työmarkkinakierroksen suma alkaa purkautua                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011076628.html |       0 |                      3 |
| 206 | Poliittisessa ohjauksessa pitää noudattaa lakia                                                                | https://www.hs.fi/paakirjoitukset/art-2000011079750.html |      -6 |                     -3 |
| 207 | EU ei enää edes yritä edetä yhtä jalkaa                                                                        | https://www.hs.fi/paakirjoitukset/art-2000011072406.html |      -3 |                      0 |
| 208 | Terveysveroksi naamioitu veronkorotus ei lentänyt                                                              | https://www.hs.fi/paakirjoitukset/art-2000011074165.html |      -2 |                      3 |
| 209 | Euroopalta tarvitaan uudenlaista kovuutta                                                                      | https://www.hs.fi/paakirjoitukset/art-2000011073248.html |       0 |                      2 |
| 210 | Nesteen hallitus teki pahan virheen                                                                            | https://www.hs.fi/paakirjoitukset/art-2000011073776.html |      -2 |                     -6 |
| 211 | Britannialla on nyt halu ja kyky toimia Euroopan kriisijohtajana                                               | https://www.hs.fi/paakirjoitukset/art-2000011061396.html |      -2 |                      3 |
| 212 | Helsinkiin on luvassa tiukka kamppailu vallasta                                                                | https://www.hs.fi/paakirjoitukset/art-2000011071422.html |      -2 |                      0 |
| 213 | Trumpin järkyttämä Tanska panee nyt rahaa puolustukseen                                                        | https://www.hs.fi/paakirjoitukset/art-2000011065749.html |      -2 |                      2 |
| 214 | Hiilinielujen kasvattamiseksi tarvitaan uskottavia toimia                                                      | https://www.hs.fi/paakirjoitukset/art-2000011063314.html |      -3 |                     -2 |
| 215 | Yritysjohtajien pitäisi osallistua rohkeammin yhteiskunnalliseen keskusteluun                                  | https://www.hs.fi/paakirjoitukset/art-2000011056794.html |      -3 |                      3 |
| 216 | Sääntelykoneisto yrittää muuttaa tapojaan                                                                      | https://www.hs.fi/paakirjoitukset/art-2000011066176.html |       0 |                      5 |
| 217 | Venäjän jäädytetyt varat tarvitaan Ukrainalle                                                                  | https://www.hs.fi/paakirjoitukset/art-2000011058689.html |      -3 |                      2 |
| 218 | Murron raportin esityksiä ei pidä tyrmätä hätiköiden                                                           | https://www.hs.fi/paakirjoitukset/art-2000011065241.html |      -2 |                      4 |
| 219 | Asuntokauppa elpyy, mutta tunnelmat eivät                                                                      | https://www.hs.fi/paakirjoitukset/art-2000011062603.html |       0 |                      2 |
| 220 | Transatlanttisten suhteiden superviikko syvensi Euroopan huolia                                                | https://www.hs.fi/paakirjoitukset/art-2000011063199.html |      -4 |                     -3 |
| 221 | Härski diili Ukrainan mineraaleista tuskin johtaa mihinkään                                                    | https://www.hs.fi/paakirjoitukset/art-2000011059719.html |      -3 |                     -4 |
| 222 | Ulkomaisista opiskelijoista kannattaa pitää kiinni                                                             | https://www.hs.fi/paakirjoitukset/art-2000011051397.html |      -3 |                     -2 |
| 223 | Suomi matkaa kohti Japania                                                                                     | https://www.hs.fi/paakirjoitukset/art-2000011057291.html |      -3 |                      4 |
| 224 | Merzin johtama Saksa tarvitsee poikkeuksellista yhteistyötä                                                    | https://www.hs.fi/paakirjoitukset/art-2000011053783.html |      -3 |                      2 |
| 225 | Palkkasovusta pitää rakentaa katto myös vaalilupauksille                                                       | https://www.hs.fi/paakirjoitukset/art-2000011054223.html |       2 |                      5 |
| 226 | Kiina on seurannut hiljaisen tyytyväisenä Yhdysvaltojen linjauksia                                             | https://www.hs.fi/paakirjoitukset/art-2000011045261.html |      -3 |                     -2 |
| 227 | Tutkimusrahan kasvu tuo apua tuottavuuteen – ellei hyviä aineksia vesitetä muilla toimilla                     | https://www.hs.fi/paakirjoitukset/art-2000011047012.html |      -3 |                      2 |
| 228 | Petolinnut kiertävät Ukrainan yllä                                                                             | https://www.hs.fi/paakirjoitukset/art-2000011045110.html |      -3 |                      2 |
| 229 | Saksan vaalit vaikuttavat koko Euroopan päätöksentekoon                                                        | https://www.hs.fi/paakirjoitukset/art-2000011047016.html |      -4 |                     -2 |
| 230 | Jos työmarkkinoilla syntyy sopu, Suomessa on yksi huoli vähemmän                                               | https://www.hs.fi/paakirjoitukset/art-2000011050157.html |       0 |                      3 |
| 231 | Yhdysvaltojen äkkikäännös repii reikiä Euroopan turvallisuuteen                                                | https://www.hs.fi/paakirjoitukset/art-2000011047837.html |      -6 |                     -3 |
| 232 | Suomi odottaa taloudelleen pelastajaa ulkopuolelta                                                             | https://www.hs.fi/paakirjoitukset/art-2000011042131.html |      -2 |                      4 |
| 233 | Helsinki-hallista toivotaan tuottavaa viihdetehdasta                                                           | https://www.hs.fi/paakirjoitukset/art-2000011043245.html |       0 |                      3 |
| 234 | Teollisuusliiton taakse tulee lisää työntäjiä                                                                  | https://www.hs.fi/paakirjoitukset/art-2000011039876.html |       0 |                      4 |
| 235 | Euroopan on vaikea torjua Ukrainan rauhan riskejä                                                              | https://www.hs.fi/paakirjoitukset/art-2000011039444.html |      -3 |                     -2 |
| 236 | USA:n kahtiajako halkoo nyt Suomen hallitusta                                                                  | https://www.hs.fi/paakirjoitukset/art-2000011038153.html |      -6 |                     -3 |
| 237 | Trumpilla on enemmän valtaa Euroopassa kuin Yhdysvalloissa                                                     | https://www.hs.fi/paakirjoitukset/art-2000011031768.html |      -3 |                     -2 |
| 238 | Nokia on Euroopalle strateginen ja ostettavissa                                                                | https://www.hs.fi/paakirjoitukset/art-2000011031130.html |      -2 |                      3 |
| 239 | Trump yrittää pelotella arabimaita sovintoon                                                                   | https://www.hs.fi/paakirjoitukset/art-2000011034548.html |      -3 |                     -2 |
| 240 | Eurooppa etsii itseään, kun USA menee menojaan                                                                 | https://www.hs.fi/paakirjoitukset/art-2000011036090.html |      -3 |                     -2 |
| 241 | Trump iski korttinsa pöytään ja pakotti kaikki muut rinkiin                                                    | https://www.hs.fi/paakirjoitukset/art-2000011030792.html |      -3 |                     -2 |
| 242 | Iso ydinvoimala toisi lisälaskun kaikille sähkön käyttäjille                                                   | https://www.hs.fi/paakirjoitukset/art-2000011025944.html |      -3 |                     -2 |
| 243 | Teknoyritykset ovat alkaneet vähentää väkeä                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011028898.html |       0 |                      3 |
| 244 | Kaksi epäsuosittua ehdokasta vääntää vallasta Saksassa                                                         | https://www.hs.fi/paakirjoitukset/art-2000011023073.html |      -3 |                      2 |
| 245 | Fatim Diarra haukkui väärää puuta                                                                              | https://www.hs.fi/paakirjoitukset/art-2000011026446.html |      -2 |                      0 |
| 246 | Nokia palkkasi taas muutosjohtajan                                                                             | https://www.hs.fi/paakirjoitukset/art-2000011023375.html |       0 |                      2 |
| 247 | Eurooppa odottaa Trumpin avausta Ukrainasta                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011006862.html |       0 |                      2 |
| 248 | Baby ei poraa, jos se ei kannata                                                                               | https://www.hs.fi/paakirjoitukset/art-2000011012486.html |      -3 |                      3 |
| 249 | Näpit irti Suomen kouluista, poliitikot!                                                                       | https://www.hs.fi/paakirjoitukset/art-2000011018717.html |      -5 |                     -2 |
| 250 | Työtaisteluissa odotellaan vahvistuksia satamista                                                              | https://www.hs.fi/paakirjoitukset/art-2000011017953.html |       0 |                      4 |
| 251 | Helsingin johdossa on edessä sukupolvenvaihdos                                                                 | https://www.hs.fi/paakirjoitukset/art-2000010999148.html |      -2 |                      1 |
| 252 | Väkivalta uhkaa Ruotsia monesta suunnasta                                                                      | https://www.hs.fi/paakirjoitukset/art-2000011013074.html |      -2 |                      1 |
| 253 | Ulko- ja turvallisuuspolitiikan vallanjako ei ratkea vain hyvällä tahdolla                                     | https://www.hs.fi/paakirjoitukset/art-2000011011422.html |      -3 |                     -2 |
| 254 | Puolustuksen yhteisvelka voi olla Suomen etu                                                                   | https://www.hs.fi/paakirjoitukset/art-2000011009586.html |      -2 |                      3 |
| 255 | Trumpin tullipolitiikka yksinkertaisesti selitettynä                                                           | https://www.hs.fi/paakirjoitukset/art-2000011008256.html |      -3 |                      3 |
| 256 | Trumpin suurvaltapolitiikka ajaa EU-maat ahtaalle                                                              | https://www.hs.fi/paakirjoitukset/art-2000011003477.html |      -3 |                      1 |
| 257 | Hallituksen tarjoama nikotiinikoukku maistuu mentolilta                                                        | https://www.hs.fi/paakirjoitukset/art-2000011002494.html |      -6 |                     -4 |
| 258 | Nuoret perivät maan – ja maksamattomat laskut                                                                  | https://www.hs.fi/paakirjoitukset/art-2000010999762.html |      -6 |                     -5 |
| 259 | Saimaalla kuutti parkaisee, kiitos kolaajien                                                                   | https://www.hs.fi/paakirjoitukset/art-2000010999907.html |      -3 |                     -2 |
| 260 | Ympäristöministerin ei pitäisi vähätellä Suomen vastuuta                                                       | https://www.hs.fi/paakirjoitukset/art-2000010996643.html |      -3 |                     -2 |
| 261 | Hallitukselle tehdään viimeiset tilaukset                                                                      | https://www.hs.fi/paakirjoitukset/art-2000011002045.html |      -3 |                     -4 |
| 262 | Helsingin autokeskustelu lähti koville kierroksille                                                            | https://www.hs.fi/paakirjoitukset/art-2000010997105.html |      -2 |                      3 |
| 263 | Koraaninpolttajan ampuminen kiristää jännitystä Ruotsissa                                                      | https://www.hs.fi/paakirjoitukset/art-2000010999401.html |      -3 |                      2 |
| 264 | Kriisiviestinnässä kannattaa olla avoin ja nöyrä                                                               | https://www.hs.fi/paakirjoitukset/art-2000010996930.html |      -2 |                      0 |
| 265 | Trumpin edessä ei voi taipua – me olemme kaikki tanskalaisia                                                   | https://www.hs.fi/paakirjoitukset/art-2000010992642.html |      -6 |                     -4 |
| 266 | Orpon hallituksen ei pidä enää tehdä uusia säästöjä                                                            | https://www.hs.fi/paakirjoitukset/art-2000010995030.html |      -2 |                     -4 |
| 267 | Ammattiliitoilla on nyt onnistumisen pakko                                                                     | https://www.hs.fi/paakirjoitukset/art-2000010991542.html |       0 |                      3 |
| 268 | Nato partioi Itämerellä, mutta kiusa jatkuu                                                                    | https://www.hs.fi/paakirjoitukset/art-2000010991376.html |       0 |                      2 |
| 269 | Macron hajottaa hallitakseen                                                                                   | https://www.hs.fi/paakirjoitukset/art-2000010986725.html |       2 |                      5 |
| 270 | Hallitus hakee uutta rytmiä                                                                                    | https://www.hs.fi/paakirjoitukset/art-2000010986507.html |      -2 |                      1 |
| 271 | Trump yrittää käskeä, mutta talous tuskin tottelee                                                             | https://www.hs.fi/paakirjoitukset/art-2000010981410.html |      -3 |                     -2 |
| 272 | Eagle S -alusta on nyt tutkittu – mitä sitten?                                                                 | https://www.hs.fi/paakirjoitukset/art-2000010983425.html |      -2 |                      0 |
| 273 | Yle säästää ja vähentää väkeä                                                                                  | https://www.hs.fi/paakirjoitukset/art-2000010987949.html |      -2 |                      2 |
| 274 | Liitot yrittävät lakkoilla kohtuuden rajoissa                                                                  | https://www.hs.fi/paakirjoitukset/art-2000010978261.html |       2 |                      4 |
| 275 | Intia sai mahdollisuuden parantaa asemaansa                                                                    | https://www.hs.fi/paakirjoitukset/art-2000010983913.html |      -2 |                      3 |
| 276 | Kelan pääjohtajan paikan ei pidä olla palkkio                                                                  | https://www.hs.fi/paakirjoitukset/art-2000010976284.html |      -3 |                     -4 |
| 277 | Trump punnitsee heti EU:n kauppapolitiikan                                                                     | https://www.hs.fi/paakirjoitukset/art-2000010981270.html |      -3 |                     -2 |
| 278 | Sdp etenee nyt kieli keskellä suuta                                                                            | https://www.hs.fi/paakirjoitukset/art-2000010978992.html |       0 |                      0 |
| 279 | Trump julisti terveen järjen vallankumousta                                                                    | https://www.hs.fi/paakirjoitukset/art-2000010979096.html |      -3 |                     -2 |
| 280 | Eurooppalaiset jäävät Trump-huolineen yksin                                                                    | https://www.hs.fi/paakirjoitukset/art-2000010975359.html |      -3 |                     -2 |
| 281 | Työeläkkeiden uudistuksesta syntyi lihava sopu                                                                 | https://www.hs.fi/paakirjoitukset/art-2000010975488.html |       0 |                      3 |
| 282 | Aika ei ole sotivan Venäjän puolella                                                                           | https://www.hs.fi/paakirjoitukset/art-2000010959027.html |      -3 |                      3 |
| 283 | Sopimisen paine kasvaa työmarkkinoilla kohti helmikuuta                                                        | https://www.hs.fi/paakirjoitukset/art-2000010970112.html |       0 |                      4 |
| 284 | Diktaattori Trump näyttää korttinsa                                                                            | https://www.hs.fi/paakirjoitukset/art-2000010970148.html |      -4 |                     -3 |
| 285 | Pikkurosvokki sai vihdoin nimen – hyppyhäntäiset odottavat yhä vuoroaan                                        | https://www.hs.fi/paakirjoitukset/art-2000010971210.html |      -2 |                     -1 |
| 286 | Monella pojalla menee ihan hyvin                                                                               | https://www.hs.fi/paakirjoitukset/art-2000010970139.html |      -3 |                     -2 |
| 287 | Poliitikkoja varjostaa väkivallan uhka                                                                         | https://www.hs.fi/paakirjoitukset/art-2000010969897.html |       0 |                      0 |
| 288 | Trumpin pelko tuo tulitauon Gazaan                                                                             | https://www.hs.fi/paakirjoitukset/art-2000010966961.html |      -3 |                     -2 |
| 289 | EU-tuomioistuimen tulee valvoa vallan rajoja                                                                   | https://www.hs.fi/paakirjoitukset/art-2000010966998.html |       3 |                      5 |
| 290 | Kansanedustajat yrittävät sulkea silmänsä huumeilta                                                            | https://www.hs.fi/paakirjoitukset/art-2000010961665.html |      -6 |                     -3 |
| 291 | Merioikeuden tulkinta jakaa Natossa                                                                            | https://www.hs.fi/paakirjoitukset/art-2000010964627.html |      -2 |                      2 |
| 292 | Isoa ydinvoimalaa lobataan, koska pieni ei tähän hätään ehdi                                                   | https://www.hs.fi/paakirjoitukset/art-2000010961565.html |      -2 |                      1 |
| 293 | Maakuntalentojen ostamista ei pidä jatkaa                                                                      | https://www.hs.fi/paakirjoitukset/art-2000010963317.html |       0 |                      5 |
| 294 | Euroopan johtajat varovat sanojaan Trumpin pelossa                                                             | https://www.hs.fi/paakirjoitukset/art-2000010959156.html |      -3 |                     -2 |
| 295 | Kansanedustaja löysi lopulta syyllisen humalatilaansa                                                          | https://www.hs.fi/paakirjoitukset/art-2000010960313.html |      -3 |                     -2 |
| 296 | Moralisointi ei auta ratkaisemaan palvelujen ongelmia                                                          | https://www.hs.fi/paakirjoitukset/art-2000010952245.html |       0 |                      6 |
| 297 | Asuntokin on sijoitus, ja kaikki sijoitukset voivat pettää                                                     | https://www.hs.fi/paakirjoitukset/art-2000010954138.html |       0 |                      3 |
| 298 | Tatua ja Patua saa muuttaa, mutta historiaa pitää suojella                                                     | https://www.hs.fi/paakirjoitukset/art-2000010949460.html |      -3 |                     -1 |
| 299 | Outo Queen sulatti katsojien sydämet                                                                           | https://www.hs.fi/paakirjoitukset/art-2000010952503.html |      -3 |                     -2 |
| 300 | Itämerestä tuli Naton ja Venäjän konfliktin etulinja                                                           | https://www.hs.fi/paakirjoitukset/art-2000010955495.html |      -2 |                      1 |
| 301 | Kalifornian paloista pitää oppia                                                                               | https://www.hs.fi/paakirjoitukset/art-2000010955416.html |      -3 |                     -4 |
| 302 | Musk vie, Eurooppa vikisee                                                                                     | https://www.hs.fi/paakirjoitukset/art-2000010948652.html |      -5 |                     -4 |
| 303 | Harkimon puolue ei ole lunastanut lupauksiaan                                                                  | https://www.hs.fi/paakirjoitukset/art-2000010952633.html |      -2 |                      3 |
| 304 | Hallituksen valomerkki lähestyy – kokoomus vyöryttää perintöveron poistamista                                  | https://www.hs.fi/paakirjoitukset/art-2000010949169.html |      -3 |                     -5 |
| 305 | Suomettumisen kokemus ruokkii tiedeväen epäluuloa                                                              | https://www.hs.fi/paakirjoitukset/art-2000010949066.html |      -3 |                      2 |
| 306 | Trudeaun mukana jätetään hyvästejä yhdelle aikakaudelle                                                        | https://www.hs.fi/paakirjoitukset/art-2000010946031.html |      -3 |                     -2 |
| 307 | Ukrainaa ei auteta pelkillä puheilla                                                                           | https://www.hs.fi/paakirjoitukset/art-2000010946933.html |      -3 |                     -2 |
| 308 | Suomen talous sai lahjoja rajojen takaa                                                                        | https://www.hs.fi/paakirjoitukset/art-2000010907274.html |      -6 |                     -3 |
| 309 | Vanha rakennus on parempi kunnostaa kuin korvata uudella                                                       | https://www.hs.fi/paakirjoitukset/art-2000010864992.html |      -3 |                     -4 |
| 310 | Kuluttajan kannattaa vahtia ruokakauppojen hintoja                                                             | https://www.hs.fi/paakirjoitukset/art-2000010940410.html |       0 |                      4 |
| 311 | Grönlanti ei ole kaupan edes Trumpille                                                                         | https://www.hs.fi/paakirjoitukset/art-2000010938230.html |      -2 |                      1 |
| 312 | Trumpin lähipiirissä puhkesi kiista maahanmuutosta                                                             | https://www.hs.fi/paakirjoitukset/art-2000010938293.html |      -4 |                     -2 |
| 313 | Valko-Venäjän despootti valmistautuu vaaliteatteriin                                                           | https://www.hs.fi/paakirjoitukset/art-2000010938812.html |      -6 |                     -2 |
| 314 | Finlandia-talo sai arvoisensa remontin                                                                         | https://www.hs.fi/paakirjoitukset/art-2000010939738.html |      -2 |                      0 |
| 315 | Merkitystään maailman­kartalla hakeva Britannia tasa­painottelee Trumpin ja EU:n välissä                       | https://www.hs.fi/paakirjoitukset/art-2000010904019.html |      -2 |                      1 |
| 316 | Yrittäjien tielle on kasautunut uusia kiviä                                                                    | https://www.hs.fi/paakirjoitukset/art-2000010934042.html |      -2 |                      2 |
| 317 | EU on harhautunut matkallaan tähtiin, mutta Suomen jäsenyys unionissa oli oikea valinta                        | https://www.hs.fi/paakirjoitukset/art-2000010904969.html |      -3 |                      2 |