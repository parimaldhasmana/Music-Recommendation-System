# Music-Recommendation-System
Music Recommendation System using Spotify API

**Introduction**
The goal of this project is to recommend songs for a given playlist. This project starts from data collection all the way to model deployment

**Preprocessing**
Before extracting any features, there are two preprocessing steps needed after importing the raw data extracted.

**Data Selection**
The data selection procedure involves two tasks. The first one is dropping duplicate songs. Since the data imported was originally Spotify playlist data, it is crucial to delete replicate songs that exist between multiple playlists. The process involves collecting the artist name and the track titles so that we do not accidentally delete songs that have the same name but by different artists.


**Process****
After extracting all the data of each song, we now discuss the process of performing a content-based filtering algorithm. Two steps were implemented in the algorithm. These two steps are needed every time some enters a new playlist query:

**Playlist Summarization**

Summarization process illustration. Image by Madhav Thaker and modified author.
In this step, we want to summarize all songs in a playlist into one vector that can be compared to all other songs in the dataset to find their similarities.

First, we would need to import a playlist dataframe. The only thing needed in the dataframe is the track id. Having the track id data, we can first separate between songs that are in the playlist and those that are not. It is important to exclude the songs in the playlist since we do not want to recommend existing songs.

