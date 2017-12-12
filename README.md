<img src="https://devmounta.in/img/logowhiteblue.png" width="250" align="right">

# Project Summary

This project is designed to replicate what you might receive on the job. There won't be any guided instruction on what you'll need to do. We will only provide you with design specifications and technical requirements. Your mentors have also been asked to provide only minimal guidance. They can point you in the right direction, but cannot help you code. This project is a chance for you to combine and showcase the skills you've learned so far.

With this specification/requirement only structure, we believe this project will showcase what you can do at this point of the program. Because of this, we feel this project will be worth putting in your portfolio.

Good luck and work hard!

# Color Palette & Font

<img src="https://raw.githubusercontent.com/Alan-Miller/music-simulation/master/assets/color-palette.png" />

<b><a href="https://fonts.google.com/specimen/Open+Sans?selection.family=Open+Sans">Google Font - Open Sans</a></b>
<br/>

### The icons are included in the assets folder of this repository


# Application Design

## Auth View
<img src="https://raw.githubusercontent.com/Alan-Miller/music-simulation/master/views/login.png" />

## All Songs View
<img src="https://raw.githubusercontent.com/Alan-Miller/music-simulation/master/views/all-songs.png" />

## Song Details View
<img src="https://raw.githubusercontent.com/Alan-Miller/music-simulation/master/views/song-details.png" />

## Playlist View
<img src="https://raw.githubusercontent.com/Alan-Miller/music-simulation/master/views/playlist.png" />

## All Playlists View

<img src="https://raw.githubusercontent.com/Alan-Miller/music-simulation/master/views/all-playlists.png" />

## Add Song View
<img src="https://raw.githubusercontent.com/Alan-Miller/music-simulation/master/views/add-song.png" />

## Edit Song View
<img src="https://raw.githubusercontent.com/Alan-Miller/music-simulation/master/views/edit-song.png" />

# Technical Requirements - Front-end

## Auth View
* User can log in into their account.
* User can register for an account.
* User should be navigated to the All Songs view on a successful login or successful registration.

## All Songs View
* User can view All Songs available for checkout
* User can filter songs by name / artist / album
* User can reset an applied filter to see a list of All Songs again
* User can navigate to Song Details view by clicking on a song in the list
* User can navigate to Add Song view through link in top corner
* User can log out and be redirected back to the Auth View

## Details View
* User is able to add song to playlist from here
* User is able to navigate to Edit Song view 
* User is able to delete a song from the database
    * This should redirect the user back to the All Songs View
* User is able to navigate to previous view
* User should be redirected to the All Songs view after adding the song to the playlist

## Checkout / Playlist View
* User is able to remove a song from playlist and playlist is updated in header and component
* User can check out
  * Should add the songs in the playlist to an order on the past orders page
  * Should clear the Playlist View
* User should be redirected to the All Songs view on checkout

## All Playlists View
* User can see all playlists

## Add Song View
* User can add a song to the All Songs view with all the appropriate values
  * Name
  * Artist
  * Album
* User is able to navigate to previous view, canceling the addition of a new song
* User should be redirected to the All Songs view on completion

## Edit Song View
* User populates an editable section based on the selected song's details to update and change information about the song 
* User is able to navigate to previous view, canceling the edit
* User should be redirected to the All Songs view on completion

# Technical Requirements - Back-end
* The back end should be created using Express.
* Massive will be used to establish a connection to your database and manipulate/retrieve data with SQL files
* Student will create tables using the supplied data

## Endpoints

### Authorization Endpoints

* POST - /api/auth/login - Sets the user information on the session.
  * On success return a status of 200 and the user object.
  * A user object should have the following properties:
    * id - This is the UserId you are using for your database.
    * username - This is the username associated with the UserId.
  * The database should store the password, but you should not send this information to the front end as part of the user object
  * On failure return a status of 500.
* POST - /api/auth/register - Registers a user to the database. Sets the user information on the session.
  * On success return a status of 200 and the user object.
  * A user object should have the following properties:
    * id - This is the UserId you are using for your database.
    * username - This is the username associated with the UserId.
  * The database should store the password, but you should not send this information to the front end as part of the user object
  * On failure return a status of 500.
* POST - /api/auth/logout - Destroys the session. Sends a status of 200.

#### NOTE: This is in no way a secure or effective way of storing user credentials. This is required for you to demonstrate your knowledge of data transfer and correspondence between the user and your server using sessions. Do not ever rely on this method in anything bound for production.
