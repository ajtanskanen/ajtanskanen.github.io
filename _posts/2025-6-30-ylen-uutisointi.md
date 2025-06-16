---
title: 'Ylen uutisoinnin poliittisuus ja arvot'
date: 2025-06-30
permalink: /posts/2025/6/ylenuutisointi/
summary: 'Blogi | Ylen uutisointia on toisinaan pidetty vihervasemmistolaisena, toisinaan oikeistolaisena, vaikka uutisoinnin pitäisi olla neutraalia. Uutisoinnin neutraaliutta voi analysoida suurilla kielimalleilla. Tässä käytämme Anthropicin Claudea, jonka mukaan Ylen uutisointi on pääosin neutraalia, vaikka keskimäärin se on hieman kallellaan poliittiseen vasemmistoon ja arvoliberaaliin suuntaan.'
tags:
  - ylen uutisointi
  - poliittisuus
  - arvot
---

Ylen uutisointia on toisinaan arvosteltu vihervasemistolaiseksi ja liian arvoliberaaliksi. Mutta onko näin? Tätä voi analysoida melko neutraalisti suurella kielimallilla. 

![YLEn uutisten poliittisuuden jakauma](/images/YLE/jakauma.png)<br>
_Kuvio 1. YLEn uutisjuttujen poliitisen näkökulma (vaaka-akseli) ja arvojen (pystyakseli) yhteisjakauma._

1 Menetelmä ja aineisto
===

Suurella kielimallilla voi luokitella kirjoituksia. Tässä käytetään Anthropicin Claude Opus 4.0 -mallia.
Tarkastelemme 83 uutista YLEn verkkosivuilla, jotka haettiin scraperilla. Aineistosta on poistettu 7 uutista, joita scraper ei onnistunut keräämään kunnolla (pääosin vain otsikko tuli mukaan ja varsinainen teksti jäi pois). Lisäksi yhdessä tapauksessa Claude ei osannut tuottaa numeerista arviota.
Tulokset lähdeviittauksiin ovat liitteenä blogin lopussa.

Promptit, joita analyysissä on käytetty ovat kaikessa yksinkertaisuudessaan tällainen (mitään muuta promptia ei analyysissä käytetä):
Systeemi-prompti:
> You are an AI assistant tasked with analyzing political biases in works. Your goal is to provide insightful commentary on polical leaning, and liberal/conservative leaning. output in JSON format with keys: \“arvot\” (asteikko (-10,10)), \"poliittinen suuntaus\" (asteikko (-10,10)), \"perustelut arvot\", and \"perustelut poliittinen suuntaus\".\n

Analyysi-prompti:
> Analysoi kirjoitus. Onko se kirjoitettu arvoliberaalista vai arvokonservatiivisesta näkökulmasta? arvioi asteikolla (-10,10). Arvo -10 tarkoittaa hyvin arvoliberaalia, arvo 10 hyvin arvokonservatiivista. Entä onko se kirjoitettu vasemmistolaisesta vai oikeistolaisesta näkökulmasta? arvioi asteikolla (-10,10). Arvo -10 tarkoittaa hyvin vasemmistolaista, arvo 10 hyvin oikeistolaista. Vastaa JSON muodossa. (encode special chars properly)

Promptin tarkoituksena on tuottaa numeerinen arvio YLEn kirjoituksen poliittisuudesta ja sen arvoista. Poliittisuus arvioidaan vasemmisto-oikeisto -akselilla, kun taas kirjoituksen arvot arvioidaan arvoliberaali-konservatiivi -akselilla. Näiden pitäisi vastata esimerkiksi Helsingin Sanomien tekemien arvokarttojen asteikkoja, vaikka metodologia on erilainen.

Jokaista tekstiä varten keskustelu avataan uudestaan, jotta aiemmat vastaukset eivät sotke tuloksia. Lämpötila on 1.0, jotta tulokset olisivat toistettavissa.

Blogin analyysin ei ole tarkoitus olla kattava. Aineistossa oli vain 83 juttua, joista 76 päätyi lopulliseen analyysiin. Laajempi tutkimus kertoisi paremmin, miten neutraalia Ylen uutisointi on ja paikallistaisi mahdolliset ylilyönnit eri suuntiin. Samaa metodologiaa voi käyttä helposti muihinkin viestintävälineisiin. 
Clauden vastaukset muuttuvat eri ajokerroilla hieman, vaikka promptit ja aineistot pysyvät samoina. Vaihtelu ei kuitenkaan vaikuta oleva kovin suurta.


2 Arvot ja poliittisuus
===

Kirjoitusten arvojen keskiarvo on -0,84 ja mediaani 0,0, kun asteikko on -10 -- +10. Kirjoitusten arvot ovat lähellä neutraalia, vaikka ne painottuvat arvoliberaaliin suuntaan.

![YLEn uutisten arvojen jakauma](/images/YLE/arvot.png)<br>
_Kuvio 2. YLEn uutisjuttujen arvojen jakauma._

Arvojen jakauma painottuu arvoliberaaliin suuntaan. Kuitenkin selvästi arvokonservatiivisia havaintoja on myös joukossa.

![YLEn uutisten poliittisuuden jakauma](/images/YLE/poliittinen.png)<br>
_Kuvio 3. YLEn uutisjuttujen poliittisuuden jakauma._

Kirjoitusten poliittisen näkökulmien keskiarvo on -0,63 ja mediaani 0,0. Asteikko on -10 -- +10. Kirjoitusten arvot ovat lähellä neutraalia, vaikka niiden näkökulmaat keskimäärin painottuvat vasemmistoon.

Arvojen ja polittiisen näkökulman Yhteisjakauma (Kuvio 1) näyttää että suurin osa uutisista on vasemmisto/arvoliberaali - oikeisto/arvokonservatismi -akselilla. Yhteisjakaumassa on vähän havaintoja oikeisto/arvoliberaali -neljänneksestä tai vasemmisto/arvokonservatiivi -neljänneksestä. Tämä sama ilmiö näkyy vaalien yhteydessä tehdyissä ehdokkaiden arvokartoissa.

3 Esimerkkejä tuloksista
===

3.1 Sudenmetsästys
==

Sudenmetsästyksestä kertova [juttu](https://yle.fi/a/74-20165944) arvioidaan lievästi arvokonservatiiviseksi (+2) ja maltillisen oikeistolaiseksi (+3).

> Suden metsästyksen helpottaminen on tyypillisesti oikeistolainen teema, joka korostaa maaseudun elinkeinoja, omaisuuden suojaa ja yksilön oikeuksia suhteessa ympäristönsuojeluun. Toisaalta tekstissä mainitaan hoitosuunnitelman päivitys ja lupamenettely, jotka viittaavat sääntelyyn. Kokonaisuutena lievästi oikeistolainen sävy.

> Kirjoitus käsittelee suden metsästyksen mahdollistamista, mikä yleisesti liittyy arvokonservatiiviseen näkemykseen perinteisistä elinkeinoista, maaseudun elämäntavasta ja ihmisen oikeudesta hallita luontoa. Teksti on kuitenkin neutraalisti muotoiltu uutinen, joka ei ota voimakkaasti kantaa puolesta tai vastaan.

3.2 Vaalirahoitus
==
Vaalirahoituksesta kertova [juttu](https://yle.fi/a/74-20167070) arvioidaan arvoliberaaliksi (-3,5) ja vasemmistolaisesta näkökulmasta kirjoitetuksi (-6).

> Kirjoitus on selvästi kriittinen oikeistohallituksen päätöstä kohtaan nostaa vaalirahoituksen ilmoitusrajoja. Se nostaa esiin opposition (SDP, Vihreät) kriittiset kannat ja antaa heille äänen. Lisäksi mainitaan, että ehdotus tuli kokoomuksen Vestmanilta, ei hallituksen esityksestä. Kirjoitus korostaa huolta siitä, että raha saa liikaa valtaa vaaleissa, mikä on tyypillinen vasemmistolainen huolenaihe.

> Kirjoitus korostaa vaalirahoituksen avoimuutta ja läpinäkyvyyttä demokratian edellytyksenä. Tämä on liberaali arvo, sillä se painottaa kansalaisten oikeutta tietää ja vallan valvontaa. Kirjoitus esittää kriittisesti hallituksen päätöksen nostaa ilmoitusrajoja, mikä viittaa avoimuuden ja läpinäkyvyyden arvostamiseen.

3.3 Jalkaväkimiinat
==

Jalkaväkimiinakiellosta kertovat [juttu](https://yle.fi/a/74-20167408) arvioidaan selvästi arvokonservatiiviseksi (+5) ja näkökulmaltaan oikeistolaiseksi (+4).

> Tekstissä kannatetaan Ottawan sopimuksesta irtautumista ja jalkaväkimiinojen palauttamista puolustusjärjestelmään turvallisuustilanteen perusteella. Tämä on arvokonservatiivinen kanta, koska se asettaa turvallisuuden ihmisoikeuksien ja kansainvälisten humanitaaristen sopimusten edelle. Kansainvälisistä sopimuksista irtautuminen on myös konservatiivista reaalipolitiikkaa.

> Jalkaväkimiinoista luopuminen ja kansainvälisten sopimusten allekirjoittaminen on ollut erityisesti vasemmiston ja liberaalien puolueiden ajama linja. Irtautumisen kannattaminen on pikemminkin oikeiston ja keskustan turvallisuuspoliittista linjaa. Että vain vasemmistoliitto jätti eriävän mielipiteen tukee tätä tulkintaa.

3.4 Sofia Virta
==

Sofia Virraste kertova [juttu](https://yle.fi/a/74-20163230) arvioidaan lievästi arvoliberaaliksi (-3) ja maltillisen vasemmistolaiseksi (-3).

> Kirjoitus lähtee lievästi arvoliberaalista näkökulmasta. Tämä näkyy esimerkiksi myönteisenä asenteena maahanmuuttajanuoriin, sukupuolten tasa-arvokysymyksiin ja kriittisenä näkemyksenä perussuomalaisten politiikkaa kohtaan. Kuitenkin näkökulma pysyy suhteellisen neutraalina toimittajan roolissa.

> Kirjoitus on lievästi vasemmistolainen. Puheenjohtaja Sofia Virta korostaa hyvinvointivaltion pelastamista, lasten ja nuorten suojelemista leikkauksilta, sekä ympäristönäkökulmia. Kirjoitus käsittelee oppositiossa olevan vihreän puolueen näkemyksiä oikeistohallitusta vastaan, mikä tuo vasemmistolaisen näkökulman esiin.

3.5 Mika Poutala
==

Mika Poutalasta kertova [juttu](https://yle.fi/a/74-20162150) arvioidaan arvoneutraaliksi (0) ja poliittisesti neutraaliksi (0).

> Teksti on neutraali reportaasi henkilön liikuntaharrastuksista ja ministerinimityksen kuvaus. Siinä ei ole arvovalintoihin viittaavia elementtejä tai kannanottoja yhteiskunnallisiin arvoihin. Keskittyy vain faktojen esittämiseen henkilön taustoista ja tavoista.

> Teksti ei ota kantaa vasemmisto-oikeisto-akseliin liittyviin kysymyksiin. Se on puhdas henkilöön liittyvä faktakuvaus ilman poliittisia kannanottoja tai viittauksia talouspolitiikkaan, hyvinvointivaltioon tai muihin poliittisiin kysymyksiin. Kristillisdemokraattinen puoluetausta mainitaan, mutta sitä ei arvoteta.

4 Yhteenveto
===

Onko Ylen uutiskirjoittaminen epäpoliittista ja arvovapaata? Ei, mutta se on kylläkin melko neutraalia. Toimittajan oma arvomaailma näkyy jutuissa, mutta niin sen tietyssä määrin pitääkin. Tuloksissa näkyy lievä vasemmistolais-arvoliberaali painotus, mutta verrattuna julkisen keskustelun käsityksiin, vinouma on pientä. Tämän analyysin lopputulos on se, että melko pienellä viilauksella Yle voisi tehdä omasta uutistoiminnasta vieläkin neutraalimpaa.  


Liite
===

|    | otsikko                                                                                                                       | Linkki                            |   arvot |   poliittinen suuntaus |
|---:|:------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|--------:|-----------------------:|
|  0 | Päätös eduskunnan pääsihteeri Antti Pelttarin hyllyttämisestä siirtyi ensi keskiviikkoon                                      | https://yle.fi/a/74-20167571      |    -2   |                    0   |
|  1 | Mikko Polvinen ehdolla Perussuomalaisten kolmanneksi varapuheenjohtajaksi                                                     | https://yle.fi/a/74-20167573      |     3   |                    5   |
|  2 | Valiokunta visioi jalkaväkimiinoista vientituotetta Suomelle                                                                  | https://yle.fi/a/74-20167477      |     2   |                    3   |
|  3 | SDP:n Tuppurainen: Ryhmä teki päätöksen tukea miinasopimuksesta lähtemistä, ja se sitoo kaikkia edustajia                     | https://yle.fi/a/74-20167519      |     0   |                    0   |
|  4 | Professori katsoo, että eduskunnan pääsihteeri Antti Pelttari tulisi pidättää virastaan – epäillään virkarikoksista           | https://yle.fi/a/74-20167469      |     0   |                    0   |
|  5 | Saamelaislaki repii hallituspuolueiden rivejä, RKP:n Adlercreutz pitää perussuomalaisten irtiottoja valitettavina             | https://yle.fi/a/74-20167423      |    -6   |                   -3   |
|  6 | ”Jos joku on alisuoriutunut, se on hallitus” – oppositio arvosteli irtisanomisten helpottamista kyselytunnilla                | https://yle.fi/a/74-20167394      |    -2   |                   -7   |
|  7 | Hämmentävä tilanne: vasemmistoliitto ei kerro, onko kansanedustaja Johannes Yrttiaho yhä puolueen jäsen                       | https://yle.fi/a/74-20167392      |     0   |                   -2   |
|  8 | Puolustusvaliokunta puoltaa miinasopimuksesta irtautumista                                                                    | https://yle.fi/a/74-20167408      |     5   |                    4   |
|  9 | Presidentti Stubb osallistuu Bilderberg-tapaamiseen Tukholmassa – mukana myös Sanna Marin                                     | https://yle.fi/a/74-20167377      |     0   |                    0   |
| 10 | Elinkeinoministeriksi nousee pian perussuomalainen fysiikan tohtori, jota kehutaan jopa oppositiosta                          | https://yle.fi/a/74-20165321      |    -4   |                   -3   |
| 12 | Ex-ministeri Carl Haglund valittiin Aktian toimitusjohtajaksi                                                                 | https://yle.fi/a/74-20167326      |     0   |                    0   |
| 13 | Israelin parlamentti torppasi opposition aloitteen parlamentin hajottamisesta                                                 | https://yle.fi/a/74-20167286      |     0   |                    0   |
| 14 | Sebastian Tynkkynen hakee perus­suomalaisten kolmanneksi vara­puheenjohtaksi                                                  | https://yle.fi/a/74-20167274      |     2   |                    6   |
| 15 | HS: Lulu Ranteen mukaan alaikäisten yöajeluun ajetaan lakimuutosta jo tänä vuonna                                             | https://yle.fi/a/74-20167235      |     3   |                    2   |
| 16 | Eduskunta hyväksyi esityksen saamelaiskäräjälain muuttamisesta ensimmäisessä käsittelyssä                                     | https://yle.fi/a/74-20167217      |     2   |                   -2   |
| 17 | Turun tunnin junasta neuvotellaan jälleen tauon jälkeen – rahoituksesta puuttuu 500 miljoonaa euroa                           | https://yle.fi/a/74-20167142      |    -2   |                   -1   |
| 18 | Kokoomuslainen Multialta ja vasemmistolainen Torniosta kertovat, miksi allekirjoittivat Sinimustan liikkeen kannattajakortit  | https://yle.fi/a/74-20166905      |    -6   |                   -4   |
| 19 | Eduskunta päätti: Suurempia summia vaalirahaa voi jatkossa antaa nimettömästi                                                 | https://yle.fi/a/74-20167070      |    -3.5 |                   -6   |
| 20 | Uusnatsit yrittivät järjestää salaa kesätapahtuman, mutta Sinimustan liikkeen aktiivit paljastivat vahingossa osallistujia    | https://yle.fi/a/74-20167106      |    -6   |                   -5   |
| 21 | Häkkänen Ylelle: Kaikki puolueet otetaan sittenkin mukaan päättämään puolustusmenoista                                        | https://yle.fi/a/74-20167114      |     0   |                    1   |
| 22 | Katso video: Eero Reijosen 24 vuoden ura puheenjohtajana päättyi Liperissä – koki ilkeilyksi ja julisti muuttavansa pois      | https://yle.fi/a/74-20166985      |     0   |                    0   |
| 23 | Sara Seppänen kohautti lapintakissaan eduskunnassa – haluaa tukea metsälappalaisen kulttuurin elvyttämistä                    | https://yle.fi/a/74-20166967      |    -2.5 |                   -2   |
| 24 | Vihreiden Hanna-Kaisa Lähde etsi rakkautta – näin kävi, kun hän löysi perussuomalaisen miehen                                 | https://yle.fi/a/74-20165699      |    -4   |                   -1   |
| 25 | Nato haluaa jäsenmaiden puolustusmenot viiteen prosenttiin BKT:sta – Yle selvitti kaikkien puolueiden kannat                  | https://yle.fi/a/74-20166824      |     1   |                    0   |
| 26 | Ylen lähteet: Suomi ei ole lupaamassa Palestiinan valtion tunnustamista ensi viikon YK-kokouksessa                            | https://yle.fi/a/74-20166852      |     0   |                    0   |
| 27 | Kuvernööri Newsom vie Trumpin kansalliskaartipäätöksen oikeuteen – Valkoinen talo ”tyytyväinen” vastakkainasetteluun          | https://yle.fi/a/74-20166906      |    -3   |                   -4   |
| 28 | Analyysi: Suomen turvallisuuspolitiikan johtajiin iski vauhtisokeus                                                           | https://yle.fi/a/74-20166823      |    -2   |                   -3   |
| 29 | IL: Mauri Peltokangas ei haluakaan jatkaa perus­suomalaisten vara­puheen­johtajana                                            | https://yle.fi/a/74-20166995      |     0   |                    3   |
| 30 | Amerikkalaiskenraali tyrmää kansalliskaartin lähettämisen Los Angelesiin                                                      | https://yle.fi/a/74-20166874      |    -6   |                   -7   |
| 31 | Saarikolle ja Nurmiselle vapautus kansanedustajan tehtävästä                                                                  | https://yle.fi/a/74-20166984      |     0   |                    0   |
| 32 | Kultaranta-keskustelut alkavat ensi maanantaina – teemana muuttuva maailmanjärjestys                                          | https://yle.fi/a/74-20166853      |     0   |                    0   |
| 34 | Vasemmistoliiton varakansanedustaja eroaa puolueesta – kritisoi Johannes Yrttiahon saamaa kohtelua                            | https://yle.fi/a/74-20166886      |    -1   |                   -7   |
| 35 | Isotalus ja Pietilä Kokkolan johtoon                                                                                          | https://yle.fi/a/74-20166799      |     0   |                    0   |
| 36 | Eduskunta hakee entiseltä kansanedustajalta Ano Turtiaiselta ulosotossa kymmeniätuhansia euroja                               | https://yle.fi/a/74-20166725      |     0   |                    0   |
| 37 | Rovaniemen ympäristölautakunnan puheenjohtajiksi lyhytvuokrauksen harjoittaja ja kriitikko                                    | https://yle.fi/a/74-20166760      |     1   |                   -3   |
| 38 | Yhteinen kotikuntamme -ryhmä ei saanut yhtään puheenjohtajan paikkaa Ranualla, vaikka mikään ryhmä ei ole sitä suurempi       | https://yle.fi/a/74-20166757      |    -2   |                    0   |
| 39 | Oppositio vaatii laajempaa keskustelua puolustusmenojen nostosta – Häkkänen vetoaa kiireeseen                                 | https://yle.fi/a/74-20166708      |     2   |                    3   |
| 40 | Mauri Pekkarinen valittiin odotetusti Jyväskylän kaupungin­valtuuston puheen­johtajaksi                                       | https://yle.fi/a/74-20166752      |     0   |                    0   |
| 41 | Pitkäaikaisen kaupungin­johtajan potkut käynnistivät Savonlinnassa täydellisen johdon uudistumisen                            | https://yle.fi/a/74-20164531      |    -2   |                   -1   |
| 42 | Tutkijat: Keskustelussa puolustus­menoista tapahtui käänne – opposition kritiikki mursi yksimielisyyden                       | https://yle.fi/a/74-20166441      |     2   |                   -3   |
| 43 | ”Teemmekö jotain väärin?” – vihreiden edustajat pohtivat keinoja kannatusalhon murtamiseksi                                   | https://yle.fi/a/74-20166440      |    -4   |                   -6   |
| 44 | Matthew Kern pyörittää kahvilaa Helsingissä, mutta silti häntä saattaa uhata häätö Suomesta uuden lain takia                  | https://yle.fi/a/74-20166230      |    -4   |                   -3   |
| 45 | Analyysi: Miten vihreät saisi piristettyä kannatustaan, joka muistuttaa kuolleen sydänkäyrää?                                 | https://yle.fi/a/74-20166386      |    -1   |                   -1   |
| 46 | Hallitus linjasi isoista korotuksista puolustusmenoihin – oppositio älähti                                                    | https://yle.fi/a/74-20166398      |    -2   |                   -3   |
| 47 | Vihreät sai uudet varapuheenjohtajat: Allu Pyhälammi, Jenni Pitko ja Shawn Huff                                               | https://yle.fi/a/74-20165964      |    -2   |                   -3   |
| 48 | Orpo Venäjä-pakotteista: Nyt pitäisi saada päätöksiä, meidän pitää pakottaa Putin neuvottelupöytään                           | https://yle.fi/a/74-20166342      |    -1   |                    2   |
| 49 | Vihreiden Tynkkynen tyytymätön hallitukseen: Puolustusmenojen nostosta miljardeilla pitää keskustella enemmän                 | https://yle.fi/a/74-20165910      |    -6   |                   -7   |
| 50 | Urheiluministerinä aloittava Mika Poutala juoksee 15 kilometrin työmatkansa – aikoo vaikuttaa erityisesti apurahoihin         | https://yle.fi/a/74-20162150      |     0   |                    0   |
| 51 | Brittitutkija Stubbin roolista maailman­politiikassa: ”Tärkeät suunnitelmat ovat tosiasiassa syntyneet Helsingissä”           | https://yle.fi/a/74-20163672      |    -1   |                    2   |
| 52 | Vihreiden puoluekokous alkaa Hämeenlinnassa                                                                                   | https://yle.fi/a/74-20166328      |     0   |                    0   |
| 53 | Suomen Lappiin tuleva Nato-joukko alkaa rakentua: Britannia mukana                                                            | https://yle.fi/a/74-20166307      |     2   |                    3   |
| 54 | Saamelaiskäräjien hallitus hyväksyi perustuslakivaliokunnan muutosehdotukset                                                  | https://yle.fi/a/74-20166308      |     0   |                    0   |
| 55 | Puolustusmenot nousemassa miljardeilla – Orpo: Venäjän uhan takia Suomen puolustus on pakko hoitaa                            | https://yle.fi/a/74-20166298      |     0   |                    6   |
| 56 | Vihreiden venäläinen ehdokas ei kelvannut Lieksan kaupungin elinkeino­yhtiöön – puolue syyttää syrjinnästä                    | https://yle.fi/a/74-20166288      |    -4   |                   -2   |
| 57 | Lentoliikenteen työriidassa ei sopua perjantaina, sovittelu jatkuu maanantaina                                                | https://yle.fi/a/74-20166283      |     0   |                    0   |
| 58 | Puheenjohtaja uskoo, että ongelmat Turun vasemmisto­liitossa ovat vihdoin ohi: ”Tämä on ollut tosi pitkä tie”                 | https://yle.fi/a/74-20166133      |    -2   |                   -3   |
| 59 | Analyysi: Kansanedustajia lähtee eduskunnasta kuin hollituvasta, mutta ei Arkadianmäestä kannata vankilaakaan tehdä           | https://yle.fi/a/74-20166141      |     2   |                    0   |
| 60 | Ilmari Nurminen pyysi eroa eduskunnasta                                                                                       | https://yle.fi/a/74-20166275      |     0   |                    0   |
| 61 | Oliver Stubb erottui ”selvästi muista hakijoista” – sai harjoittelu­paikan presidentti-isänsä erikoisalalta                   | https://yle.fi/a/74-20166232      |    -1   |                    0   |
| 62 | Uudenkaupungin ääni palaa eduskuntaan – Mauri Kontu ottaa haasteen vastaan Annika Saarikon seuraajana                         | https://yle.fi/a/74-20166199      |     2   |                    3   |
| 63 | Alankomaissa äänestetään uudesta hallituksesta lokakuussa                                                                     | https://yle.fi/a/74-20166219      |    -1   |                    0   |
| 64 | Hallitus sai eduskunnan luottamuksen välikysymysäänestyksessä                                                                 | https://yle.fi/a/74-20166179      |    -1   |                   -3   |
| 65 | Annika Saarikko jättää valtakunnanpolitiikan ja siirtyy YTHS:n toimitusjohtajaksi                                             | https://yle.fi/a/74-20166132      |     0   |                    0   |
| 66 | Sofia Virta tietää, milloin ei kannata puhua ilmastokriisistä – nyt hän kertoo puolueen talousteesit                          | https://yle.fi/a/74-20163230      |    -3   |                   -3   |
| 67 | Kontiolahdella hylättiin eniten ääniä kevään kuntavaaleissa – katso missä kunnissa ääniä mitätöitiin eniten                   | https://yle.fi/a/74-20166096      |     0   |                    0   |
| 68 | USU: Hyvinvointialueet hakevat joukolla lisää rahaa                                                                           | https://yle.fi/a/74-20166089      |     0   |                   -1   |
| 69 | Analyysi: Trump sai tahtonsa läpi Natossa                                                                                     | https://yle.fi/a/74-20166052      |     0   |                    2   |
| 70 | Trump ja Saksan Merz kohtasivat Valkoisessa talossa – ”Antaa lapsien tapella”, totesi Trump Ukrainasta                        | https://yle.fi/a/74-20166047      |     0   |                    1   |
| 71 | Hallitus tiukentaa pysyvän oleskeluluvan ehtoja – edellytyksiin kuuluu kielitaito, bonusta 40 000 euron vuosituloista         | https://yle.fi/a/74-20166033      |     4   |                    6   |
| 72 | Kansanedustaja Karoliina Partanen kertoo joutuneensa seksuaalisen häirinnän kohteeksi – oikeudenkäynti maanantaina            | https://yle.fi/a/74-20165996      |    -3   |                    0   |
| 74 | Ministeriö haluaa, että susia voisi metsästää Suomessa jo ensi vuonna                                                         | https://yle.fi/a/74-20165944      |     3   |                    2   |
| 75 | Katso paljon puhuva video, jolla ministerit kommentoivat rasismikoulutusta – Wille Rydman vastaa pitkän hiljaisuuden jälkeen  | https://yle.fi/a/74-20165908      |    -4   |                   -3   |
| 76 | Halla-aho: Kukaan ei epäile Antti Pelttaria maanpetoksesta, eduskunnan kansliatoimikunta päätti lisäkuulemisista              | https://yle.fi/a/74-20165925      |    -2.5 |                    0.5 |
| 77 | Suomeakin odottaa puolustuksen miljardilasku – Häkkänen: Seuraava hallitus voi rahoittaa tekemällä cocktailin                 | https://yle.fi/a/74-20165890      |     0   |                    2   |
| 78 | Analyysi: Ukrainan taitava drooni-isku voi johtaa sodan kiihtymiseen                                                          | https://yle.fi/a/74-20165854      |    -3   |                   -2   |