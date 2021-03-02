This package is an example.
It does nothing else then printout the version of the template package.
The script will be install in $DESTDIR/usr/bin/ directory.

How to proceed:

## Open a terminal

## create a new repository root directory:
```bash
   mkdir NuTyX-packages
```
##  change to this directory
```bash
   cd NuTyX-packages
```
## clone this package:
```bash
   git clone https://github.com/NuTyX-packages/template.git
```
## Make sure you add the $PWD directory in your /etc/cards.conf as new repository directiory (in my example /hone/tnut/NuTyX-packages

```bash
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
```

### Notes that the global url is commented and a new url is specified for each remote repository.
