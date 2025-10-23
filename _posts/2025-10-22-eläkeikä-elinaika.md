---
title: 'Eläkeikä huomioi elinajan'
date: 2025-10-22
permalink: /posts/2025/10/eläkeikä/
hidden: true
summary: 'Blogi | Eläkeiässä huomioidaan elinajan odote, mutta ei täysimääräisesti. Tässä blogissa näytetään, millä osuudella näin on.'
tags:
  - työeläkkeet
  - elinajanodote
  - vanhuuseläkeikä
---

Eläkeiässä huomioidaan elinajan odote, mutta ei täysimääräisesti. Tässä blogissa näytetään, millä osuudella näin on.

1 Vanhuuseläkeikä työeläkeissä
===

Suomen työeläkejärjestelmässä alin vanhuuseläkeikä riippuu ikäluokasta, jota kutsutaan myös nimellä kohortti. Vuonna 1962 syntyneille alin vanhuuseläkeikä on 65 vuotta. Samoin 1963 ja 1964 syntyneille. Vuodesta 1965 alkaen alin vanhuuseläkeikä on kytketty elinajanodotteeseen. Työntekijän eläkelaissa 83 §:ssä määrätään, että 

> Vuonna 1965 ja sen jälkeen syntyneen työntekijän alin vanhuuseläkeikä määrätään siten, että alimman vanhuuseläkeiän ja 18 ikävuoden erotuksen suhde alimmassa vanhuuseläkeiässä laskettuun elinajanodotteeseen on sama kuin suhde on vuonna 2025. Elinajanodote lasketaan käyttäen kulloisenkin viiden viimeisen vuoden käytettävissä olevia Tilastokeskuksen kuolevuustilastoja. Vuoden 2025 suhdetta laskettaessa alimpana vanhuuseläkeikänä käytetään 65 vuotta ja elinajanodote lasketaan Tilastokeskuksen vuosien 2020–2024 kuolevuustilastojen perusteella.

Toisin sanoen, alin vanhuuseläkeikä riippuu elinajanodotteesta alimmassa vanhuuseläkeiässä.

2 Elinajan kasvun ja alimman vanhuuseläkeiän suhde
===

Merkitään $x$ vanhuuseläkeikää ja $q$ elinajan odotetta alimmassa vanhuuseläkeiässä. Tällöin suhde $\beta$, josta laki puhuu on
$$
\beta = \frac{x-18}{q}.
$$
Tässä yritämme laskea sitä, millä suhteella $\alpha$ alin vanhuuseläkeikä $x$ muuttuu, kun elinajanodote $q$ muuttuu. Merkitään elinajanodoteen kasvua $d$, jolloin elinajanodote iässä $x$ kasvaa arvosta $q$ arvoon $q+d$. Samalla alin vanhuuseläkeikä kasvaa arvosta $x$ arvoon $x+\alpha d$. Tällöin eläkkeelläoloaika kasvaa itse asiassa
arvoon $q+d-\alpha d$. Lain mukaan suhde $beta$ säilyy samana, joten
$$
\beta = \frac{x-18}{q} = \frac{x+\alpha d-18}{q+d-\alpha d}.
$$
Tästä ratkaisemalla saamme
$$
(x-18)(q+(1-\alpha)d) = q(x+\alpha d-18).
$$
Toisin sanoen
$$
xq+x(1-\alpha)d-18q-18(1-\alpha)d = xq + q\alpha d-18q.
$$
Ja edelleen
$$
x-\alpha x-18+18\alpha = q\alpha,
$$
ja 
$$
x-18 = (q+x-18)\alpha,
$$
mistä näkee suoraan, että suhde
$$
\alpha = \frac{x-18}{q+x-18}.
$$
Kiemuraista tietä päädyttiin lopputulokseen. Suhteessa yläkerrassa on työssäoloaika 18-vuotiaasta alimpaan vanhuuseläkeaikaan ja alakerrassa karkeasti 18 vuotiaan elinajan odote. Tarkkaan ottaen alakerrassa on alimman vanhuuseläkeiän ja elinajanodotteen siinä summa vähennettynä 18:sta.

3 Alin vanhuuseläkeikä kasvaa noin 70 prosenttia elinajanodotteesta
==

Jos alin vanhuuseläkeikä on 65 vuotta, on alimmassa vanhuuseläkeiässä elinajanodote on 20,57 vuotta (Human mortility database, 2024). Jos alin vanhuuseläkeikä on 65 vuotta, saamme suhteeksi noin 70 prosenttia.
$$
\alpha = \frac{65-18}{85,57-18} \sim 0,696.
$$
Toisin sanoen, ikääntyneiden elinajan kasvaessa hieman yli kaksi kolmannesta kasvusta huomioidaan alimmassa vanhuuseläkeiässä ja hieman alle yksi kolmannes kasvattaa vanhuuseläkkeellä oloaikaa.

