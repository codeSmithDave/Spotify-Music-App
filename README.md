# Spotify-Music-App
A ReactJS application that uses Spotify Api to allow the user to search Spotify for songs and save them to custom playlists.

# Node Modules
Besides the default Node modules, this app also uses node-sass

# Spotify Api
In order for this app to work, we need 2 things:
- An access token
- Access token expiry time

After the user accepts the Spotify authorization process, they get redirected to this app's url (in this case, http://localhost:3000/)

The access token and its expiry time will be in the url so we'll use regex to find the information (as it can be seen in src/Util/Spotify.js).

In this app we will be using several things from the Spotify Api:

1) Get authorization from the user using the Implicit Grant Flow - More Information: https://developer.spotify.com/documentation/general/guides/authorization-guide/#implicit-grant-flow

2) Search Spotify for songs - More Info: https://developer.spotify.com/documentation/web-api/reference/search/search/

3) Create playlist - More Info: https://developer.spotify.com/documentation/web-api/reference/playlists/create-playlist/

4) Add songs to newly created playlist - More Info: https://developer.spotify.com/documentation/web-api/reference/playlists/add-tracks-to-playlist/

# The App
![The Music App](/app-img/app.jpg)

1) Before the user can search anything, they must give us permision to some parts of their account
![Spotify Auth Page](/app-img/authorize.jpg)

2) Upon successful authorization, the user can search songs and create playlists
![The Music App with search results](/app-img/search-songs.jpg)

3) The created playlist
![Created playlist on Spotify](/app-img/playlist.jpg)
