This package is an example.
It does nothing else then printout the version of the template package.
The script will be install in $DESTDIR/usr/bin/ directory.

How to proceed:

1/ Open a terminal

2/ create a new repository root directory:

   mkdir NuTyX-packages

3/  change to this directory

   cd NuTyX-packages

4/ clone this package:

   git clone https://github.com/NuTyX-packages/template.git

5/ Make sure you add the $PWD directory in your /etc/cards.conf as new repository directiory (in my example /hone/tnut/NuTyX-packages

# No global url should be defined
# We need to specify an url only for remote repositories collection
#
# Default server URL
# url http://downloads.nutyx.org
#
# My own repository (this repository) without specified url 
dir /home/tnut/NuTyX-packages
#
## For all the main desktops (KDE,XFCE,LXDE,MATE)
# Comment following line
# If you don't want to install any of those interfaces
#
dir /var/lib/pkg/depot/desktops
#
## For all the graphical applications
dir /var/lib/pkg/depot/gui-extra|http://downloads.nutyx.org
#
## For a minimal graphical interface
dir /var/lib/pkg/depot/gui|http://downloads.nutyx.org
#
## For all the console applications
dir /var/lib/pkg/depot/cli-extra|http://downloads.nutyx.org
#
## For a minimal console interface
dir /var/lib/pkg/depot/cli|http://downloads.nutyx.org
#
## Chroot system without reboot possibilities for a chroot
dir /var/lib/pkg/depot/base|http://downloads.nutyx.org
#
## Normaly you want to keep base and
base ${DEPOT}/base
#
#
## If you want to keep more collections remove comments below
# Adjust to your needs
#
# base /var/lib/pkg/depot/cli
# base /var/lib/pkg/depot/cli-extra
# base /var/lib/pkg/depot//gui
# base /var/lib/pkg/depot/gui-extra
# base /var/lib/pkg/depot/...

6/ Notes that the global url is commented and a new url is specified for each remote repository.
