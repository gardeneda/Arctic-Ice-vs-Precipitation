Data attained from:

NOAA (National Oceanic and Atmospheric Administration)
- CMAP Precipitation

https://psl.noaa.gov/data/gridded/data.cmap.html

<hr>

The original data 'cmap-means.csv' could not be included due to the size of the file. (5432832 lines of data)<br>
The extraction process is under <code>data_management.ipynb</code>, under the heading <strong>Setting up Data for Precipitation</strong>.
<br>
For convenience; the code used to filter the data was done with the following lines of code:
<pre>
for num in range(0, len(precipitation)):
    if precipitation.iloc[num]['lat'] < 60:
        precipitation = precipitation[:num]

        break

precipitation.to_csv("./Precipitation/filtered_precipitation_data.csv", index=False)
</pre>