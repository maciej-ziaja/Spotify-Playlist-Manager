## 👨‍💻 Built with
![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)

##  Descripction

The object of this project is to extend usability of a Spotify music app.

In my opinion, Spotify app lacks two features:

1. Ability to listen to all the artists that I follow. 

To fix that, I have created a script that pulls the list of all the artists that I follow, then pulls a list of Top 10 songs of all these artists. Next step is to create a new playlist and then add Top 10 songs to it.

2. Ability to merge different playlists into one.

I gather songs on playlists according to a variety of characteristics. I also wanted to merge some of my playlists to create a Car Playlist. Thats why I wrote another script. It pulls the list of all user's playlists, then, after choosing some of them, pulls all the songs that are on those playlists. After that it creates a new playlist and add those songs to it.


## Authorization and authentication

Spotify API requests creating an app on it's [Spotify fot Developers](developer.spotify.com) website. After that a user is free to use the API. 
I used [Authorization Code Flow](https://developer.spotify.com/documentation/general/guides/authorization/code-flow/) to get authorization code, token and refresh token.


## Using the Web API

Both applications in this notebook follow the same principles. Well written [Spotify Documentation](https://developer.spotify.com/documentation/web-api/) was very helpful in understanding the process.
I used GET method to pull the data from Spotify servers (list of songs, artists or playlists) and POST method to create data on Spotify servers (authentication process, creating playlists and adding songs to playlist).

The main issue that I encountered is was that Spotify API can take and return a very limited amount of positions. That required using loops to go through long lists of data.

## How to use it?

If you want to use my notebook with your Spotify account, feel free to do so.
To successfully run a script you need to go to create an app. Follow instructions on [Quick Start](https://developer.spotify.com/documentation/web-api/quick-start/) website.
After that, you will need to provide a **spotify_secrets.py** file in the repository. Copy the structure from my file:

client_id = 'Your Client ID'
client_secret = 'Your Client Secret'
refresh_token = 'Your Refresh Token'

When you confirm the scope of your app in the browser, make sure that you copy an authorization code correctly. See documentation for the [Authorization Code Flow](https://developer.spotify.com/documentation/general/guides/authorization/code-flow/)