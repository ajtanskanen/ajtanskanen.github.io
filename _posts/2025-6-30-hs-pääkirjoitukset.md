---
title: 'Helsingin sanomien pääkirjoitusten poliittisuus ja arvot'
date: 2025-06-21
permalink: /posts/2025/6/paakirjoitukset/
summary: 'Blogi | Helsingin Sanomien pääkirjoituksissa otetaan usein kantaa ajankohtaisiin asioihin. Uutisoinnin neutraaliutta voi analysoida suurilla kielimalleilla. Tässä käytämme Anthropicin Claudea, jonka mukaan HS:n pääkirjoitukset painottuvat vahvasti arvoliberalismia kannattaviksi ja maltillisen vasemmistolaisiksi.'
tags:
  - pääkirjoitukset
  - poliittisuus
  - arvot
---

Helsingin Sanomat on arvostettu suomalainen lehti, joka on suorastaan instituutio. Hesari ei ole pelkkää passiivinen asioiden seuraaja, vaan ottaa lehtenä kantaa ajankohtaisiin asioihin. Lehden linjaa esitellään pääkirjoituksissa. Tässä blogissa analysoidaan, mihin kohtaan arvokarttaa pääkirjoitukset sijoittuvat. Tulosten mukaan HS on vahvasti arvoliberaali ja maltillisen vasemmistolainen lehti.

![HS:n uutisten poliittisuuden jakauma](/images/HS/jakauma.png)<br>
_Kuvio 1. HS:n uutisjuttujen poliittisen näkökulman (vaaka-akseli) ja arvojen (pystyakseli) yhteisjakauma. Pystyakselilla alhaalla arvoliberalisti, ylhäällä arvokonservatismi. Vaaka-akselilla vasemmalla vasemmmisto, oikealla oikeisto._

1 Aineisto
===

Helsingin Sanomat kuvaava itse [pääkirjoitusten](https://www.hs.fi/info/art-2000010221266.html) linjaa näin:
> Pääkirjoituksissa määritellään lehden kanta eri asioihin, mutta uutistoimituksen työtä pääkirjoitukset eivät määritä. Niiden linjaukset eivät myöskään poista objektiivisuuden tai tasapuolisuuden vaadetta uutissisällöissä.

Blogin analyysin ei ole tarkoitus olla kattava. Aineistossa oli vain 40 pääkirjoitusta, jotka on kerätty 31.5.2025-20.6.2025 väliltä. Laajempi tutkimus pystyisi arvioimaan tätä tutkimusta paremmin, miten HS sijoittuu arvokartalle. Olisi myös kiinnostavaa nähdä, onko HS:n sijainti arvokartalla muuttunut ajan kuluessa.

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

Pääkirjoitukset ovat selvästi arvoliberaaleja: keskiarvo on -2,4 asteikolla (-10; 10). Tyypillinen pääkirjoitus on sekin selvästi arvoliberaali, sillä mediaani on -2.
Tämä lienee odotettua, koska HS on jo aikoinaan perustettu kannattamaan liberaaleja arvoja.

![HS:n pääkirjoitusten arvojen jakauma](/images/HS/arvot.png)<br>
_Kuvio 2. HS:n pääkirjoitusten arvojen jakauma._

Vaikka arvojen jakauma painottuu vahvasti arvoliberaaliin suuntaan, on pääkirjoitusten joukossa myös arvokonservatiivisesta näkökulmia.

4 Poliittisuus
===

Kirjoitusten näkökulmien on hyvin lievästi vasemmistolainen: keskiarvo on -0,23 asteikolla (-10; 10). Tyypillinen pääkirjoitus taas on maltillisen vasemmistolainen, sillä mediaani on -1. Tämä siis tarkoittaa, että myös pääkirjoitusten joukossa on selvästi oikeistolaisia pääkirjoituksia. Tämä näkyy kuviosta 3.

![HS:n pääkirjoitusten poliittisuuden jakauma](/images/HS/poliittinen.png)<br>
_Kuvio 3. HS:n pääkirjoitusten poliittisuuden jakauma._

Arvojen ja polittiisen näkökulman yhteisjakauma (Kuvio 1) osoittaa että suuri huippu uutisjuttuille on arvoliberaalissa vasemmistossa. 
Kiinnostavasti jakaumalla on kaksi huippu, joista toinen sijoittuu "arvoneutraaliin" oikeistoon. Jakauman paino on selvästi arvolilberaalissa vasemmistossa.

5 Esimerkkejä tuloksista
===

Seuraavaksi käyn hieman yksityiskohtaisemmin läpi Clauden arviot muutamasta pääkirjoituksesta.

5.1 Myllypuro uudistui ja kaikki voittivat – paitsi ennakkoluulot
==

[Myllypuron uudistamisesta kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011292427.html) arvioidaan selvästi arvoliberaaliksi (-6) ja vasemmistolaiseksi (-4).

> Kirjoituksessa on maltillisia vasemmistolaisia piirteitä. Se puolustaa valtion tukemaa asuntorakentamista (ARA-järjestelmä) ja näkee sen positiivisena tekijänä alueen kehityksessä. Vuokrasäännöstely esitetään hyvänä asiana, joka suojeli alkuperäisiä asukkaita. Kirjoitus kritisoi markkinaehtoista asumispolitiikkaa epäsuorasti ja korostaa julkisen sektorin roolia aluekehityksessä.

> Kirjoitus on selkeästi arvoliberaali. Se kritisoi maahanmuuttovastaisuutta ja stereotypioita, puolustaa monimuotoisuutta ja monikulttuurisuutta positiivisena asiana. Erityisesti perussuomalaisten edustajan kommentti 'minareeteista ja sharia-laista' esitetään negatiivisessa valossa. Kirjoitus korostaa Itä-Helsingin monimuotoisuutta ja torjuu ennakkoluuloja.

5.2 Ilmailun työtaistelu
==
[Ilmailun työtaistelusta kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011274686.html) arvioidaan lievästi arvokonservatiiviseksi (+2) ja selvästi oikeistolaisesta näkökulmasta kirjoitetuksi (+5).

> Kirjoitus ei käsittele varsinaisia arvokonservatiivisia tai -liberaaleja teemoja kuten perhepolitiikkaa, sukupuolikysymyksiä tai maahanmuuttoa. Se keskittyy työmarkkinapolitiikkaan ja taloudellisiin kysymyksiin. Lievä konservatiivinen sävy tulee esiin siinä, että kirjoitus puolustaa olemassa olevia rakenteita (vientimalli, sovittelujärjestelmä) ja vastustaa niiden muuttamista.

> Kirjoitus on selvästi oikeistolainen. Se puolustaa työnantajien näkökulmaa, kritisoi lakkoja ja niiden taloudellisia vaikutuksia, korostaa Finnairin tuloksen ja osinkovirtojen tärkeyttä valtiolle, sekä puolustaa vientimallia ja maltillisia palkankorotuksia. Kirjoittaja näkee työntekijöiden vaatimukset kohtuuttomina ja perusteettomina, eikä osoita ymmärrystä heidän näkökulmalleen. Erityisen paljastava on lause 'Taustalla vaikuttava mutta vähemmän mainostettu lähtökohta', joka vihjaa työntekijöillä olevan piilotettuja motiiveja.

5.3 Piispat tekivät ison linjauksen samaa sukupuolta olevien vihkimisestä 
==

[Kirkolliskokouksen päätöstä arvioiva pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011278250.html) on selvästi arvoliberaali (-6) ja poliittiselta lievästi vasemmistolainen (-2).

> Kirjoitus on kirjoitettu selkeästi arvoliberaalista näkökulmasta. Teksti kuvaa positiivisena kehityksenä piispojen linjauksen olla rankaisematta samaa sukupuolta olevien parien vihkiviä pappeja. Kirjoittaja kutsuu tilannetta 'merkittäväksi askeleeksi' ja pitää ratkaisua 'parhaana tapana' selvittää asia. Hän ei kritisoi yhteiskunnallista muutosta tasa-arvoisen avioliittolain suuntaan, vaan päinvastoin esittää kirkon perinteisen avioliittokäsityksen ja nykytilanteen välisen ristiriidan ongelmallisena ja kirkkoa 'repivänä'. Kirjoittaja rinnastaa myös samaa sukupuolta olevien vihkimisen eronneiden vihkimiseen, vihjaten että kyse on samanlaisesta luonnollisesta kehityksestä.

> Kirjoituksessa ei oteta kantaa taloudellisiin tai muihin perinteisiin vasemmisto-oikeisto -jakolinjoihin. Teksti keskittyy puhtaasti kirkon sisäiseen arvomaailmaan ja avioliittokäsitykseen liittyviin kysymyksiin. Kirjoittaja ei ota kantaa esimerkiksi kirkon ja valtion suhteeseen, kirkon rahoitukseen, työntekijöiden asemaan tai muihin poliittisen vasemmisto-oikeisto -akselin teemoihin. Näkökulma on neutraali suhteessa poliittiseen suuntaukseen.

5.4 Raja railona aukeaa Suomen sisällä
==

[Väestöllisestä painopisteestä kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011279927.html) on maltillisen arvokonservatiivinen (2) ja maltillisen oikeistolainen (+4).

> Kirjoitus on lievästi arvokonservatiivinen. Se hyväksyy väestön keskittymisen ja alueellisen eriarvoisuuden luonnollisena kehityksenä, eikä kyseenalaista markkinavetoista kehitystä. Toisaalta se ei sisällä vahvoja arvokonservatiivisia teemoja kuten perinteiden tai yhteisöllisyyden korostamista.

> Kirjoitus on selkeästi oikeistolainen. Se kritisoi aluepolitiikkaa ja julkisten varojen käyttöä alueellisten erojen tasaamiseen, korostaa taloudellista realismia ja markkinoiden roolia. Erityisen paljastava on lause 'Eikä Weberin pistettä saa edes nykymaailmassa peruuttamaan rahalla työntämällä', joka viittaa markkinatalouden ylivoimaan valtiolliseen ohjaukseen nähden.

5.5 Telakka tuo rahaa ja työtä Suomeen
==
[Telakasta kertova pääkirjoitus](https://www.hs.fi/paakirjoitukset/art-2000011272057.html) arvioidaan arvoneutraaliksi (0) ja poliittisesti neutraaliksi (3).

> Kirjoitus ei käsittele arvoliberaaleja tai arvokonservatiivisia teemoja kuten ihmisoikeuksia, tasa-arvoa, perinteisiä arvoja tai yhteiskunnallisia normeja. Se keskittyy puhtaasti taloudellisiin ja elinkeinopoliittisiin kysymyksiin, joten arvoulottuvuudella ei ole merkitystä tässä tekstissä.

> Kirjoitus kallistuu lievästi oikealle useista syistä: 1) Se korostaa yksityisen sektorin investointien ja viennin merkitystä talouskasvulle, 2) Kritisoi implisiittisesti vihreän siirtymän investointeja niiden vähäisen työllistävyyden vuoksi, 3) Kehuu telakkateollisuuden säilyttämistä markkinatalouden näkökulmasta, 4) Mainitsee valtion takausvastuut myönteisessä valossa nimenomaan siksi, että ne tukevat yksityistä liiketoimintaa. Toisaalta kirjoitus ei ole voimakkaan oikeistolainen, sillä se hyväksyy valtion roolin talouden tukijana.


6 Yhteenveto
===

Tulosten mukaan Helsingin Sanomat tunnustaa arvokysymyksissä selvästi väriä: pääkirjoitukset on kirjoitettu vahvasti arvoliberaalista näkökulmasta. Tätä ei ehkä voi pitää yllättävänä, koska Hesarin tausta on liberaalissa nuorsuomalaisessa liikkeessä.

Poliittisesti tulos ei ole yhtä selvä, vaikka pääkirjoituksissa painottuu maltillinen vasemmistolaisuus. Tyypillisin näkökulma on loiva vasemmmistolaisuus, mutta mukana on myös oikeistolaisia näkökulmia. Jyrkkää oikeistolaista tai jyrkkää vasemmistolaista näkökulmaa pääkirjoituksissa ei oteta.
Ehkä tulokset voi summata niin, että Hesari on jonkinlainen arvoliberaali oikeistososialidemokratti. 


Liite
===
|    | otsikko                                                                                     | linkki                                                   |   arvot |   poliittinen suuntaus |
|---:|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------|--------:|-----------------------:|
|  0 | Valtio voisi ottaa mallia arkkipiispan anteeksipyynnöstä saamelaisilta                      | https://www.hs.fi/paakirjoitukset/art-2000011303517.html |      -6 |                     -4 |
|  1 | Helsingin uusi silta on veronmaksajalle ilonaihe                                            | https://www.hs.fi/paakirjoitukset/art-2000011309509.html |       0 |                      3 |
|  2 | Suomalaisten kielitaitoon kuuluvat myös farsi ja tagalog                                    | https://www.hs.fi/paakirjoitukset/art-2000011275924.html |      -5 |                     -2 |
|  3 | Eurooppa seuraa Iranin ja Israelin konfliktia katsomosta                                    | https://www.hs.fi/paakirjoitukset/art-2000011310634.html |      -2 |                      1 |
|  4 | Pelttarin tapaus ajaa muuttamaan virkarikoksia koskevia pykäliä                             | https://www.hs.fi/paakirjoitukset/art-2000011307176.html |      -3 |                     -2 |
|  5 | Valtiovarainministeriö taloudesta: paremmalta näyttää jo, kunhan ei katso kovin kauas       | https://www.hs.fi/paakirjoitukset/art-2000011304178.html |       0 |                     -3 |
|  6 | Osuuskuntien omistajien kannattaisi terävöityä                                              | https://www.hs.fi/paakirjoitukset/art-2000011303530.html |       0 |                     -2 |
|  7 | Kultarannassa nähtiin, että hopealuodit maailman ongelmiin ovat vähissä                     | https://www.hs.fi/paakirjoitukset/art-2000011304824.html |      -2 |                      0 |
|  8 | Eduskunnan on hyväksyttävä uusi saamelaiskäräjälaki                                         | https://www.hs.fi/paakirjoitukset/art-2000011299499.html |      -6 |                     -3 |
|  9 | Helsingin ydinkeskustasta pitää tehdä viihtyisämpi                                          | https://www.hs.fi/paakirjoitukset/art-2000011298342.html |      -2 |                      3 |
| 10 | Myllypuro uudistui ja kaikki voittivat – paitsi ennakkoluulot                               | https://www.hs.fi/paakirjoitukset/art-2000011292427.html |      -6 |                     -4 |
| 11 | Kala olisi kiva ostaa suoraan kalastajalta                                                  | https://www.hs.fi/paakirjoitukset/art-2000011295902.html |     nan |                    nan |
| 12 | Talousennustajien tähtäin oli säädetty liian ylös                                           | https://www.hs.fi/paakirjoitukset/art-2000011295704.html |       0 |                      2 |
| 13 | Nyt tai ei koskaan – Israel yrittää estää Iranin ydinaseen                                  | https://www.hs.fi/paakirjoitukset/art-2000011299143.html |      -2 |                      1 |
| 14 | Perussuomalaiset alkaa valmistautua Purran jälkeiseen aikaan                                | https://www.hs.fi/paakirjoitukset/art-2000011296551.html |      -3 |                     -2 |
| 15 | Lentäjien sopimuksen viivästyminen tuli kalliiksi                                           | https://www.hs.fi/paakirjoitukset/art-2000011295176.html |       0 |                      5 |
| 16 | Veneilijänkin pitää nyt varautua Venäjän häirintään                                         | https://www.hs.fi/paakirjoitukset/art-2000011293354.html |       0 |                      1 |
| 17 | Kesäloman juhlat eivät kuulu työnantajalle                                                  | https://www.hs.fi/paakirjoitukset/art-2000011292933.html |      -6 |                     -5 |
| 18 | Suomessa konkurssia hävetään turhaan                                                        | https://www.hs.fi/paakirjoitukset/art-2000011289952.html |      -2 |                      6 |
| 19 | Ääniveturit vetivät yllätysehdokkaita kuntien valtuustoihin                                 | https://www.hs.fi/paakirjoitukset/art-2000011290503.html |      -2 |                     -1 |
| 20 | Trump haastaa riitaa Kalifornian kanssa                                                     | https://www.hs.fi/paakirjoitukset/art-2000011288471.html |      -6 |                     -5 |
| 21 | Suomalaisten ylipaino maksaa ja koskee                                                      | https://www.hs.fi/paakirjoitukset/art-2000011264522.html |       0 |                      2 |
| 22 | Perusäänestäjä muistuttaa perusehdokasta                                                    | https://www.hs.fi/paakirjoitukset/art-2000011282959.html |      -4 |                     -3 |
| 23 | Hyviä uutisia taloudesta                                                                    | https://www.hs.fi/paakirjoitukset/art-2000011280206.html |      -1 |                      2 |
| 24 | Raja railona aukeaa Suomen sisällä                                                          | https://www.hs.fi/paakirjoitukset/art-2000011279927.html |       2 |                      4 |
| 25 | Maanpuolustus kuuluu niin naisille kuin miehillekin                                         | https://www.hs.fi/paakirjoitukset/art-2000011283601.html |      -4 |                     -2 |
| 26 | Yliopistojen valintakokeiden hiominen alkaa nyt                                             | https://www.hs.fi/paakirjoitukset/art-2000011281362.html |      -2 |                     -1 |
| 27 | Venäjä valmistelee vielä kostoaan                                                           | https://www.hs.fi/paakirjoitukset/art-2000011283508.html |      -3 |                     -2 |
| 28 | Petteri Orpo on tehnyt sen, mitä kokoomus on pitkään halunnut                               | https://www.hs.fi/paakirjoitukset/art-2000011267971.html |      -3 |                     -4 |
| 29 | Piispat tekivät ison linjauksen samaa sukupuolta olevien vihkimisestä                       | https://www.hs.fi/paakirjoitukset/art-2000011278250.html |      -6 |                     -2 |
| 30 | Rajalaissa poikkeuksesta tehtiin uusi normaali                                              | https://www.hs.fi/paakirjoitukset/art-2000011278329.html |      -3 |                     -2 |
| 31 | Suomi sai EU:lta armoviitosen ja välttyi tarkkailuluokalle joutumiselta                     | https://www.hs.fi/paakirjoitukset/art-2000011278493.html |       0 |                      3 |
| 32 | Ilmailun työtaisteluissa kamppaillaan palkkojen ohella Finnairin ja vientimallin kohtalosta | https://www.hs.fi/paakirjoitukset/art-2000011274686.html |       2 |                      5 |
| 33 | Trumpin uhkaukset ovat muuttuneet pelottavista huvittaviksi                                 | https://www.hs.fi/paakirjoitukset/art-2000011275091.html |      -3 |                     -2 |
| 34 | Telakka tuo rahaa ja työtä Suomeen                                                          | https://www.hs.fi/paakirjoitukset/art-2000011272057.html |       0 |                      3 |
| 35 | Ukrainan iskut pääsevät vielä sotataidon oppikirjoihin                                      | https://www.hs.fi/paakirjoitukset/art-2000011272652.html |      -3 |                      0 |
| 36 | Vihreät tyytyvät puolueen kutistumiseen                                                     | https://www.hs.fi/paakirjoitukset/art-2000011263892.html |      -3 |                      2 |
| 37 | Ilman maahanmuuttoa Suomi joutuu kriisiin pitkällä aikavälillä                              | https://www.hs.fi/paakirjoitukset/art-2000011266091.html |      -5 |                     -3 |
| 38 | Puolalla on taas valinnan paikka                                                            | https://www.hs.fi/paakirjoitukset/art-2000011267641.html |      -6 |                     -3 |
| 39 | Suomen on päästävä takaisin jatkuvan kasvun oravanpyörään                                   | https://www.hs.fi/paakirjoitukset/art-2000011267513.html |       0 |                      5 |