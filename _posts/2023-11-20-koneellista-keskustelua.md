---
title: 'Välähdys tulevaisuudesta: suuri kielimalli hoitaa sosiaalisen median keskustelut yksinään'
date: 2023-11-20
permalink: /posts/2023/11/koneellista-keskustelua/
image: /images/gpts/robot.jpg
summary: 'Blogi | Suuret kielimallit osaavat keskustella jo keskenään. Miltä tämä näyttää?'
tags:
  - GPT
  - AI
  - tekoäly 
---

Ainakin joka kymmenes X/Twitter-tili on botti [^1]. 
Miten helposti suurella kielimallin avulla voi opettaa botin, joka edustaa tiettyä näkemystä?
Yllättävän helposti. Tuloksetkin ovat melko vakuuttavia. Eri aineistoilla optetut botit voi myös laittaa keskustelemaan keskenään. Tässä blogissa näytän esimerkin, jossa on opetettu botit EK:n ja SAK:n blogiaineistolla. Bottien keskustelu on sujuvaa, mutta hieman latteaa tai tahmeaa, eivätkä kommentit kaikilta osin vastaa tausta-aineistoa. Ehkä bottien välinen keskustelu antaa kuitenkin välähdyksen sosiaalisen median tulevaisuudesta.

[^1]: Lähde: [Clare Duffy ja Brian Fung, Elon Musk commissioned this bot analysis in his fight with Twitter. Now it shows what he could face if he takes over the platform](https://edition.cnn.com/2022/10/10/tech/elon-musk-twitter-bot-analysis-cyabra/index.html)

Keskusteleva kielimalli
---

ChatGPT on näyttänyt, miten suuri kielimalli pystyy uskomattoman ihmismäiseen keskusteluun. Askel askeleelta malli kehittyy paremmaksi. Tuoreimmassa, marraskuun päivityksessä[^2] OpenAI toi käyttöön assistentit, jotka osaavat analysoida tiedostoja ja muokata 
näkemyksiään niiden perusteella. Kokeillaanpa.

[^2]: [OpenAI:n DevDay](https://devday.openai.com/)

Hain verkosta suuren joukon Elinkeinoelämän keskusliitto EK:n blogeja. Tähän väliin lienee syytä todeta, että EK on työnantajani. Botit on opetettu blogiaineistolla, muuten bottien säätö on jätetty minimiin.  Kuka tahansa pystyy säätämään botteja vastaavasti kuin tässä on kuvattu. 

Tärkeintä on, että aineistoa on riittävästi. EK:n sivuilta löytyy erittäin suuri määrä blogeja, mikä helpottaa opettamista. Annoin koko blogi-aineiston assistentille lähtötiedoiksi. Kutsun assistenttia EK-botiksi. Tähän väliin on syytä laittaa disclaimer: *EK-botti ei edusta EK:n näkemyksiä tai ole EK:n hyväksymä*.

Hain myös SAK:n kaikki julkisesti saatavilla olevat blogit ja annoin ne lähdeaineistoksi assistentille. Kutsun seuraavassa assistenttia SAK-botiksi. Tähänkin disclaimer: *SAK-botti ei edusta SAK:ta tai SAK:n näkemyksiä, eikä ole SAK:n missään mielessä hyväksymä*.

Työttömyysturva: seesteistä keskustelua
----

Laitetaan botit keskustelemaan keskenään työttömyysturvasta. EK-botti aloittaa ja SAK-botti vastaa. Keskustelun formaatti on twiitti.

Ohjeistin botit keskustelemaan asiallisesti ja edustamaan työnantajien (EK-botti) ja työntekijöiden (SAK-botti) näkemyksiä. Toistetaan nyt vielä uudestaan, että botit *eivät* edusta sen enempää EK:n kuin SAK:n todellista näkemystä. Aineisto on näin valittua, koska se on helposti saatavissa ja sitä on kohtuullinen määrä. Mitä enemmän aineistoa on, sitä paremmin malli on mahdollista opettaa.

> ###  EK-botti
> *Suomessa työttömyysturvan uudistamisen on keskityttävä kannustavuuden ja joustavuuden parantamiseen. Työn vastaanottamisen tulee aina olla taloudellisesti houkuttelevaa. Järjestelmää tulee yksinkertaistaa ja byrokratiaa vähentää, jotta se tukee paremmin yksilöllisiä työllistymispolkuja. #työttömyysturva #uudistus #työllisyys*
> 
> ### SAK-botti
> *Työttömyysturvan uudistuksessa on tärkeää, että se kannustaa työn vastaanottoon, mutta myös turvaa toimeentulon epävarmoina aikoina. Työttömyysturvan pitää olla reilu ja riittävä, sekä tukea aktiivista työnhakua ilman kohtuutonta byrokratiaa. Joustavuus on hyvä, mutta ei työntekijän oikeuksien kustannuksella. #Työttömyysturva #Työllisyys*
> 
> ### EK-botti
> *Täysin samaa mieltä! Työnteon tulee aina kannattaa, mutta turvaverkon on oltava riittävä epävarmoissa tilanteissa. Uudistuksessa keskeistä on tasapaino joustavuuden ja turvallisuuden välillä. Kannatamme reilua työttömyysturvaa, joka tukee aktiivista työnhakua vähentäen byrokratiaa, ilman että työntekijän perusoikeudet kärsivät. #TyöttömyysturvaUudistus #TyöllisyysPlus*
> 
> ### SAK-botti
> *Olemme yhtä mieltä kannustavuuden merkityksestä. Työttömyysturvan uudistuksessa on löydettävä oikea balanssi kannustimen ja turvan välillä. On tärkeää, että uudistus edistää aktiivisuutta ja vähentää byrokratiaa, mutta samalla turvataan työntekijöiden oikeudet ja toimeentulo. #Työllisyys #ReiluTyöttömyysturva*
> 
> ### EK-botti
> *Juuri näin, oikeanlainen balanssi on avainasemassa. Työttömyysturvan uudistuksen tulee edistää työn hakemista ja löytämistä, samalla kun se suojaa työntekijöitä taloudellisesti epävarmoina hetkinä. Kannustavuus ja turvan takaaminen eivät sulje toisiaan pois, vaan ne ovat molemmat tärkeitä elementtejä kestävän ja dynaamisen työmarkkinan rakentamisessa. #Työttömyysturva #Työelämä2023*


Keskustelu on sivistynyttä ja vastaa karkeasti lähdeaineistoa. Hieman sitä kuitenkin vaivaa hajuttomuus ja mauttomuus. Hieman tekstissä kiinnittää huomiota "joustavuus" EK-botin peräänkuuluttamana. Sitä ei työttömyysturvan yhteydessä EK:n blogiaineistossa esiinny. EK myös kannattaa byrokratian purkua yleisesti, mutta erityisesti työttömyysturvan kohdalla siitä ei aineistossa puhuta. EK-botti siis huomioi lähdeaineiston, mutta tulkinnat eivät täysin vastaa sitä. Samat ongelmat vaivaavat SAK-botin toiminnassa, mutta vähemmän silmiinpistävästi.

Työelämä: vastakkainasettelun aika ei olekaan ohi!
----

Bottien keskustelu työttömyysturvasta oli niin väritöntä, että lisätään napakkuutta, särmää ja edunvalvonta-asennetta säätämällä botin ohjeita. Entä mitä botit sanovat työelämän uudistamisesta?
 
> ### EK-botti
> *Suomen työelämän sääntely kaipaa modernisointia! Tarvitaan joustavuutta & yrittäjyyden kunnioittamista. Pois turhat kahleet – annetaan yritysten hengittää ja innovoida! #työelämä #joustavuus #vapaamarkkinat #EK 💼🔗🚀* 
> 
> ### SAK-botti
> *Tervehdys! Kehotan perehtymään tosiasioihin. Joustavuus ei saa tarkoittaa työntekijöiden oikeuksien polkemista. Sääntely takaa turvaa ja reilut pelisäännöt. Isojen yritysten "hengittäminen" ei saa tukehduttaa palkansaajia. #työolot #oikeudenmukaisuus #SAK 💪🛠️📜✊* 
> 
> ### EK-botti
> *Turvallisuus ja oikeudenmukaisuus ovat ytimessämme, mutta tunkkainen sääntely kuristaa kilpailukykyä. Aito joustavuus tuo mahdollisuuksia kaikille, ei vain isoille yrityksille. Innovation ja työpaikkojen luominen ei ole nollasummapeliä. #työelämä #uudistus #kilpailukyky 🚀💡📈👷* 
> 
> ### SAK-botti
> 
> *On aika herätä todellisuuteen! Ei voi puhua "aidosta joustavuudesta", jos se tarkoittaa työntekijöiden turvaverkkojen purkua. Kilpailukyky ei kasva työehtojen kurjistamisella. Työ on ihmisarvoa, ei pelkkää kauppatavaraa. Oikeudenmukaisuus ennen voittoja! #reilutyöelämä #työntekevänSuomi #SAK 💪🏗️📊✊* 

Nyt botit ryhtyvät jo vääntämään ja inttämään. Tekstit näyttävät kyllä X/Twitteriltä, mutta eivät oikein vastaa oikeiden SAK:n ja EK:n twiittejä. 

Julkinen talous: edunvalvonta-asennetta etsimässä
---

Väännetään särmää hieman pienemmälle ja kokeillaan vielä kerran, jos sävy menisi paremmin kohdilleen.
Tällä kertaa SAK-botti aloittaa aiheesta "Miten vahvistaa julkista taloutta ja pienentää kestävyysvajetta?"

> ### SAK-botti
> *Työllisyysaste ylös, harmaa talous kuriin, ja investoinnit koulutukseen sekä tutkimukseen vahvaksi! Kun työssäkäyvien määrä kasvaa, kasvaa myös verotulot ja talous. Sijoitukset osaamiseen tuottavat tulevaisuudessa. #kestävyysvaje #julkistalous #työllisyys* 
> 
> ### EK-botti
> *Työllisyysasteen nousu 👍, mutta älkäämme unohtako yritysten tarpeita! Ilman kilpailukykyistä toimintaympäristöä ja kevennettyä sääntelytaakkaa emme yllä tavoitteisiin. Harmaa talous on kitkettävä järein ottein! 🔨 Satsaukset osaamiseen ovat hyvä, mutta ne vaativat myös markkinat, jonne innovaatiot voidaan kaupallistaa. #tehokkuus #innovaatio #yritysystävällisyys* 
> 
> ### SAK-botti
> *Yritysten kilpailukyky on tärkeää, mutta ei työntekijöiden oikeuksien kustannuksella. Sääntelyn purkamisen on oltava harkittua ja kohtuullista. Markkinoille pääsyn helpottaminen ei saa tarkoittaa työehtojen polkemista. Harmaa talous on torjuttava tiukasti, mutta tasapainoista politiikkaa unohtamatta. Työntekijöiden edut ovat yritysten menestyksen kulmakivi. #työehto #oikeudenmukaisuus #työntekijöidenoikeudet* 
> 
> ### EK-botti
> 
> *Kilpailukyvyn ja työntekijöiden oikeuksien vastakkainasettelu on vanhanaikaista ajattelua. Vahvat yritykset tarvitsevat vahvoja työntekijöitä. Sääntelypurku ei tarkoita työehtojen heikkenemistä, vaan turhan byrokratian karsimista. Työmarkkinoiden joustavuus 🔀➡️ tuottavuus. Harmaan talouden torjunnassa ei kompromisseja! Kaikkien etu, että pelataan samalla säännöillä. #työnantaja #työntekijä #yhteistyölläetu_bp* 

Keskustelu menee edelleen inttämiseksi ja varsinainen pihvi, julkisen talouden vahvistaminen, unohtuu boteilta. 
Ihan eivät nämä botit vielä korvaa ihmistä keskustelijana. Kehitys on kuitenkin ollut huimaa, eikä lakipistettä vielä ole saavutettu.

Sosiaalisen median ja keskustelunpalstojen tulevaisuus
----

Mutta mitä bottien kasvavat kyvyt tarkoittavat sosiaaliselle medialle ja keskustelupalstoille? Päivystävätkö jatkossa keskustelupalstoilla automaattiset mielipideautomaatit? Olisi melko helppo tehdä botti, joka vastaisi kaikkiin tietyn aihepiirin kommentteihin. Tai vaikka seuraisi tiettyä tahoa ja vastaisi aggressiivisesti kaikkiin ko. tahon viesteihin. Jos jokaisella mielipiteeseen vaikuttamaan pyrkivällä taholla olisi oma bottiarmeija, hukkuisi sosiaalinen media nopeasti bottien viesteihin.

Bottien esittämiä mielipiteitä ei välttämättä pysty erottamaan ihmisten esittämistä. 
Jokainen voi helposti kouluttaa itselleen botin, joka pääsee melko lähelle tavoiteltuja näkemyksiä.
Valtiolliset toimijat, kuten Venäjä, voivat hyödyntää -- ja varmasti hyödyntävät jo nyt -- botteja tuottamaan tarkoituksellisen provosoivaa sisältöä. Tämä tuskin tulee vähenemään. 

Jos keskustelupalstat muuttuvat bottien temmellyskentäksi, tappaa tämä ihmisten välisen keskustelun. Elon Muskin huoli boteista ei ole perusteeton. Selvyyden vuoksi on hyvä todeta, että tämän blogin on kirjoittanut ihminen.


Mitä kokeilusta jäi käteen?
----

Botit osaavat keskustella ja seurata lähdeaineistoansa mielipiteissään. Keskustelun sävyn säätäminen vaatii jonkin verran työtä, eivätkä bottien tekstit aina oikein vastaa lähdeaineistoa. Lopputulos on kuitenkin pelottavankin hyvä. Tulevaisuudessa botit saattavat hallita sosiaalisen median keskusteluja niin hyvässä kuin pahassa.
