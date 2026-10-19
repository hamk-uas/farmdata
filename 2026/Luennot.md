Syksy 2026

© 2026 HAMK Hämeen Ammattikorkeakoulu. Tekijät: Olli Koskela, Olli Niemitalo

# 1. Luento 28.10.2026 Colab, Pythonin perusteet osa 1

## Python

Python on ohjelmointikieli, joka on erittäin suosittu tietojen analysoinnissa. Tietokoneohjelman kirjoittaminen tietojen analysointia varten on kätevää, koska ohjelma tarvitsee kirjoittaa vain kerran ja sitä voidaan sitten käyttää toistuvasti eri syötedatojen kanssa. Pythonin suosion vuoksi Internetissä on paljon apua, varsinkin englanniksi, ja sitä kannattaa hakea esim. Google-haulla ja tekoäly (AI) -chattien avulla. Pythonin ominaisuuksia voidaan laajentaa käyttämällä *moduuleita*, esimerkiksi taulukkomuotoisen datan käsittelemiseksi tai kuvaajien piirtämiseksi. Moduuleilla on yleensä omat online-dokumentaationsa, joihin voi tutustua.

Sinun ei tarvitse muistaa tarkkaan miten mikäkin asia voidaan tehdä Pythonilla. Googlaa rohkeasti tai kysy tekoälyltä! Tyypillisesti monilla ihmisillä on ollut sama ongelma kuin sinulla, ja he ovat pyytäneet apua esim [<u>Stack Overflow</u>](https://stackoverflow.com/) -palvelussa, joka on ilmainen kysymys- ja vastauspalvelu. Joskus riittää, että virheilmoitusta käytetään hakuavaimena tai promptina AI:lle.

Tekoälytyökalut voivat auttaa sinua ja voit käyttää niitä vapaasti tällä kurssilla koodin luomiseen. Sinulle on luultavasti tärkeämpää "saada homma hoidettua" kuin opiskella Python-kieli juurta jaksain. Tekoälyä voi ajatella apulaisena, joka kirjoittaa koodia puolestasi. Seuraavassa osiossa tutustutaan Google Gemini -tekoäyn käyttöön. Muita hyödyllisiä tekoälyjä Python-koodin kirjoittamiseen ovat mm. ChatGPT, Gemini, Copilot, Grok, Manus, ja Claude. Niiden käyttö vähäisissä määrin on ilmaista ja yhä useammat niistä pystyvät myös itse ajamaan ja testaamaan koodia.

Jos olet aikeissa lähettää tekoälylle tietoa, joka on salassa pidettävää tai yksityistä, varmista palvelun käyttöehdoista ja tietosuojakäytännöistä miten lähettämääsi dataa käytetään. Harkitse myös luotatko palvelun tarjoajaan.

## Colab

Colab on Googlen palvelu, joka on HAMKin opiskelijoiden saatavilla Google-tilin kautta. Colabissa Pythonia voidaan käyttää interaktiivisesti Jupyter Notebookissa.

Asiaa ei tällä kurssilla käydä kummemmin läpi, mutta on mahdollista asentaa Python ja Jupyter Notebook omalle tietokoneelle. Visual Studio Code on suosittu koodieditori, ja Git on erittäin suosittu työkalu ohjelmistokehityksen versiohallintaan. Versiohallinta tarkoittaa lähdekoodin kumulatiivisen historian tallentamista kehityksen aikana. GitHub on erittäin suosittu palvelu, jossa versiohallittuja ohjelmistoprojekteja voi säilyttää.

**Luo uusi notebook** avaamalla [<u>https://colab.research.google.com/</u>](https://colab.research.google.com/). Voit kirjoittaa haluamasi notebookin nimen.

**Etsi notebookisi Google Drivesta** napsauttamalla *File*→*Locate in Drive*. Voit halutessasi siirtää notebookin johonkin kansioon.

Kun Python-koodi suoritetaan Colabissa, koodi suoritetaan *suorituspalvelussa*, joka on Googlen isännöimä virtuaalikone. Suorituspalvelu luodaan automaattisesti sinulle, kun suoritat koodisolun ensimmäistä kertaa muistikirjassa.

**Suorita tyhjä koodisolu** painamalla play-nappia. Hetken saat suorituspalvelun.

Suorituspalvelu on virtuaalikone, ja sillä on omat paikalliset tiedostonsa. Kaikki suorituspalvelun paikalliset tiedostot poistetaan, kun suorituspalvelu suljetaan. Tämä tapahtuu toisinaan odottamatta, ja myös silloin, jos tietokoneeltasi ei ole jonkin aikaa yhteyttä, esimerkiksi jos kannettavan tietokoneen selaimen välilehti suljetaan, tietokone menee lepotilaan tai Internet-yhteytesi katkeaa. Myös kaikki Python-muuttujiin tallennetut tiedot menetetään, kun suorituspalvelu suljetaan. Koodisi sisältävä notebook on kuitenkin tallennettu Google Driveen, eikä sitä poisteta. Toisin kuin Google Docs -asiakirjoissa, sinun on ehkä tallennettava manuaalisesti kaikki notebookiin tekemäsi muutokset.

**Tarkista suorituspalvelu** tutkimalla *Runtime*-valikkoa.

**Tarkista suorituspalvelun paikalliset tiedostot**, napsauttamalla vasemmalla olevaa kansiokuvaketta.

**Yritä luoda uusia teksti- ja koodisoluja.**

**Muokkaa uusien solujen sisältöä.**

**Suorita koodi solussa** painamalla Ctrl-Enter (Windows) tai Cmd-Enter (Apple) tai solun play-nappia.

Colab antaa käyttöoikeuden Gemini-tekoälyn (artificial intelligence, AI) ominaisuuksiin kuten *Generate code* -painike, jolla voi luoda koodia kehotteeseen syötetyn pyynnön mukaan, ja *Explain error* -painike.

### Google tilin vaihtaminen

Oikeassa yläkulmassa olevasta profiilikuvakkeesta saa avattua valikon, josta voi Lisää tili (Add account) -valinnalla kirjautua uuteen tiliin.

<img src="assets/datatalous/media/image6.png" style="width:7.31771in;height:2.87876in" />

## Pythonin perusteet osa 1

Tämä alaosio kattaa Python-ohjelmoinnin perusteet koodiesimerkkien avulla. Kirjoita tai kopioi ja liitä kukin koodiesimerkki Colabin koodisoluun ja suorita solu. Yritä ymmärtää tulos. Muokkaa koodia ohjeiden mukaan ja suorita se uudelleen. Voit myös luoda uuden solun ja kirjoittaa siihen omaa koodia.

Pythonissa voi luoda omia muuttujia. Muuttuja viittaa aina johonkin arvoon. Arvoja on eri tyyppisiä. Tutustumme joihinkin tyyppeihin tässä osiossa. Riippuen siitä, minkä tyyppiseen arvoon muuttuja viittaa, muuttujaa tai paremminkin sen arvo voi käyttää eri tavoin tavoin.

Python-tulkki ajaa Python-ohjelman tai koodisolun koodin rivi kerrallaan ylhäältä alas. Jos tulkki kohtaa virheen, suoritus keskeytyy ja näyttöön tulee virheilmoitus. Python-tulkki muistaa kaikkien muuttujien arvot aiemmin suoritetusta koodista. Voit poistaa kaikki luodut muuttujat napsauttamalla *Runtime*→*Restart*. Tämä ei poista suorituksen aikana tallennettuja paikallisia tiedostoja.

### Kommentit, muuttujat, tyypit (numerot, merkkijonot), peruslaskutoimitukset, tulostus

```python
# Tämä on kommentti. Kommentit alkavat #-merkillä, eikä niitä suoriteta.

# Määritä muuttujille numeeriset arvot (engl. numerical values)
x = 5
y = 2.5

# Sijoita tulos muuttujaan (engl. variable)
result = x + y

# Tulosta numeerisen muuttujan arvo
print(result) # Tulostaa 7.5
```

Pythonissa välilyönneillä rivin alussa jaotellaan koodia lohkoihin, mihin tutustutaan myöhemmin. Muuten välilyöntejä voi laittaa koodin sekaan varsin vapaasti. Välilyöntien sopiva käyttö tekee koodista luettavampaa.

Viimeinen rivi on myös esimerkki funktion kutsumisesta, tässä tapauksessa Pythonin sisäänrakennetun print-funktion. Funktiota kutsutaan kirjoittamalla pilkuilla erotetut syötearvot sulkuihin funktion nimen jälkeen. Funktio voi palauttaa arvon. Sisäänrakennettuja funktioita on monia, ja voit myös luoda omia funktioita.

### Harjoitustauko luennolla

**Muuta syötelukuja ja katso kuinka tulos muuttuu.**

**Tee koodista versiot jotka tekevät 1) vähennyslaskun ja 2) kertolaskun.** Katso: [<u>Python-operaattorit</u>](https://www.w3schools.com/python/python_operators.asp).

**Laske jonkin luvun neliöjuuri (engl. square root).** Voit googlettaa / kysyä AI:lta kuinka se tehdään.

### Luento jatkuu

```python
# Määritä muuttujalle merkkijonoarvo (engl. string)
sentence = "Nimeni on"

# Liitä merkkijonot (engl. concatenate)
name = "Petri"
sentence = sentence + " " + name

# Tulosta merkkijonomuuttujan arvo
print(sentence)

# Tee sama käyttämällä muotoiltua merkkijonoa (engl. formatted string)
sentence = f"Nimeni on {name}"
print(sentence)
```

### Harjoitustauko luennolla

**Luo uusi muuttuja ja aseta sen arvoksi jokin uusi nimi.**

**Lisää uusi nimi lauseeseen uutta muuttujaa käyttäen.** Lopputuloksena esim. “Meidän nimemme ovat Petri ja Eeva”.

## Python-harjoitus 1: Fibonaccin luvut

Fibonaccin luvut ovat sarja kokonaislukuja, joka alkaa luvuilla 0 ja 1. Seuraavat luvut ovat kahden edellisen luvun summia.\
**Kirjoita Python-ohjelmakoodi, joka tulostaa 15 ensimmäistä Fibonaccin lukua.\
Palauta kuvakaappaus koodista ja tulosteesta.** Alla on esimerkki kuvakaappauksesta koodille joka laskee pisteitä viivalla.

<img src="assets/datatalous/media/image7.png" style="width:5.83333in;height:3.36458in" />

# 2. Luento 4.11.2026

# 3. Luento 11.11.2026

# 4. Luento 18.11.2026

# 5. Luento 25.11.2026

# 6. Luento 2.12.2026

# 7. Luento 9.12.2026

# 8. Raporttien purkutilaisuus 15.12.2026
