Link to original repository: https://github.com/JLaoo/kpop-classification

# Kpop Classification
Classifying various kpop songs by their groups via machine learning

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
3) Modeling
- Reading the documentation for CNNs and RNNs at 1 in the morning made my head hurt so I just went with a simple neural net with the feature extraction methods in the LibROSA library.
- Running the neural net several times seemed to give me an average of around 60% accuracy with my best being 70%
- The nueral net can obviously be fine tuned, I pretty much took someone else's neural net from their music classification project and simplified it.

# Remarks
I wanted to do something with kpop so here we are. Dataset is quite small for such an ambitious project, but the accuracy is similar to the one in the blog post and the blog post had a dataset size of 1000 compared to my 300. I suppose I could cut down the 30 second clips into 10 second clips and then maybe take more than 2:30 from each song which would most likely increase my dataset size to >1000. Using Keras is still confusing for me, but I'm slowly getting the hang of it.

Copyright for all audio files are owned by their respective creators.
Inspired by Parul Pandey's blog post found here: https://towardsdatascience.com/music-genre-classification-with-python-c714d032f0d8
