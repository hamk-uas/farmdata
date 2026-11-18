# Viikkotehtävä 4

## Osa 1: Ulkoiset datalähteet
Miettikää mitä ulkoisia datalähteitä tai datatuotteita tiiminne voisi käyttää. Palauttakaa lista harkitsemistanne datalähteistä tai datatuotteista ja lyhyet arviot, millä tavoin kyseinen ulkoinen data voisi tuoda lisäarvoa analyysiprojektiin. Jos näette haasteita ulkoisen datan käyttöönotossa, voitte kirjata niitäkin ylös.

## Osa 2: Traktoriaineistoon tutustuminen Pythonilla (täydentyy)

```
import pandas as pd

df_fuel = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/tractor_fuel.csv')
df_gps = pd.read_csv('https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/tractor_gps.csv')

print(df_fuel.head())
print("")
print(df_gps.head())
```

Annettu [luennolla 18.11.2026](Luennot.md#4-luento-18112026).
