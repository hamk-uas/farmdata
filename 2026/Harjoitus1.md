# Harjoitus 1

Luennon päivämäärä: 28.10.2026

## Tehtävä
Kopio alla oleva koodi yhteen ohjelmasoluun Colabin Python Notebookissa ja täydennä ohjeiden mukaan puuttuvat kohdat. Tee tiedostosta lopuksi PDF-tuloste ja palauta se Moodleen.

## Kommenttiriveistä
Osa riveistä alkaa kommenttimerkillä, jotta koodia voi suorittaa ilman virheilmoituksia vaiheittain etenemällä. Nämä rivit on merkitty `# Poista kommenttimerkki`. Esimerkki

```
# viesti = "Tämä rivi on kommentoitu pois käytöstä"  # Poista kommenttimerkki
# print(viesti)                                      # Poista kommenttimerkki
```
ja kun etenet tehtävää kyseiselle riville, riittää poistaa kommenttimerkki, jotta rivi tulee mukaan ohjelmaan ja tulostus näkyviin eli
```
viesti = "Tämä rivi on kommentoitu pois käytöstä"  # Poista kommenttimerkki
print(viesti)                                      # Poista kommenttimerkki
```
## Täydennettävä ohjelmakoodi

```
# -----------
# 1. Harjoitellaan lukujen käsittelyn perusteet
# Täydennä lukujen a ja b summa, erotus ja tulo
a = 10
b = 3

#summa =   # Poista kommenttimerkki
#erotus =  # Poista kommenttimerkki
#tulo =    # Poista kommenttimerkki

#print("Summa:", summa)    # Poista kommenttimerkki
#print("Erotus:", erotus)  # Poista kommenttimerkki
#print("Tulo:", tulo)      # Poista kommenttimerkki

# -----------
# 2. Täydennä muuttujat. Nimi on merkkijono ja ikä numero
name = ""
age = 0

# -----------
# 3. Tulosta tervehdys eli lisää nimi pilkun jälkeen
# print("Hei", )

# -----------
# 4. Lasketaan montako karkausvuotta olet elänyt
# Tässä osassa ei tarvitse tehdä muutoksia
year_now = 2026
birth_year = year_now - age

leap_years = 0

for year in range(birth_year, year_now + 1):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        leap_years += 1

print("Karkausvuosia elämässäsi:", leap_years)

# -----------
# 5. Nyt voidaan laskea montako päivää henkilö on vanha eli kerrotaan ikä
# tavallisen vuoden päivien määrällä 365 ja lisätään siihen karkauspäivien määrä

# age_in_days =            # Poista kommenttimerkki
# print("Ikä päivinä:", )  # Poista kommenttimerkki

# -----------
# 6. Tutustutaan pienesti vielä taulukkoon datarakenteena. Täydennä loppuun 
# tulostusriveille sarakkeiden lasketut summat ja keskiarvot
# import-komennolla voidaan tuoda tiettyjä valmiita koodikokoelmia oman ohjelmamme
# käyttöön. Näitä kutsutaan kirjastoiksi. Käytämme tässä pandas kirjastoa ja
# lyhennämme sen nimen muotoon pd
import pandas as pd

# Luodaan esimerkki taulukko kooltaan 10 x 2
taulukko = [
    [5, 8],
    [3, 7],
    [6, 4],
    [9, 2],
    [1, 5],
    [4, 6],
    [8, 3],
    [2, 9],
    [7, 1],
    [5, 4]
]

# Muutetaan DataFrameksi (pandas kirjaston nimitys tietyn tyyppiselle taulukolle),
# jonka sarakkeiden nimet ovat lämpötila ja sademäärä
df = pd.DataFrame(taulukko, columns=["Temperature", "Rainfall"])

# Tulostetaan taulukko näkyviin
display(df)

# Lasketaan sarakkeiden summat hyödyntäen pandas-kirjastoa
summa1 = df["Temperature"].sum()
summa2 = df["Rainfall"].sum()

# Lasketaan sarakkeiden keskiarvot hyödyntäen pandas-kirjastoa
ka1 = df["Temperature"].mean()
ka2 = df["Rainfall"].mean()

#print("Lämpötilasumma:", )  # Poista kommenttimerkki
#print("Sademääräsumma:", )  # Poista kommenttimerkki

#print("Lämpötilojen keskiarvo:", )  # Poista kommenttimerkki
#print("Sademäärien keskiarvo:", )   # Poista kommenttimerkki

# -----------
# 7. Kultainen leikkaus on piste janalla, joka jakaa janan niin, että pidemmän osan
# pituuden suhde koko janan pituuteen on sama kuin lyhyemmän osan pituuden suhde
# pidämmen osan pituuteen. Pyydä tekoälyä luomaan koodi, jolla voit laskea
# kultaisen leikkauksen mukaisen jaon haluamasi pituiselle janalle ja kopioi
# koodi tähän alle.
```


[Takaisin luentomuistiinpanoihin](Luennot.md)
