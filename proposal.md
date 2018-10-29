# X-Team Spotify Feature Identifier Project Proposal 

## Problem Description
We would like to figure out how the actions that a Spotify user takes affect the features of the songs that Spotify recommends to that user.

Our program could take in a feature constraint (e.g. BPM less than 120) and a playlist size (e.g. 100). The feature contraints we could use would be based on song metadata available from Spotify's and Lyric Genius's API. Once the user input is given, we could have Spotify generate random playlist of the given size. We could then import this playlist and use Spotify's and Lyric Genius's API to associate the relevant feature value with each song and store this pair in our Playlist ADT. We could then filter the songs according to whether or not they fulfilled the given feature constraint. This filtered list would then serve as the seed of the next playlist that Spotify generates. We would repeat this process 100 times or until 95% of the songs fulfilled the feature constraint. If the latter condition was fulfilled then we could graph the feature profile over each generated playlist to the observe the rate at which Spotify adapted its generated playlist to the given constraint. In order to conduct comprehensive testing of the individual units, we could create an artificial playlist that meets our future constraints in order to test the functionality of the code created that is complied with the use of Spotify API. 

## Questions to answer for Exercise #2

1. Name: Spotify Feature Identifier

2. Output: List of features that Spotify uses in its recommendation selection algorithm, Graphing feature value over time.

3. Input:
Our input would be Spotify's generated playlist. We can get metadata from this playlist using Spotify's API and Lyric Genius's API. We would have the user enter a feature constraint and the size of the playlist it wants spotify to generate. For example, the user could input "songs less than 120 BPM" as a feature constraint, and 100 as the size of the playlist it wants Spotify to generate.

Example: 

 >User: "Songs less than 120", 2

 >Spotify: "Hurt, Johnny Cash", "Billy Jean, Michael Jackson" 

 >Spotify: "Miracles, Insane Clown Posse", "Oh Comely, The Neutral Milk Hotel" 


4. User Interface: We will create this UI where the user will select a feature to look for, then hit 'Start' and it will run in the background while the user uses Spotify. The program will run in the background and collecty datat from the music that the user listens
to. It will collect information on whether a user likes, skips, searches, or adds a song to a playlist and
create a record of this activty. Once finished, the user will hit 'Stop'. The program will look at Spotify's recommended 
playlist and identify the features Spotify used to create it based on the liked and disliked songs. We we will create 
data files that contain this data.

5. Types List: 

 >Main.java - The main program runs in this class.

 >Playlist.java - A playlist that contains song name and feature value

 >PlaylistADT.java - ADT for playlist; contains signatures for size, name, delete, insert, lookup/get, sift, isEmpty

 >SpotifySyncer.java - Uploads and gets playlists from Spotify

 >DataGrapher.java - takes in playlists and graphs their feature value


