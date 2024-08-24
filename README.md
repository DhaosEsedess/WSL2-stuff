This is my little personal information into things I have done to resolve problems with WSL2

for errors with display :0 this is the fix i used
download /WSL2/wslg.conf and place it in /etc/tmpfiles.d/
after that return to PowerShell or command prompt and use the “wsl –shutdown” command then relaunch the WSL distro and you should have the display working again.
