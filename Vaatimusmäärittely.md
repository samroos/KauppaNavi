#KirjastoNavi
**Sovellus kirjojen löytämiseen, tietoa mitä kirjoja kaverit ovat lainanneet ja olivatko kirjat hyviä**

Ryhmän nimi: **Lukutoukat**
####Sam Roos, Fredrik Gundersen, Toni Nummelin, Antti-Ville Pääkkönen
26.11.2013

##Johdanto
Kirjastot ovat pullollaan kirjoja ja niiden löytäminen saattaa olla erittäin hankalaa vaikka kirjat olisivatkin luokiteltuna ja aakkosjärjestyksessä, sillä juuri se kirja mikä pitäisi löytää saattaa kuulua moneen eri luokkaan tai sitten kirjan nimeä ei tiedä. Kirjaston laajasta valikoimasta saattaa tulla ongelma, jos etsii kirjaa josta on monia versioita ja kirjan nimestä selviää lähes samoja asioita. Ongelma on siis löytää juuri omia tarpeita parhaiten tyydyttävä kirja.
Tässä työssä esitellään ratkaisu sovellus, joka nopeuttaa oikean kirjan hakua. Sovelluksessa pystyy hakemaan kirjoja, missä ne tarkalleen sijaitsevat ja onko kyseistä kirjaa tällä hetkellä hyllyssä. Sovelluksessa käyttäjillä on mahdollisuus arvostella lainaamiaan kirjoja, jotta muut voivat lukea tarkemmin mitä kirja sisältää, onko kirjasta ollut hyötyä ja kenelle siitä voisi olla hyötyä. Sovelluksessa voi myös katsoa mitä kirjoja omat kaverit ovat lainanneet tai kommentoineet.

##2.Käyttötapaukset
####A= asiakas
####T= työntekijä
-	A haluan tietää missä tuote sijaitsee
-	A haluan kirjautua palveluun
-	A haluan kirjautua ulos palvelusta
-	A haluan tietää tuotteen tiedot
-	A haluan tietää oman sijainnin
-	T haluan tietää missä tuote sijaitsee
-	T haluan tietää onko tuotetta jäljellä
-	T haluan tietää tuotteen tiedot
-	T haluan tietää minne tuotteet laitetaan
-	T haluan tietää missä muut käyttäjät sijaitsevat
-	T haluan nähdä pohjapiirustuksen
-	T haluan tietää asiakkaan tiedot
-	T haluan kirjautua palveluun
-	T haluan kirjautua ulos palvelusta


###Kirjan haku vuokaavio
![alt tag](http://users.metropolia.fi/~samr/kauppa_projekti/KauppaNavi/flowchart.jpg)

###Käyttötapaus kaavio
![alt tag](http://users.metropolia.fi/~fredrikg/ohjelmisto/käyttötapauskaavio.png)

##3.Järjestelmäarkkitehtuuri
###Korkean abstraktiotason yleiskuvaus
![alt tag](http://users.metropolia.fi/~toninu/abstraktio.PNG)

**Järjestelmän pääkomponentit ja niiden toiminnallisuuksien määrittely**

###Tuotetietokanta
Tuotetietokanta koostuu tuotteista, jotka ovat kirjaston tuoteluettelossa. Tuotteiden saatavuustilanne päivittyy sovellukseen automaattisesti, jolloin asiakkaan on helppo nähdä mitä tuotetta on saatavilla ja mitä ei. 

###Asiakastietokanta
Asiakastietokanta koostuu kirjaston rekisteröityneistä asiakkaista. Tietokanta sisältää asiakkaan perustiedot. Tietokantaan tallennetaan myös asiakkaan tekemät lainaukset ja varaukset.

###Tuotteen haku
Asiakkaat ja henkilökunta voivat hakea tuotteita, tuotteen tietoja ja paikantaa tuotteen.

###Langattomat verkot
Sovellus käyttää langattomia verkkoja joiden avulla asiakkaat ja henkilökunta löytävät etsimänsä tuotteet.

###Tukiasemat
Langattomat verkot toimivat tukiasemien kautta.

