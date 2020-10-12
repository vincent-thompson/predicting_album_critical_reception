# Album Score Predictor

### Description

My goal with this project is to see whether or not I can predict the critical reception of an album using data scraped from [metacritic](https://www.metacritic.com) and audio features collected from the Spotify Web API with the help of the Python library [Spotipy](https://spotipy.readthedocs.io/en/2.16.0/)


### Target Variable

- Metascore, a weighted average of critic reviews, [as aggregrated by metacritic](https://www.metacritic.com/about-metascores) (range: 0 - 100)

### Features 
Each of these was looked into, but not all of them ended up being used in the final model

- Release Month 
- Day of the week released
- Number of tracks
- Average track length
- Total album length
- Artist's monthly Spotify listeners
- Percentage of explicit tracks on the album

Audio features as calculated by [Spotify](https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/) (for each feature, I chose to use the mean of the value for each track on the album in order to get an album level metric:

- Acousticness: values from 0 to 1 as a confidence measure of whether the track is acoustic
- Danceability: values from 0 to 1 based on a combination of musical elements that indicate danceability
- Energy: values from 0 to 1 based on a measure of intensity and activity
- Instrumentalness: value from 0 to 1 as a confidence measure of whether a track contains no vocals
- Liveness: Values from 0 to 1 measuring probability that the track was being performed live during recording
- Loudness: Overall loudness of a track in decibels, averaged across the entire track
- Speechiness: A measure from 0 to 1 representing the ratio of presence of spoken words to the presence of music
- Valence: A measure from 0 to 1 describing the musical positiveness/happiness of a track
- Tempo: Overall estimated tempo of a track in BPM

### Data Used
- Scraped data for approximately 3,000 albums from metacritic's [new releases](https://www.metacritic.com/browse/albums/release-date/new-releases/date).
- Collected additional audio features from Spotify's API through a python library called [Spotipy](https://spotipy.readthedocs.io/en/2.16.0/#)

### Tools Used
- Python
- [NumPy](https://numpy.org/doc/stable/#) and [Pandas](https://pandas.pydata.org/docs/index.html): data structures, data cleaning
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#): HTML web scraping
- [Scikit-learn](https://scikit-learn.org/stable/index.html) and [Statsmodels](https://www.statsmodels.org/dev/index.html): Model fitting, predicting, evaluation, and some pre-processing
- [Seaborn](https://seaborn.pydata.org/index.html#) and [Matplotlib](https://matplotlib.org/): visualizations
- [Spotipy](https://spotipy.readthedocs.io/en/2.16.0/#): interacting with Spotify's Web API

### Possible Impacts 
- Identifying factors that can increase or decrease the critical perception of a release




