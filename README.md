# Spotify-Music-App
This is a ReactJS application designed for seamless interaction with the Spotify API, enabling users to manage their music content directly from their account. This project makes use of API integration and user authentication through Spotify's API's, as well as the standard ReactJS components to create a user interface. Key functionalities include:

**Authorization:** Implements Implicit Grant Flow client-side authentication which gives the app access to the user's account for a set amount of time before needing to re-authenticate.

**Song Search:** Features a search interface where users can input keywords to query Spotify's API for song results. The results are dynamically displayed, offering an interactive user experience.

**Playlist Management:** Users can create custom playlists by adding songs from the search results to a temporary playlist container. Upon saving, the app interfaces with Spotify to reflect these new playlists in the user's account.

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

### 1) Before the user can search anything, they must give us permision to some parts of their account

![Spotify Auth Page](/app-img/authorize.JPG)

### 2) Upon successful authorization, the user can search songs and create playlists

![The Music App with search results](/app-img/search-songs.JPG)

### 3) The created playlist

![Created playlist on Spotify](/app-img/playlist.JPG)
