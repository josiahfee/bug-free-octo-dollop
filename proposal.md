# X-Team Spotify Feature Identifier Project Proposal

See https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code for tips on using *Markdown* tags to format __.md__ files

## Goal

Work as a team to create a project proposal for your X-team to complete together.
The project does not have to be extremely difficult,
but there must be work to do for each member of your team.
You may reference figures using "See figure 1".  
Be sure to submit corresponding image files, i.e. figure1.png (or figure1.jpg) for each figure.

## Grading: To earn full credit, your team's proposal must include:

* (md) documentation: [this file] describing purpose and use of your program

* Description of a program that has:

  ** a main Java program class in a file named Main.java
  
  ** a custom data structure designed and built by your team
  
  ** comprehensive testing of individual units
  
 Caution: You are not being asked to implement this program, at least not yet. 
 We just want your group to make a proposal or pitch for your program.
 
 Tip: Your custom data structure can be composed of or extensions of data structures that you have learned and used in previous programming assignments.  We're looking for decisions about how to build a high-level data structure that will likely have lower-level components.

## Problem Description

Briefly describe a problem that your team would like to solve.  
Describe at a high level a program that could solve that problem.

## Questions to answer for Exercise #2

1. Name: Spotify Feature Identifier
//Give your project proposal a name (and edit the top line of this file)

2. Output: List of features that Spotify uses in its recommendation selection algorithm, Graphing feature value over time.
//Describe the output your program will produce.  Include and example format of the output produced.

3. Input: Describe the data that is needed to solve your problem. Include an example format of the input data.
Our input would be Spotify's generated playlist. We can get this from Spotify's API and Lyric Genius's API. We would have the user enter a feature constraint and the size of the playlist it wants spotify to generate. For example, the user could input "songs less than 120 BPM" as a feature constraint, and 100 as the size of the playlist it wants spotify to generate.

4. User Interface: We will create this UI where the user will select a feature to look for, then hit 'Start' and it will run in the background while the user uses Spotify. The program will run in the background and collecty datat from the music that the user listens
to. It will collect information on whether a user likes, skips, searches, or adds a song to a playlist and
create a record of this activty. Once finished, the user will hit 'Stop'. The program will look at Spotify's recommended 
playlist and identify the features Spotify used to create it based on the liked and disliked songs. We we will create 
data files that contain this data.

5. Types List: 

Main.java - The main program runs in this class.

Playlist.java - A playlist that contains song name and feature value

PlaylistADT.java - ADT for playlist; contains signatures for size, name, delete, insert, lookup/get, sift, isEmpty

SpotifySyncer.java - Uploads and gets playlists from Spotify

DataGrapher.java - takes in playlists and graphs their feature value

## Edit and Submit this file and any figures referenced by this document.

