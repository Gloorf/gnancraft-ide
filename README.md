This code was an experiment that I used to let my kids and my brother
edit ScriptCraft files on our Bukkit (Minecraft) server. I'm pushing
it out in case it's a useful starting point for others.

WARNING: this code was experimental, so there might be security issues
here. I'm making no claims about dogs being held hostage by
aliens. Just mentioning it.


Installing and running 
----------------------
Playing around with it should be fairly simple. 

* First, you need to edit create_auth.py to add user names and passwords. 
* Then you need to run create_auth.py to set up authentication. 
* Create players directory (or an other dir to store all players script)
* Create one or two player dir
* Then run `SRCDIR=players main.py`

Using it should simply be a matter of pointing your editor to one of these: 

   [http://localhost:8095/edit/](http://localhost:8095/edit/)

   To edit the files in the jsfiles directory. 

or 

   [http://localhost:8095/logfile](http://localhost:8095/logfile)

   To inspect the logfile from the server. 

To use it with a live Minecraft server, do the following: 

* Replace the file called mcserver.log with a symbolic link to the Minecraft server's logfile.
* Modify JSDIR in main.py to point to the directory with files you want to edit. 


Backups
-------
The editor automatically creates a backup of the edited file every time you press save. The backups are 
saved in "backups" (defined in main.py). 

Ace
--- 

This version uses a CDN version of ace. If you want to host it locally, 
you can add it to content/ace and edit content/templates/editfile_ace.html 
and point to /edit/ace/ace.js instead of the CDN version. 


