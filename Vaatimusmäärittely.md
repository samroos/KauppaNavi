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

##4. Vaatimukset
Tuotteen on suoriuduttava käyttäjien hakukyselyistä, kirjastonhoitajan palveluista ja tuote tulisi toimia jokaisella alueella kirjastossa. Alueet ratkaistaan lisäämällä tukiasemia sen verran, että kirjaston sivut ja reunat ovat myös tukiasemien kuuluvuusalueella. Asiakkaan käyttöön sisältyy kirjojen etsiminen ja tämän kautta voi pyytää laitteelta avustusta kirjan sijaintiin. Asiakas näkee pohjapiirrustuksen/kartan jossa oma sijainti on merkitty ja osoittaa suunnan kirjan sisältävälle hyllyvälille. Kirjaston henkilökunta saa saman palvelun mutta pystyvät myös näkemään palvelua kättävät asiakkaat kartan avulla.

Ohjelmisto on käytettävissä kirjaston auki-olo aikojen mukaan. Näin ollen päivityksiin ja järjestelmän huoltoihin on mahdollista käyttää loput päivästä. Esimerkiksi kirjaston ollessa auki 8-17, ohjelmisto voi olla pois käytöstä kello viidestä seuraavan päivän klo 8:aan asti. Näin ollen ylläpitotoimenpiteille saadaan tarpeeksi aikaa.
Ohjelmiston skaalattavuus ei tarvitse olla suuri, sillä ohjelmistoa käyttää saman-aikaisesti suurimmillaan n.100 käyttäjää.
Ohjelmisto pitäisi olla toimiva kaikilla alustoilla, joilla on mahdollisuus kytkeytyä kirjaston langattomaan verkkoon. Ohjelmiston päätoiminen suunta on kuitenkin mobiililaitteille, mutta ohjelmistoa voi käyttää myös kannettavalla.
Työ saadaan minimoitua eri alustoille tekemällä järjestelmä verkkosivustoksi joka liitetään alustalle tehtyyn app:iin. Näin saadaan helposti portattava versio jokaiselle laitteelle.
Järjestelmän tietoturva taataan ominaisuuksien avaamisella vain kirjautuneille kirjaston asiakkaille ja henkilökunnalle. Näin ollen asiakkaat näkevät tietyt ominaisuudet ja henkilökunnalla on kaikki ominaisuudet nähtävissä. Henkilökunta pystyy seuraamaan asiakkaiden liikkeitä ja tutkimaan asiakastietoja tarpeen mukaan. Vartijalla on mahdollisuus samoihin ominaisuuksiin kuin kirjastonhoitajallakin.
Tietokannan eli kirjojen sun muiden ylläpito tapahtuu alkuperäisen kirjastojärjestelmän kautta, jolloin henkilökunnalle ei tule erillistä työtä kahden tietokannan välillä. Näin saadaan järjestelmän huoltoihin ja päivityksiin myös tehtävä yhdistää kirjastojärjestelmän tiedot myös ohjelmistoon.
Ohjelmiston suorituskyky taataan ohjelmiston verkkosivujen nopeudella ja puhelimen omilla resursseilla. Palvelun verkkosivuston tehtävä on lähettää vain tieto puhelimelle ja puhelin päättää paikan itselleen ladatun pohjapiirrustuksen kautta. Näin saadaan laskenta siirrettyä puhelimen omaan prosessoriin ja itse järjestelmä ei kuormitu suuresta käyttäjämäärästä.
Ohjelmiston ollessa verkkosivusto, taataan näin kaikille asiakkaille samanlainen käyttökokemus. Ohjelmisto on helposti päivitettävissä muuttamalla sivuston ulkoasua/toiminnalisuutta ja app:in päivittämisellä tarpeen mukaan. Mobiililaittessa päivitys toteutetaan laitteiden omissa ohjelmiston jakelu järjestelmillä kuten Android puhelimen Play ja Windows Phone Marketplace:n avulla, mutta jos muutos tapahtuu itse verkkosivulla, ei päivitystä tarvitse implementoida kuin pelkästään verkkosivuston tiedostoihin.
Palvelun vastausaikoihin voidaan vaikuttaa lisäämällä kaistaa verkkosivuston ja mobiililaitteen kanssa. Laitteella ei kuitenkaan pitäisi mennä pitempään kuin pari minuuttia saada tietoa ohjelmistolta. Kirjautuminen tarvittaisiin tehdä vain kerran joten käyttäjän nopeus käyttää ohjelmistoa nopeutuisi. Tämä tallennettaisiin mobiililaitteen muistiin tulevaisuutta varten. Selkeä käyttöliittymä ja nopeat latausajat takaavat nopean etsimisen kirjastossa ja näin asiakas välttää tarpeen etsiä tietokonetta kirjastosta, jossa kirjan sijainti saadaisiin tietään. 
