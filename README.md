# ACServerManager
Web based server manager for Assetto Corsa directly manipulating the ini files on the server as an alternative to the windows app and having to copy files to your server.

Start and stop the server, stracker and MinoRating directly from the application, meaning you can make changes to the server configuration and restart the server directly from your browser or mobile phone.

##Installation
###Prep
The application needs some additional files added to the server/content/tracks and server/content/cars folders to be able to choose track configurations and car skins.

Copy acServerManager.bat to your root aessettocorsa folder and run it to copy the required folders into server/content/*. You'll then need to copy the content folder to your server.

For tracks it will copy the ui folder which will contain sub folders when there are multiple track configurations. It will also copy the contents of these directories which contains additional track information which is displayed when choosing a track.

For cars it will copy the skins/* folder structure but not the files; this is just to be able to choose the skin when setting up the entry list.

###NodeJS
Download and install NodeJS and your server from https://nodejs.org/

###Web Application
Copy the web application to your server, it doesn't matter where you choose to put it.

###Configuration
Open settings.js and set the correct values for your setup:
- serverPath: The path to your server folder containing acServer.exe
- sTrackerPath: The path to your stracker folder container stracker.exe (If you don't run stracker just leave this as an empty string ('') to disable it
- minoRatingPath: The path to your MinoRating folder container MinoRatingPlugin.exe (If you don't run MinoRatingPlugin just leave this as an empty string ('') to disable it. Note that you can use MinoRatingPlugin AND sTracker if you will use sTrackers UDP Proy function (see sTracker manuall to set this up). 
- username/password: Set these values if you want basic authentication on the application
- port: The port that the application will listen on (Be sure to open up this port on firewalls)

##Usage
- Run start.bat
- Browse to the application using your servers public IP and the chosen port (or any DNS configured)
- Click the Start button under Assetto Corsa Server section
- If using sTracker wait until the AC server has started and the click Start in the sTracker Server section

The server will now be running. You'll be able to see any server output in the command window and it will be logged to a file in the AcServerManager folder.

You can change any setting and it will be applied directly to server_cfg.ini and entry_list.ini on the server. After making a change just stop and start the server from the Server Status page.

##Screenshots
###Server Status
![Server Status](http://www.burnoutcrew.de/wp-content/uploads/2017/06/ServerStatus.png)

###Server Configuration
![Server Config](http://www.yeahyou.com/ACServerManager/server-config.jpg)

###Entry List
![Server Config](http://www.yeahyou.com/ACServerManager/entry-list.jpg)

###Rules
![Server Config](http://www.yeahyou.com/ACServerManager/rules.jpg)

###Advanced
![Server Config](http://www.yeahyou.com/ACServerManager/advanced.jpg)
