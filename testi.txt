from pathlib import Path

content = r"""# Bellgallery

## Kuvagalleria

**Koulutus:** Tieto- ja viestintätekniikka  
**Tekijät:** Elmeri Uitto, Joonatan Lipiäinen, Max Röytiö, Tuomas Kilpeläinen  
**Vuosi:** 2025

---

## Tiivistelmä

Projektin tavoitteena oli luoda toimiva kuvagalleriasivusto, johon sisältyy käyttäjän rekisteröinti, sisäänkirjautuminen sekä kuvien lataus palvelimelle. Lisävaatimuksina oli kuvien tallennus tiedostotyypin mukaan omiin kansioihin sekä kuvien skaalaus sopiviin resoluutioihin.

Projekti toteutui onnistuneesti, ja sivustosta saatiin moderni sekä helppokäyttöinen. Toteutuksen painopiste oli helppokäyttöisyydessä, käyttäjäystävällisyydessä sekä toiminnallisuuksien tehokkuudessa.

**Avainsanat:** Django, Python, kuvagalleria

---

## Abstract

The aim of this project was to create a functional photo gallery website that includes user registration, login, and image uploading to the server. Additional requirements included saving images into separate folders based on file type, as well as scaling the images to the appropriate resolutions.

The project was successfully completed, and the site was made modern and easy to use. The focus of the project was on user-friendliness, ease of use, and functional efficiency.

**Keywords:** Django, Python, photogallery

---

# Sisällys

1. [Johdanto](#1-johdanto)
2. [Käytetyt tekniikat](#2-käytetyt-tekniikat)
   - [2.1 Taustajärjestelmätekniikat (backend)](#21-taustajärjestelmätekniikat-backend)
   - [2.2 Käyttöliittymä](#22-käyttöliittymä)
   - [2.3 Tietoturvallisuus](#23-tietoturvallisuus)
   - [2.4 Tietokantarakenne](#24-tietokantarakenne)
3. [Toiminnallisuudet](#3-toiminnallisuudet)
   - [3.1 Yleisnäkymä](#31-yleisnäkymä)
   - [3.2 Käyttäjien tunnistautuminen](#32-käyttäjien-tunnistautuminen)
   - [3.3 Kuvien katselu ja hakeminen](#33-kuvien-katselu-ja-hakeminen)
   - [3.4 Postauksen lisääminen ja poistaminen](#34-postauksen-lisääminen-ja-poistaminen)
   - [3.5 Ylläpitosivusto (Admin-sivusto)](#35-ylläpitosivusto-admin-sivusto)
   - [3.6 Julkaisualusta (PythonAnywhere)](#36-julkaisualusta-pythonanywhere)
4. [Työnjako](#4-työnjako)
5. [Yhteenveto ja analyysi](#5-yhteenveto-ja-analyysi)
6. [Lähteet](#lähteet)

---

# Kuvat

- Kuva 1. Kotisivu, kun käyttäjä ei ole kirjautunut sisään
- Kuva 2. Sivupalkki
- Kuva 3. Kotisivu, kun käyttäjä on kirjautunut sisään
- Kuva 4. Käyttäjän profiili
- Kuva 5. Hakutoiminto
- Kuva 6. Julkaisulaatikko

> **Huomio:** Lisää kuvat tähän kansioon esimerkiksi `images/`-hakemistoon ja päivitä alla olevat kuvalinkit vastaamaan tiedostojen nimiä.

---

# 1. Johdanto

Tämän projektin tavoitteena oli kehittää verkkopohjainen kuvagalleriasovellus hyödyntäen Django-verkkokehystä. Sovellus tarjoaa käyttäjille mahdollisuuden rekisteröityä, kirjautua sisään sekä lisätä ja hallita omia kuvia ja GIF-tiedostoja. Sovelluksen profiilisivu tarjoaa käyttäjille mahdollisuuden tarkastella ja poistaa lataamiansa postauksia.

Projektissa hyödynnettiin nykyaikaisia teknologioita ja kirjastoja, jotka mahdollistivat toimivan, interaktiivisen ja ylläpidettävän verkkosovelluksen rakentamisen. Taustajärjestelmä (backend) toteutettiin Djangon avulla, mikä tarjosi tehokkaan ja helppokäyttöisen pohjan sovellukselle. Käyttöliittymä (front-end) rakennettiin HTML5-, CSS- ja JavaScript-tekniikoilla, jotka mahdollistivat käyttäjäystävällisen ja modernin ulkoasun.

Sovellus keskittyy tarjoamaan turvallisen ja helppokäyttöisen ympäristön, jossa käyttäjät voivat lisätä kuviaan, hallita niitä ja käyttää monipuolisia toiminnallisuuksia, kuten hakutoimintoja ja TAG-merkintöjä. Projekti yhdistää teknologian ja käytettävyyden luoden kokonaisuuden, joka vastaa modernin verkkosovelluksen vaatimuksia.

---

# 2. Käytetyt tekniikat

Toteutuksessa hyödynnettiin useita nykyaikaisia teknologioita ja kirjastoja, jotka jakautuvat taustajärjestelmän (backendin), käyttöliittymän (front-endin) ja ulkoisten kirjastojen kesken. Näiden avulla pystyttiin rakentamaan toimiva, interaktiivinen ja ylläpidettävä verkkosovellus.

## 2.1 Taustajärjestelmätekniikat (backend)

"Backend" eli taustajärjestelmä viittaa verkkosivuston kehityksen palvelinpuoleen, jossa kehittäjä keskittyy sivuston toiminnallisuuteen. Se koostuu palvelimista, tietokannoista, koodista ja sovelluksista. Backendissä kirjoitettu koodi mahdollistaa sovelluksen kommunikoinnin tietokannan kanssa esimerkiksi tietojen lukemisen, tallentamisen, päivittämisen tai poistamisen tietokannasta. (W3Schools, n.d.)

Projektissa käytettiin Django-web-kehystä ja Python-ohjelmointikieltä.

Django on korkeatasoinen Python-pohjainen web-sovelluskehys, joka perustuu avoimeen lähdekoodiin. (Meet Django, n.d.) Django mahdollisti pohjan web-sovellukselle, koska se on helppokäyttöinen sekä kevyt ajaa. Projektissa käytettiin Djangon sisäänrakennettuja ominaisuuksia, kuten `ImageField`-kenttää sekä `Authentication System` -järjestelmää. Nämä mahdollistivat helpon sisäänkirjautumisen nettisivulle sekä kuvien latausominaisuuden.

## 2.2 Käyttöliittymä

Käyttöliittymä tarkoittaa ohjelmistossa käyttäjälle näkyvää osaa, jonka kautta käyttäjä pystyy ohjaamaan ohjelmistoa. Projektin käyttöliittymä luotiin hyödyntäen HTML5- ja CSS-merkkauskieliä sekä JavaScript-ohjelmointikieltä.

Sivun rakenne tehtiin käyttäen HTML5:tä, jonka jälkeen sivusto tyyliteltiin CSS:n avulla. Toiminnalliset asiat, kuten valikot, tehtiin käyttäen JavaScriptiä.

## 2.3 Tietoturvallisuus

Projektissa hyödynnettiin Djangon suosittelemia turvallisuutta parantavia middleware-asetuksia. Asetuksiin sisältyy muun muassa CSRF- ja istuntoevästeiden suojaus, XSS- ja MIME-tyyppien suojaukset sekä WhiteNoise, joka on kirjasto staattisten tiedostojen jakeluun. (Django, n.d.-b)

Salasanojen suojauksessa käytettiin Djangon salasanavalidaattoreita, jotka estävät muun muassa yksinkertaisten salasanojen käytön.

Sivusto vaatii kaikissa API-pyynnöissä CSRF-tokenin, mikä suojaa sivustojen välisiltä pyyntöhuijauksilta (Cross-Site Request Forgery). (Django, n.d.-b)

## 2.4 Tietokantarakenne

Sovelluksen tietokantarakenne hyödyntää Djangon omaa ORM-pohjaista rakennetta, joka koostuu sovelluksessa kolmesta eri mallista: `User`, `Category` ja `Photo`. (Django, n.d.-c)

### User

`User`-malli käyttää Djangon sisäänrakennettua käyttäjämallia, joka tallentaa käyttäjien tunnistetiedot tietokantaan ja pystyy sieltä varmistamaan oikean käyttäjän sekä kuvien omistajuuden.

### Category

`Category`-malli on kuvien tageille tehty tietokanta, josta sovelluksen hakutoiminto voi kerätä yhteen kaikki samat tagit omaavat kuvat.

### Photo

`Photo`-malli sisältää kaikki kuvat sekä GIF-tiedostot. Se tallentaa tietokantaan kuvat sekä niiden kuvatekstit.

Tietokanta osaa tallentaa eri kuvamuodot omiin kansioihinsa niiden tiedostomuodon perusteella: JPG, GIF ja PNG.

`Photo`-malli sisältää jokaiseen kuvaan liittyvät tiedot:

- käyttäjä, joka on ladannut kuvan
- kategoriat eli tagit
- itse kuvatiedosto
- kuvateksti
- julkaisupäivämäärä

---

# 3. Toiminnallisuudet

Projektista oli tarkoitus tehdä käyttäjäystävällinen sekä moderni kuvagalleria-applikaatio käyttäen Django-websovelluskehystä. Sovelluksessa käyttäjien on mahdollista tehdä postauksia, jotka sisältävät kuvan, tekstin sekä tageja. Käyttöliittymä on yksinkertainen ja helppokäyttöinen.

Sivustolle täytyy luoda oma käyttäjä ennen postauksien tekemistä. Tätä varten suunniteltiin rekisteröinti- sekä kirjautumissivut.

## 3.1 Yleisnäkymä

![Kuva 1. Kotisivu, kun käyttäjä ei ole kirjautunut sisään](images/kuva1.png)

**Kuva 1.** Kotisivu, kun käyttäjä ei ole kirjautunut sisään.

Sivustolla on vasemmassa kulmassa valikko, kuten kuvassa 2 näkyy. Siitä käyttäjä voi valita pääsivun, hakuominaisuuden ja oman profiilin. Sivupalkista voi myös kirjautua sisään ja ulos.

Etusivulta käyttäjä voi nähdä uusimmat julkaisut ja tehdä omia julkaisuja.

![Kuva 2. Sivupalkki](images/kuva2.png)

**Kuva 2.** Sivupalkki.

## 3.2 Käyttäjien tunnistautuminen

Sivustolla on toteutettu käyttäjien kirjautumis- ja rekisteröitymisjärjestelmä hyödyntäen Djangon sisäänrakennettua Authentication-järjestelmää sekä AJAX-toimintoja.

Käyttäjä pystyy luomaan käyttäjän ja kirjautumaan sillä sisään. Kirjautuneena käyttäjälle avautuu ominaisuus ladata kuvia sivustolle.

![Kuva 3. Kotisivu, kun käyttäjä on kirjautunut sisään](images/kuva3.png)

**Kuva 3.** Kotisivu, kun käyttäjä on kirjautunut sisään.

Rekisteröityminen sivulle toteutettiin JavaScriptin avulla AJAX-pyyntönä. Pyyntö välittää saadut rekisteröintitiedot Djangon palvelimelle, joka tallentaa uuden käyttäjän rekisteriin ja palauttaa JSON-muotoisen (`True` tai `False`) viestin siitä, onnistuiko rekisteröinti vai ei.

Jos rekisteröinti epäonnistui, sivusto kertoo tarkan syyn, esimerkiksi:

> "Käyttäjänimi on jo olemassa."

Sisäänkirjautuminen on toteutettu samalla tekniikalla. JavaScript lähettää AJAX-pyynnön palvelimelle, joka varmistaa käyttäjänimen ja salasanan oikeellisuuden. Tämän jälkeen se palauttaa JSON-vastauksen onnistuneesta sisäänkirjautumisesta.

## 3.3 Kuvien katselu ja hakeminen

Julkaisut näkyvät gallerian etusivulla uusimmasta vanhimpaan. Kirjautunut käyttäjä voi myös nähdä omat postauksensa omalta profiilisivultaan, kuten kuvassa 4.

![Kuva 4. Käyttäjän profiili](images/kuva4.png)

**Kuva 4.** Käyttäjän profiili.

Hakusivulle on rakennettu hakukenttä, kuten kuvassa 5 esitetään. Tämän ansiosta käyttäjä pystyy etsimään kuvia haluamansa kuvauksen tai tagien avulla.

Kaikki hakukriteeriä vastaavat kuvat tulevat syötteeseen, ja hakutulokset voidaan järjestää uusimmasta vanhimpaan tai päinvastoin.

Toiminto toimii myös klikkaamalla kuvien tageja, jolloin ohjelmisto etsii kaikki kuvat, joissa tämä tagi esiintyy.

![Kuva 5. Hakutoiminto](images/kuva5.png)

**Kuva 5.** Hakutoiminto.

## 3.4 Postauksen lisääminen ja poistaminen

Sivustolle on toteutettu helppokäyttöinen kuvien latausominaisuus hyödyntäen Djangon `ImageField`-kenttää, kuten kuvassa 6 näkyy.

Postaukset on sallittu vain sisään kirjautuneille käyttäjille, ja toiminto käyttää `@login_required`-dekoraattoria varmistaakseen tämän.

Kun käyttäjä on kirjautunut, hän voi lisätä postauksen etusivun yläosassa olevasta kentästä. Postaus sisältää pakollisen kuvan, kuvauksen ja vapaaehtoisia tageja.

Tiedot lähetetään palvelimelle HTML-lomakkeella ja Django käsittelee lomakkeen POST-pyynnön. Palvelin tallentaa kuvan tietokantaan `Photo`-oliona ja liittää siihen kuvauksen, tagit, päivämäärän ja käyttäjänimen.

Käyttäjä pystyy myös helposti poistamaan postauksiaan oman profiilinsa kautta painamalla **Poista**-painiketta. Toiminto toimii samalla periaatteella kuin lisääminen. Sivu lähettää POST-pyynnön ja poistaa kuvan sekä tekstit palvelimelta.

![Kuva 6. Julkaisulaatikko](images/kuva6.png)

**Kuva 6.** Julkaisulaatikko.

## 3.5 Ylläpitosivusto (Admin-sivusto)

Djangossa on sisäänrakennettu ylläpitosivusto, jonka kautta moderaattorit sekä adminit voivat hallita sivuston sisältöä ja käyttäjiä muokkaamatta koodia.

Sivusto vaatii vähintään yhden superuserin, joka voi antaa oikeudet muille käyttäjille.

Työkalua hyödynnettiin projektissa lisäämällä sinne ominaisuudet muokata ja poistaa postauksia sekä kuvia ja niiden tekstejä. Sivustolta näkee myös kaikki käyttäjät, ja se antaa mahdollisuuden poistaa sekä lisätä niitä.

## 3.6 Julkaisualusta (PythonAnywhere)

Julkaisualustana käytettiin PythonAnywhere-palvelua, joka mahdollistaa verkkosivun julkaisun suoraan selainpohjaisesti. PythonAnywhere tukee Pythonia sekä laajaa valikoimaa valmiiksi asennettuja kirjastoja. (PythonAnywhere, 2024)

Alustalle luotiin ensin tyhjä virtuaaliympäristö, johon Django asennettiin. Tämän jälkeen projekti ladattiin suoraan GitHubin kautta palvelimelle, johon myös määriteltiin oikeat reitit staattisille tiedostoille (`static`).

Sivusto toimii virtuaalikoneen sisällä olevassa virtuaaliympäristössä (`venv`), joka luotiin koneeseen manuaalisesti.

Tietoturvasyiden vuoksi sivustolle lisättiin käyttäjätunnus sekä salasana, jotta vain halutut henkilöt pääsevät sitä kokeilemaan.

---

# 4. Työnjako

Alkuperäisesti suunnittelimme, että Joonatan tekee HTML-pohjan, Elmeri hoitaa tietokannan ja Max sekä Tuomas tekevät backend-koodauksen.

Hyvin nopeasti huomasimme, että työnjakoa täytyi muuttaa, koska alkuperäinen suunnitelma sivun toteutuksesta muuttui täysin. Tämä johti siihen, että jokainen alkoi itsenäisesti ideoida ja toteuttaa projektin osia.

Loppujen lopuksi kaikki tekivät yksittäisiä ominaisuuksia ja antoivat oman panoksensa projektille. Kiireen myötä Tuomas joutui kokeneempana ottamaan enemmän vastuuta projektin koodauksesta.

Max sai loppujen lopuksi Elmerin kanssa sivuston julkaistua netissä, ja projekti saatiin valmiiksi.

---

# 5. Yhteenveto ja analyysi

Projektin toteuttaminen onnistui melko hyvin, ja saimme luotua toimivan sekä modernin sivuston. Tekniset ratkaisut onnistuivat suunnitellusti, ja kaikki halutut toiminnot saatiin toteutettua.

Projektin suurimpia haasteita olivat aikataulutus sekä ryhmän vähäinen kommunikointi. Heikko viestintä johti myös erilaisiin toteutustapoihin, kuten CSS-tyylien kirjoittamiseen sekä HTML-tiedostoihin että erillisiin CSS-tiedostoihin.

Teknisesti haastavinta oli saada sivusto toimimaan ulkopuolisessa palvelimessa. Yritimme aluksi käyttää Azuren virtuaalikonetta, mutta tämä osoittautui hankalaksi, koska sisäänkirjautuminen sivulle vaati HTTPS-sertifikaatin. Lopulta saimme palvelimen toimimaan käyttäen PythonAnywhere-alustaa.

Sivustoa voisi jatkokehittää lisäämällä sinne tykkäyspainikkeet sekä mahdollisuuden kommentoida muiden julkaisemia postauksia. Nämä ominaisuudet jätettiin kuitenkin projektin ulkopuolelle, koska aikaa oli rajatusti.

Tietokanta olisi myös voitu vaihtaa SQLitestä paremmin skaalautuvaan tietokantaan, kuten MySQL:ään tai PostgreSQL:ään.

---

# Lähteet

- Django. (n.d.-a). *Meet Django.*  
  https://www.djangoproject.com/

- Django. (n.d.-b). *Middleware.*  
  https://docs.djangoproject.com/en/5.2/ref/middleware/#securitymiddleware

- Django. (n.d.-c). *Models.*  
  https://docs.djangoproject.com/en/5.2/topics/db/models/

- PythonAnywhere. (2024). *Host, run and code Python in the cloud!*  
  https://www.pythonanywhere.com/

- W3Schools. (n.d.). *Backend development tools.*  
  https://www.w3schools.in/web-development/backend-web-development
"""

path = Path("/mnt/data/Bellgallery_raportti.md")
path.write_text(content, encoding="utf-8")

print(f"Markdown-tiedosto luotu: {path}")
