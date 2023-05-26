# Challenge-Playlist-maker

# Step 1: We've created a database of songs and artists, and you'll make playlists from them in this challenge. In this first step, select the title of all the songs by the artist named 'Queen'.

Select title
from songs
where artist = "Queen";

## Step 2: Now you'll make a 'Pop' playlist. In preparation, select the name of all of the artists from the 'Pop' genre. (Tip: Make sure you type it 'Pop', SQL considers that different from 'pop'.)

Select name
from artists
where genre = "Pop";

### Step 3: To finish creating the 'Pop' playlist, add another query that will select the title of all the songs from the 'Pop' artists. It should use IN on a nested subquery that's based on your previous query.

Select name
from artists
where genre = "Pop" IN (Select title from songs where genre = "Pop");

Select title 
from songs
where artist IN ( select name from artists where genre = "Pop");
