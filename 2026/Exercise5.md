<!-- Translation sync: this file is up to date with the Finnish source 2026/Harjoitus5.md as of commit 80080b5696ee64becb99e488730d36c80ea93424. To catch up, translate the changes shown by: git diff 80080b5696ee64becb99e488730d36c80ea93424 HEAD -- 2026/Harjoitus5.md (then update the commit hash here). -->
# Weekly exercise 5

Given in the [lecture on 25.11.2026](Lectures.md#5-lecture-25112026).

Assignment 1

Using the frequency band images B04, B08, B8A and B11 provided in the assets folder, calculate the vegetation index NDVI and moisture index NDMI in Google Colab. Next, determine how to isolate a specific field area in Mustiala and calculate the average NDVI and NDMI values for that field.

Tip: You can obtain the polygon required to define the field area, for example, from the Copernicus Browser using the polygon drawing tool. Use the coordinate copy function to transfer the polygon coordinates.

Assignment 2

Using the NDVI/NDMI values calculated above and the tractor data from Assignment 4 (together with the code used to read the data):

Define what constitutes a tractor “drive” in an appropriate way.

Consider different alternatives and their suitability.
Possible approaches include:
a time-based definition (e.g. all driving activity occurring within a single day), or
routes that start and end at a suitable location (e.g. the farmyard/stable location with an appropriate radius).
Can you think of any other alternatives?

Plot the driving route on the same map as the moisture index.

Create a scatter plot (XY chart) showing the relationship between instantaneous fuel consumption and moisture, either per drive or per day.

Repeat the analysis above for three suitable days. Select days during the summer, including at least one from June and one from August, when cloud cover does not obstruct the satellite imagery. Is there a suitable satellite image available for July?

Summarise and discuss your observations regarding the relationship between fuel consumption and the moisture index.

Submission

Submit your program code and discussion/analysis in Moodle. The discussion may be included as text within the Colab notebook or submitted separately as a PDF document.
