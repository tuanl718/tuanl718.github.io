# Predicting the Danceability of a Song Based on its Audio Features
CMSC 320 Final Tutorial - Fall 2019
Tuan Le, Joseph Johnson, Andrew Thai

# Introduction
Music plays an important role in all of our lives and has a profound cultural impact within society as a whole. Music has been created, shared, and cherished in every corner of the globe since the beginning of human civilization. It has grown and evolved with time, spawning many different genres and styles, each having its own unique elements. Along with this, music has also birthed many of the world's most influential figures like Beethoven, The Beatles, Michael Jackson, Kanye West, and much more. When our group was brainstorming potential project ideas, we knew we wanted to choose a topic that we each deeply cared about. We wanted a topic that plays a big role in our lives everyday. In music, we found just that. 

When looking at potential datasets on Kaggle, we found the Top Spotify Tracks of 2018 dataset by Nadin Tamer. Spotify is one of the most popular music streaming platforms out there and our group uses it everyday. At the end of each year, Spotify compiles a playlist of the songs streamed most often over the course of that year. This dataset includes the top 100 most streamed songs. 

As stated by Tamer, the audio features for each song were extracted using the Spotify Web API and the spotipy Python library. The .csv file includes: 

- Spotify URI for the song
- Name of the song
- Artist(s) of the song
- Audio features for the song 

The audio features include:

1) Danceability
2) Energy
3) Key
4) Loudness
5) Mode
6) Spechiness
7) Acousticness
8) Instrumentalness
9) Liveness
10) Valence
11) Tempo
12) Duration
13) Time Signature
