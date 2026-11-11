# Viikkotehtävä 3

Annettu [luennolla 11.11.2026](Luennot.md#3-luento-11112026)

## Harjoitus: Lämpöstressin (THI) ja maitotuotoksen välinen yhteys tekoälyn avulla

### Tausta

Lypsykarjan lämpöstressiä arvioidaan usein Temperature Humidity Indexin (THI) avulla. Tässä harjoituksessa tutustut maatalouden datan analysointiin käyttäen tekoälyä apuna sekä datan käsittelyssä että visualisointien tuottamisessa.

Sinulle on annettu seuraavat aineistot, joiden lukemiseen on mallikoodit alla:
1. df_jokioinen: ulkoilman sääasema-aineisto
1. df_barnA, df_barnB, df_barnC ja df_barnD: navetan sisäilmamittauksia eri mittauspisteistä
1. df_milk: karjan päivittäinen maitotuotos

THI:n laskentaan käytetään tässä harjoituksessa kaavaa (Dikmen & Hansen, 2009, J. Dairy Sci. 92:109–116, doi:10.3168/jds.2008-1370):
THI2 = Tdb + 0.36Tdp + 41.2,
missä Tdb​ on ilman lämpötila (°C) (dry bulb temperature) ja Tdp​ on kastepistelämpötila (°C) (dew point temperature). Kastepiste tulee arvioida lämpötilan ja suhteellisen kosteuden perusteella käyttäen Magnus-Tetens kaavaa.

### Tavoite

Tavoitteena on tutkia:
1. Mittausaineistojen laatua.
1. Navetan lämpö- ja kosteusolosuhteita.
1. THI-indeksin vaihtelua ajan suhteen.
1. THI:n mahdollista yhteyttä maitotuotokseen.
1. Tekoälyn tuottaman analyysin ja koodin luotettavuutta.

### Vaiheet

Harjoitus tehdään vaiheittain käyttäen tekoälyä  (esim. Copilot, ChatGPT tai Gemini) Python- ohjelmakoodin tuottamisen tukena.

1. Tutustu aineistoihin. Pyydä tekoälyä visualisoimaan annettuja aineistoja.
1. Datan laadun tarkastus. Pyydä tekoälyä etsimään poikkeavia havaintoja ja tarvittaessa poistamaan ne käsiteltävästä aineistosta.
1. THI-indeksin laskeminen. Kerro tekoälyllä käytettävä THI kaava ja muistuta huomioimaan, että kastepistelämpötila Tdp pitää arvioida annetuista ilman lämpötiloista, joita voidaan käyttää Tdb-muuttujassa.
1. Päiväkohtaisten keskiarvojen muodostaminen. Koska maitotuotos on päiväkohtaista, muodosta myös THI:stä päiväkohtaiset keskiarvot.
1. THI ja maitotuotos aikasarjoina. Tee kuvaaja, jossa: x-akselilla on aika, vasemmalla y-akselilla maitotuotos ja oikealla y-akselilla THI
1. Hajontakuvaaja eli muodosta kuvaaja, jossa x-akselilla päivän keskimääräinen THI ja y-akselilla päivän maitotuotos

### Palautus

Palauta PDF-tuloste Colabissa tehdystä Python Notebookista. Kirjoita ohjelman lisäksi loppuun tekstisoluun havaintojasi. Tarkastele esimerkiksi

1. mitä syötteitä käytitte tekoälylle tekoälyn ohjaamiseen
1. mitä ymmärrättä ohjelman tekevän ja mitkä ovat tuotetut käsittelyvaiheet
1. onko THI:llä ja lypsytuotoksella yhteyttä, näkyykö maitotuotoksessa viivästynyt reaktio lämpöstressiin
1. miksi ja milloin navetan THI on sama tai eri kuin ulkoilman THI
1. miten eri mittauspisteet navetassa suhtautuvat toisiinsa mittausarvojen perusteella


### Mallikoodi harjoituksen aloittamiseen

```
import pandas as pd

# Data of Jokioinen Ilmala 2019
df_jokioinen = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Jokioinen%20Ilmala_%201.1.2019%20-%2031.12.2019.csv')

# Clear extra characters from column names (spaces and quotation marks)
df_jokioinen.columns = df_jokioinen.columns.str.replace('"', '').str.strip()

# Data of indoor temperature and humidity
df_barnA = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Barn4_A_data.csv')
df_barnB = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Barn4_B_data.csv')
df_barnC = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Barn4_C_data.csv')
df_barnD = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Barn4_D_data.csv')

df_milk = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Barn4_cattle_milk.csv',delimiter=";")

print(df_jokioinen.head().to_string())
print()
print(df_barnA.head().to_string())
print()
print(df_barnB.head().to_string())
print()
print(df_barnC.head().to_string())
print()
print(df_barnD.head().to_string())
print()
print(df_milk.head().to_string())
```
