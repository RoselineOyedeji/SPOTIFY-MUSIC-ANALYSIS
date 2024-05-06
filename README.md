
# Spotify Musis Analysis

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiMjdhM2MzOTktYmM4NS00YTgyLThmZmItMmU0NGEwM2ZkZDcwIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

## Insights

This dashboard helps users understand streaming behaviour of people. It helps users know the streams of a track by an artist and the most streamed tracks.Users get to know the artist who is likely favoured by streams on the platform.

According to the dataset used, "Blinding Lights" is the top streamed track by "The Weekend".

Also users can see which artist tracks get the most stream on a daily basis. And the total streams of tracks by the date in which they are released.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a xlsx file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Power Query automatically gave each column a name but it was changed by using first row as headers.
- Step 4 : It was observed that some of the columns had the wrong data type and it was changed to the right data types.
- Step 5 : In power query, none of the columns had nulls except the key column(text) and in_shazam_charts(whole number) from null to "none" and null to 0.
- Step 6 : In_shazam_charts was later removed because it was not needed for this analysis.
- Step 7 : In power query, a column named streams had a 1% error and after checking if it won't affect our analysis if it's removed, the error was removed
- Step 8 : In power query, we had a released year, released month, and released day column, it was merge together to get a single date column.
- Step 9 : An artist dimension's table was then created, duplicate values was then removed and queries was merge to the fact table.
- Step 10 : In the report view, under canvas background a new background was imported.
- Step 11 : Four card visuals were added to the canvas, one representing total stream, total track, average stream & other representing total artists with a stream growth rate progress bar.
           Using visual level filter from the filters pane, basic filtering was used & blank values were unselected.
           
           Although, by default the year slicer showed all of the years but it was filtered down to the years that has values in them.
- Step 10 : A line chart was added to the canvas showing the streams by their released dates. 
- Step 11 : A new slicer was then added containing all tracks and their cover images but was filtered to the top 5 tracks streamed.
- Step 12 : A new table was created named "ProgressBarChart".

![Progresstable](https://github.com/RoselineOyedeji/SPOTIFY-MUSIC-ANALYSIS/assets/161141258/a679d946-175c-4773-ad13-943d8bfd3a8b)



- Step 13: A new column was added to it named "Percentage"

![Percentage](https://github.com/RoselineOyedeji/SPOTIFY-MUSIC-ANALYSIS/assets/161141258/dd72c0ad-2a88-4a5d-91dc-7ec5aeb17859)


- Step 13 : Few measures were created to get the progressbar

To get the constant line
    Constant line = 65

To get High
    
    High = 65

To get Low
    
    Low = 35

`These are just random figures that fit the visual, it can be changed`

To get Growth Symbol
	
    GrowthSymbol = 
    IF(MAX(ProgressBarChart[Percentage]) = ROUND([Streaming growth rate], 2), 30)

To get Growth Bar
	
    GrowthBar = 
    IF(MAX(ProgressBarChart[Percentage]) <= [Streaming growth rate], 50)

`Also, a line chart was used to work around the progress bar.`

![constant line](https://github.com/RoselineOyedeji/SPOTIFY-MUSIC-ANALYSIS/assets/161141258/23764335-dfd5-44c3-ad42-2e69a4c809f1)

 
  
`In our dataset, some cover images were not found so therefore they won't show any image on the dashboard.`




Snap of the dashboard

![Spotify](https://github.com/RoselineOyedeji/SPOTIFY-MUSIC-ANALYSIS/assets/161141258/b119e026-b7de-4392-8d93-ee783b8c00e5)



# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.


# Spotify Music Analysis.md.txt
Displaying # Spotify Music Analysis.md.txt.
