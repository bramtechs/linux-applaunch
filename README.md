# linux-applaunch 

AppLaunch is a simple bash script that launches the selected Flatpak from a dmenu window. 
This script is ideal for Window Managers like i3 that don't deal with .desktop files or application menu-launchers.

## Installation

1) Install [Flatpak](https://flatpak.org/setup/) for your distro.

2) Install [dmenu](https://tools.suckless.org/dmenu/) (Debian)
```console
sudo apt install suckless-tools 
```
3) Download and install the script
```console
sudo wget -O /usr/local/bin/applaunch "[github link]" && \
sudo chmod +x /usr/local/bin/applaunch
```
4) (Optional) Add a shortcut to your i3 config.
```
...
bindsym $mod+Shift+d exec --no-startup-id dmenu_run
...
```
The menu will show by pressing WIN/ALT + Shift + d.

## Deinstallation
```console
sudo rm /usr/local/bin/applaunch
```

## Usage
```console
applaunch
```

## TODO
- [ ] Check if Flatpak is actually installed before running.
- [ ] Show Snap packages if available.
- [ ] Show AppImages placed in a configured folder.
