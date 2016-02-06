# tv_show
####Help to browse and watch your TV shows from command line.

The command "tv" displays all episodes.

The command "tv -u" displays only episodes that are unwatched.

The command "tv -name" or "tv --name" followed by the keyword can be used to display tv shows having having that keyword

* Make tv.sh an executable using chmod command.
* Create an alias for "sh /path/to/tv.sh" and you are good to go to use tv.sh from any location on terminal.

### Requirements:
* vlc media player
* Linux OS
* git

### Installation:
* Copy the https URL given for this repository
* Open terminal and type "git clone copied_url"

### While running program for first time
* You need to specify the path to your TV shows directory.
* The format must be: TV show name(directory) -> Season number(directory) -> episodes(media files)
* There should not be an extra directory between episodes and Season Number. e.g: The following path won't work
  TvShow/Show_name/Show_season/Extra_directory/episode.mp4

#### If your tv shows are on the other device which is connected to your LAN and has ssh server running
* You need to install sshfs utility. To install sshfs, type
  "apt-get install sshfs" on the terminal
* You need to uncomment a few lines from the code and enter appropriate details according to your device.
* You need to create a mount point to mount it virtually. The command sshfs is used to mount virtually.
* For example: If your remote device is a raspberry pi with ip "192.168.1.101" and username "pi", then the complete command can look like this(example): sshfs pi@192.168.1.101:"/media/pi/MY_HD/TV_shows/" "/mount_point/"
* Don't forget to save after this.
* You need to run the command using sudo, hence create alias accordingly.

#### For more help, you can use "tv.sh -h" command.

