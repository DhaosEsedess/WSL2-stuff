setting up WSL2

make sure Systemd is working

sudo nano /etc/wsl.conf
add this to the top of the file

[boot]
systemd=true

save and exit

to prevent problems with WSLg

sudo nano /etc/tmpfiles.d/wslg.conf
add this to the fiels contents

#  This file is part of the debianisation of systemd.
#
#  systemd is free software; you can redistribute it and/or modify it
#  under the terms of the GNU General Public License as published by
#  the Free Software Foundation; either version 2 of the License, or
#  (at your option) any later version.

# See tmpfiles.d(5) for details

# Type Path           Mode UID  GID  Age Argument
L+     /tmp/.X11-unix -    -    -    -   /mnt/wslg/.X11-unix

save and exit

to prevent windows programs not working with WSLInterop

sudo nano /usr/lib/binfmt.d/WSLInterop.conf
add this to the file contents

:WSLInterop:M::MZ::/init:PF

save and exit

make sure to use the wsl --shutdown command and restart the distro after the files are edited

I will have intructions con compiling the windows linux 6.6 kernal once i figure out how to make it work with kvm after compile
