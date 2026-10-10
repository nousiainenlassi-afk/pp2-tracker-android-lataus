# PP2 Tracker Android 1.0.3 beta

Laskee Pro Pilkki 2:n kisatuloksen puhelimella pelattaessa. Peli ei näytä
kisan tulosta kesken kisan; PP2 Tracker lukee nostot ruudulta ja näyttää
tuloksen pienessä palkissa pelin päällä.

**Tämä on Android-versio.** Windows-version asennusohjelma on eri tiedosto.

> **Beta:** testattu Android-emulaattorilla (näyttö 2400 × 1080). Eri
> kokoisilla näytöillä tunnistus voi vaatia säätöä – kerro jos jokin ei
> toimi (ks. *Ongelmia?* alla).

## Vaatimukset

- Android 11 tai uudempi
- Pro Pilkki 2 Androidille (Play Kaupasta)

## Asennus

1. Lataa puhelimella tiedosto **PP2-Tracker-Android-1.0.3-beta.apk**.
2. Avaa ladattu tiedosto (ilmoituksista tai Tiedostot-sovelluksen
   Lataukset-kansiosta).
3. Android kysyy, sallitaanko asennus tästä lähteestä: valitse
   **Asetukset → Salli tästä lähteestä** ja palaa takaisin.
4. Paina **Asenna**.
5. Jos Play Protect varoittaa tuntemattomasta sovelluksesta, valitse
   **Lisätietoja → Asenna silti**. Varoitus tulee kaikista Play Kaupan
   ulkopuolisista sovelluksista.

## Käyttöönotto (kerran)

1. Avaa **PP2 Tracker**.
2. Salli **ilmoitukset**, kun sovellus kysyy. Ilmoituksesta näkee, että
   laskuri on päällä, ja siitä sen voi lopettaa.
3. Paina **Salli tulospalkki pelin päällä** ja kytke lupa päälle
   PP2 Trackerille. Palaa takaisin.

## Pelaaminen

1. Avaa PP2 Tracker ja paina **Aloita ruudun luku**.
2. Android kysyy lupaa ruudun jakamiseen: valitse **Koko näyttö** (englanniksi *Share entire screen*; uusimmat
   Androidit ehdottavat oletuksena yhtä sovellusta, vaihda se
   alasvetovalikosta) ja
   **Aloita**. Lupa kysytään joka kerta – se on Androidin vaatimus.
3. Avaa peli ja pelaa. Tulospalkki näkyy pelin päällä:

   ```
   KL: 1 234 g              ↶ │ ✕
   Viim. Ahven 370 g  •  7 kpl
   ```

   - Ylärivi: kisatyyppi lyhenteenä ja kisan tulos (paino tai kappaleet
     kisatyypin mukaan).
   - Alarivi: viimeisin kala ja kaikkien kalojen määrä.
   - **↶** peruu viimeisimmän kalan.
   - **✕ pitkällä painalluksella** nollaa koko saaliin. Lyhyt napautus
     ei nollaa mitään.
   - Palkkia voi siirtää raahaamalla tekstistä.

Laskuri hoitaa loput itse:

- **Nostot** luetaan pelin vihreästä nostoviestistä ("Ahven 317G").
  Alamittaiset ja kisatyyppiin kuulumattomat kalat eivät kasvata tulosta.
- **Kisatyyppi** luetaan pelin yläpaneelista. Sen voi myös valita käsin
  sovelluksen valikosta.
- **Uusi kisa nollaa laskurin** automaattisesti: kun kisatyyppi vaihtuu
  tai kisan kello alkaa alusta. Laskurin voi käynnistää myös kesken kisan;
  jo kirjatut kalat säilyvät.

Lopetus: ilmoituksen **Lopeta**-nappi tai sovelluksen **Lopeta ruudun luku**.

## Kisatyyppien lyhenteet

| Lyhenne | Kisatyyppi | Lyhenne | Kisatyyppi |
|---|---|---|---|
| Norm | Normaali | Kiiski / Kiiski kpl | Vain kiiski (, kpl) |
| Kpl | Kappalemäärä | Ahven / Ahven kpl | Vain ahven (, kpl) |
| KL / KL kpl | Kaikki lajit (, kpl) | Hauki | Vain hauki |
| S.kala | Suurin kala | S.hauki | Suurin hauki |
| Lajit | Eniten lajeja | Kuha / S.kuha | Vain kuha / Suurin kuha |
| K&T / K&T kpl | Kirjo ja taimen (, kpl) | Särkik. / Särkik. kpl | Vain särkikalat (, kpl) |
| Pasuri / Pasuri kpl | Vain pasuri (, kpl) | S.särkik. | Suurin särkikala |
| Made / Made kpl | Vain made (, kpl) | Top 3 / Top 5 | Kolme / Viisi suurinta kalaa |
| Siika / Siika kpl | Vain siika (, kpl) | Ruutu / Ruutu kpl | Ruutupilkki (, kpl) |
| Harj. | Harjoittelu | | |

## Kieli ja englanninkielinen peli

Sovelluksen kieli vaihdetaan pääikkunan **Kieli**-valinnasta: Automaattinen
(puhelimen kieli; suomi → suomi, muut → englanti), Suomi tai English.
Kielen vaihto näkyy heti, myös tulospalkissa.

Laskuri toimii myös englanninkielisellä pelillä: kalojen nimet (Perch,
Ruffe, Slv.bream ...) ja kisatyyppi (GAME TYPE) tunnistetaan sekä suomeksi
että englanniksi. Pelin kieli ja sovelluksen kieli ovat toisistaan
riippumattomat. Ukrainan- ja venäjänkielistä peliä ei vielä tueta.

## Kisaloki

Jokaisen kisan tapahtumat (nostot, peruutukset, kisatyypin vaihdot) ja
kisan päättyessä kalat lajeittain tallentuvat tekstitiedostoon kansioon
**Lataukset/PP2 Tracker/kisalokit** (yksi tiedosto kisaa kohden, enintään
30 uusinta). Siitä voi tarkistaa jälkikäteen, jäikö kala laskematta tai
tuliko se kahdesti. Erillistä tallennuslupaa ei tarvita.

## Ongelmia?

| Ongelma | Korjaus |
|---|---|
| Palkki ei näy | Sovelluksessa: *Salli tulospalkki pelin päällä*. Aloita sitten ruudun luku uudelleen. |
| Kaloja ei lasketa | Valitse ruudun jakamisessa **Koko näyttö**, ei yksittäistä sovellusta. |
| Kala puuttuu tai paino on väärin | ↶ poistaa väärän kalan (käsin lisäys ei vielä onnistu). Ota testikuva (alla) ja lähetä. |
| Laskuri nollautui itsestään | Kerro milloin – uuden kisan tunnistus on betassa. |

**Testikuva vikailmoitusta varten:** paina sovelluksessa
**Tallenna testikuva**, palaa peliin ja odota hetki. Kuva tallentuu
puhelimen kansioon `Android/data/fi.pp2tracker/files/testikuvat`.
Lähetä se ja kerro, mitä pelissä näkyi.

## Tietosuoja

Kaikki käsitellään puhelimessa. Sovellus ei lähetä mitään minnekään eikä
tallenna ruutua – paitsi kun itse painat *Tallenna testikuva*. Ruudun
jakamisen lupa on voimassa vain, kunnes lopetat luvun.

Ainoa verkkoyhteys on päivitystarkistus: kun sovellus avataan, se kysyy
enintään kerran vuorokaudessa GitHubista uusimman version numeron. Mitään
tietoja ei lähetetä; GitHub näkee pyynnön kuten minkä tahansa nettisivun
avauksen. Laskuri toimii myös ilman verkkoa.

Tekstintunnistuksen (Google ML Kit) omat käyttötilastot on kytketty pois.
Versiot 1.0 ja 1.0.1 beta lähettivät niitä Googlelle (ei ruutukuvia eikä
saalistietoja).

## Päivitys ja poisto

- **Päivitys:** lataa uusi APK ja asenna se vanhan päälle. Annetut luvat
  säilyvät. Muutokset: *PAIVITYSHISTORIA.txt* julkaisun tiedostoissa.
  Kun uusi versio julkaistaan, sovelluksen pääikkunaan tulee ilmoitus ja
  **Lataa**-nappi. Vanhallakin versiolla voi jatkaa pelaamista.
- **Poisto:** kuten muutkin sovellukset (paina kuvaketta pitkään →
  Poista).

## Tunnetut rajoitukset (beta)

- Testattu vain emulaattorilla, näyttö 2400 × 1080.
- Saalis häviää, jos Android sulkee sovelluksen taustalla.
- Kalaa ei voi vielä lisätä käsin.
- Ukrainan- ja venäjänkielistä peliä ei tueta (suomi ja englanti toimivat).
