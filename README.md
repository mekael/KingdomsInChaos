# Kingdoms In Chaos 

## What is KIC?

Kingodoms In Chaos is an abandoned / dead MMORPG (https://store.steampowered.com/app/1333650/Kingdoms_In_Chaos/), that is still listed for download on Steam and had it's last update in 2023. Since then the servers have been taken offline, and the discord has become a ghost town. 

Example gameplay:  https://www.youtube.com/watch?v=H2NZQU8YExk 



Interestingly enough, like several other Unity based MMO's, the client and the server both use the unity libraries for pathing, mesh, etc et. Unlike other MMO's, the server code was never removed from the client base, and indeed there is a "server only" button on the login panel which allows a user to start a server instance hosted on port 7777 (the default for the Mirror networking library when used with Unity).  The client though has a single "North American" server hard-coded in it's level0 asset and there is no easy/direct way to replace it. 


## What is this repo?

This repo provides a modified library which removes the hard-coded server entry, and instead reads a list of servers from a config file. 


## How do I use this on the server side?

0. make sure port 7777 is open on the machine you're intending on using, and that the server is accessible as well. (this may require you to run a reverse proxy)
1. Start the game as normal
2. Hit the "server only" button to start

## How do I use this on the client side?

1. Drop Assembly-CSharp.dll into {STEAM_LIBRARY_FOLER}/Kingdoms In Chaos_Data/Managed
2. Drop servers.txt right next to {STEAM_LIBRARY_FOLER}/Kingdoms In Chaos.exe
3. Modify servers.txt to point to the server(s) you wish to connect to
4. Start the game, select the server, and hit start.

```
SERVER_NAME_1,ip_address_or_server_hostname1
SERVER_NAME_2,ip_address_or_server_hostname2
```

## How good is the game?

 To be honest, I haven't a damn clue what the gameplay is really like, as i've played a total of like 6 minutes of the game after I got the server working. 


