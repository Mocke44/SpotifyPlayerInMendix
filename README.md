# SpotifyPlayerInMendix
A simple implementation of the Spotify Web API in mendix. This repository includes the complete app package for the Mendix Project( import guide https://docs.mendix.com/refguide/import-app-package-dialog/)

Configuration
    ===================================================================
1. Dependencies
    1. Deeplink Module https://docs.mendix.com/appstore/modules/deep-link/
    2. Microflow Timer Widget https://docs.mendix.com/appstore/widgets/microflow-timer/
2. Setup
    1. Configure all constants in the Constants folder
        1. @Spotify.AppURL = your app URL + port number (Configure for each environment
        2. @Spotify.ClientID = Your Spotify Client ID
        3. @Spotify.ClientSecret = Your Client Secret
        4. @Spotify.ShowDialog = If true will show the dialog from Spotify each time a personal Spotify token needs to be refreshed for the user (Token valid for 3600 seconds/1 hour)
    2. Log in as Administrator to Create a deep link 
        1. @Spotify.AppURL+'/link/spotifyauthentication'
        2. it should call the microflow ‘ACT_HandleSpotifyRedirect’ which is in the Authorization folder

Deploy the app locally and log in as MxAdmin in order to create an account with the user role "User".
Log out, and log back in as the user you just created. After logging in you should be redirected to Spotify to approve the use of your account. After approval, you will be able to search and play any track, artist, or album available on Spotify. You can also transfer playback between any Spotify-connected device or speaker
