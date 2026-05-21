# Wäsänen – pääsivun suunnitelma (digitaaliset ratkaisut)

Tämä dokumentti kuvaa uuden **etusivun** (`index.html` juuressa) rakenteen, sisällön ja toteutuksen. Laser-/puutyöpalvelu elää erillään kansiossa [`laser/`](laser/) ja mainitaan pääsivulla vain lyhyesti.

---

## 1. Tavoite ja rooli

| Kohde | Rooli |
|--------|--------|
| **Juuri (`/`)** | Pääliiketoiminta: digitaaliset ratkaisut (verkkosivut, työkalut, analytiikka, IoT, pilvi jne.) |
| **`laser/`** | Sivutoimi: puutyöt ja kaiverrukset; oma sivu, sama brändi ja yhteystiedot |

**Ydinviesti:** Asiakkaalla on ongelma → ratkaistaan digitaalisesti. Asiakkaan tehtävä on kertoa ongelma (paikan päällä, puhelu tai viestit); loput hoituu Wäsäsen puolella.

**Sävy:** Ammattimainen mutta rehellinen – vahva kokemus, mutta harrastusprojekti → edullinen kuukausimaksu, runsaasti ilmaista ennen sopimusta.

---

## 2. Yhteiset tiedot (kopioi laser-sivulta)

Nämä pysyvät **identtisinä** laser-sivun kanssa:

| Kenttä | Arvo |
|--------|------|
| Yrityksen nimi | **Wäsänen** |
| Sähköposti | `contact@wasanen.fi` |
| Instagram | [@wasanen.store](https://instagram.com/wasanen.store) |
| Sijainti | Nurmijärvi · Uusimaa, Suomi |
| Vastausaika (teksti) | Yleensä saman päivän aikana |
| Lomake (Formspree) | `action="https://formspree.io/f/xnnzbwee"`, kentät: email, subject (vapaaehtoinen), message |
| Lomakkeen JS | Async submit + onnistumisviesti (sama logiikka kuin `laser/index.html`) |
| Schema.org `LocalBusiness` | name, email, address (Nurmijärvi, Uusimaa, FI), areaServed FI, sameAs Instagram |
| Footer-tagline | © Wäsänen · Anna mä wäsään. · Tehty ✦ Nurmijärvellä |

**Erot laser-sivuun:** meta-otsikot, kuvaus, avainsanat, `knowsAbout`, hero-tekstit ja navigaation ankkurit vastaavat digitaalipalvelua. Logo voidaan käyttää samaa (`logo.png` juureen tai `assets/`).

---

## 3. Sivun rakenne (osiot)

### 3.1 Header / navigaatio

Kiinteä header (scroll → tausta, kuten laser).

| Linkki | Ankkuri | Huomio |
|--------|---------|--------|
| Mitä teen | `#about` | Tai "Tarina" |
| Ratkaisut | `#solutions` | Esimerkkityökalut / osa-alueet |
| Miten etenee | `#process` | **Keskeisin osio** – 7 vaihetta |
| Hinnoittelu | `#pricing` | Ilmainen vaihe + kuukausimaksu |
| Laser & puu | `laser/` tai `#laser` | Lyhyt, linkki alisivulle |
| CTA | `#contact` | Ota yhteyttä |

### 3.2 Hero (`#top`)

**Eyebrow:** Digitaaliset ratkaisut · Nurmijärvi  

**Otsikko (luonnos):**  
*Ongelma pieniin osiin. Ratkaisu digitaalisesti.*

**Alaotsikko:**  
Autan yrityksiä ja yksityisiä asiakkaita, kun jokin arkea tai liiketoimintaa hidastaa tai puuttuu kokonaan. Verkkosivut, työkalut, analytiikka, älylaitteet ja pilvipalvelut – rakennetaan yhdessä, askel kerrallaan.

**CTA:**  
- Ensisijainen: `#contact` – Kerro ongelmastasi  
- Toissijainen: `#process` – Näin työ etenee  

**Hero-meta (ala):** Nurmijärvi · Uusimaa · FI · (ei puupajan viittausta)

**Visuaali:** Uusi banner/kuva – digitaalinen, ei `laser/banner.png`. Voi olla abstrakti (verkko, data, laitteet) tai työpöytä/koodi; ei pakollinen valokuva.

### 3.3 Marquee (valinnainen)

Pyörivä tekstiraita avainsanoilla, esim.:  
Verkkosivut · Työkalut · Analytiikka · IoT · Pilvi · Inventaario · Kellotus · Ravintoladata · Yhteistyöjärjestelmät · Raspberry Pi · ESP · ...

### 3.4 Tarina / mitä teen (`#about`)

**Otsikko:** Ratkaisen ongelmia digitaalisesti.

**Sisältö (bullet-logiikka kappaleissa):**

1. Asiakkaalla on ongelma – mikä tahansa: data puuttuu, prosessi on kökkö, järjestelmät eivät puhu keskenään.
2. Vahva kokemus: vuosia työkaluja, jakaminen pieniin osiin ja rakentaminen niistä on erityistaito.
3. Harrastus, ei massafirma → reilu ja läpinäkyvä hinnoittelu.
4. Asiakkaan panos on minimaalinen: kutsu paikalle (asennus ilmainen, **matkakulut** asiakkaalle), puhelu, videopalaveri tai viestit.

**Stats-rivi (3 laatikkoa, kuten laser):**

| Luku | Selite |
|------|--------|
| 0 € | Suunnittelu, demot ja tarjous ennen sopimusta |
| 1 | Ongelma kerrallaan – selkeä polku |
| ∞ | Rajattomat työkalutyypit (ei listaa lopullisena rajana) |

**Kuva:** Ei laser-galleriaa; valinnainen kuva työstä/koodista tai ilman kuvaa vain typografia.

### 3.5 Ratkaisut / esimerkit (`#solutions`)

**Otsikko:** Mitä voi syntyä?

**Lead:** Ei valmista tuotelistaa vaan esimerkkejä – lopullinen ratkaisu räätälöidään aina ongelmasta.

**Kortit (3–6 kpl, grid):**

| Kortti | Kuvaus |
|--------|--------|
| Data & analytiikka | Esim. ravintola: kävijät, kiinnostus, toimivuus – mittaus ja näkymät |
| Inventaario & varasto | Yrityksen tavaroiden seuranta, raportit |
| Kellotus & aikataulut | Työvuorot, muistutukset, integraatiot |
| Älyelektroniikka | Raspberry Pi, ESP, anturit, näytöt – fyysinen + digitaalinen |
| Verkkosivut & työkalut | Julkinen sivu, sisäiset työkalut, hallintapaneelit |
| Pilvi & yhteistyö | Pilvipalveluihin perustuvat collab-järjestelmät, synkronointi |

Jokaisessa kortissa: lyhyt kappale + tag (esim. "Ravintolat", "Teollisuus", "Pienyritys").

**Huomio copyssa:** "Ja oikeastaan mitä tahansa" – yksi kortti tai lead-lause, joka avaa rajattoman toimialan.

### 3.6 Prosessi (`#process`) – tärkein osio

Neljä–seitsemän vaihetta, tumma tausta (kuten laser-prosessi). **Tarkka järjestys käyttäjän kuvauksen mukaan:**

| # | Vaihe | Sisältö |
|---|--------|---------|
| 01 | Yhteydenotto | Lomake tai sähköposti. Kerro ongelma vapaasti. |
| 02 | Kartoitus | Keskustellaan ongelma läpi (puhelu, videotapaaminen, viestit tai paikan päällä). |
| 03 | Ensimmäinen demo | Ilmainen demo + lyhyt briiffi, miten ratkaisu toimisi käytännössä. |
| 04 | Viimeinen demo | Toinen demo; esitys kasvotusten tai videopalaverissa. |
| 05 | Tarjous | Kun kaikki on selvä, tarjous sähköpostiin. **Tähän asti kaikki ilmaista** – myös sinulle harjoittelua. |
| 06 | Käyttöönotto | Työkalu otetaan käyttöön; **ilmainen asennus** paikan päällä. Laitteet (Raspberry Pi, ESP, palvelimet, näytöt jne.) **laskutetaan erikseen** ostohinnalla. |
| 07 | Ylläpito | Kiinteä, edullinen **kuukausimaksu** työkalusta; arvio tarjouksessa, ei yllätyksiä. |

**Lead prosessille:**  
Selkeä polku ilman piilokuluja suunnitteluvaiheessa. Maksat vasta kun ratkaisu on käytössä ja kuukausimaksu alkaa.

### 3.7 Hinnoittelu (`#pricing`)

**Ei tarkkoja eurosummia** sivulla (ne tulevat tarjoukseen). Kolme–neljä korttia:

| Kortti | Otsikko | Sisältö |
|--------|---------|---------|
| Ilmainen vaihe | Suunnittelu & demot | Kartoitus, 2 demoa, esitys, tarjous – 0 € |
| Laitteet | Laitteistokulut | Ostot asiakkaalle (Pi, ESP, palvelin, näytöt…) – läpinäkyvä erittely tarjouksessa |
| Käyttöönotto | Asennus | Ilmainen työ; matkakulut erikseen |
| Käyttö | Kuukausimaksu | Kiinteä, arvioitu tarjouksessa; edullinen koska harrastus |

**Info-laatikko (kuten laser `pricing-note`):**  
Kuukausihinta riippuu mm. hostingista, datamäärästä, käyttäjämäärästä ja ylläpidon laajuudesta. Kerrataan: ammattitaito + harrastushinta.

### 3.8 Laser-viittaus (`#laser` tai erillinen pieni band)

**Lyhyt osio** (ei kilpaile hero:n kanssa):

- Otsikko: *Sivutoimena myös puutyöt*
- 2–3 lausetta: laserkaiverrus, leikkuulautat, lahjat – sama Wäsänen, erillinen palvelu.
- Painike: **Siirry laser-palveluun** → `laser/` (suhteellinen linkki)

Ei galleriaa eikä hinnoittelua laserille pääsivulla.

### 3.9 Yhteys (`#contact`)

**Identtinen rakenne** laser-sivun kanssa:

- Vasen: otsikko, lead, contact-list (sähköposti, Instagram, sijainti, vastausaika)
- Oikea: tumma lomake, Formspree, sama kentät

**Muutokset copyyn:**

- Otsikko: *Mikä ongelma pitäisi ratkaista?*
- Lead: Kerro tilanteesta – mitä pitäisi mitata, automatisoida tai rakentaa. Pienikin alku riittää.
- Lomake-otsikko: *Aloita keskustelu*
- Placeholder viestissä: esim. "Ravintolassa haluaisin nähdä kävijämäärät…" / "Tarvitsen inventaarion…"

### 3.10 Footer

- Brändi + kuvaus digitaalisista ratkaisuista (1–2 lausetta)
- Sarake **Sivut**: about, solutions, process, pricing, laser-linkki, contact
- Sarake **Yhteys**: sama kuin laser
- Bottom: sama copyright-rivi

---

## 4. Visuaalinen suunta (ero laser-sivuun)

Laser käyttää lämpimää puu-/metsäestetiikkaa (`--bg` cream, `--forest` vihreä, `--gold` kulta, Fraunces + Inter).

**Pääsivulle ehdotus:**

| Elementti | Laser | Pääsivu (ehdotus) |
|-----------|--------|-------------------|
| Tunnelma | Käsityö, luonto | Teknologia, selkeys, luottamus |
| Tausta | Lämmin cream | Hieman viileämpi neutraali (esim. `#eef1f4` / `#0d1117` hero) |
| Korostusväri | Kulta + metsänvihreä | Esim. syvä sininen/teal + yksi accent (sähköinen sininen tai minttu) |
| Fontit | Fraunces + Inter | Säilytä Inter body; otsikot voivat pysyä Fraunces **tai** vaihtaa esim. DM Sans / Space Grotesk digimaisemmaksi |
| Hero-kuva | Puupaja-banner | Uusi digi-banner (luodaan/myöhemmin placeholder) |
| Ikoniot | Puu/lahja | Data, verkko, laite, pilvi (SVG inline kuten laser) |

**Toteutusvaihtoehdot:**

1. **Kopioi laser-CSS-rakenne** (design tokens, komponentit) ja vaihda vain värit + tekstit → nopein, yhtenäinen brändi Wäsänen-nimellä.
2. **Uusi CSS-tiedosto** juuressa, jaettu vain logo + lomake-JS.

Suositus: **vaihtoehto 1** ensimmäisessä versiossa (nopea julkaisu), visuaalinen erottelu token-tasolla.

---

## 5. Tekninen toteutus

### 5.1 Tiedostorakenne (tavoite)

```
wasanen/
├── index.html          # Pääsivu (digitaaliset ratkaisut)
├── plan.md             # Tämä tiedosto
├── logo.png            # Kopio tai symlink laser/logo.png
├── banner.png          # Uusi (pääsivu)
├── llms.txt            # Digitaalipalvelun yhteenveto
├── robots.txt
├── sitemap.xml         # Juuri + laser/
├── CNAME               # wasanen.store → juuri
└── laser/
    ├── index.html      # Nykyinen puu/laser-sivu (päivitä canonical → /laser/)
    └── ...
```

### 5.2 Laser-alisivun päivitykset (pieni erillinen tehtävä)

- `canonical` ja `og:url` → `https://wasanen.store/laser/` (tai vastaava polku)
- Headeriin linkki: **Etusivu** → `/`
- Footer/maininta: "Digitaaliset ratkaisut" → `/`

### 5.3 Pääsivun SEO

```html
<title>Wäsänen – Digitaaliset ratkaisut</title>
<meta name="description" content="Räätälöidyt digitaaliset työkalut, verkkosivut, analytiikka ja IoT-ratkaisut Nurmijärveltä. Ilmainen suunnittelu ja demot ennen tarjousta." />
```

Avainsanat: digitaaliset ratkaisut, verkkosivut, analytiikka, IoT, työkalut, Nurmijärvi, Wäsänen, Raspberry Pi, pilvi, inventaario, …

### 5.4 Saavutettavuus & suorituskyky

- Sama käytännöt kuin laser: `lang="fi"`, semantic sections, aria-label navissa, `prefers-reduced-motion`
- Yksi HTML-tiedosto, inline CSS (kuten laser) – ei build-stepiä
- Formspree + fetch submit

### 5.5 llms.txt (juuri)

Uusi `llms.txt` kuvaa digitaalipalvelun, prosessin 7 vaihetta, hinnoitteluperiaatteen ja linkin `laser/`-sivulle.

---

## 6. Copy-cheatsheet (valmiit lauseet)

**Hero CTA:** Kerro ongelmastasi  

**Prosessin ydin:**  
> Ennen kuin maksat mitään, käymme ongelman läpi, teen kaksi ilmaista demoa ja lähetän tarjouksen. Sen jälkeen asennan järjestelmän ilmaiseksi – maksat laitteet ja myöhemmin vain edullisen kuukausimaksun.

**Laser-blokki:**  
> Harrastan myös puutöitä ja laserkaiverrusta. Ne löytyvät omalta sivultaan – sama yhteyshenkilö, eri palvelu.

**Pricing-note:**  
> Kuukausimaksu arvioidaan tarjouksessa ja pysyy kiinteenä. Olen tehnyt työkaluja vuosia, mutta pidän hinnoittelun reiluna, koska tämä on minulle myös intohimo.

---

## 7. Toteutusjärjestys (checklist)

- [ ] **Vaihe 1:** Luo `index.html` juureen – kopioi laser-rakenne (header, section, footer, JS), vaihda tekstit ja värit `plan.md` mukaan
- [ ] **Vaihe 2:** Lisää `#laser`-osio + linkki `laser/index.html`
- [ ] **Vaihe 3:** Päivitä `laser/index.html` – linkki etusivulle, canonical polku
- [ ] **Vaihe 4:** `logo.png`, uusi `banner.png` (tai väliaikainen gradientti)
- [ ] **Vaihe 5:** `llms.txt`, `sitemap.xml`, `robots.txt` juureen
- [ ] **Vaihe 6:** Testaa lomake, mobiilivalikko, ankkurilinkit
- [ ] **Vaihe 7 (myöhemmin):** Case-esimerkit / screenshotit demotyökaluista kun luvallista näyttää

---

## 8. Avoimet päätökset (täytä ennen koodausta)

| # | Kysymys | Ehdotus |
|---|---------|---------|
| 1 | Päädomain juuri vs. alikansio | `wasanen.store/` = digi, `/laser/` = puu |
| 2 | Lomakkeen aihekentän placeholder | "Esim. kävijälaskenta ravintolaan" |
| 3 | Näytetäänkö henkilön nimi/kuva | Vain Wäsänen-brändi, kuten nyt |
| 4 | Englanninkielinen versio | Ei ensimmäisessä versiossa |
| 5 | Referenssiprojektit sivulla | Vaihe 7 – kun materiaalia on |

---

## 9. Yhteenveto brändistä yhdellä sivulla

**Wäsänen** (Nurmijärvi) ratkaisee asiakkaiden ongelmia jakamalla ne pieniksi osiksi ja rakentamalla digitaalisia työkaluja – verkkosivuista IoT:hen ja analytiikkaan. Polku on läpinäkyvä ja pääosin ilmainen ennen sopimusta; maksullinen vaihe on laitteet + edullinen kuukausimaksu käytöstä. Laser- ja puutyöt ovat erillinen, lyhyesti mainittu sivuliiketoiminta samoilla yhteystiedoilla.
