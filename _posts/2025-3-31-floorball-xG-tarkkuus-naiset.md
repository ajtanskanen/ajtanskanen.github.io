---
title: 'Salibandyn maaliodottama xG:n tarkkuus naisten F-Liigassa'
date: 2025-03-16
permalink: /posts/2025/3/salibandy_xG_tarkkuus_naiset/
image: /images/floorball/xG/miehet_goals_xG.png
largeimage: /images/floorball/xG/miehet_goals_xG.png
summary: 'Blogi | Analysoidaan vastaako odotettujen maalien määrä ottelun tulosta naisten F-Liigassa.'
tags:
  - salibandy
  - tilastot
  - maalit
  - xG  
---

Maaliodottama xG kertoo, kuinka monta maalia ottelussa esiintyneistä tilanteista F-Liiga -joukkue keskimäärin tekee. Tämä blogi kertoo, millaisia eroja toteutuneen tuloksen ja maaliodottaman välillä on naisten F-Liigassa.

1 Maaliodottaman ero toteumaan
===

Kuvio 1 kertoo ottelussa tehtyjen maalien määrän ja maaliodottaman xG:n erotuksen naisten F-Liigassa. Toisin sanoen, Kuvio 1 näyttää, kuinka suuri "virhe" on maaliodottamassa.

Aineisto, johon xG on sovitettu, on sama kuin analyysiaineisto, joten eron keskiarvon pitäisi olla nolla. Näin se lähes onkin. Eron keskiarvo on 0,054 maalia ottelussa.

Keskiarvoa kiinnostavampi asia on toteuman ja xG:n eron keskihajonta. Eron keskihajonta on 3,94 maalia ottelua kohden. Ottelutuloksissa on muutamia todella suuria, yli 10 maalin eroja. Toisin sanoen, muutamassa ottelussa joukkue on ali- tai ylisuorittanut maaliodottamaan nähden erittäin paljon.

![Maalien jakauma](/images/floorball/predict/distwomen_frq_minus_xG.png)<br>
_Kuvio 1. Tehtyjen maalien ja maaliodottaman ero maaleina ottelua kohden._

2 Kotijoukkueen etu
===

Kotijoukkue tekee keskimäärin enemmän maaleja kuin vierasjoukkue (Kuvio 2). Ero on 0,25 maalia ottelua kohden. Sitä vastoin maaliodottama xG on kotijoukkueelle keskimäärin 0,10 maalia/ottelu pienempi kuin vierasjoukkueelle. Näin laskien kotijoukkue keskimäärin ylittää maaliodottama xG:n 0,35 maalilla/ottelu. Tämä on kotietu, josta usein puhutaan.

![Maalien jakauma](/images/floorball/predict/koti_miinus_vieraas_naiset.png)<br>
_Kuvio 2. Montako maalia kotijoukkue tekee vierasta enemmän. Toteuman ja maaliodottama xG:n vertailu._


3 Ennustaako xG ottelun tuloksen?
===

Jos ottelun tuloksen laskee xG:n avullaa, saa arvion siitä, montako maalia syntyisi, jos kaikki joukkueet olisivat yhtä hyviä viimeistelemään. 

Aineistossa otteluita on 132, joista kotivoitto 69, vierasvoitto 57 ja tasapeli 6.
Maaliodottama saa otteluissa oikean voittajan 138:ssa ottelussa. Osuus on siis 67 prosenttia.
Jos vaaditaan, että maaliodottaman ero on vähintään 0,2, maaliodottama ennusti oikein voittajan 102:ssä kaikkiaan 132:sta ottelusta, siis tarkkuudella 77 prosenttia.

Kotivoitoista maaliodottama ennusti oikein voittajan 56:ssä kaikkiaan 69:sta ottelusta. Tarkkuus oli siis 81 prosenttia, kun voiton ennustaminen tarkoittaa sitä, että kotijoukkueen maaliodottama on 0,2 korkeampi kuin vierasjoukkueen.
Vierasvoitoista maaliodottama ennusti 44 kaikkiaan 57:sta tarkkuus siis 72 prosenttia (maaliodottamien ero on vähintään 0,2).
Tasapelin (maaliodottaman ero alle 0,4) maaliodottama ennusti 5 kaikkiaan 17:sta tarkkuus siis 29 prosenttia.
Maaliodottama siis ennusti vierasvoitot parhaiten. 

Kotijoukkueen tehtyjen maalien ja maaliodottaman ero on korkeintaan 1 maali/ottelu 55 prosentissa otteluista.
Vierasjoukkueen tehtyjen maalien ja maaliodottaman ero on korkeintaan 1 maali/ottelu 73 prosentissa otteluista.

otteluita 132, oikeavoittaja 102, osuus 0.7727272727272727
kotivoitto 69, oikeavoittaja 56, osuus 0.8115942028985508
tasapeli 6, oikeatulos 2, osuus 0.3333333333333333
vierasvoitto 57, oikeavoittaja 44, osuus 0.7719298245614035
virhe05_koti 73, osuus 0.553030303030303
virhe05_vieras 96, osuus 0.7272727272727273