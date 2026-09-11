# hsasennus.fi — staattinen versio

Tässä kansiossa on neljä html-sivua ja yksi yhteinen style.css, jotka on rakennettu alkuperäisen hsasennus.fi-sivuston sisällöstä. Ei riippuvuuksia, ei build-vaihetta — pelkkää html/css:ää, joten sopii suoraan GitHub Pagesille.

## Käyttöönotto GitHub Pagesilla

1. Luo GitHubiin uusi repositorio (esim. `hsasennus-fi`)
2. Lataa tämän kansion tiedostot (`index.html`, `palvelut.html`, `yhteystiedot.html`, `yleista.html`, `style.css`) repositorion juureen
3. Mene repositorion asetuksiin: **Settings → Pages**
4. Valitse lähteeksi **Deploy from a branch**, branch `main`, kansio `/ (root)`
5. Tallenna — sivusto ilmestyy muutaman minuutin päästä osoitteeseen `https://<käyttäjätunnus>.github.io/hsasennus-fi/`

## Oman verkkotunnuksen (hsasennus.fi) liittäminen

Jos haluatte käyttää samaa hsasennus.fi-osoitetta jatkossakin:

1. Lisää repositorion juureen tiedosto `CNAME`, sisältönä pelkkä rivi `hsasennus.fi`
2. Verkkotunnuksen DNS-hallinnassa (siellä missä domain on rekisteröity) lisätään joko A-tietueet GitHubin IP-osoitteisiin tai CNAME-tietue osoittamaan `<käyttäjätunnus>.github.io`:hon — tarkat ohjeet GitHubin dokumentaatiosta kohdasta "Managing a custom domain for your GitHub Pages site"
3. Tämä vaihe kannattaa tehdä vasta kun sivusto on ensin testattu toimivaksi github.io-osoitteessa

## Huomioita sisällöstä

- Blogi-sivu jätettiin pois, koska sitä ei ollut olemassa nykyisellä sivustolla
- Palvelut-sivun "Huolto ja ylläpito" -kohdan viimeinen lause oli alkuperäisessä tallenteessa katkennut kesken ("...osaavat asentajamm...") — täydensin sen luontevasti sanoihin "asentajamme ovat osaavia". Kannattaa tarkistaa tämä kohta alkuperäiseltä sivustolta ja korjata tarvittaessa
- Väripaletti (tumma sininen + keltainen/amber) ja fontit (Archivo otsikoihin, Inter leipätekstiin) on poimittu alkuperäisen sivuston CSS:stä, mutta ulkoasu on rakennettu uudelleen puhtaalta pöydältä — ei siis pikselintarkka kopio vanhasta, vaan samaan henkeen tehty kevyempi versio
