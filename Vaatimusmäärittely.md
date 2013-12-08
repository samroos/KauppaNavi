#KirjastoNavi
**Sovellus kirjojen ja muiden tuotteiden hakemiseen sekä paikantamiseen**

Ryhmän nimi: **Lukutoukat**
####Sam Roos, Fredrik Gundersen, Toni Nummelin, Antti-Ville Pääkkönen
26.11.2013

##Johdanto
Kirjastot ovat pullollaan kirjoja ja niiden löytäminen saattaa olla erittäin hankalaa vaikka kirjat olisivatkin luokiteltuna ja aakkosjärjestyksessä, sillä juuri se kirja mikä pitäisi löytää, saattaa kuulua moneen eri luokkaan tai sitten kirjan nimeä ei tiedä. Kirjaston laajasta valikoimasta saattaa tulla ongelma, jos etsii kirjaa josta on monia versioita ja kirjan nimestä selviää lähes samoja asioita. Ongelma on siis löytää juuri omia tarpeita parhaiten tyydyttävä kirja.

Tässä työssä esitellään sovellus, joka nopeuttaa oikean kirjan hakua. Sovelluksessa käyttäjä pystyy hakemaan kirjoja, missä ne tarkalleen sijaitsevat ja onko kyseistä kirjaa tällä hetkellä hyllyssä.


##2.Käyttötapaukset
####A= asiakas
####T= työntekijä
-	A haluan tietää missä tuote sijaitsee
-	A haluan kirjautua palveluun
-	A haluan kirjautua ulos palvelusta
-	A haluan tietää tuotteen tiedot
-	A haluan tietää oman sijainnin
-	T haluan tietää missä tuote sijaitsee
-	T haluan tietää onko tuotetta hyllyssä
-	T haluan tietää tuotteen tiedot
-	T haluan tietää minne tuotteet laitetaan
-	T haluan tietää missä muut käyttäjät sijaitsevat
-	T haluan nähdä pohjapiirustuksen
-	T haluan tietää asiakkaan tiedot
-	T haluan kirjautua palveluun
-	T haluan kirjautua ulos palvelusta
	

###Käyttäjäskenaario
![alt tag](http://users.metropolia.fi/~toninu/K%e4ytt%e4j%e4skenaario.JPG)

###Kirjan haku vuokaavio
![alt tag](http://users.metropolia.fi/~samr/kauppa_projekti/KauppaNavi/flowchart.jpg)

###Käyttötapaus kaavio
![alt tag](http://users.metropolia.fi/~fredrikg/ohjelmisto/käyttötapauskaavio.png)

##3.Järjestelmäarkkitehtuuri
###Korkean abstraktiotason yleiskuvaus
![alt tag](http://users.metropolia.fi/~toninu/abstraktio1.PNG)

**Järjestelmän pääkomponentit ja niiden toiminnallisuuksien määrittely**

###Tuotetietokanta
Tuotetietokanta koostuu tuotteista, jotka ovat kirjaston tuoteluettelossa. Tuotteiden saatavuustilanne päivittyy sovellukseen automaattisesti, jolloin asiakkaan on helppo nähdä mitä tuotetta on saatavilla ja mitä ei. 

###Asiakastietokanta
Asiakastietokanta koostuu kirjaston rekisteröityneistä asiakkaista. Tietokanta sisältää asiakkaan perustiedot. Tietokantaan tallennetaan myös asiakkaan tekemät lainaukset ja varaukset.

###Tuotteen haku
Asiakkaat ja henkilökunta voivat hakea tuotteita, tuotteen tietoja ja paikantaa tuotteen.

###Langattomat verkot
Sovellus käyttää langattomia verkkoja joiden avulla asiakkaat ja henkilökunta löytävät etsimänsä tuotteet.

###Palvelin
Asiakas- ja tuotetietokanta haetaan palvelimelta.

##4. Vaatimukset
Tuotteen on suoriuduttava käyttäjien hakukyselyistä, kirjastonhoitajan palveluista ja sen tulisi toimia jokaisella alueella kirjastossa. Alueet ratkaistaan lisäämällä tukiasemia sen verran, että kirjaston sivut ja reunat ovat myös tukiasemien kuuluvuusalueella. Järjestelmän tietoturva taataan ominaisuuksien avaamisella vain kirjautuneille kirjaston asiakkaille ja henkilökunnalle. Näin ollen asiakkaat näkevät tietyt ominaisuudet ja henkilökunnalla on kaikki ominaisuudet nähtävissä. Henkilökunta pystyy seuraamaan asiakkaiden liikkeitä ja tutkimaan asiakastietoja tarpeen mukaan. Vartijalla on mahdollisuus samoihin ominaisuuksiin kuin kirjastonhoitajallakin.

Asiakkaan käyttöön sisältyy kirjojen etsiminen ja tämän kautta voi pyytää laitteelta avustusta kirjan sijaintiin. Asiakas näkee pohjapiirustuksen / kartan jossa oma sijainti on merkitty ja osoittaa suunnan kirjan sisältävälle hyllyvälille. Kirjaston henkilökunta saa saman palvelun mutta pystyvät myös näkemään palvelua käyttävät asiakkaat kartan avulla.

Ohjelmisto on käytettävissä kirjaston aukioloaikojen mukaan. Näin ollen päivityksiin ja järjestelmän huoltoihin on mahdollista käyttää loput päivästä. Esimerkiksi kirjaston ollessa auki 8-17, ohjelmisto voi olla pois käytöstä kello viidestä seuraavan päivän klo 8:aan asti. Näin ollen ylläpitotoimenpiteille saadaan riittävästi aikaa. 

Ohjelmiston skaalautuvuuden ei tarvitse olla suuri, sillä ohjelmistoa käyttää samanaikaisesti suurimmillaan n.100 käyttäjää. Ohjelmiston pitäisi toimia kaikilla alustoilla, joilla on mahdollisuus kytkeytyä kirjaston langattomaan verkkoon. Ohjelmiston päätoiminen suunta on kuitenkin mobiililaitteille, mutta ohjelmistoa voi käyttää myös kannettavalla. Työ saadaan minimoitua eri alustoille tekemällä järjestelmä verkkosivustoksi, joka liitetään alustalle tehtyyn appiin. Näin saadaan helposti portattava versio jokaiselle laitteelle.

Ohjelmiston ollessa verkkosivusto, taataan kaikille asiakkaille samanlainen käyttökokemus. Ohjelmisto on helposti päivitettävissä muuttamalla sivuston ulkoasua / toiminnallisuutta ja appiin päivittämisellä tarpeiden mukaan. Mobiililaitteissa päivitys toteutetaan laitteiden omilla ohjelmiston jakelujärjestelmillä kuten Android puhelimen Play ja Windows Phone Marketplace:n avulla, mutta jos muutos tapahtuu itse verkkosivulla, ei päivitystä tarvitse implementoida kuin pelkästään verkkosivuston tiedostoihin.

Tuotetietokannan ja asiakastietokannan ylläpito tapahtuu alkuperäisen kirjastojärjestelmän kautta, jolloin henkilökunnalle ei tule erillistä työtä kahden tietokannan välillä.
Ohjelmiston suorituskyky taataan ohjelmiston verkkosivujen nopeudella ja puhelimen omilla resursseilla. Palvelun verkkosivuston tehtävä on lähettää tieto puhelimelle ja puhelin päättää paikan itselleen ladatun pohjapiirustuksen kautta. Näin saadaan laskenta siirrettyä puhelimen omaan prosessoriin ja itse järjestelmä ei kuormitu suuresta käyttäjämäärästä.

Palvelun vastausaikoihin voidaan vaikuttaa lisäämällä kaistaa verkkosivuston ja mobiililaitteen kanssa. Laitteella  pitäisi mennä enintään pari minuuttia saada tietoa ohjelmistolta. Kirjautuminen tehdään vain kerran, jotta käyttäjän voisi käyttää ohjelmistoa nopeammin. Kirjautumistiedot tallennettaisiin mobiililaitteen muistiin tulevaisuutta varten. Selkeä käyttöliittymä ja nopeat latausajat takaavat tehokkaan etsimisen kirjastossa ja näin asiakkaan ei tarvitse etsiä tietokonetta kirjastosta, josta kirjan sijainti saataisiin selville.
 

##5. Käyttöliittymä
####Näkymä 1. Kirjautuminen
![alt tag](http://users.metropolia.fi/~anttivip/Ohjelmistotuotanto/projekti/KauppaNavi/images/naytto_sign_in.jpg)

####Näkymä 2. Home
![alt tag](http://users.metropolia.fi/~anttivip/Ohjelmistotuotanto/projekti/KauppaNavi/images/naytto.jpg)

####Näkymä 3. Hakutulokset
![alt tag](http://users.metropolia.fi/~anttivip/Ohjelmistotuotanto/projekti/KauppaNavi/images/naytto_search.jpg)

####Näkymä 4. Kartta
![alt tag](http://users.metropolia.fi/~anttivip/Ohjelmistotuotanto/projekti/KauppaNavi/images/naytto_kartta.jpg)


##6. Projektinhallinta
**Työhön kuluneet tunnit:**40 h

**Dokumentin kirjoittamiseen kuluneet tunnit:**10 h/hlö

Työmäärää oli vaikea arvoida, sillä ryhmällä ei ollut aikaisempaa taustaa tämän tyyppisestä projektista ja mitä siihen kuuluu.

Projekti oli melko onnistunut odotuksiin nähden. Seuraavan projektin voisi aloittaa aikaisemmin ja perehtyä kaikkeen siihen liittyvään syvemmin.

Vaikeinta dokumentioinnissa oli toiminnallisten ja ei toiminnallisten vaatimuksien laatiminen.
