<!-- Translation sync: this file is up to date with the Finnish source 2026/Harjoitus2.md as of commit e01f6b51c997b0d8fe076be19c049a447881c962. To catch up, translate the changes shown by: git diff e01f6b51c997b0d8fe076be19c049a447881c962 HEAD -- 2026/Harjoitus2.md (then update the commit hash here). -->
# Weekly exercise 2

Given in the [lecture on 4.11.2026](Lectures.md#2-lecture-4112026).

The purpose of this exercise is to visualize growing seasons using graphs of cumulative temperature and precipitation sums. These graphs illustrate how weather conditions accumulate in the field over time during the growing season. A growing season is defined as a continuous period during which the daily mean temperature remains above +5°C.

The code provided below downloads hourly weather observations from the Finnish Meteorological Institute (FMI) for the period 1 January 2020 – 27 October 2026. The data are hosted on GitHub and originate from two weather stations Ilmala, Jokioinen (the closest weather station to Mustiala) and Pelmaa, Seinäjoki. The Finnish Meteorological Institute has licensed the data under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.

The objective of this exercise is to practice weather data processing and visualization. From the hourly measurements, you will calculate daily mean temperatures and daily precipitation sums. Based on these values, you will calculate cumulative sums and create graphs similar to the example provided for one weather station and one year.

Copy the code below into your own Python Notebook in the Google Colab environment and complete the tasks step by step. It is recommended to perform each task in a separate code cell.
1. Examine the output of the initial code. You will notice that the timestamp components are separated into the columns Year, Month, Day, and Time. Combine these columns into a single datetime object that can be used for time-based calculations.
1. Calculate the daily mean temperature and the daily total precipitation. Then create graphs showing these daily values.
1. Determine the growing season dates for the years 2021 and 2025. For both weather stations, identify the start and end dates of the continuous period during which the daily mean temperature remained above +5°C.
1. For both weather stations and both years, use the growing season dates determined separately for each weather station (in case you also calculated common dates for both stations) and
    1. Plot the daily mean temperatures during the growing season.
    1. Plot the daily precipitation totals during the growing season.
    1. Calculate and plot the cumulative temperature sums.
    1. Calculate and plot the cumulative precipitation sums.
1. Finally, write a short discussion summarizing the observations from your graphs. Compare differences between locations and years.

Export your completed notebook as a PDF file and submit it to Moodle.

## Model code

```
import pandas as pd

# Data of Jokioinen Ilmala
file_path = 'https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Jokioinen%20Ilmala_%201.1.2020%20-%2027.10.2026.csv'
df_jokioinen = pd.read_csv(file_path)

# Data of Seinäjoki Pelmaa
file_path = 'https://raw.githubusercontent.com/hamk-uas/farmdata/refs/heads/main/2026/assets/Sein%C3%A4joki%20Pelmaa_%201.1.2020%20-%2027.10.2026.csv'
df_seinajoki = pd.read_csv(file_path)

# Puhdistetaan sarakkeiden nimistä ylimääräiset lainausmerkit ja välilyönnit
df_jokioinen.columns = df_jokioinen.columns.str.replace('"', '').str.strip()
df_seinajoki.columns = df_seinajoki.columns.str.replace('"', '').str.strip()

print(df_jokioinen.head().to_string())
print("")
print(df_seinajoki.head().to_string())
```

## Example of end result

If you end up with a result like this, you are definitely on the right track. The layout, colors, and number of the graphs may vary, but the curves should look roughly like this.

![](assets/analyzing-data/media/Exercise2example.png)
