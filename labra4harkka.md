http://www.theseus.fi/bitstream/handle/10024/39057/Tiainen_Tuukka.pdf?sequence=1 
     
## Harjoitus 4: projektin vaatimusmäärittely

### A. Vaatimusmäärittelydokumentteihin tutustuminen, analyysi

#### 1. Tehtävänäsi on etsiä netistä ohjelmistokehitysprojektien vaatimusmäärittelydokumentteja ja valita yksi analysoitavaksi.
**Esimerkkikyselyitä hakukoneelle:**
  - '[site:www.thl.fi  vaatimusmäärittely pdf](https://www.google.fi/#q=site:www.thl.fi+vaatimusm%C3%A4%C3%A4rittely+pdf)'
  - '[vaatimusmäärittely pdf](https://www.google.fi/#q=vaatimusm%C3%A4%C3%A4rittely+pdf)'
  - '[terveydenhuoltojärjestelmä  vaatimusmäärittely pdf](https://www.google.fi/#q=terveydenhuoltoj%C3%A4rjestelm%C3%A4++vaatimusm%C3%A4%C3%A4rittely+pdf)'
  - '[kanta vaatimusmäärittely pdf](https://www.google.fi/#q=kanta+vaatimusm%C3%A4%C3%A4rittely+pdf)'

#### 2. Luo oma markdown-tiedosto ryhmänne Github repoon, jossa pohdit seuraavia aiheita:

##### (johdanto)
- mikä projekti? **ajanvarausjärjestelmä**
- lukijakunta, kenelle dokumentti on tarkoitettu? **vaatimustenhallinnalle**
- tilanne?
- motivaatio, miksi dokumentti on luotu? **Oktacode on aloittamassa ensimmäisen tuotteen kehitystä, jota varten se tarvitsee kattavasti tehdyn vaatimusmäärittelyn.**
- dokumentin rakenne, millainen se on esim. verrattuna projektissa käytettävään malliin? Kts. myös [Wikipediasta löytyvä runko](http://fi.wikipedia.org/wiki/Ohjelmiston_vaatimusm%C3%A4%C3%A4rittely).**Malli on pitkälti samanlainen, otsikot sun muut on samat kuin aikaisemmin nähdyissä malleissa ja mindmapit ovat melkeinpä identtiset**

##### (käyttötapaukset)
- mitä sillä voi tehdä?**Varata järjestelmästä ajan ja admin voi hallinnoida varattuja aikoja**
- käyttötapauskaavio(t)? **TAULUKKO 1. Käyttötapaus 4: ajan varaaminen**
**Käyttötapaus 4: Ajan varaaminen / ylläpitäjä, työntekijä**
**orittaja: Ylläpitäjä, Työntekijä**
**Käytettävyysvaatimukset: Käyttäjä voi varata asiakkaalle palvelun ja mahdollisen tuottajan asiakkaan tarpeiden mukaan.**
**Alkuehdot: Käyttäjä on kirjautunut järjestelmään.**
**Kuvaus: Käyttäjä valitsee asiakkaan, palvelun, mahdollisen tuottajan ja ajankohdan. [Poikkeus: Uusi asiakas]. Käyttäjä tekee varauksen järjestelmään.**
**Poikkeukset: Uusi asiakas: Käyttäjä siirtyy uuden asiakkaan lisäämiseen.**
**Loppuehdot: Varattu aika on tallennettu järjestelmään.**
**Täyttää vaatimukset: Y12, Y1**
- kuinka yksityiskohtaisesti kuvattu?**Erittäin yksityiskohtaisesti**
- skenaariot? tarinat?**Aivan järkyttävä määrä käyttäjätarinoita! katso vaikka itse:**
- Keskinkertainen: Parantaa ohjelmiston käyttökelpoisuutta huomattavasti. Ohjelmisto kuitenkin toimii ilman sitä. Suurin osa keskinkertaisista vaatimuksista toteutetaan ensimmäisessä tuotteen versiossa.
Matala: Tuo lisäarvoa jo käyttökelpoiseen järjestelmään. Se voidaan toteuttaa mahdollisesti tulevien iteraatioiden aikana.
Vaatimusten numerointi
Vaatimukset on numeroitu ja niihin on liitetty kirjaintunnus ryhmästä riippuen. Ryhmien tunnukset ovat:
48
Asiakas, A
Työntekijä, T
Ylläpitäjä, Y
Asiakas
Tämä loppukäyttäjäryhmä koostuu suurimmalta osin kotikäyttäjistä, jotka tekevät ajanvarauksia eri palveluihin eri palveluntarjoajilta.
Prioriteetti: tärkeä
A1. Asiakas voi valita haluamansa resurssin.
A2. Asiakas voi valita haluamansa palvelun/palvelut.
A3. Asiakas voi valita haluamansa kellonajan ja päivämäärän varaukselle.
A4. Asiakas voi tarkastaa haluamansa palvelun hinnan.
A5. Asiakas voi perua varauksen.
Prioriteetti: keskinkertainen
A6. Asiakas voi rekisteröityä järjestelmään.
A7. Asiakas voi kirjautua järjestelmään.
A8. Asiakas voi muokata omia tietojaan.
A9. Asiakas voi poistaa itensä palvelusta halutessaan.
A10. Asiakas voi tilata salasanan rekisteröinnissä annettuun sähköpostiosoitteeseen.
A11. Asiakas voi jättää palautetta palvelusta.
A12. Asiakas voi lähettää viestin ylläpidolle tai työn tekijälle.
.
Prioriteetti: matala
A13. Asiakas voi tunnistautua luotettavaksi käyttäjäksi.
A14. Asiakas voi selailla käynti- ja palveluhistoriaansa.
A15. Asiakas voi halutessaan valita teksti- tai/ja sähköpostiviestimuistutuksen varatusta ajasta.
Työntekijä
49
Järjestelmässä voi olla käytössä työntekijä-ryhmä, jos ympäristö sen vaatii. Esimerkiksi parturikampaamossa voi olla yksi ylläpitäjä ja useita työntekijöitä, joilla on alhaisemmat käyttäjäoikeudet.
Prioriteetti: tärkeä
T1. Työntekijä voi merkata omat työaikansa, jonka perusteella varauksia voi tehdä.
T2. Työntekijä voi muokata omia tietojaan.
T3. Työntekijä voi liittää itsellensä palveluita.
T4. Työntekijä voi poistaa itseltään palveluita.
Prioriteetti: keskinkertainen
T5. Työntekijä voi tulostaa merkattujen työaikojen ja varausten perusteella työaikalistan.
T6. Työntekijä voi luoda työaikarungon.
T7. Työntekijä voi poistaa työaikarungon.
T8. Työntekijä voi muokata työaikarunkoa.
Prioriteetti: matala
T9. Työntekijä voi lisätä tauon työaikaansa.
Ylläpitäjä
Tällä ryhmällä on kaikista suurimmat oikeudet ajanvarausjärjestelmässä. Jossakin ympäristössä tämä voi olla ainut ryhmä asiakkaan lisäksi. Esimerkiksi liikuntahallin varauksissa ei välttämättä tarvita muuta ylläpidollista ryhmää.
Prioriteetti: tärkeä
Y1. Ylläpitäjä voi lisätä asiakkaalle tilin.
Y2. Ylläpitäjä voi poistaa asiakkaan.
Y3. Ylläpitäjä voi muokata asiakkaan tietoja.
Y4. Ylläpitäjä voi lisätä työntekijälle tilin.
Y5. Ylläpitäjä voi muokata työntekijän tietoja.
Y6. Ylläpitäjä voi poistaa työntekijän.
Y7. Ylläpitäjä voi lisätä palvelun.
Y8. Ylläpitäjä voi poistaa palvelun.
50
Y9. Ylläpitäjä voi muokata palvelun tietoja.
Y10. Ylläpitäjä voi liittää palvelun työntekijälle.
Y11. Ylläpitäjä voi poistaa palvelun työntekijältä.
Y12. Ylläpitäjä voi lisätä varauksen.
Y13. Ylläpitäjä voi perua varauksen.
Prioriteetti: keskinkertainen
Y14. Ylläpitäjä voi passivoida työntekijän tilin.
Y15. Ylläpitäjä voi liittää työntekijälle varattavia aikoja.
Prioriteetti: matala
Y16. Ylläpitäjä voi lähettää järjestelmän kautta asiakkaille asiakaskirjeen.
Y17. Ylläpitäjä voi liittää asiakkaan tietoihin edellisten käyntien palvelut.
Y18. Ylläpitäjä voi liittää asiakastapahtumille lisätietoja.

##### (järjestelmän yleisrakenne) 
- MITÄ KAAVIOTEKNIIKOITA KÄYTETÄÄN? MIKSI?**järjestelmän tietosisältö,taulukko, mindmap, pylvästaulukkoa. Näitä tekniikoita käytetään asioiden selkeyttämiseen.**

##### (funktionaaliset & ei-funktionaaliset vaatimukset)
- esitetäänkö listauksena?**ei**
- tunnistetiedot? numeroitu?**kyllä, esimerkiksi ylhäällä olevat käyttäjätarinat on numeroitu ja priorisoitu**
- jäljitettävyys? mitattavuus? (Miten voidaan jälkikäteen todentaa, että vaatimukset on myös toteutettu, kuten suunniteltu?)**Mittaamalla käyttäjien nopeutta ajanvarauksessa ja sen helppokäyttöisyydellä**

##### (miltä se näyttää)
- onko käyttöliittymästä kuvia?**Radio buttoneita kyllä, mutta muuten ei mitään**
- luonnoksia vai kuvakaappauksia valmiista käyttöliittymästä?**Ei ole, pelkästään luonnoksia**
- miten eri näkymien (views) välillä liikutaan?**Erilaisilla linkeillä sivustossa**

##### (prosessimalli)
- onko kuvattu? voi olla myös erillisessä projektisuunnitelmadokumentissa **ei ole**
- resurssit? budjetti? **Budjetista mainitaan kerran, mutta sitä ei dokumentissa paljasteta**
- riskianalyysi?**Ei ole kyseistä analyysia** 

##### (johtopäätökset, oma mielipide)
- mikä tekee hyvän dokumentin?**Dokumentti, joka vastaa kaikkiin ylhäällä oleviin kysymyksiin hyvin, jos sellaiseen on tarve.**
- onko tämä sellainen? miksi?**EI OLE, aivan liikaa tekstiä, joka jaarittelee ja kiertelee kuten nämä meidän vastauksetkin..**
- kaavioiden käyttö: laatu? määrä? hyöty? **Kaaviot ovat itseasiassa erittäin selkeät, eli iso plussa dokumentin tekijälle niistä. Ainakin itse ymmärsin hyvin kaavioista eri ominaisuuksien tarkoitukset**

#### 3. Palauta linkki tiedostoosi Githubissa tuubiin yhdessä B-kohdan vastauksen kanssa. Pienryhmistä (2-3 hlö) jokainen jäsen palauttaa linkin erikseen, jotta saa läsnäolopisteet ja mahdollisuuden nähdä muiden vastauksia.
#### 4. Valmistaudu esittelemään työsi.

### B. Oman projektin aloitus

##### Edelliseen analyysiin pohjautuen luonnostele seuraavia asioita ryhmäsi projektiin liittyen:

- lyhyt kuvaus projekti-ideastanne**paikannnusjärjestelmä kauppakeskuksiin ja marketeihin asiakkaita ja henkilökuntaa varten**
- käyttötapaukset (use cases): listaa oleellsimmat ranskalaisin viivoin käyttäjäryhmäkohtaisesti tai piirrä käyttötapauskaavio**Vartija näkee käyttäjät tarvittaessa, kun kauppa on sulkeutumassa. Myyjä näkee kolleegansa, ketkä ovat tauolla ja ketkä ei. Asiakas löytää tuotteet hyllyltä softan antamien neuvojen avulla. Myyjä löytää tuotteet hyllytettäviksi laitteen avulla ja löytää nopeasti perille. Vartija löytää esimerkiksi taskuvarkaan, ja nappaa sen kiinni kartalla merkitystä alueesta. Taskuvaras näkee vain tuotteet kun  myyjä näkee näiden lisäksi käyttäjiä ja vartija näkee kolleegat, myyjät, asiakkaat, tuotteet, paikkojen nimet ja sun muut infot mitä ikinä keksitäänkään.**
- toiminnalliset vaatimukset (functional requirements)**hae tuote, näytä tuote kartalla, opasta tuotteelle, näytä käyttäjä, arvioitu aika määränpäähän, databasesta tuotteiden haku, näytä käyttäjät**
- laadulliset vaatimukset (non-functional requirements)**Paikannus toimii automaattisesti ja ainoa asia mitä asiakkaan pitää tietää, on tuotteen nimi ja kirjoittaa se hakupalkkiin ja softa alkaa automaattisesti jäljittää asiakasta ja tuotteen paikkaa ehdottaakseen nopeimman reitin tuotten luo**
- käyttöliittymäluonnos (mockup)**Google maps tyylinen pohja piirros jossa haluttu tuote on pilkulla merkitty pohjapiirrokseen. Pohjapiirrustuksessa on myös visualisoitu hyllyt, niiden numerot ja klikkaamalla hyllyä tulee tieto hyllyalueella olevista tuotteista. Ikkunassa on myös hakupalkki jolla voi hakea esim: tuotteita ja softa aloittaa paikannuksen välittömästi.**

##### Toimintaohje

1. Tallenna luomasi tiedostot oman ryhmäsi Github repoon. 
2. Pyydä opettajalta kommentit/apuja joko lopuksi tai jos et ole aivan varma, mitää pitää tehdä.
3. Palauta tuubiin A-kohdan vastauksen lisäksi linkit B-kohdassa luotuihin tiedostoihin ja Github käyttäjätunnuksesi.


