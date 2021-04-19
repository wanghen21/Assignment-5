# Assignment-5
Pyber Challenge
The purpose of this exploratory data analysis is to identify key ride sharing metrics by type of city and create a graphical representation of the total weekly fares based on the city types which will help improve access to ride sharing services and determine ride affordability.
Technical Analysis
The total drivers, total rides ,total fares and average fare per ride were obtained using the groupby function along with the sum , count and mean functions while the average fare per driver was obtained by dividing the total fares per city type by the total drivers per city type. To obtain the data frame used for plotting the multiple line graph, the following tasks was performed:
Columns of the main data was renamed using the rename column function
Index was set to date time using the date time index function
A new dataframe was created with city type and fare columns using the copy function
The index of the new data frame was checked using the info function
Groupby function was used used to group the fares by city and date and this was placed in a data frame using the dataframe function
A pivot table was created using the pivot table function
Loc function was used to organize the pivot table within the given date range
The pivot table was resampled using the resample and sum functions
Results

As shown in the data frame above, the rural cities had the highest average fare per driver and ride while the urban cities had the lowest and the high fares observed in the rural cities was due to the low number of total rides and total drivers in those cities.

As shown in the multiple line graph above, the urban cities had the highest total fare within the months of January to April 2019 followed by the rural cities while the urban cities had the lowest fare and the low fares can be attributed to the empty cells observed in the rural cities column after arranging the data into the specified date range using the loc function. In summary, the drop in the number of ride usage in the rural cities within the months of January to April, 2019 could be due to the low number of available rides and drivers in those cities and allocating more rides & drivers to the rural cities will most likely reduce average fare per ride & driver which will invariably boost ride affordability. In addition, although the available data is limited to 2019, the Urban cities might also benefit from more ride allocation within the months of January to April as this will help meet the demands for rides in those months , increase revenue and enhance affordability.
Challenges Encountered during Analysis
Formatting the horizontal axis in the multiline plot to resemble the graph provided in the challenge question was a bit difficult. Upon plotting the graph, the date format on the horizontal axis had the format 2019–01–01, and the challenge question asked us to show the months and day format ( Jan 2019, Feb, Mar , Apr).
Resolution strategy
To resolve this issue, I used the plt.xticks() funtion to view the numerical format of the dates and then added the dates into the function along with the calender month format. See a screen shot showing the code used to format the horizontal axis below:

Recommendation(s)
In addition to the above analysis, I would recommend obtaining more information about the demographics of those living the the three city types and additional two to five previous year city and ride data.
Recommended Future Analysis
With the demographic information such as population and age range, we can group the fares by age and city type or by population and city type. These information will shed more light on the reason why some of the city types had high average fare per driver and ride. Also, using the loc function on two to five previous year data might better explain why the rural and suburban cities had low fares within the month of January to April.
