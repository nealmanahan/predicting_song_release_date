# Predicting Song Release Date Using Billboard and Spotify Data

---

## Creator
 
[Neal Manahan](https://www.linkedin.com/in/neal-manahan/)  

---

## Problem Statement and Overview

As a major label artist, planning and preparing a successful release goes further than finding a great single or recording a critically acclaimed album. A strategic rollout is essential to standing out and cutting through noise in this highly competitive industry. The target of this project is to pinpoint an effective time to release new music.

In order to achieve this, I decided to gather data from the largest music streaming service, Spotify, along with chart data from the industry publication Billboard to analyze the songs that see the most success while on the best selling/most listened to charts.


---

## Contents
[Dictionary](#dictionary)  
[Executive Summary](#executive-summary)  
[Limitations/Future Iterations](#known-issues)    
[Sources](#sources)

---

<a id='data-dictionary'></a>

## Data Dictionary

<p align="left"> 
    
|Feature|Description|
|---|---|
|track_name|Name of song; derived from Billboard and Spotify|
|artist_name|Name of song performer(s); derived from Spotify|
|released_on|Date of song's initial release; derived from Spotify|
|streams|Number of plays on the Spotify platform a track has|
|bb_hot_100_peak|The peak position a track achieved on the Billboard Hot 100 top songs chart (released weekly)|
|sp_top_200_peak|The peak position a track achieved on the Spotify Top 200 top songs in the US chart (released weekly)|
|genres|Listed genres of a track's performer(s); derived from Spotify|
|artist_popularity|Measure of Performer's current popularity; calculated by Spotify|
|artist_followers|Number of users that follow a track's artist|
|month_released|Calendar month that a track was initially released|
|season|Quarter of the year a song was released|

</p>

---

<a id='executive-summary'></a>

## Executive Summary

There are a number of factors to consider when selecting a release date for a new song or record. Streaming services and digital downloads have replaced spins on the radio and prime placement at the record store, which stood as the best ways to get music into the ears of consumers worldwide. While the time from song idea to final product release can now be measured in a matter of days, a strategy should still be employed to pick the correct release day.

Using data from the Billboard Hot 100 songs chart and Spotify, I set out to create a prediction model that would determine when a song was released. The data I used included artist information (genres, platform followers, popularity) and streaming numbers for songs that spent time on both the Billboard chart and the Spotify US Top 200 chart. The reasoning for selecting Spotify was that their platform has the largest number of daily active users among the major streaming services and the availability of data from the company. Based on this data, success on the Spotify platform directly relates to success on the Billboard Hot 100 chart.

Through analysis of the data, a clear pattern emerged detailing when top songs are released. April and June had significantly higher concentrations of top songs streamed, while cumulatively Q4 (Late Fall/Winter) had a high output of top songs released. Reasons that lead me to believe this include the pre-existing retail trend of product released in time for holiday shopping, and releasing a potential “Song of the Summer” in Q2 (April/June), is also an ideal time for Grammy Award consideration.

Based on this analysis and the Random Forest model used to determine release dates of existing top songs over the last 3 years, a lead up single should be released in May when the release schedule is much less crowded and still reaps the benefits mentioned above. A follow up single or album should be released in June to again capitalize on the award consideration season. Songs and albums that receive nominations and awards tend to see an additional bump in streams and overall sales after the Grammy Awards in Q!, which is another major benefit to this release strategy.

While ideally this analysis aimed to deal with artists of all sizes, there are some limitations in the availability of total streaming/sales data. Because Spotify top chart streaming numbers were the only “sales” data I was able to pull, these recommendations are only advised for established acts with a major label backing. Moving forward, with access to full proprietary data from Nielsen Soundscan, I am confident this analysis will evolve to make strong recommendations for artists of all career maturity levels.

---

<a id='known-issues'></a>

## Limitations/Future Iterations

Upon commencement of this project, it was my understanding that Soundscan data used to calculate Billboard chart positions was publicly available. The project unfortunately had to pivot to investigate the impact of streaming data as opposed to total sales numbers. This led to an expected lack of accuracy and was accounted for in analysis by limiting the scope of data to include only Spotify and Billboard. There were also challenges in the labeling of track names between Billboard and Spotify, which led to a workaround process that eliminated roughly 30 songs from the three years of data. While small compared to the overall dataset, any loss should work to be avoided. 

Future iterations of the project would include data from Nielsen Soundscan to more accurately predict release date. Other data sources including social media influence/followers and other streaming platforms’ data would also be included. The model and analysis do provide proof of concept that there is a trend in what the best period of time is to release a song.

---

<a id='data-sources'></a>

## Data Sources

 [Spotify](https://developer.spotify.com/dashboard/login)  
 [Billboard](https://www.billboard.com/charts/hot-100)  

---
## Sources

 [Billboard API Wrapper](https://github.com/guoguo12/billboard-charts)
 [Spotipy API Wrapper](https://github.com/plamere/spotipy)
 [Spotipy Documentation](https://spotipy.readthedocs.io/en/latest/)
 [Add multiple csv files at once - Stack Overflow](https://stackoverflow.com/questions/20906474/import-multiple-csv-files-into-pandas-and-concatenate-into-one-dataframe)
 [Remove duplicate strings from a list in python - Stack Overflow](https://stackoverflow.com/questions/8200342/removing-duplicate-strings-from-a-list-in-python)
 [Match similar strings from different data sources - Stack Overflow](https://stackoverflow.com/questions/3437059/does-python-have-a-string-contains-substring-method?rq=1)
[Selecting Parameters for Random Forest Model - Towards Data Science, Author: Will Koehrsen](https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74)

