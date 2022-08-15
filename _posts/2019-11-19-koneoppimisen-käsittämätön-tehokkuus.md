---
title: 'Koneoppimisen käsittämätön tehokkuus'
date: 2019-11-19
permalink: /posts/2019/11/Koneoppimisen käsittämätön tehokkuus
tags:
  - AI
  - tekoäly
---

Viime aikoina olen rakentanut koneoppimispohjaista elinkaarimallia (Tanskanen 2020), joka etsii optimaalisia työllistymispäätöksiä yksilön elinkaaren aikana. Suomeksi sanottuna malli miettii, milloin yksilön kannattaa mennä töihin, milloin ei. Elinkaarimallin tavoitteena on pystyä arvioimaan, miten esimerkiksi sosiaaliturvamuutokset ja niistä aiheutuvat käyttäytymismuutokset heijastuvat työllisyyteen.

Mallissa yksilö päättää 3 kuukauden välein jatkaako samassa tilassa vai vaihtaako tilaa. Päätös perustuu tulevien hyötyjen nykyarvoon, missä hyöty tarkoittaa nettotulojen logaritmia lisättynä vapaa-ajan menetystä kuvaavalla rangaistustermillä.

Päätöspohjaisten tilasiirtymien lisäksi mallissa on ulkoa-annettuja siirtymätodennäköisyyksiä, kuten joutuminen työkyvyttömyyseläkkeelle. Palkat kehittyvät satunnaisesti kuitenkin niin, että keskimäärin ne vastaavat havaittuja palkkoja. Mallissa yksilöt siis tekevät päätöksiä epävarmassa ympäristössä.

Elinkaarimalli ratkaistaan koneoppimismenetelmällä, jossa käytetään keinotekoista neuroverkkoa oppimaan esimerkkien avulla optimaalista käytöstä (esim. Karpathy 2016). Kuten kuva 1 näyttää, tuottaa malli järkevän näköisiä työllistymis- ja työttömyysasteita.

Elinkaarimallissa on diskretoituna luokkaa \(10^{20}\) tilaa. Koneoppija oppii järkevän käytöksen noin 25 000 elinkaaren otoksesta, joissa on yhteensä noin 5 miljoonaa päätöshetkeä. Näistä tiloista neuroverkko yleistää ”lähes optimaalisen” toiminta-arvionsa koskemaan kaikkia tiloja. Skaalaero on \(10^{13}\) kertainen, joten voi pitää melko hämmentävänä, että koneoppiminen pystyy löytämään lainkaan järkeviä päätöksiä.

Kuitenkin elinkaarimalli on yksinkertaistus todellisesta maailmasta ja siinä pätevistä säännöistä. Silti ihmiset pystyvät toimimaan paljon laajemmassa ja monimutkaisemmassa maailmassa. Jos koneoppiminen on käsittämättömän tehokasta, niin mitä pitää sanoa ihmisaivoista?

Viittaukset
=====

Karpathy, A. (2016) [”Deep Reinforcement Learning: Pong from Pixels”](http://karpathy.github.io/2016/05/31/rl/)

Tanskanen, A.J. (2020) [”Työllisyysvaikutuksien arviointia tekoälyllä: Unelmoivatko robotit an- siosidonnaisesta sosiaaliturvasta?” Kansantaloudellinen aikakauskirja 2/2020: 291-323](https://www.taloustieteellinenyhdistys.fi/wp-content/uploads/2020/06/KAK_2_2020_WEB-94-123.pdf)