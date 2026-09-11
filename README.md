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

## Yhteydenottolomakkeen käyttöönotto

Yhteystiedot-sivulla on nyt lomake ("Ota yhteyttä / pyydä tarjous"), mutta se ei vielä lähetä mitään minnekään — GitHub Pages ei osaa käsitellä lomakkeita itse, joten tarvitaan ilmainen kolmannen osapuolen palvelu:

1. Rekisteröidy osoitteessa [formspree.io](https://formspree.io) (ilmainen taso riittää pienelle yritykselle, n. 50 viestiä/kk)
2. Luo uusi lomake ja kopioi sen antama osoite (muotoa `https://formspree.io/f/xxxxxxxx`)
3. Avaa `yhteystiedot.html` ja korvaa lomakkeen `action`-kentän arvo `https://formspree.io/f/YOUR_FORM_ID` omalla osoitteellasi
4. Poista samalla tiedostosta rivi `<p class="form-note">Lomake vaatii vielä käyttöönoton...</p>`, kun lomake on käytössä

Vaihtoehtoja Formspreelle: Web3Forms ja Getform toimivat samalla periaatteella.

## Etusivun kuva

Etusivun hero-kuvaksi valitsin toistaiseksi Verkatehdas-kuvan referensseistä (`assets/img/Verkatehdas-julkisivu.png`), koska se on visuaalisesti vaikuttava kohde. Jos haluat käyttää jotain muuta kuvaa (esim. työmaakuva tai kuva tiimistä), vaihda polku `index.html`-tiedoston `<img>`-tagista.

## Favicon ja SEO-perusasiat

- Favicon-kuvakkeet on generoitu logon salamakuviosta (matala resoluutio, mutta toimii tarkoituksessaan pienessä koossa)
- Jokaisella sivulla on nyt og:- ja twitter-metatiedot somejakoja varten
- Etusivulla on schema.org-merkintä (tyyppi "Electrician"), joka auttaa hakukoneita ymmärtämään mistä yrityksestä on kyse
- Kaikki og:image ja schema-kuva osoittavat toistaiseksi logoon — vaihda oikeaan valokuvaan kun sellainen on saatavilla

## Kartan responsiivisuus

Yhteystiedot-sivun kartta on nyt korjattu skaalautumaan mobiilissa (suhteellinen kokoluokka kiinteän pikselikoon sijaan).

## Huomioita sisällöstä


- Blogi-sivu jätettiin pois, koska sitä ei ollut olemassa nykyisellä sivustolla
- Palvelut-sivun "Huolto ja ylläpito" -kohdan viimeinen lause oli alkuperäisessä tallenteessa katkennut kesken ("...osaavat asentajamm...") — täydensin sen luontevasti sanoihin "asentajamme ovat osaavia". Kannattaa tarkistaa tämä kohta alkuperäiseltä sivustolta ja korjata tarvittaessa
- Väripaletti (tumma sininen + keltainen/amber) ja fontit (Archivo otsikoihin, Inter leipätekstiin) on poimittu alkuperäisen sivuston CSS:stä, mutta ulkoasu on rakennettu uudelleen puhtaalta pöydältä — ei siis pikselintarkka kopio vanhasta, vaan samaan henkeen tehty kevyempi versio
