Link to original repository: https://github.com/JLaoo/kpop-classification

# Kpop classification

# Introduction

In this project, I'm going to attempting to classify various kpop songs by their group. Current music classification techniques don't seem to be too accurate, even with datasets significantly larger than what I will be attempting to work with. As a result, I'm not expecting too high of an accuracy with my classifier, especially since classifying groups within a genre is also much harder than classifying genres in general. Current classification techniques I'm considering are CNN and RNN as well as simple feature extraction with librosa and running various sklearn models on them.

# Steps

1) scrape_mp3s
- I'm scraping videos from youtube with youtube_dl and saving them locally as mp3s.
- I'm choosing 6 groups total with 10 songs from each group. I have 3 male groups and 3 female groups for the sake of balance.
- I tried to choose musically distinct groups, but im gonna be honest, the male groups kinda all sound the same.
2) clip_mp3s
- The mp3s are each clipped into 5 30 second clips composed of the first 2 minutes and 30 seconds of each song.
- The clipping is done to not only to prevent bias during learning, but also to quintuple the size of the dataset.

Copyright for all audio files are owned by their respective creators.
