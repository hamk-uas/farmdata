# Viikkotehtävä 4

## Osa 1: Ulkoiset datalähteet
Miettikää mitä ulkoisia datalähteitä tai datatuotteita tiiminne voisi käyttää. Palauttakaa lista harkitsemistanne datalähteistä tai datatuotteista ja lyhyet arviot, millä tavoin kyseinen ulkoinen data voisi tuoda lisäarvoa analyysiprojektiin. Jos näette haasteita ulkoisen datan käyttöönotossa, voitte kirjata niitäkin ylös.

## Osa 2: Traktoriaineistoon tutustuminen Pythonilla

Tavoite on löytää tapoja havainnollistaa traktorin käyttöprofiilia. Haastattele tekoälyä ideoista ja dokumentoi keskustelu tiivistetysti. Käytä erilaisia kuvaajatyyppejä. Mitä aineistoa erityisesti tässä pitäisi vielä hankkia lisää (esim. peltotyyppien jakauma).

Tutki esimerkiksi
* Ajoreittien pituuksia ja kestoja sekä keski- ja kokonaiskulutuksia.
* Päiväkohtaista ajomäärää ja etäisyyttä lähtöpisteestä.

Tarvittaessa voit palauttaa pohdinnat ja koodin eri PDF-tiedostoina tai voit dokumentoida kaiken Colabiin. Valitse niin, että tulostus on luettava.

```
import pandas as pd

df_fuel = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/tractor_fuel.csv')
df_gps = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/tractor_gps.csv')

# Convert timestamp to datetime if needed
df_fuel["timestampKafka"] = pd.to_datetime(df_fuel["timestampKafka"], format='ISO8601')
df_gps["timestampKafka"] = pd.to_datetime(df_gps["timestampKafka"], format='ISO8601')


print(df_fuel.head())
print("")
print(df_gps.head())
```

Annettu [luennolla 18.11.2026](Luennot.md#4-luento-18112026).
