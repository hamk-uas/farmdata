<!-- Translation sync: this file is up to date with the Finnish source 2026/Harjoitus3.md as of commit f42af17ff81dda9d0014cc30f146bdf1191d365c. To catch up, translate the changes shown by: git diff f42af17ff81dda9d0014cc30f146bdf1191d365c HEAD -- 2026/Harjoitus3.md (then update the commit hash here). -->
# Weekly exercise 3

Given in the [lecture on 11.11.2026](Lectures.md#3-lecture-11112026)

## Exercise: Investigating the Relationship Between Heat Stress (THI) and Milk Yield Using Artificial Intelligence

### Background

Heat stress in dairy cattle is commonly assessed using the Temperature Humidity Index (THI). In this exercise, you will learn the fundamentals of agricultural data analysis by using artificial intelligence to assist with both data processing and visualization.

You are provided with the following datasets (example code for loading the data is provided below):

1. df_jokioinen: outdoor weather station data
1. df_barnA, df_barnB, df_barnC, and df_barnD: indoor barn environmental measurements collected at different sensor locations
1. df_milk: daily herd milk yield data

For this exercise, THI is calculated using the equation presented by Dikmen & Hansen (2009, J. Dairy Sci. 92:109-116, doi:10.3168/jds.2008-1370): 
THI2=Tdb+0.36Tdp+41.2
where
Tdb is the dry-bulb air temperature (°C)
Tdp is the dew point temperature (°C)

The dew point temperature should be estimated from air temperature and relative humidity using the Magnus-Tetens equation.

### Study Context

Environmental conditions inside dairy barns can significantly affect animal welfare and production performance. Elevated temperature and humidity levels may cause heat stress, which has been associated with reduced feed intake, altered behavior, and decreased milk production. Continuous environmental monitoring provides an opportunity to study these relationships in greater detail.

In this exercise, you will analyze data collected in the Mustiala Research Dairy Barn operated by Häme University of Applied Sciences (HAMK). The barn was equipped with environmental sensors measuring temperature and relative humidity at multiple locations, while production records provide information on daily milk yield. Weather observations from the nearest Finnish Meteorological Institute weather station are also available for comparison.

The objectives of this exercise are to:

1. assess and clean real-world sensor data,
1. calculate derived variables such as dew point and THI,
1.combine environmental and production datasets,
1. visualize temporal and statistical relationships,
1. investigate possible associations between THI and milk production,
1. critically evaluate both AI-generated code and AI-generated interpretations.

Artificial intelligence tools such as Copilot, ChatGPT, or Gemini may be used to generate Python code and assist with analysis. However, all generated code, calculations, visualizations, and conclusions should be critically reviewed before acceptance.

Additional background information on the measurement setup and the original study can be found in file https://github.com/hamk-uas/farmdata/blob/main/2026/assets/analyzing-data/media/Barn%204.0%20poster%20engl%20translation.pdf.

### Learning Objectives

By completing this exercise, you will gain practical experience in:

1.data quality assessment and cleaning,
1. feature engineering,
1. time-series aggregation,
1. exploratory data analysis,
1. data visualization,
1. correlation analysis,
1. critical evaluation of AI-generated code and results.

The primary goal is not simply to produce figures, but to understand what the figures reveal about the data, evaluate the quality of the underlying measurements, and assess the reliability of AI-assisted analysis workflows.

### Procedure

This exercise should be completed in sequential phases using an artificial intelligence tool (e.g., Copilot, ChatGPT, or Gemini) to assist in generating Python code.

1. Explore the datasets. Ask the AI to visualize and summarize the provided datasets to gain an overview of their structure and contents.
1. Assess data quality. Ask the AI to identify anomalous observations and, if necessary, remove or correct them before further analysis.
1. Calculate the THI index. Provide the AI with the THI equation and remind it that the dew point temperature (TdpT_{dp}) must first be estimated from the available temperature and relative humidity measurements. The air temperature measurements should be used as the dry-bulb temperature (TdbT_{db}).
1. Create daily averages. Since milk yield is reported on a daily basis, aggregate the environmental measurements and calculate daily average THI values.
1. Visualize THI and milk yield as time series. Create a graph where the x-axis represents time, the left y-axis represents milk yield, and the right y-axis represents THI.
1. Create a scatter plot. Generate a graph where the x-axis represents the daily average THI, and the y-axis represents the daily milk yield.

### Submission

Submit a PDF export of your Colab notebook. In addition to the Python code, include a final text cell summarizing your observations and reflections on both the analysis process and the results.

Consider addressing at least the following questions:

1. What prompts or instructions did you provide to the AI in order to guide the analysis?
1. Based on your understanding, what does the program do and what are the main data-processing steps performed?
1. Is there a relationship between THI and milk yield? Is there evidence of a delayed response in milk production following periods of heat stress?
1. Why and under what conditions are the barn THI values similar to or different from the outdoor THI values?
1. How do the different measurement locations within the barn compare with one another based on the recorded environmental measurements?

Your discussion should demonstrate not only that the code runs successfully, but also that you understand the analytical workflow, the assumptions made during the analysis, and the interpretation of the results.

### Model code to start the assignment

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
