Syksy 2026

© 2026 HAMK Hämeen Ammattikorkeakoulu. Tekijät: Pirita Rantala, Olli Koskela, Olli Niemitalo

# 1. Luento 28.10.2026
<!-- Älä muuta luennon otsikkoa, koska siihen syvälinkataan Moodlesta! Lisää lyhyt kuvaus alle! -->

Tällä luennolla käydään läpi Colab, AI:n käyttö ja Pythonin perusteet osa 1.

### Python

Python on ohjelmointikieli, joka on erittäin suosittu tietojen analysoinnissa. Tietokoneohjelman kirjoittaminen tietojen analysointia varten on kätevää, koska ohjelma tarvitsee kirjoittaa vain kerran ja sitä voidaan sitten käyttää toistuvasti eri syötedatojen kanssa. Pythonin ominaisuuksia voidaan laajentaa käyttämällä *moduuleita*, esimerkiksi taulukkomuotoisen datan käsittelemiseksi tai kuvaajien piirtämiseksi. Moduuleilla on yleensä omat online-dokumentaationsa, joihin voi tutustua.

Pythonin suosion vuoksi tekoälytyökalut tuntevat sen hyvin ja apua sen käyttöön kannattaa hakea tekoäly (AI) -chattien avulla. Viimeisen vuoden aikana modernimpi AI:n hyödyntämisen tapa, itsenäisesti ohjelmaa kehittävien AI-agenttien käyttäminen, on noussut chatteja tehokkaammaksi. Agentit pystyvät luomaan lähdekooditiedostoja, ajamaan niitä, testaamaan ohjelman toimintaa ja korjaamaan bugeja. Agenttiominaisuuksia voi olla tarjolla myös AI-chateissa.

Jotta AI osaisi auttaa sinua parhaan kykynsä mukaan, sille kannattaa "promptissa" kertoa ratkaistava ongelma ja että mitä ajatuksia sinulla on ratkaisun suhteen ja kuinka varma olet niistä tai haluatko että AI itse valitsee ratkaisun menetelmiä. Jos ohjelman suorituksessa tapahtuu virhe, virheilmoitus sellaisenaan on AI:lle käyttökelpoista tietoa virheen selvittämiseen ja se kannattaa antaa sille.

Tekoälytyökalut voivat auttaa sinua ja voit käyttää niitä vapaasti tällä kurssilla koodin luomiseen. Sinulle on luultavasti tärkeämpää "saada homma hoidettua" kuin opiskella Python-kieli juurta jaksain. Tekoälyä voi ajatella apulaisena, joka kirjoittaa koodia puolestasi. Seuraavassa osiossa tutustutaan Google Gemini -tekoäyn käyttöön. Muita hyödyllisiä tekoälyjä Python-koodin kirjoittamiseen ovat mm.: ChatGPT, Gemini, Copilot, Mistral, Grok, Deepseek, Manus, ja Claude. Niiden käyttö vähäisissä määrin on ilmaista ja yhä useammat niistä pystyvät myös itse ajamaan ja testaamaan koodia. Kun krediitit loppuvat yhdessä palvelussa voi vaihtaa toiseen.

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

Tällä luennolla varmistetaan viikkotehtävän PDF-palautus, kerrataan Pythonin perusteita (ohjelman eteneminen, muuttujat ja ehtolauseet) ja aloitetaan säädatan käsittely ja kuvaajien piirtäminen tekoälyn avulla. Näitä taitoja tarvitaan viikkotehtävässä 2.

## Viikkotehtävän palautus PDF-tiedostona

Luennon alussa varmistetaan, että kaikki ovat saaneet tehtyä viikkotehtävän 1 notebookista PDF-tiedoston Moodle-palautusta varten. Kaikki viikkotehtävät palautetaan samalla tavalla.

1. Suorita notebookin kaikki solut valitsemalla *Runtime*→*Run all*. Tarkista, että tulosteet ja kuvaajat näkyvät eikä solujen alla ole virheilmoituksia.
1. Valitse *File*→*Print* tai paina Ctrl+P (Mac: Cmd+P).
1. Valitse selaimen tulostusikkunassa tulostimeksi PDF-tiedostoon tallentaminen. Vaihtoehdon nimi riippuu selaimesta ja käyttöjärjestelmästä, mutta siinä on yleensä sana PDF, esimerkiksi *Tallenna PDF-muodossa* / *Save as PDF* tai *Microsoft Print to PDF*. Macin tulostusikkunassa PDF-tallennus löytyy *PDF*-valikosta.
1. Avaa tallennettu PDF ja tarkista, että kaikki solut, tulosteet ja kuvaajat ovat mukana. Jos pitkät koodirivit katkeavat, kokeile vaakasuuntaa (engl. landscape) tai pienempää skaalausta. Jos tulostus ei onnistu lainkaan, kokeile toista selainta.
1. Palauta PDF-tiedosto Moodleen.

## Notebookin käyttö

Harjoittele näitä toimintoja luennon harjoitustauoilla, niin niistä tulee rutiinia.

| Toiminto | Miten |
|---|---|
| Uusi notebook | *File*→*New notebook in Drive* |
| Uusi koodi- tai tekstisolu | *+ Code*- tai *+ Text* -painike |
| Solun suorittaminen | Solun play-nappi tai Ctrl+Enter (Mac: Cmd+Enter) |
| Solun siirtäminen tai poistaminen | Solun oikean yläkulman nuoli- ja roskakoripainikkeet |
| Kaikkien solujen suorittaminen ylhäältä alas | *Runtime*→*Run all* |
| Muuttujien tyhjentäminen ja kaikkien solujen suorittaminen | *Runtime*→*Restart session and run all* |
| Kokonaan uusi suorituspalvelu | *Runtime*→*Disconnect and delete runtime* ja sen jälkeen jokin solu tai *Run all* |

*Run all* pysähtyy ensimmäiseen soluun, jossa tulee virhe. Korjaa tai poista virheen aiheuttava solu ja suorita uudelleen.

## Pythonin perusteet osa 2

Tavoitteena ei ole opetella Pythonia ulkoa vaan ymmärtää, miten ohjelma etenee ja mitä muuttujille tapahtuu. Silloin pystyt lukemaan ja tarkistamaan myös tekoälyn kirjoittamaa koodia ja muokkaamaan sitä omiin tarpeisiisi.

**Luo tätä luentoa varten uusi notebook** ja kopioi jokainen esimerkki omaan koodisoluunsa.

### Ohjelma etenee rivi kerrallaan ylhäältä alas

```python
# Aamun lämpötila
temperature = 4
print("Aamulla:", temperature)

# Muuttujaan sijoitetaan uusi arvo, ja vanha arvo unohtuu
temperature = 15
print("Päivällä:", temperature)

# Uusi arvo voidaan laskea vanhasta arvosta
temperature = temperature - 6
print("Illalla:", temperature)
```

Muuttujan arvo on aina se, joka siihen on viimeksi sijoitettu. Yhtäsuuruusmerkki `=` ei tarkoita matemaattista yhtäsuuruutta vaan *sijoitusta*: ensin lasketaan oikean puolen arvo ja sitten se tallennetaan vasemmalla olevaan muuttujaan. Siksi rivi `temperature = temperature - 6` laskee vanhasta arvosta uuden arvon (15 − 6 = 9) ja tallentaa sen samaan muuttujaan.

**Mieti ennen suorittamista, mitä seuraava koodi tulostaa:**

```python
a = 3
b = a + 2
a = 10
print(a, b)
```

<details>
<summary>Vastaus</summary>

Koodi tulostaa `10 5`. Muuttujan `b` arvo lasketaan toisella rivillä, jolloin `a` on vielä 3. Kun muuttujaan `a` sijoitetaan myöhemmin uusi arvo, `b` ei muutu.

</details>

### Kertymä eli kumulatiivinen summa

Muuttujaa päivittämällä voidaan laskea esimerkiksi sademäärän *kertymä* eli *kumulatiivinen summa*: jokaisen päivän kohdalla kaikkien siihen asti satanneiden sademäärien summa. Kertymiä käytetään [viikkotehtävässä 2](Harjoitus2.md).

```python
# Kertymä on aluksi nolla
total_rain = 0

total_rain = total_rain + 2.5   # 1. päivänä satoi 2,5 mm
print("1. päivä:", total_rain)

total_rain = total_rain + 0.0   # 2. päivänä ei satanut
print("2. päivä:", total_rain)

total_rain = total_rain + 6.1   # 3. päivänä satoi 6,1 mm
print("3. päivä:", total_rain)
```

### Solujen suoritusjärjestys

```python
print(rainfall)
rainfall = 3.2
```

Koodi aiheuttaa virheen `NameError: name 'rainfall' is not defined`, koska ensimmäinen rivi suoritetaan ennen kuin muuttujalle on annettu arvo. Virheilmoituksen alla olevalla *Explain error* -painikkeella voit pyytää Geminiä selittämään virheen.

Colabissa muuttujat säilyvät solusta toiseen, ja solut suoritetaan siinä järjestyksessä, jossa ne ajat. Jos muutat ylempää solua, suorita myös sitä käyttävät solut uudelleen, tai suorita kaikki solut ylhäältä alas valinnalla *Runtime*→*Run all*.

### Harjoitustauko luennolla

**Lisää kertymäesimerkkiin neljäs päivä**, jolloin satoi 1,4 mm.

**Lisää esimerkkien yläpuolelle tekstisolut**, joihin kirjoitat lyhyen otsikon, esimerkiksi `# Kertymä`. Rivin alussa oleva `#` tekee tekstisolussa rivistä otsikon, joka näkyy vasemman reunan sisällysluettelossa.

**Valitse *Runtime*→*Restart session and run all*.** Suoritus pysähtyy `NameError`-esimerkkiin. Korjaa tai poista se solu ja kokeile uudelleen, kunnes kaikki solut menevät läpi.

### Luento jatkuu

### Ehtolauseet: if, elif ja else

Vertailu, kuten `temperature > 5`, tuottaa *totuusarvon* `True` (tosi) tai `False` (epätosi). *Ehtolauseella* (engl. if statement) ohjelma voi valita datan perusteella, mitkä rivit suoritetaan. Kasvukauden aikana vuorokauden keskilämpötila on yli +5 °C:

```python
temperature = 7.3

if temperature > 5:
    print("Keskilämpötila on yli +5 °C.")
    print("Kasvit kasvavat.")
else:
    print("Keskilämpötila on enintään +5 °C.")
    print("Kasvu on pysähdyksissä.")

print("Tarkistus valmis")
```

- `if`-rivin lopussa on kaksoispiste `:`.
- Sisennetyt rivit muodostavat *lohkon*. `if`-lohko suoritetaan vain, jos ehto on tosi, ja `else`-lohko muulloin. `else`-osa ei ole pakollinen.
- Sisentämätön rivi `print("Tarkistus valmis")` suoritetaan aina.

Vertailuoperaattorit ovat `==` (yhtä suuri), `!=` (eri suuri), `<`, `>`, `<=` ja `>=`. Huomaa ero: `=` sijoittaa arvon muuttujaan, kun taas `==` vertaa kahta arvoa. Ehtoja voi yhdistää sanoilla `and` (molemmat tosia) ja `or` (ainakin toinen tosi).

Vaihtoehtoja voi olla useampia. Ehdot tarkistetaan ylhäältä alas, ja vain ensimmäisen toteutuvan ehdon lohko suoritetaan:

```python
temperature = -2

if temperature < 0:
    print("Pakkasta")
elif temperature <= 5:
    print("Viileää, kasvu ei vielä käynnisty")
else:
    print("Kasvulle riittävän lämmintä")
```

### Harjoitustauko luennolla

**Muuta lämpötilaa niin, että jokainen kolmesta vaihtoehdosta tulostuu vuorollaan.** Mieti ennen suorittamista, mikä tulostuu. Mitä tulostuu, kun lämpötila on tasan 5?

**Kirjoita ehtolause, joka tulostaa "Runsas sade", jos muuttujan `rain` arvo on yli 10 mm, ja muuten "Vähän tai ei lainkaan sadetta".**

## Datan käsittely ja kuvaajat

### Kuvaajan piirtäminen: matplotlib.pyplot.plot()

Kuvaajat piirretään matplotlib-kirjaston pyplot-moduulilla, joka tuodaan käyttöön lyhenteellä `plt`. Funktio [`plt.plot()`](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.plot.html) piirtää viivakuvaajan: ensimmäisenä annetaan x-akselin arvot ja toisena y-akselin arvot. Samaan kuvaajaan voi piirtää useamman käyrän kutsumalla funktiota useasti.

```python
import matplotlib.pyplot as plt

# Lista (engl. list) sisältää useita arvoja hakasulkeissa järjestyksessä
days = [1, 2, 3, 4, 5, 6, 7]
temperatures_jokioinen = [6.1, 7.4, 5.2, 8.9, 10.3, 9.5, 11.0]
temperatures_seinajoki = [4.8, 6.0, 4.1, 7.5, 9.2, 8.8, 9.9]

# "o-" piirtää pisteet palloina ja yhdistää ne viivalla, label nimeää käyrän
plt.plot(days, temperatures_jokioinen, "o-", label="Jokioinen")
plt.plot(days, temperatures_seinajoki, "o-", label="Seinäjoki")
plt.xlabel("Päivä")
plt.ylabel("Keskilämpötila [°C]")
plt.title("Viikon keskilämpötilat")
plt.legend()  # Selite, jossa näkyvät käyrien nimet
plt.show()
```

### Harjoitustauko luennolla

**Piirrä kertymäesimerkin sademäärien kertymä kuvaajaksi** kirjoittamalla päivät ja kertymät listoihin.

### Luento jatkuu

### Säädatan lukeminen

Seuraava koodi lukee Ilmatieteen laitoksen tuntikohtaiset säähavainnot Jokioisten Ilmalan tai Seinäjoen Pelmaan sääasemalta. Samoja datoja käytetään viikkotehtävässä 2. Luettava tiedosto valitaan ehtolauseella muuttujan `station` perusteella. Data luetaan pandas-kirjaston *DataFrame*-taulukkoon `df`, jonka jokainen rivi on yhden tunnin havainto.

```python
import pandas as pd
import matplotlib.pyplot as plt

# Valitse sääasema: "Jokioinen" tai "Seinäjoki"
station = "Jokioinen"

if station == "Jokioinen":
    file_path = 'https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Jokioinen%20Ilmala_%201.1.2020%20-%2027.10.2026.csv'
elif station == "Seinäjoki":
    file_path = 'https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Sein%C3%A4joki%20Pelmaa_%201.1.2020%20-%2027.10.2026.csv'
else:
    # raise pysäyttää ohjelman ja näyttää oman virheilmoituksen
    raise ValueError(f"Tuntematon sääasema: {station}")

# Datassa puuttuvat havainnot on merkitty viivalla "-".
# na_values="-" kertoo pandasille, että viiva tarkoittaa puuttuvaa arvoa.
df = pd.read_csv(file_path, na_values="-")

# Puhdistetaan sarakkeiden nimistä ylimääräiset lainausmerkit ja välilyönnit
df.columns = df.columns.str.replace('"', '').str.strip()

display(df.head())
print(df.columns)
```

Ilman `na_values="-"`-asetusta pandas tulkitsisi lämpötila- ja sademääräsarakkeet merkkijonoiksi, eikä niillä voisi laskea. Pandas merkitsee puuttuvat arvot `NaN` (engl. *not a number*) ja ohittaa ne esimerkiksi keskiarvoa laskettaessa. Puuttuvia arvoja on lähes kaikissa mittausaineistoissa, joten ne kannattaa tarkistaa.

Sarake valitaan kirjoittamalla sen nimi hakasulkeisiin. Pandas osaa laskea sarakkeesta suoraan esimerkiksi keskiarvon ja kertymän (`cumsum()`), joka tekee saman kuin aiempi kertymäesimerkki, mutta jokaiselle riville:

```python
print("Puuttuvat arvot sarakkeittain:")
print(df.isna().sum())

print("Keskilämpötila koko ajalta:", df["Average temperature [°C]"].mean())

rain_cumulative = df["Precipitation [mm]"].cumsum()
print("Sademäärän kertymä, viimeiset rivit:")
print(rain_cumulative.tail())
```

### Rivien valinta ehdolla

Kun saraketta verrataan arvoon, saadaan totuusarvo jokaiselle riville erikseen. Sen avulla voidaan valita taulukosta ne rivit, joilla ehto on tosi:

```python
is_warm = df["Average temperature [°C]"] > 5
print(is_warm.head())

# Valitaan yhden päivän rivit ja piirretään sen tuntilämpötilat
one_day = df[(df["Year"] == 2025) & (df["Month"] == 7) & (df["Day"] == 15)]

plt.plot(one_day["Time [Local time]"], one_day["Average temperature [°C]"], "o-")
plt.xticks(rotation=90)  # Käännetään x-akselin kellonajat pystyyn
plt.xlabel("Kellonaika")
plt.ylabel("Lämpötila [°C]")
plt.title(f"{station} 15.7.2025")  # Muotoiltu merkkijono, ks. luento 1
plt.show()
```

Pandasin ehdoissa käytetään sanan `and` sijaan merkkiä `&` ja sanan `or` sijaan merkkiä `|`, ja jokainen ehto kirjoitetaan sulkuihin. Tällaisia yksityiskohtia ei tarvitse muistaa, koska tekoäly osaa ne. Riittää, että ymmärrät mitä koodi tekee.

Pidemmällä ajanjaksolla x-akselin kellonajat toistuisivat eikä niistä näkisi päivämäärää. Viikkotehtävässä 2 sarakkeet Year, Month, Day ja Time yhdistetään yhdeksi aikaleimaksi, jolloin x-akselille saadaan päivämäärät.

### Harjoitustauko luennolla

**Vaihda sääasema.** Muuta `station = "Seinäjoki"` ja valitse *Runtime*→*Run all*. Samat koodit laskevat ja piirtävät nyt tulokset Seinäjoelle. Kummalla asemalla oli lämpimämpää 15.7.2025?

**Kirjoita aseman nimi väärin** ja suorita solu. Mitä tapahtuu?

**Aloita kokonaan uudella suorituspalvelulla:** *Runtime*→*Disconnect and delete runtime* ja sen jälkeen *Runtime*→*Run all*. Koska kaikki tarvittava on notebookissa, se toimii myös tyhjästä aloitettaessa.

### Luento jatkuu

### Datan käsittely tekoälyn avulla

Colabin Gemini-tekoäly osaa kirjoittaa datan käsittelyyn ja kuvaajien piirtämiseen tarvittavan koodin. Geminin saa käyttöön esimerkiksi tyhjän koodisolun *Generate*-linkistä tai Colab-ikkunan Gemini-painikkeesta. Hyvän tuloksen saa näin:

1. **Suorita ensin datan lukeva koodi** ja kerro promptissa DataFramen ja muuttujien nimet sekä sarakkeiden nimet tarkasti.
1. **Kerro, mitä haluat laskea ja miten tulos esitetään**, esimerkiksi kuvaajana `plt.plot()`-funktiolla akseleiden otsikoiden kanssa.
1. **Etene pienin askelin**, yksi asia ja koodisolu kerrallaan.
1. **Lue koodi ja tarkista, onko tulos järkevä.** Esimerkiksi heinäkuun keskilämpötilan pitäisi olla noin +15–20 °C. Jos et ymmärrä jotain kohtaa, pyydä tekoälyä selittämään se.
1. **Jos tulee virhe**, paina *Explain error* tai kopioi virheilmoitus tekoälylle.

Colabin Geminin ilmainen käyttö on rajoitettua. Jos käyttökerrat tai krediitit loppuvat, voit käyttää muita tekoälyjä, kuten ChatGPT:tä, Copilotia, Claudea, Mistralia tai Deepseekiä. Ne eivät näe notebookiasi, joten kerro promptissa kaikki tarvittava: muuttujien ja sarakkeiden nimet, oma koodisi ja virheilmoitukset kokonaisuudessaan. Kopioi saamasi koodi Colabin koodisoluun.

Esimerkki promptista:

> DataFramessa `df` on sääaseman tuntikohtaiset säähavainnot ja muuttujassa `station` on sääaseman nimi. Sarakkeet ovat "Year", "Month", "Day", "Time [Local time]", "Average temperature [°C]", "Precipitation [mm]" ja "Average air pressure [hPa]". Laske vuoden 2025 jokaisen kuukauden keskilämpötila ja sademäärien summa ja näytä ne taulukkona. Piirrä keskilämpötilat kuvaajaan matplotlib.pyplot.plot-funktiolla niin, että x-akselilla on kuukauden numero. Lisää akseleille otsikot ja kuvaajan otsikkoon sääaseman nimi.

Tekoäly vastaa joka kerta hieman eri tavalla, mutta tulos voi näyttää esimerkiksi tältä:

```python
# Valitaan vuoden 2025 rivit
df_2025 = df[df["Year"] == 2025]

# Ryhmitellään rivit kuukausittain ja lasketaan jokaiselle kuukaudelle
# lämpötilojen keskiarvo ja sademäärien summa
monthly = df_2025.groupby("Month").agg({
    "Average temperature [°C]": "mean",
    "Precipitation [mm]": "sum"
})
display(monthly)

plt.plot(monthly.index, monthly["Average temperature [°C]"], "o-")
plt.xlabel("Kuukausi")
plt.ylabel("Keskilämpötila [°C]")
plt.title(f"{station}, kuukausien keskilämpötilat 2025")
plt.show()
```

Funktio `groupby()` jakaa rivit ryhmiin, tässä kuukauden mukaan, ja `agg()` laskee jokaiselle ryhmälle halutut tunnusluvut. Samalla periaatteella tuntikohtaisista havainnoista saadaan päiväkohtaiset keskiarvot ja summat, joita tarvitaan viikkotehtävässä 2.

### Harjoitustauko luennolla

**Pyydä tekoälyä piirtämään vuoden 2025 kuukausittaiset sademäärät.** Onko vuoden yhteenlaskettu sademäärä järkevä? Suomessa vuotuinen sademäärä on tyypillisesti noin 500–700 mm.

**Vaihda sääasema ja suorita kaikki solut.** Myös tekoälyn tuottama koodi toimii toiselle asemalle sellaisenaan: ohjelma kirjoitetaan kerran ja sitä voi käyttää eri datan kanssa.

**Tee tästä notebookista PDF-tiedosto** ja tarkista, että kuvaajat näkyvät siinä.

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
