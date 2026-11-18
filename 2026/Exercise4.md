<!-- Translation sync: this file is up to date with the Finnish source 2026/Harjoitus4.md as of commit ce4258c884301eed27c40b82162669ada421c23a. To catch up, translate the changes shown by: git diff ce4258c884301eed27c40b82162669ada421c23a HEAD -- 2026/Harjoitus4.md (then update the commit hash here). -->
# Weekly exercise 4

Given in the [lecture on 18.11.2026](Lectures.md#4-lecture-18112026).

## Part 1: External data sources
Think about what external data sources or data products your team could use. Submit a list of the data sources or data products you have considered, along with brief assessments of how each external dataset could add value to the analysis project. If you foresee challenges in adopting the external data, you can write those down as well.

## Part 2: Grasping tractor data with Python

Objective is to identify ways to visualize the tractor’s operating profile. 
Interview an AI assistant and document the discussion in a concise summary.
Use a variety of chart types and visualization methods.
What additional data would be particularly useful for this analysis (e.g., distribution of field types, field boundaries, soil conditions, implement information)?

Based on data, study for example
* Length and duration of driven routes and average and total consumption of fuel.
* Daily driven kilometers and maximum distances from the starting point.

You may submit your reflections and code in separate PDF files if needed, or document everything in a Google Colab notebook, provided that the output is clear and readable.

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
