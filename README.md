# group34-proj1-3
# Nicholas Cancar ncc2137, Kanak  Singh ks3775



Google Cloud info from Part2:
     Project name: COMS-4111-MUSICDB
     Account used: ncc2137@columbia.edu
     Command used to log in:psql -U ncc2137 -h 35.231.103.173 -d proj1part2 VM instance: instance-1

Music Database

Our idea was to create a Database desgined for a digital music library. 
Our database accounts for how songs are related to albums, artist, playlists. 
It accoounts for users following other users, playlists, and artists... 
and gives them the option to create new playlists and upload new songs not already in our database

For our web app, we have three different categories: search, update, and upload. Each request the user makes
weather it is searching for a song or following an artist or uploading a song interacts and updates our 
database on the back end connected to the URI: "postgresql://ncc2137:3749@35.231.103.173/proj1part2".

The site doesn't do explicit error checking however it will not break. If a user inputs information in correctly
their request will simply not get processed. They can try again with the right input.

The site doesn't do explicit error checking however it will not break. If a user inputs information in correctly
their request will simply not get processed. They can try again with the right input.

Searching a user yields not only data from the user_account table, but also from other relationship tables like userfollowartist, userfollowuser, usercreateplaylist, userfollowplaylist. We chose an arbitrary subset of these to include in the page but to include the others is directly analogous. Also, we used a string_agg function to list all artists that one user follows for example. This looks better/ more compact than listing multiple rows for the same user with just the artist name being different.

The set of important database operations we used were to allow the user to add songs to the database, or add a user-follow-x relationship instance in the database. This would allow the user to actually interact with the web-app and make it their own.


Link: http://35.185.66.203:8111/

