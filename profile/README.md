# Wishgranter project

This project aims to implement a versatile, source-agnostic music player.

The core idea is that one's musical collection should be able to survive media
availability.

## The problem

Traditional music files such as .mp3 are several mega bytes large, requiring 
storage space and are vulnerable to hardware failure or data loss.

Online streaming services offer convenience but lock the user into their 
catalog, a finite catalog the user cannot supplement with their own media.

If a service loses licensing for a given artist or track, that music becomes 
unavailable to the user regardless of their personal connection to it.

Storage space, hardware failure, third-party shenanigans, all are threats to 
one's musical collection.

The common thread is that all these approaches tie the collection to a 
particular medium or provider.

## The solution

The solution is to decouple the collection from the actual media. Instead of
listing MP3 files or streaming URLs, define a playlist by what the music
*is*: its title, artist, album, genre etc.

At the core is the **[Descriptive Playlist (DPLS)](https://github.com/Wishgranter-project/descriptive-playlist-definition)** 
file format comes in. A DPLS file describes each entry by its metadata alone. 

A player built for it can then resolve the actual audio from whichever source 
has it available, local files, a streaming service, or elsewhere, without the 
playlist itself being aware of the source.

The result is a music collection that outlives its current media, is portable
across providers, and stays readable and version-controllable as plain text.
