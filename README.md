# Liikennemerkkien alueellinen jakautuminen Helsingissä – konenäköavusteinen tutkimus
![image](https://github.com/pyrypp/helsinki-liikennemerkit/assets/120693130/a2f0e129-32be-4860-aadf-dc2da6686dc5)

Autolla ajamisen kokemus vaihtelee eri puolilla Helsinkiä. Tämä tutkimus pyrkii selvittämään, mitä liikennemerkit paljastavat kaupungista. Tutkimuksen päätavoite on siis vertailla, miten eri liikennemerkkejä esiintyy eri kaupunginosissa.

Kesällä 2020 voimaan astunut uusi tieliikennelaki (729/2018) velvoittaa tienpitäjiä toimittamaan tietoja asetetuista liikenteenohjauslaitteista, kuten liikennemerkeistä, ajoratamaalauksista ja liikennevaloista Väylävirastolle (vayla.fi, päivitetty 14.4.2023). Väylävirasto hallinnoi tietoja Digiroad-tietojärjestelmässä, johon on koottu Suomen tie- ja katuverkon keskilinjageometria ja tärkeimmät ominaisuustiedot.

Tutkimuksen kirjoittamisen aikaan (09/2023) Digiroad-järjestelmän tiedot pääkaupunkiseudun liikennemerkeistä olivat melko puutteellisia. Sen sijaan pienempien kuntien, kuten Järvenpään, Keravan ja Orimattilan, rekisterit liikennemerkeistä olivat hyvin kattavat.

Kattavampaa paikkatietoa Helsingin liikennemerkeistä tarjoaa esimerkiksi ruotsalaisen Mapillary AB:n Mapillary-palvelu. Mapillary kerää katunäkymäkuvia käyttäjiltään ja konenäköä hyödyntäen inventoi katuominaisuuksia, kuten katuvaloja, liikennevaloja ja liikennemerkkejä.

Tämän tutkimuksen tarkoituksena on luoda oma tutkimusaineisto ja tunnistaa liikennemerkkejä konenäön avulla. Mapillary-palvelun paikkatietoa Helsingin liikennemerkeistä käytetään tutkimuksessa vertailuaineistona (ground truth), johon omia tuloksia verrataan.

Tutkimusartikkeli:
https://github.com/pyrypp/helsinki-liikennemerkit/blob/3900c2393c17d068eb469c93acad81df33a32af3/Helsinki%20-%20Liikennemerkkianalyysi.pdf

![image](output_images/comps/Pysäköinti%20kielletty.png)

## Mitä opin?
- Vektorikarttojen käsittely
  - Kirjastot (Geopandas, Folium, Pyproj ja Shapely)
  - Kartta-aineistojen yhdistäminen (union, intersection...)
  - Tien suuntien laskeminen
- Oman aineiston luominen API:n avulla
  - Google Street View API
  - Tiedostojen hallinta Pythonilla
- Kohteentunnistusmallin käyttö (Yolov7)
  - Siirto-oppiminen
  - Aineiston valmistelu (mm. augmentaatio, copy-paste -metodi ja luokkajakauman tasaaminen)
  - Mallin kouluttaminen ja hyperparametrien säätäminen (Tensorboard)
  - Mallin arvioinnin perusteita (precision, recall ja mAP)
- Kuvien käsittely Pythonilla
  - Kirjastot (Cv2, Pillow ja Matplotlib)
  - Hex-värien logiikka
  - Kuvien manipulointi matriiseilla
- Tehokkaampaa oman koodin paketoimista funktioihin
- Julkisen datan hakeminen ja hyödyntäminen
  - Väylävirasto
  - Maanmittauslaitos
  - Helsingin kaupungin karttapalvelu
- Uusi tieliikennelaki (729/2018) ja Digiroad-järjestelmä

## Potentiaalinen jatkokehitys
- Suurempi analysoitava aineisto
  - Suurempi alue
  - Datapisteitä tiheämmin
- Suurempi koulutusaineisto ja tasaisempi luokkajakauma
- Interaktiivinen käyttöliittymä
