# linux-fun-setup
Settings up Linux and remembering everything can be an hassle for me, this will try to keep track of everything with it. 


## Initial setup
- SSD on "/"
- HDD on "/HDD"

### Specifics for HDD
```sh
mkdir -p /HDD/home/etienne
mkdir -p /HDD/SteamLibrary
chmod -R 755 /HDD
chown etienne:etienne /HDD/home/etienne
chown etienne:etienne /HDD/SteamLibrary
```

### Symbolics links on HDD
```sh
mkdir -p /HDD/home/etienne/Desktop; ln -s /HDD/home/etienne/Desktop /home/etienne
mkdir -p /HDD/home/etienne/Documents; ln -s /HDD/home/etienne/Documents /home/etienne
mkdir -p /HDD/home/etienne/Downloads; ln -s /HDD/home/etienne/Downloads /home/etienne
mkdir -p /HDD/home/etienne/Music; ln -s /HDD/home/etienne/Music /home/etienne
mkdir -p /HDD/home/etienne/Pictures; ln -s /HDD/home/etienne/Pictures /home/etienne
mkdir -p /HDD/home/etienne/Public; ln -s /HDD/home/etienne/Public /home/etienne
mkdir -p /HDD/home/etienne/Template; ln -s /HDD/home/etienne/Template /home/etienne
mkdir -p /HDD/home/etienne/Videos; ln -s /HDD/home/etienne/Videos /home/etienne
```

### Fixed Login screen on external monitor
Considering the initial monitors setup is done in user-session.
```sh
`sudo cp ~/.config/monitors.xml ~gdm/.config/monitors.xml`
```

## Installed extensions
- Dash to panel


## Installed software
- Spotify
- Steam
- Edge
- Discord
- Lutris
- vim

### Spotify
Disable "Show desktop notifications when the song changes" in settings

### Steam
Setup an alternative download location to /HDD/SteamLibrary

### Lutris
#### Overwatch
Add the follow game env variable :
VK_ICD_FILENAMES=/usr/share/vulkan/icd.d/nvidia_icd.json


### Edge
#### Fonts
- Standard font: Serif
- Serif font: DejaVu Serif
- Sans-serif font: DejaVu Sans
- Fixed-width font: DejaVu Sans Mono


## Configs files
### ~/.bashrc
`alias ulogout='/usr/bin/gnome-session-quit --no-prompt'`

## TROUBLESHOOT
### Laptop screen going black
`sudo rm /etc/X11/xorg.conf`
