![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

Welcome Silvia Saverino,

This is the Code Institute student template for Gitpod. We have preinstalled all of the tools you need to get started. It's perfectly ok to use this template as the basis for your project submissions.

You can safely delete this README.md file, or change it for your own project. Please do read it at least once, though! It contains some important information about Gitpod and the extensions we use. Some of this information has been updated since the video content was created. The last update to this file was: **September 1, 2021**

## Gitpod Reminders

To run a frontend (HTML, CSS, Javascript only) application in Gitpod, in the terminal, type:

`python3 -m http.server`

A blue button should appear to click: _Make Public_,

Another blue button should appear to click: _Open Browser_.

To run a backend Python file, type `python3 app.py`, if your Python file is named `app.py` of course.

A blue button should appear to click: _Make Public_,

Another blue button should appear to click: _Open Browser_.

In Gitpod you have superuser security privileges by default. Therefore you do not need to use the `sudo` (superuser do) command in the bash terminal in any of the lessons.

To log into the Heroku toolbelt CLI:

1. Log in to your Heroku account and go to *Account Settings* in the menu under your avatar.
2. Scroll down to the *API Key* and click *Reveal*
3. Copy the key
4. In Gitpod, from the terminal, run `heroku_config`
5. Paste in your API key when asked

You can now use the `heroku` CLI program - try running `heroku apps` to confirm it works. This API key is unique and private to you so do not share it. If you accidentally make it public then you can create a new one with _Regenerate API Key_.

------

## Release History

We continually tweak and adjust this template to help give you the best experience. Here is the version history:

**September 1 2021:** Remove `PGHOSTADDR` environment variable.

**July 19 2021:** Remove `font_fix` script now that the terminal font issue is fixed.

**July 2 2021:** Remove extensions that are not available in Open VSX.

**June 30 2021:** Combined the P4 and P5 templates into one file, added the uptime script. See the FAQ at the end of this file.

**June 10 2021:** Added: `font_fix` script and alias to fix the Terminal font issue

**May 10 2021:** Added `heroku_config` script to allow Heroku API key to be stored as an environment variable.

**April 7 2021:** Upgraded the template for VS Code instead of Theia.

**October 21 2020:** Versions of the HTMLHint, Prettier, Bootstrap4 CDN and Auto Close extensions updated. The Python extension needs to stay the same version for now.

**October 08 2020:** Additional large Gitpod files (`core.mongo*` and `core.python*`) are now hidden in the Explorer, and have been added to the `.gitignore` by default.

**September 22 2020:** Gitpod occasionally creates large `core.Microsoft` files. These are now hidden in the Explorer. A `.gitignore` file has been created to make sure these files will not be committed, along with other common files.

**April 16 2020:** The template now automatically installs MySQL instead of relying on the Gitpod MySQL image. The message about a Python linter not being installed has been dealt with, and the set-up files are now hidden in the Gitpod file explorer.

**April 13 2020:** Added the _Prettier_ code beautifier extension instead of the code formatter built-in to Gitpod.

**February 2020:** The initialisation files now _do not_ auto-delete. They will remain in your project. You can safely ignore them. They just make sure that your workspace is configured correctly each time you open it. It will also prevent the Gitpod configuration popup from appearing.

**December 2019:** Added Eventyret's Bootstrap 4 extension. Type `!bscdn` in a HTML file to add the Bootstrap boilerplate. Check out the <a href="https://github.com/Eventyret/vscode-bcdn" target="_blank">README.md file at the official repo</a> for more options.

------

## FAQ about the uptime script

**Why have you added this script?**

It will help us to calculate how many running workspaces there are at any one time, which greatly helps us with cost and capacity planning. It will help us decide on the future direction of our cloud-based IDE strategy.

**How will this affect me?**

For everyday usage of Gitpod, it doesn’t have any effect at all. The script only captures the following data:

- An ID that is randomly generated each time the workspace is started.
- The current date and time
- The workspace status of “started” or “running”, which is sent every 5 minutes.

It is not possible for us or anyone else to trace the random ID back to an individual, and no personal data is being captured. It will not slow down the workspace or affect your work.

**So….?**

We want to tell you this so that we are being completely transparent about the data we collect and what we do with it.

**Can I opt out?**

Yes, you can. Since no personally identifiable information is being captured, we'd appreciate it if you let the script run; however if you are unhappy with the idea, simply run the following commands from the terminal window after creating the workspace, and this will remove the uptime script:

```
pkill uptime.sh
rm .vscode/uptime.sh
```

**Anything more?**

Yes! We'd strongly encourage you to look at the source code of the `uptime.sh` file so that you know what it's doing. As future software developers, it will be great practice to see how these shell scripts work.

---

Happy coding!


**steps to follow for this module**
in the terminal type: 
1)wget https://raw.githubusercontent.com/lerocha/chinook-database/master/ChinookDatabase/DataSources/Chinook_PostgreSql.sql (+pasteURLRawChinookLink)

2) launch Postgres CLI:
type:
set_pg
psql

3) to view or list and database in pur enviroment type:
\l

4) to create a new database using chinook:
type: CREATE DATABASE chinook;  
this will create another database, hit \l again to see its name chinook

5) If we needed to switch between databases, we can simply type \c (stands for connect )followed by the name
of the database we want to switch over to.
\c postgres 
type: \c chinook

6) Finally, while we're connected to our new chinook database, we need to initialize or
install the downloaded sample Chinook PostgreSQL database.
The \i generally means include, integrate, install, or initialize.
type: \i Chinook_PostgreSql.sql 

7) \q to quit

--------------------------------------------------------------------

'psql -d chinook' . This will start the server, and tell it that
the database we want to connect to is the one called "chinook", as declared by using the -d flag to specify a database name.

Next, we need to confirm that all tables and data were successfully added to the database.
'\dt' . This will allow us to display tables on our database.

First, let's start by retrieving all data from the Artist table.
type: SELECT * FROM "Artist";

Technically you don't need to write the SQL commands in capital letters, but it's standard
practice to distinguish between the different pieces of your query string.
The asterisk is a common programming method to signify a wildcard, which essentially means
to select anything and everything.
Also note, I've used double-quotes intentionally, because using single-quotes will throw a 'syntax error', 

type: q to return - NOT \q

Next, let's query the same table, but this time, only retrieve the "Name" column.
SELECT "Name" FROM "Artist";

For the next query, I will search the same table, but this time I am going to specify
a particular artist name using the WHERE clause.
SELECT * FROM "Artist" WHERE "Name" = 'Queen';

As you may have noticed, I've used double-quotes again, except when it comes to the specific
value I'd like to search for, which must be in single-quotes.
This is to distinguish between the various table and column names, versus the specific
context or value I need to find.

I'll perform the same exact query, but this time we'll specify the ArtistId of 51 instead of the artist name.
Since 51 is a primary key and integer, we don't need the single-quotes, but it will
still work if you include them.
SELECT * FROM "Artist" WHERE "ArtistId" = 51;

...now looking at the Album table
SELECT * FROM "Album" WHERE "ArtistId" = 51;

For our final sample query, I'm going to look within the table called "Track", and use the
column header of "Composer" to search for all tracks by Queen.
You can see that only 9 tracks are listed, all of which belong to the "Greatest Hits 2" album,
SELECT * FROM "Track" WHERE "Composer" = 'Queen';

In a real-world scenario, you should probably consider making the Composer column actually
be the ArtistId foreign key, to keep with the relational database schema.

-------------------------------------------------------------------------------
to create a json file or csv file from these tables, type:
\copy (SELECT * FROM "Track" WHERE "Composer" = 'Queen') TO 'test.csv' WITH CSV DELIMITER ',' HEADER;

\o test.json

SELECT json_agg(t) FROM (SELECT * FROM "Track" WHERE "Composer" = 'Queen') t;