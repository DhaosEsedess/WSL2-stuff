This is my little personal information into things I have done to resolve problems with WSL2

for errors with display :0 this is how I fixed it
sudo nano /etc/tmpfiles.d/wslg.conf
enter the contense of the file below then save and exit

#  This file is part of the debianisation of systemd.
#
#  systemd is free software; you can redistribute it and/or modify it
#  under the terms of the GNU General Public License as published by
#  the Free Software Foundation; either version 2 of the License, or
#  (at your option) any later version.

# See tmpfiles.d(5) for details

# Type Path           Mode UID  GID  Age Argument
L+     /tmp/.X11-unix -    -    -    -   /mnt/wslg/.X11-unix

after that return to PowerShell or command prompt and use the “wsl –shutdown” command then relaunch the WSL distro and you should have the display working again.
