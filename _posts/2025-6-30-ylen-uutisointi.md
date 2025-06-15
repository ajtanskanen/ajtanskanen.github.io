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

Ylen uutisointia on toisinaan arvosteltu vihervasemistolaiseksi ja liian arvoliberaaliksi. Tätä voi analysoida melko neutraalisti suurella kielimallilla. 

1 Menetelmä ja aineisto
===

Suurella kielimallilla voi luokitella kirjotuksia. Tässä käytetään Anthropicin Claude Opus 4.0 -mallia.
Tarkastelemme 83 uutista YLEn verkkosivuilla, jotka haettiin scraperilla. Aineistosta on poistettu 7 uutista, joita scraper ei onnistunut keräämään kunnolla (pääosin vain otsikko tuli mukaan ja varsinainen teksti jäi pois). Lisäksi yhdessä tapauksessa (numero 11) Claude ei osannut tuottaa numeerista arviota.
Aineisto ja tulokset ovat liitteenä blogin lopussa.

Promptit, joita analyysissä on käytetty ovat kaikessa yksinkertaisuudessaan tällainen (mitään muuta promptia ei analyysissä käytetä):
Systeemi-prompti:
> You are an AI assistant tasked with analyzing political biases in works. Your goal is to provide insightful commentary on polical leaning, and liberal/conservative leaning. output in JSON format with keys: \“arvot\” (asteikko (-10,10)), \"poliittinen suuntaus\" (asteikko (-10,10)), \"perustelut arvot\", and \"perustelut poliittinen suuntaus\".\n

Analyysi-prompti:
> Analysoi kirjoitus. Onko se kirjoitettu arvoliberaalista vai arvokonservatiivisesta näkökulmasta? arvioi asteikolla (-10,10). Arvo -10 tarkoittaa hyvin arvoliberaalia, arvo 10 hyvin arvokonservatiivista. Entä onko se kirjoitettu vai oikeistolaisesta näkökulmasta? arvioi asteikolla (-10,10). Arvo -10 tarkoittaa hyvin vasemmistolaista, arvo 10 hyvin oikeistolaista. Vastaa JSON muodossa. (encode special chars properly)

Promptin tarkoituksena on tuottaa numeerinen arvio YLEn kirjoituksen poliittisuudesta ja sen arvoista. Poliittisuus arvioidaan vasemmisto-oikeisto -akselilla, kun taas kirjoituksen arvot arvioidaan arvoliberaali-konservatiivi -akselilla. Näiden pitäisi vastata esimerkiksi Helsingin Sanomien tekemien arvokarttojen asteikkoja, vaikka metodologia on erilainen.

Jokaista tekstiä varten keskustelu avataan uudestaan, jotta aiemmat vastaukset eivät sotke tuloksia. Lämpötila on 1.0, jotta tulokset olisivat toistettavissa.

2 Arvot ja poliittisuus
===

Kirjoitusten arvojen keskiarvo on -1,45 ja mediaani -0,5. Asteikko on -10 -- +10, joten keskimäärin kirjoitusten arvot ovat lähellä neutraalia, vaikka ne painottuvat arvoliberaaliin suuntaan.

![YLEn uutisten arvojen jakauma](/images/YLE/arvot.png)<br>
_Kuvio 1. YLEn uutisten arvojen jakauma._

Arvojen jakauma painottuu arvoliberaaliin suuntaan.

![YLEn uutisten poliittisuuden jakauma](/images/YLE/poliittinen.png)<br>
_Kuvio 2. YLEn uutisten poliittisuuden jakauma._

Kirjoitusten poliittisen näkökulman keskiarvo on -1,45 ja mediaani -0,5. Asteikko on -10 -- +10, joten keskimäärin kirjoitusten arvot ovat lähellä neutraalia, vaikka ne painottuvat arvoliberaaliin suuntaan.

Poliittisten näkökulmien jakauma painottuu vasemmistoon.

![YLEn uutisten poliittisuuden jakauma](/images/YLE/jakauma.png)<br>
_Kuvio 3. YLEn uutisten yhteisjakauma._

Arvojen ja polittiisen näkökulman Yhteisjakauma...

3 Esimerkkejä tuloksista
===

3.1 Sudenmetsästys
==

Esimerkiksi sudenmetsästyksestä kertovat juttu (https://yle.fi/a/74-20165944) arvioidaan arvokonservatiiviseksi (+5) ja lievästi oikeistolaiseksi (+3), koska 

> Kirjoitus käsittelee sudenmetsästyksen mahdollistamista, mikä heijastaa jossain määrin arvokonservatiivista näkemystä, jossa korostetaan ihmisen oikeutta hallita luontoa ja maaseudun elinkeinojen suojelua. Teksti on kuitenkin neutraalisti muotoiltu, eikä siinä oteta voimakkaasti kantaa suuntaan tai toiseen. Arvoliberaali näkökulma korostaisi todennäköisesti enemmän luonnonsuojelua ja eläinten oikeuksia.

> Kirjoitus on sävyltään melko neutraali uutisteksti, joka kertoo ministeriön toimista. Kuitenkin susimetsästyksen helpottaminen liittyy usein maaseudun elinkeinojen, kuten karjatalouden ja metsästyksen edistämiseen, jotka ovat perinteisesti oikeistolaisia teemoja. Vasemmistolaisesta näkökulmasta korostettaisiin todennäköisesti enemmän ympäristönsuojelua ja luonnon monimuotoisuutta.

3.2 Vaalirahoitus
==
vastaavasti vaalirahoituksesta kertova juttu (https://yle.fi/a/74-20167070) arvioidaan arvoliberaaliksi (-5) ja vasemmistolaisesta näkökulmasta kirjoitetuksi (-5), koska

> Kirjoitus on kirjoitettu vasemmistolaisesta näkökulmasta. Tämä näkyy siinä, että oppositiopuolueiden (SDP, Vihreät) kriittiset näkemykset nostetaan keskeisesti esiin, erityisesti Tiina Elon kommentti siitä, että vaalit eivät saa olla rahalla ratkaistava kilpailu. Myös oikeusministeriön ja Transparency Internationalin vastustus mainitaan. Kokoomuksen perustelut muutokselle esitetään lyhyesti ilman syvempää analyysiä, mikä viittaa kriittiseen näkökulmaan hallituksen toimintaa kohtaan.

> Kirjoitus on kirjoitettu arvoliberaalista näkökulmasta, sillä siinä korostetaan poliittisen rahoituksen avoimuutta ja läpinäkyvyyttä. Kirjoituksessa tuodaan kriittisesti esiin ilmoitusrajan nostaminen ja nostetaan esiin opposition ja järjestöjen huolta vaalirahoituksen avoimuuden vähenemisestä. Avoimuuden ja demokraattisen läpinäkyvyyden korostaminen on tyypillisesti arvoliberaali positio.

3.3 Miinat
==

- arvot: 4
- poliittinen suuntaus: 5

> Kirjoitus on miltei neutraali uutismaisessa sävyssään, mutta siinä ei kyseenalaisteta miinojen käyttöönottoa humanitääriseltä kannalta. Siitä puuttuvat ihmisoikeusjärjestöjen huolet siviileistä ja vammoista. Vasemmistoliiton ja SPR:n kriittinen kanta mainitaan vain ohimennen. Tämä viittaa arvokonservatiiviseen painotukseen, jossa turvallisuus ja taloudelliset mahdollisuudet menevät humanitääristen näkökohtien edelle.

> Kirjoitus keskittyy positiivisesti puolustusteollisuuden liiketoimintamahdollisuuksiin ja vientipotentiaaliin. Keskustan edustajan näkemykset esitetään kritiikittä. Tekstissä korostetaan osaamista ja tuotantokykyä, ei työntekijöiden oikeuksia tai sosiaalisia vaikutuksia. Mainehaitat käsitellään lähinnä liiketoiminnallisina riskeinä, ei eettisinä ongelmina. Nämä viittaavat maltilliseen oikeistolaiseen näkökulmaan.

4 Analyysin puutteet
===

Tämän blogin analyysin ei ole tarkoitus olla kattava. Aineistossa oli vain 83 juttua, joista 76 päätyi lopulliseen analyysiin. Laajempi tutkimus kertoisi paremmin, miten neutraalia Ylen uutisointi on ja paikallistaisi mahdolliset ylilyönnit eri suuntiin. Samaa metodologiaa voi käyttä helposti muihinkin viestintävälineisiin.

5 Yhteenveto
===

Onko Ylen uutiskirjoittaminen epäpoliittista ja arvovapaata? Ei, mutta se on kylläkin melko neutraalia. Toimittajan oma arvomaailma näkyy jutuissa, mutta niin sen tietyssä määrin pitääkin. Tuloksissa näkyy lievä vasemmistolais-arvoliberaali painotus, mutta verrattuna julkisen keskustelun käsityksiin, vinouma on pientä. Tämän analyysin lopputulos on se, että melko pienellä viilauksella Yle voisi tehdä omasta uutistoiminnasta vieläkin neutraalimpaa.  


Liite
===


|    | otsikko                                                                                                                      | Linkki                       |   arvot |   poliittinen suuntaus |
|---:|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------|--------:|-----------------------:|
|  0 | Päätös eduskunnan pääsihteeri Antti Pelttarin hyllyttämisestä siirtyi ensi keskiviikkoon                                     | https://yle.fi/a/74-20167571 |     1   |                    2   |
|  1 | Mikko Polvinen ehdolla Perussuomalaisten kolmanneksi varapuheenjohtajaksi                                                    | https://yle.fi/a/74-20167573 |     0   |                    2   |
|  2 | Valiokunta visioi jalkaväkimiinoista vientituotetta Suomelle                                                                 | https://yle.fi/a/74-20167477 |     5   |                    5   |
|  3 | SDP:n Tuppurainen: Ryhmä teki päätöksen tukea miinasopimuksesta lähtemistä, ja se sitoo kaikkia edustajia                    | https://yle.fi/a/74-20167519 |     0   |                    0   |
|  4 | Professori katsoo, että eduskunnan pääsihteeri Antti Pelttari tulisi pidättää virastaan – epäillään virkarikoksista          | https://yle.fi/a/74-20167469 |    -1   |                    0   |
|  5 | Saamelaislaki repii hallituspuolueiden rivejä, RKP:n Adlercreutz pitää perussuomalaisten irtiottoja valitettavina            | https://yle.fi/a/74-20167423 |     4   |                   -2   |
|  6 | ”Jos joku on alisuoriutunut, se on hallitus” – oppositio arvosteli irtisanomisten helpottamista kyselytunnilla               | https://yle.fi/a/74-20167394 |    -5   |                   -6   |
|  7 | Hämmentävä tilanne: vasemmistoliitto ei kerro, onko kansanedustaja Johannes Yrttiaho yhä puolueen jäsen                      | https://yle.fi/a/74-20167392 |     0   |                    0   |
|  8 | Puolustusvaliokunta puoltaa miinasopimuksesta irtautumista                                                                   | https://yle.fi/a/74-20167408 |     3   |                    5   |
|  9 | Presidentti Stubb osallistuu Bilderberg-tapaamiseen Tukholmassa – mukana myös Sanna Marin                                    | https://yle.fi/a/74-20167377 |    -3   |                    3   |
| 10 | Elinkeinoministeriksi nousee pian perussuomalainen fysiikan tohtori, jota kehutaan jopa oppositiosta                         | https://yle.fi/a/74-20165321 |     2   |                   -3   |
| 11 | Netin halpakauppojen suitsimista vaativa kansalaisaloite menee eduskuntaan                                                   | https://yle.fi/a/74-20167299 |   nan   |                  nan   |
| 12 | Ex-ministeri Carl Haglund valittiin Aktian toimitusjohtajaksi                                                                | https://yle.fi/a/74-20167326 |     0   |                    0   |
| 13 | Israelin parlamentti torppasi opposition aloitteen parlamentin hajottamisesta                                                | https://yle.fi/a/74-20167286 |     0   |                    0   |
| 14 | Sebastian Tynkkynen hakee perus­suomalaisten kolmanneksi vara­puheenjohtaksi                                                 | https://yle.fi/a/74-20167274 |     3   |                    6   |
| 15 | HS: Lulu Ranteen mukaan alaikäisten yöajeluun ajetaan lakimuutosta jo tänä vuonna                                            | https://yle.fi/a/74-20167235 |     3   |                    1   |
| 16 | Eduskunta hyväksyi esityksen saamelaiskäräjälain muuttamisesta ensimmäisessä käsittelyssä                                    | https://yle.fi/a/74-20167217 |    -4   |                   -3   |
| 17 | Turun tunnin junasta neuvotellaan jälleen tauon jälkeen – rahoituksesta puuttuu 500 miljoonaa euroa                          | https://yle.fi/a/74-20167142 |     0   |                    0   |
| 18 | Kokoomuslainen Multialta ja vasemmistolainen Torniosta kertovat, miksi allekirjoittivat Sinimustan liikkeen kannattajakortit | https://yle.fi/a/74-20166905 |    -7   |                   -5   |
| 19 | Eduskunta päätti: Suurempia summia vaalirahaa voi jatkossa antaa nimettömästi                                                | https://yle.fi/a/74-20167070 |    -2   |                   -1   |
| 20 | Uusnatsit yrittivät järjestää salaa kesätapahtuman, mutta Sinimustan liikkeen aktiivit paljastivat vahingossa osallistujia   | https://yle.fi/a/74-20167106 |    -6   |                   -5   |
| 21 | Häkkänen Ylelle: Kaikki puolueet otetaan sittenkin mukaan päättämään puolustusmenoista                                       | https://yle.fi/a/74-20167114 |     0   |                   -2   |
| 22 | Katso video: Eero Reijosen 24 vuoden ura puheenjohtajana päättyi Liperissä – koki ilkeilyksi ja julisti muuttavansa pois     | https://yle.fi/a/74-20166985 |    -1   |                    0   |
| 23 | Sara Seppänen kohautti lapintakissaan eduskunnassa – haluaa tukea metsälappalaisen kulttuurin elvyttämistä                   | https://yle.fi/a/74-20166967 |     0   |                   -1   |
| 24 | Vihreiden Hanna-Kaisa Lähde etsi rakkautta – näin kävi, kun hän löysi perussuomalaisen miehen                                | https://yle.fi/a/74-20165699 |    -3   |                   -1   |
| 25 | Nato haluaa jäsenmaiden puolustusmenot viiteen prosenttiin BKT:sta – Yle selvitti kaikkien puolueiden kannat                 | https://yle.fi/a/74-20166824 |    -0.5 |                   -0.5 |
| 26 | Ylen lähteet: Suomi ei ole lupaamassa Palestiinan valtion tunnustamista ensi viikon YK-kokouksessa                           | https://yle.fi/a/74-20166852 |    -3   |                    0   |
| 27 | Kuvernööri Newsom vie Trumpin kansalliskaartipäätöksen oikeuteen – Valkoinen talo ”tyytyväinen” vastakkainasetteluun         | https://yle.fi/a/74-20166906 |    -5   |                   -4   |
| 28 | Analyysi: Suomen turvallisuuspolitiikan johtajiin iski vauhtisokeus                                                          | https://yle.fi/a/74-20166823 |    -3   |                   -4   |
| 29 | IL: Mauri Peltokangas ei haluakaan jatkaa perus­suomalaisten vara­puheen­johtajana                                           | https://yle.fi/a/74-20166995 |     0   |                    0   |
| 30 | Amerikkalaiskenraali tyrmää kansalliskaartin lähettämisen Los Angelesiin                                                     | https://yle.fi/a/74-20166874 |    -2   |                   -3   |
| 31 | Saarikolle ja Nurmiselle vapautus kansanedustajan tehtävästä                                                                 | https://yle.fi/a/74-20166984 |     0   |                    0   |
| 32 | Kultaranta-keskustelut alkavat ensi maanantaina – teemana muuttuva maailmanjärjestys                                         | https://yle.fi/a/74-20166853 |     0   |                    0   |
| 33 | Vasemmistoliiton varakansanedustaja eroaa puolueesta – kritisoi Johannes Yrttiahon saamaa kohtelua                           | https://yle.fi/a/74-20166886 |    -3   |                   -6   |
| 34 | Isotalus ja Pietilä Kokkolan johtoon                                                                                         | https://yle.fi/a/74-20166799 |     0   |                    0   |
| 35 | Eduskunta hakee entiseltä kansanedustajalta Ano Turtiaiselta ulosotossa kymmeniätuhansia euroja                              | https://yle.fi/a/74-20166725 |     0   |                    0   |
| 36 | Rovaniemen ympäristölautakunnan puheenjohtajiksi lyhytvuokrauksen harjoittaja ja kriitikko                                   | https://yle.fi/a/74-20166760 |    -4   |                   -3   |
| 37 | Yhteinen kotikuntamme -ryhmä ei saanut yhtään puheenjohtajan paikkaa Ranualla, vaikka mikään ryhmä ei ole sitä suurempi      | https://yle.fi/a/74-20166757 |     0   |                    0   |
| 38 | Oppositio vaatii laajempaa keskustelua puolustusmenojen nostosta – Häkkänen vetoaa kiireeseen                                | https://yle.fi/a/74-20166708 |    -5   |                    4   |
| 39 | Mauri Pekkarinen valittiin odotetusti Jyväskylän kaupungin­valtuuston puheen­johtajaksi                                      | https://yle.fi/a/74-20166752 |     0   |                    0   |
| 40 | Pitkäaikaisen kaupungin­johtajan potkut käynnistivät Savonlinnassa täydellisen johdon uudistumisen                           | https://yle.fi/a/74-20164531 |    -1   |                   -1   |
| 41 | Tutkijat: Keskustelussa puolustus­menoista tapahtui käänne – opposition kritiikki mursi yksimielisyyden                      | https://yle.fi/a/74-20166441 |     0   |                   -3   |
| 42 | ”Teemmekö jotain väärin?” – vihreiden edustajat pohtivat keinoja kannatusalhon murtamiseksi                                  | https://yle.fi/a/74-20166440 |    -6   |                   -6   |
| 43 | Matthew Kern pyörittää kahvilaa Helsingissä, mutta silti häntä saattaa uhata häätö Suomesta uuden lain takia                 | https://yle.fi/a/74-20166230 |    -6   |                   -4   |
| 44 | Analyysi: Miten vihreät saisi piristettyä kannatustaan, joka muistuttaa kuolleen sydänkäyrää?                                | https://yle.fi/a/74-20166386 |    -3   |                   -2   |
| 45 | Hallitus linjasi isoista korotuksista puolustusmenoihin – oppositio älähti                                                   | https://yle.fi/a/74-20166398 |     0   |                   -3   |
| 46 | Vihreät sai uudet varapuheenjohtajat: Allu Pyhälammi, Jenni Pitko ja Shawn Huff                                              | https://yle.fi/a/74-20165964 |    -3   |                   -4   |
| 47 | Orpo Venäjä-pakotteista: Nyt pitäisi saada päätöksiä, meidän pitää pakottaa Putin neuvottelupöytään                          | https://yle.fi/a/74-20166342 |    -2   |                    3   |
| 48 | Vihreiden Tynkkynen tyytymätön hallitukseen: Puolustusmenojen nostosta miljardeilla pitää keskustella enemmän                | https://yle.fi/a/74-20165910 |    -7   |                   -7   |
| 49 | Urheiluministerinä aloittava Mika Poutala juoksee 15 kilometrin työmatkansa – aikoo vaikuttaa erityisesti apurahoihin        | https://yle.fi/a/74-20162150 |    -7   |                   -7   |
| 50 | Brittitutkija Stubbin roolista maailman­politiikassa: ”Tärkeät suunnitelmat ovat tosiasiassa syntyneet Helsingissä”          | https://yle.fi/a/74-20163672 |     0   |                    0   |
| 51 | Vihreiden puoluekokous alkaa Hämeenlinnassa                                                                                  | https://yle.fi/a/74-20166328 |     0   |                    0   |
| 52 | Suomen Lappiin tuleva Nato-joukko alkaa rakentua: Britannia mukana                                                           | https://yle.fi/a/74-20166307 |     2   |                    3   |
| 53 | Saamelaiskäräjien hallitus hyväksyi perustuslakivaliokunnan muutosehdotukset                                                 | https://yle.fi/a/74-20166308 |    -3   |                   -2   |
| 54 | Puolustusmenot nousemassa miljardeilla – Orpo: Venäjän uhan takia Suomen puolustus on pakko hoitaa                           | https://yle.fi/a/74-20166298 |     0   |                    5   |
| 55 | Vihreiden venäläinen ehdokas ei kelvannut Lieksan kaupungin elinkeino­yhtiöön – puolue syyttää syrjinnästä                   | https://yle.fi/a/74-20166288 |     3   |                   -2   |
| 56 | Lentoliikenteen työriidassa ei sopua perjantaina, sovittelu jatkuu maanantaina                                               | https://yle.fi/a/74-20166283 |     0   |                   -1   |
| 57 | Puheenjohtaja uskoo, että ongelmat Turun vasemmisto­liitossa ovat vihdoin ohi: ”Tämä on ollut tosi pitkä tie”                | https://yle.fi/a/74-20166133 |     0   |                   -3   |
| 58 | Analyysi: Kansanedustajia lähtee eduskunnasta kuin hollituvasta, mutta ei Arkadianmäestä kannata vankilaakaan tehdä          | https://yle.fi/a/74-20166141 |     5   |                    1   |
| 59 | Ilmari Nurminen pyysi eroa eduskunnasta                                                                                      | https://yle.fi/a/74-20166275 |     0   |                    0   |
| 60 | Oliver Stubb erottui ”selvästi muista hakijoista” – sai harjoittelu­paikan presidentti-isänsä erikoisalalta                  | https://yle.fi/a/74-20166232 |     0   |                    0   |
| 61 | Uudenkaupungin ääni palaa eduskuntaan – Mauri Kontu ottaa haasteen vastaan Annika Saarikon seuraajana                        | https://yle.fi/a/74-20166199 |     2   |                    4   |
| 62 | Alankomaissa äänestetään uudesta hallituksesta lokakuussa                                                                    | https://yle.fi/a/74-20166219 |     0   |                    0   |
| 63 | Hallitus sai eduskunnan luottamuksen välikysymysäänestyksessä                                                                | https://yle.fi/a/74-20166179 |     0   |                   -3   |
| 64 | Annika Saarikko jättää valtakunnanpolitiikan ja siirtyy YTHS:n toimitusjohtajaksi                                            | https://yle.fi/a/74-20166132 |    -1   |                    0   |
| 65 | Sofia Virta tietää, milloin ei kannata puhua ilmastokriisistä – nyt hän kertoo puolueen talousteesit                         | https://yle.fi/a/74-20163230 |    -6   |                   -6   |
| 66 | Kontiolahdella hylättiin eniten ääniä kevään kuntavaaleissa – katso missä kunnissa ääniä mitätöitiin eniten                  | https://yle.fi/a/74-20166096 |     0   |                    0   |
| 67 | USU: Hyvinvointialueet hakevat joukolla lisää rahaa                                                                          | https://yle.fi/a/74-20166089 |     0   |                   -3   |
| 68 | Analyysi: Trump sai tahtonsa läpi Natossa                                                                                    | https://yle.fi/a/74-20166052 |     2   |                    4   |
| 69 | Trump ja Saksan Merz kohtasivat Valkoisessa talossa – ”Antaa lapsien tapella”, totesi Trump Ukrainasta                       | https://yle.fi/a/74-20166047 |    -3   |                   -2   |
| 70 | Hallitus tiukentaa pysyvän oleskeluluvan ehtoja – edellytyksiin kuuluu kielitaito, bonusta 40 000 euron vuosituloista        | https://yle.fi/a/74-20166033 |     5   |                    5   |
| 71 | Kansanedustaja Karoliina Partanen kertoo joutuneensa seksuaalisen häirinnän kohteeksi – oikeudenkäynti maanantaina           | https://yle.fi/a/74-20165996 |    -2   |                    2   |
| 72 | Ministeriö haluaa, että susia voisi metsästää Suomessa jo ensi vuonna                                                        | https://yle.fi/a/74-20165944 |     4   |                    3   |
| 73 | Katso paljon puhuva video, jolla ministerit kommentoivat rasismikoulutusta – Wille Rydman vastaa pitkän hiljaisuuden jälkeen | https://yle.fi/a/74-20165908 |    -3   |                   -2   |
| 74 | Halla-aho: Kukaan ei epäile Antti Pelttaria maanpetoksesta, eduskunnan kansliatoimikunta päätti lisäkuulemisista             | https://yle.fi/a/74-20165925 |     0   |                    2   |
| 75 | Suomeakin odottaa puolustuksen miljardilasku – Häkkänen: Seuraava hallitus voi rahoittaa tekemällä cocktailin                | https://yle.fi/a/74-20165890 |     5   |                    4   |
| 76 | Analyysi: Ukrainan taitava drooni-isku voi johtaa sodan kiihtymiseen                                                         | https://yle.fi/a/74-20165854 |    -2   |                   -3   |