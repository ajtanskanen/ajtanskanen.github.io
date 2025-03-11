---
title: 'Miten käy tekoälyltä rock’n’roll, osa 2: GPT-3.5 haastaa Aukustin ja Einon'
date: 2022-12-02
permalink: /posts/2022/12/Miten-käy-tekoälyltä-rocknroll-v2/
image: /images/poppis1.jpg
summary: 'Blogi | Yle Radio Suomen Poppikoulussa osallistujat kilpailevat priimuksen arvonimestä. Miten tekoäly pärjäisi kisassa? Kokeilun osa 2 uudella GPT:n versiolla.'
tags:
  - musiikki
  - AI
  - tekoäly
    poppikoulu
---

Radio Suomen Poppikoulussa osallistujat kilpailevat priimuksen arvonimestä. 
Sen saavuttaakseen kilpailijan on osattava vastata hankaliin pop-, jazz-, roots- ym. aiheisiin kysymyksiin. 
Harva osaa vastata puoleenkaan esitetyistä kysymyksistä. Tämä tekee Poppikoulusta hyvän testialustan kokeilla, 
miten hyvin tekoäly pärjää ihmisiä vastaan. 

Tässä tarkoituksessa valitsin sattumanvaraisen Poppikoulun jakson ja testasin tekoälyn terävyyttä 
Poppikoulun kysymyksillä. Tekoälyn roolissa on GPT-3, joka on OpenAI:n kehittämä tekoälypohjainen kielimalli. 
Se osaa analysoida ja tuottaa tekstiä, kunhan sille esittää kysymyksen tai sopivan alun tekstille. 
GPT-3 ei varsinaisesti ole älykäs, mutta huijaa helposti uskomaan itsensä sellaiseksi. 
Onni suosi jaksoa, jossa haastaja Aukusti ja priimus Eino vastaavat 60-luvun pop- ja elokuvamusiikkia sekä iskelmää koskeviin kysymyksiin.

Marraskuun lopussa 2022 OpenAI julkaisu uuden version GPT-3:sta, jota se kutsuu nimellä GPT-3.5. Käytetään tätä
versiota ja verrataan tuloksia. Tarkemmin sanottuna käytetään OpenAI:n GPT-3.5 versiota DaVinci-3, joka esiintyy tuloksissa
nimellä DaVinci erotuksena aiemmista GPT-3:n tuloksista.

![Kuva 1. GPT-3:lle kysymykset esitetään tekstimuodossa.](/images/poppis1.png)
Kuva 1. GPT-3:lle kysymykset esitetään tekstimuodossa.

60-luku
Kysymykset alkavat 60-luvun musiikista. Kilpailijat aloittavat vuorotellen vastausvuorossa. Ensin Aukusti.

    Minkä yhtyeen ensisingle oli vuonna 1967 ilmestynyt Break on Through?
    GPT-3: The Doors
    Aukusti: Ei mitään käryä
    Eino: The Doors
    DaVinci: The Doorsin ensisingle oli vuonna 1967 ilmestynyt kappale "Break on Through (To the Other Side)"
    
Tilanne: GPT 1, Aukusti 0, Eino 1, DaVinci 1

GPT-3 ottaa johdon yhdessä Einon kanssa heti ensimmäisessä kysymyksessä tietämällä <i>The Doorsin</i> ensisinglen.

    Minkä nimisen jazziin ja kokeelliseenkin musiikkiin keskittyneen levymerkin saksalainen Mannfred Eicher perusti vuonna 1939 Münchenissa?
    GPT-3: ECM
    Aukusti: Decca
    Eino: Jätetään tyhjä maali tähän.
    DaVinci: Mannfred Eicher perusti vuonna 1979 Münchenissa ECM Records -levymerkin.

Tilanne: GPT 2, Aukusti 0, Eino 1, DaVinci 2

Ja heti toinen oikea vastaus! GPT-3 siirtyy nyt yksin johtoon. Onko ihmisellä enää mitään mahdollisuuksia tekoälyä vastaan?

    Apassit seikkailivat 60-luvun alussa niin Yhdysvaltain kuin Yhdistyneiden Kuningaskuntien listoilla, niiden kärkisijoilla. Kenen tai minkä yhtyeen versio oli brittiykkönen? Kenen tai minkä yhtyeen USAn listan kakkonen?
    GPT-3: The Beatlesin versio oli brittiykkönen, ja The Beach Boysin versio oli Yhdysvaltain listan kakkonen.
    Aukusti: Ei vastausta
    Eino: The Shadows Briteissä, toista en tiedä
    DaVinci: Yhdistyneessä kuningaskunnassa brittiykkösenä oli The Shadowsin version ”Apache”. Yhdysvaltain listalla kakkosena oli The Venturesin version ”Walk, Don’t Run”.

Tilanne: GPT 2, Aukusti 0, Eino 2, DaVinci 3

Kolmannessa kysymyksessä oikea vastaus olisi ollut <i>The Shadows ja Jörgen Ingman</i>. GPT-3:lla on täysin varma vastauksistaan, mutta silti molemmat ovat täysin väärin. Eino taas tunnistaa epäselvästä kysymyksenasettelusta huolimatta The Shadowsin ja tämä riittää tasoittamaan pelin.

    Minkä yhtyeen perustajajäseniä Don Wilson oli? Soitti yhtyeessä eläköitymiseensä asti, lähes 60 vuotta. Missä bändissä vastikään poismennyt komppikitaristi Don Wilson soitti?
    GPT-3: The Beach Boys
    Aukusti: En osaa tähänkään vastata
    Eino: The Ventures
    DaVinci: Don Wilson oli The Beach Boysin perustajajäsen. Hän soitti bändissä alusta alkaen vuodesta 1961 eläkkeelle jäämiseensä asti, lähes 60 vuotta.

Tilanne: GPT 2, Aukusti 0, Eino 3, DaVinci 3
    
GPT-3 jatkaa kulkuaan varmana vastauksestaan, mutta on jälleen väärässä. Eino sitä vastoin siirtyy johtoon kolmella pisteellä, Aukusti jatkaa pisteittä peränpitäjänä.

Elokuva
---

Seuraavaan kysymykseen liittyy musiikkinäyte, mutta GPT-3 saa luvan pärjätä ilman.

    Lähdetään vuodesta 1953, kun Pekka Puupää oli kesälaitumilla. Elokuvassa kuultiin myös yksi Olavi Virran suosituimmista levytyksistä. Mikä Kärki-Helismaa -klassikko tuossa elokuvassa soi? + musiikkinäyte
    GPT-3: Kärki-Helismaan klassikko, joka soi elokuvassa, on Olavi Virran kappale "Puhelinlangat laulaa".
    Eino: Sua lemmin tai jotain sinnepäin
    Aukusti: Sulle salaisuuden kertoa mä voisin.
    DaVinci: Kappaleen nimi oli "Kesäyö".
    
Tilanne: GPT 2, Aukusti 0, Eino 3, DaVinci 3
    
Kun oikea vastaus olisi ollut <i>Sinun silmiesi tähden</i>, ei kysymyksestä irtoa pisteitä.

    Kuka Suomen iskelmätaivaan tähdistä oli vuoden 1968 Spede-elokuvassa Noin seitsemän veljestä bardin hommissa?
    GPT-3: Rauli Badding Somerjoki
    Eino: Fredi
    Aukusti: Danny
    DaVinci: Tauno Palo

Tilanne: GPT 2, Aukusti 1, Eino 3, DaVinci 3
    
Spede-elokuvat eivät ole GPT-3:n vahvinta osaamista: Danny on oikea vastaus. Aukusti sitä vastoin tästäkin pisteen. Hurjasta alusta huolimatta GPT:n ote on alkanut lipsua.

    David Bowien vuoden 1984 rock-video oli 21 minuuttia pitkä. Peräti, tämmöinen minielokuva oikeastaan. Mikä oli kappale, mistä tämä video tehtiin?
    GPT-3: The song was "China Girl" from David Bowie's album "Let's Dance"
    Eino: Ashes to Ashes
    Aukusti: Spaceman
    DaVinci: Kappale, josta video tehtiin, on nimeltään "Blue Jean".

Tilanne: GPT 2, Aukusti 1, Eino 3, DaVinci 4
    
David Bowien <i>Blue Jean</i> ei sitä vastoin ole kenellekään tuttu. Jatketaan elokuvakysymyksiä.

    Eräässä vuoden 1992 elokuvassa Meatloaf esitti portsaria. Samassa elokuvassa oli mukana myös tuolloin vähän yli nelikymppinen Alice Cooper. Mikä oli elokuva?
    GPT-3: Wayne's World
    Eino: Ne kaksi idioottia, Wayne’s World
    Aukusti: Ei vastausta
    DaVinci: Elokuva oli Bat Out of Hell.

Tilanne: GPT 3, Aukusti 1, Eino 4, DaVinci 4
    
<i>Wayne's World</i> oli oikea vastaus. Elokuvakysymykset olivat siinä. Siirrytään Jokeri-kysymysten pariin.

Jokeri
----
    Mitä pienoismalleja Neil Young keräilee?
    GPT-3: Neil Young keräilee pienoismalleja kaikenlaisista ajoneuvoista, joita hän on omistanut tai joita hän on ajanut.
    Aukusti: Lentokoneita
    Eino: Autoja
    DaVinci: Neil Young keräilee kaikenlaisia pienoismalleja, mukaan lukien raidat, junat, linja-autoja, purjealukset, helikoptereita ja muita lentokoneita. Hänen keräilynsä sisältää myös kuorma-autoja, traktoreita, kalustoa, kuorma-autoja ja sotilasajoneuvoja.

Tilanne: GPT 3, Aukusti 1, Eino 4, DaVinci 4
    
Neil Youngin pienoisrautateiden keräily on aivan liian vaikea niin osallistujille kuin GPT:lle.

    Mistä maasta tulevat taiko-rummut ja kuuluisimmat rumpalit?
    GPT-3: Taiko-rummut ovat peräisin Japanista, ja kuuluisimmat rumpalit ovat japanilaisia.
    Aukusti: Japanista
    Eino: Japani
    DaVinci: Taiko-rummut ovat alun perin Japanista ja suurimman osan taiko-rummuista käytetään Japanissa. Kuuluisimpia taiko-rummuttajia ovat muun muassa Eitetsu Hayashi, Leonard Eto ja Daisuke Gōda.

Tilanne: GPT 4, Aukusti 2, Eino 5, DaVinci 5
 
Vihdoin taiko-rumpujen kohdalla jokainen osallistujista kerää pisteen. Priimus Eino johtaa edelleen pisteellä GPT:tä.

    Kuka joulukuussa kuollut runoilija, lasten- ja aikuisten kirjailija teki myös satoja iskelmäsanoituksia. Sanoitti mm. Topille ja Agentseille, Harri Marstiolle ja Pedro Hietasen eri projekteihin? Eka projekti oli Magyar-yhtyeen albumin tekstien teko.
    GPT-3: Reino Helismaa
    Aukusti: Ei tule mieleen, Kirsi Kunnas
    Eino: Kirsi Kunnas
    DaVinci: Kysymyksen kysymyksen kuollut runoilija, lasten- ja aikuisten kirjailija, ja sanoittaja on Kari Tapio (1952–2019).
    
Tilanne: GPT 4, Aukusti 3, Eino 5, DaVinci 5

Jukka Itkonen ja myös seuraavan kysymyksen <i>Swallow the Sun</i> ovat liian vaikea tunnistaa. Niistä ei pisteitä.

    Ihan tuoreen Soundi-lehden numerossa lukijat ovat äänestäneet viime vuoden suosikkinsa. Kotimaisten levyjen top-5:ssa oli vain yksi englanninkielinen levy, Moon Flowers. Minkä yhtyeen levy?
    GPT-3: Moon Flowers on The Raveonettesin levy
    Aukusti: En kyllä sano mitään
    Eino: Lordi
    DaVinci: Moon Flowers on Kube-yhtyeen studioalbumi, joka julkaistiin vuonna 2020.
    
Tilanne: GPT 4, Aukusti 3, Eino 5, DaVinci 5

Iskelmä
----

    Kuka vuonna 1989 72-vuotiaana kuollut helsinkiläinen aloitteli uraansa -42 vuonna syyspihlajan alla?
    GPT-3: Urho Kekkonen
    Eino: Jätetään tähän tyhjä maali
    Aukusti: Brita Koivunen
    DaVinci: Tämä kysymys ei ole tarkka, mutta uskotaan, että tarkoitettu henkilö on Olavi Paavolainen. Paavolainen aloitti soittamisen syyspihlajan alla vuonna 1942 ja kuoli vuonna 1989 72-vuotiaana Helsingissä.

Tilanne: GPT 4, Aukusti 3, Eino 5, DaVinci 5

GPT-3 on täysin vakuuttunut, että Urho Kekkonen kuoli vuonna 1989 ja aloitti uraansa syyspihlajan alla. Tämä ei taida olla aivan oikein. <i>Henri Thiil</i> taas ei ole kenellekään kilpailijoista tuttu.

    Millä sanoilla alkaa Rakastan sinua Elämä -kappale?
    GPT-3: Rakastan sinua Elämä -kappale alkaa sanoilla "Rakastan sinua elämä, rakastan sinua kaikesta".
    Eino: Rakastan sinua elämä
    Aukusti: Rakastan elämää
    DaVinci: Rakastan sinua elämä, kunnes hautaan asti, en koskaan hetkeäkään tahtoisi jättää pois.

Tilanne: GPT 4, Aukusti 3, Eino 5, DaVinci 5

”Päättyy yö, aamu saa, uusi päivä kun kirkkaana koittaa” olisi ollut oikea vastaus sanoitukseen. Ei pisteitä.

    Kun Chicago kuoli oli Vickyn ensisinkku vuonna 75. Se kuitenkin oli singlen B-puoli. Mikä oli A-puolella tuolloin?
    GPT-3: A-puolella oli kappale "Vain yksi yö".
    Eino: Charlie Brown
    Aukusti: Charlie Brown
    DaVinci: A-puolella tuolloin oli kappale nimeltään "Fool To Cry".
    
Tilanne: GPT 4, Aukusti 3, Eino 5, DaVinci 5

Vicky Rostin kappale <i>Siinä ruutia on, kun minä rakastun</i> näyttää olevan tuntematon. Vielä viimeinen kysymys.

    ”Anna mulle tähtitaivas” on yksi Katri Helenan hittejä. Kuka sen on säveltänyt?
    GPT-3: Anna mulle tähtitaivas on Katri Helenan kappale, joka on säveltänyt ja sanoittanut Katri Helena itse. Kappale on ilmestynyt Katri Helenan albumilla Katri Helena vuonna 1967.
    Eino: Kai Hyttinen
    Aukusti: Jukka Kuoppamäki
    DaVinci: Sävellys on Katri Helenan ja Juha Vainion.

Tilanne: GPT 4, Aukusti 4, Eino 6, DaVinci 5

Lopputulos
----

GPT-3 vastaa kaikkiin kysymyksiin yhtä vakuuttavasti. Useimmat vastaukset ovat kuitenkin vääriä, 
vaikka oikeat vastaukset ovat varmasti olleet GPT-3:n opetusaineistossa. 
Jo nykyisessä muodossa tekoäly haastaa ihmiskilpailijat jotakuinkin samalla tasolla. 
Muutaman vuoden päästä tilanne voi olla jo aivan toinen: uusia, parempia tekoälypohjaisia kielimalleja on 
viime aikoina julkaistu kiivaaseen tahtiin. 

| Kilpailija | Tulos |
|-------|--------|
| Eino | 6 pistettä |
| DaVinci | 5 pistettä |
| GPT-3 | 4 pistettä |
| Aukusti | 4 pistettä |

Viimeisessä kysymyksessä Aukusti saa kolmannen pisteensä. Lopputuloksena Eino voittaa 7 pisteellä, DaVince tulee toiseksi 5 pisteellä, GPT-3 tulee kolmanneksi 4 pisteellä, ja Aukusti jää tekoälyn taakse 3 pisteellä. 
GPT-3 ei hyvästä alusta huolimatta onnistu dominoimaan Poppikoulua, vaan jää kolmanneksi. DaVinci voittaa edeltäjänsä pisteellä,
mutta Eino voittaa edelleen. 
Tätä ei voi pitää huonona saavutuksena. Itse en tiennyt ensimmäistäkään vastausta.

![Kuva 2. Tekoäly ottaa tappion raskaasti.](/images/poppis2.png)
Kuva 2. Tekoäly ottaa tappion raskaasti.
