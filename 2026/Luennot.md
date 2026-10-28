Syksy 2026

© 2026 HAMK Hämeen Ammattikorkeakoulu. Tekijät: Pirita Rantala, Olli Koskela, Olli Niemitalo

# 1. Luento 28.10.2026
<!-- Älä muuta luennon otsikkoa, koska siihen syvälinkataan Moodlesta! Lisää lyhyt kuvaus alle! -->

Tällä luennolla käydään läpi Colab, AI:n käyttö ja Pythonin perusteet osa 1.

### Python

Python on ohjelmointikieli, joka on erittäin suosittu tietojen analysoinnissa. Tietokoneohjelman kirjoittaminen tietojen analysointia varten on kätevää, koska ohjelma tarvitsee kirjoittaa vain kerran ja sitä voidaan sitten käyttää toistuvasti eri syötedatojen kanssa. Pythonin ominaisuuksia voidaan laajentaa käyttämällä *moduuleita*, esimerkiksi taulukkomuotoisen datan käsittelemiseksi tai kuvaajien piirtämiseksi. Moduuleilla on yleensä omat online-dokumentaationsa, joihin voi tutustua.

Pythonin suosion vuoksi tekoälytyökalut tuntevat sen hyvin ja apua sen käyttöön kannattaa hakea tekoäly (AI) -chattien avulla. Viimeisen vuoden aikana modernimpi AI:n hyödyntämisen tapa, itsenäisesti ohjelmaa kehittävien AI-agenttien käyttäminen, on noussut chatteja tehokkaammaksi. Agentit pystyvät luomaan lähdekooditiedostoja, ajamaan niitä, testaamaan ohjelman toimintaa ja korjaamaan bugeja. Agenttiominaisuuksia voi olla tarjolla myös AI-chateissa.

Jotta AI osaisi auttaa sinua parhaan kykynsä mukaan, sille kannattaa "promptissa" kertoa ratkaistava ongelma ja että mitä ajatuksia sinulla on ratkaisun suhteen ja kuinka varma olet niistä tai haluatko että AI itse valitsee ratkaisun menetelmiä. Jos ohjelman suorituksessa tapahtuu virhe, virheilmoitus sellaisenaan on AI:lle käyttökelpoista tietoa virheen selvittämiseen ja se kannattaa antaa sille.

Tekoälytyökalut voivat auttaa sinua ja voit käyttää niitä vapaasti tällä kurssilla koodin luomiseen. Sinulle on luultavasti tärkeämpää "saada homma hoidettua" kuin opiskella Python-kieli juurta jaksain. Tekoälyä voi ajatella apulaisena, joka kirjoittaa koodia puolestasi. Seuraavassa osiossa tutustutaan Google Gemini -tekoäyn käyttöön. Muita hyödyllisiä tekoälyjä Python-koodin kirjoittamiseen ovat mm.: ChatGPT, Gemini, Copilot, Mistral, Grok, Manus, ja Claude. Niiden käyttö vähäisissä määrin on ilmaista ja yhä useammat niistä pystyvät myös itse ajamaan ja testaamaan koodia. Kun krediitit loppuvat yhdessä palvelussa voi vaihtaa toiseen.

Jos olet aikeissa lähettää tekoälylle tietoa, joka on salassa pidettävää tai yksityistä, varmista että sinulla on lupa siihen. Voit joutua tarkistamaan tekoälypalvelun käyttöehdoista ja tietosuojakäytännöistä miten lähettämääsi dataa käytetään. Harkitse myös luotatko palvelun tarjoajaan.

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

[Viikkotehtävä 1](Harjoitus1.md)

# 2. Luento 4.11.2026
<!-- Älä muuta luennon otsikkoa, koska siihen syvälinkataan Moodlesta! Lisää lyhyt kuvaus alle! -->

[Viikkotehtävä 2](Harjoitus2.md)

# 3. Luento 11.11.2026
<!-- Älä muuta luennon otsikkoa, koska siihen syvälinkataan Moodlesta. Lisää lyhyt kuvaus alle! -->


[Viikkotehtävä 3](Harjoitus3.md)

# 4. Luento 18.11.2026
<!-- Älä muuta luennon otsikkoa, koska siihen syvälinkataan Moodlesta. Lisää lyhyt kuvaus alle! -->

[Viikkotehtävä 4](Harjoitus4.md)

# 5. Luento 25.11.2026
<!-- Älä muuta luennon otsikkoa, koska siihen syvälinkataan Moodlesta. Lisää lyhyt kuvaus alle! -->

[Viikkotehtävä 5](Harjoitus5.md)

# 6. Luento 2.12.2026
<!-- Älä muuta luennon otsikkoa, koska siihen syvälinkataan Moodlesta. Lisää lyhyt kuvaus alle! -->

[Viikkotehtävä 6](Harjoitus6.md)

# 7. Luento 9.12.2026
<!-- Älä muuta luennon otsikkoa, koska siihen syvälinkataan Moodlesta. Lisää lyhyt kuvaus alle! -->

(Ei uutta viikkotehtävää)

# Luentosarjan jälkeen

Raporttien purkutilaisuus on 15.12.2026. Pyrkikää hyödyntämään esityksessä ja raportissa ohjelmallisen data-analyysin osuudessa saamianne taitoja. Voitte esim. hankkia ja yhdistää ulkopuolista dataa projektidataan ja analysoida niitä yhdessä, käyttäen Pythonia haluamissanne työvaiheissa.

Tenttiin tulee kysymyksiä viikkotehtävistä.
