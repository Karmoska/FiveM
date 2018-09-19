# SERVER ADMINISTRATION

##Running FXServer

```
FXServer is the name of the current 
CitizenFX server version. This page shows you how to run it.
```

##Running from Build Artifacts 

###Windows

```
Make sure you have installed a newer Visual C++ redistributable, 2017 is fine ( direct link to the 2017 setup https://go.microsoft.com/fwlink/?LinkId=746572 )
Create a new folder (for example D:\FXServer).
Download the latest master branch build for Windows from the artifacts server.
Extract the build.
* Use any archiving tool (such as WinRAR or 7-Zip).
Clone cfx-server-data in a new folder (other than your FXServer folder).
* git clone https://github.com/citizenfx/cfx-server-data.git server-data
Make a server.cfg in your server-data folder. You need to copy the example cfg below into the file.
Run the server from the server-data folder. (cd /d D:\FXServer\server-data)
* D:\FXServer\run.cmd +exec server.cfg (from a new cmd window)
Generate a license code from https://keymaster.fivem.net and register for an account.
```

###Linux
```
Create a new folder (for example mkdir /home/username/server).
Download the latest master branch build for Linux from the artifacts server (copy the URL for the latest server version and use wget <url> to download it).
Extract the build using cd path/to/server/folder && tar xf fx.tar.xz (you need to have xz installed, on Debian/Ubuntu this is in the xz-utils package).
Clone cfx-server-data in a new folder (other than your FXServer folder).
* For example git clone https://github.com/citizenfx/cfx-server-data.git /home/username/server-data
Make a server.cfg file in your server-data folder (copy the example server.cfg file below into that file).
Run the server from the server-data folder.
* bash /home/username/server/run.sh +exec server.cfg
Generate a license code from https://keymaster.fivem.net and register for an account.
```

###Troubleshooting
```
If you don’t get any ‘resources found’, and it says ‘Failed to start resource’, you didn’t ‘cd’ to the right folder.
If you get a lot of errors about citizen:/scripting/, you didn’t use run.cmd.
If nothing happens at all except ‘sending heartbeat’, you didn’t use run.cmd and failed to cd to the folder.
If no resources get started, and you can’t connect, you didn’t add +exec.
Mono errors on startup (SIGSEGV, exception stack trace) are perfectly fine, and don’t signify any error condition.
If you get ‘Couldn’t load resource sessionmanager’, then input restart sessionmanager into the console input. This is a temporary workaround, and only happens after the cache was initially generated.
```