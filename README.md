TinyIB - A Lightweight and Efficient [Image Board](http://en.wikipedia.org/wiki/Imageboard) Script
====

**Got database? Get speed.**  Use [MySQL](http://mysql.com) or [SQLite](http://sqlite.org) for an efficient set-up able to handle high amounts of traffic.

**No database?  No problem.**  Store posts as text files for a portable set-up capable of running on virtually any PHP host.

For demos see [example installations](https://github.com/tslocum/TinyIB/wiki).

Features
------------
 - Reference links >>###
 - Delete post via password.
 - Management panel:
   - Administrators and moderators use separate passwords.
     - Moderators are only able to delete posts.
   - Ban offensive/abusive posters across all boards.
   - Post using raw HTML.

Installing
------------

 1. Verify the following requirements are met:
    - [PHP](http://php.net) 4 or higher is installed.
    - [GD Image Processing Library](http://php.net/gd) is installed.
      - This library is installed by default on most hosts.
 2. CD to the directory you wish to install TinyIB.
 3. Run the command:
    - `git clone git://github.com/tslocum/TinyIB.git ./`
 4. Copy **settings.default.php** to **settings.php**
 5. Configure **settings.php**
 6. [CHMOD](http://en.wikipedia.org/wiki/Chmod) write permissions to these directories:
    - ./ (the directory containing TinyIB)
    - ./src/
    - ./thumb/
    - ./res/
    - ./inc/flatfile/ (only if you use flat file for the database)
 7. Navigate your browser to **imgboard.php** and the following will take place:
    - The database structure will be created.
    - Directories will be verified to be writable.
    - The file index.html will be created containing the new image board.

Updating
------------

 1. Run the command:
    - `git pull`
 2. If TinyIB has been updated, note which files are modified.
    - If **settings.default.php** is updated, migrate the changes to **settings.php**
      - Take care to not change the value of **TINYIB_TRIPSEED**, as it would result in different secure tripcodes.
    - If other files are updated, and you have made changes yourself, review the modifications ensuring they do not interfere with yours.
      - Visit GitHub and select the relevant update commit(s) to review what changes were made.

Support
------------

Contact tslocum@gmail.com

Contributing
------------

 1. Read the [GitHub Forking Guide](http://help.github.com/forking/).
 2. Fork TinyIB.
 3. Commit code changes to your forked repository.
 4. Submit a pull request describing your modifications.
