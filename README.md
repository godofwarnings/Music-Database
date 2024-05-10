<center> <h1> ```math
SE = \frac{\sigma}{\sqrt{n}}
``` $\Large \mu$Sic </h1> </center>

# The video
The video size was getting too large for moodle so here is the onedrive link for the following

https://iiitaphyd-my.sharepoint.com/:v:/g/personal/radhikesh_agrawal_research_iiit_ac_in/EZLO7_TTk39FlQjcrl7H7tEBZETKusNRIHsgcYPBstVGZA?e=tDOOeJ

# Loading data from dump

1. Install the module prettytable for Pretty Print

```bash
pip install prettytable
```

2. In cli.py change the user and password at lines 802 and 803 according to your system

```python
con = pymysql.connect(host='localhost',
                user="demo",
                password="password",
                db='Music',
                cursorclass=pymysql.cursors.DictCursor)
```

3. start mysql and in mysql, enter this

```sql
CREATE DATABASE Music;
```

4. Quit mysql

6. To load tables into mysql, do the following in terminal

```bash
sudo mysql Music < Music.sql
```

7. Grant permissions to cli.py

```bash
chmod +x cli.py
```

8. Run cli.py and follow the instruction

#### References
* https://stackoverflow.com/questions/32737478/how-should-i-resolve-secure-file-priv-in-mysql
* https://stackoverflow.com/questions/59993844/error-loading-local-data-is-disabled-this-must-be-enabled-on-both-the-client

# Queries supported

## Projection/Retrivel
1. Select all songs of given creator.
2. Select all users which have more than treshhold plays of given genre.
3. Select Users having more than treshhold plays.
4. Select creators with less than given views, but which have won an award.
5. Select creators with less than given views.
6. Select all users whose name starts with given string.
7. Calculate number of plays for an album. 
8. Select songs with more than X plays. 
9. Print all creators which have won an award.
10. Find users which have joined a platform bw given dates.
11. List bands which user listened this month.
12. Print all users.
13. Print all songs.
14. Print all creators.
15. Get all playlists created by given user.

## Updation
1. Add user.
2. Make user listen a song.
3. Create Playlist.
4. Add song to playlist.

## Analysis
1. Generate a general report.
2. Make a user report.
3. Produce a creator report.

#### Some details

#### General report
1. Most listened song
2. Most listened artist
3. Most listened genre
4. Band with most awards
5. most listened album
6. Artist with most awards

#### User report
1. Number of songs listened this year
2. most listened artist
3. most listened genre

#### Creator report
1. Total number of streams
2. total number of songs
3. number of different genres

