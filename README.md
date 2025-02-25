# <img style="width: 52px; height: 52px;" src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/logos/ArchLinuxLogo.png"> Arch Linux Gaming Setup

> [!IMPORTANT]
> Run These When Booting Into Desktop Environment (i.e. KDE)

-----------------------------------------------------
- **Main Step**

**Enabling use of AUR:**
1. `sudo pacman -Syu`
2. `sudo pacman -S --needed base-devel git`
3. `git clone https://aur.archlinux.org/yay.git`
4. `cd yay`
5. `makepkg -si`
-----------------------------------------------------
- **Second Step**

1. `sudo pacman -S linux-lts linux-lts-headers`
-----------------------------------------------------
- **Third Step**

**Install These (Enables CachyOS Kernel and Mesa Layers):**
1. `yay -S linux-cachyos linux-cachyos-headers`
2. `sudo pacman -S vulkan-mesa-layers lib32-vulkan-mesa-layers`

**CachyOS Kernel Setup Guide:**
1. Go to _/boot/loader/entries/_ and find the default linux.conf, not the fallback one.
2. Copy that file and paste it on your desktop
3. Now edit the name to arch-cachyos.conf
4. Edit it to look like this (KEEP EVERYTHING THE SAME AFTER "initrd" SECTION!):
```
title   Arch Linux (CachyOS)
linux   /vmlinuz-linux-cachyos
initrd  /initramfs-linux-cachyos.img
```
5. Now copy arch-cachy.conf to _/boot/loader/entries/_
-----------------------------------------------------
- **Fourth Step**

**Set CachyOS Kernel As Default:**
1. Go to _/boot/loader/_ and open loader.conf then edit timeout 3 to this (waits 5 seconds before booting kernel):

`timeout 5`

2. Add this before the timeout 5 line:

`default arch-cachyos.conf`

-----------------------------------------------------
- **Final Step (No Password Automount HDD's/SSD's)**

>For when you have multiple game drives or other drives

1. Run this in your ternminal: `lsblk -f`
2. open fstab file located in etc folder
4. Look at UUID of your drive in "UUID" section, where your drives are mounted "MOUNTPOINTS" section, Format type in "FSTYPE"
5. As for # add it and you can name it to whatever you want to indentify the drive
6. See example bellow to see what it will look like

Example:

<img style="" src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/misc/AUTOMOUNTDRIVE.png">

-----------------------------------------------------

<div align="center"><b>Gaming Packages</b></div>

-----------------------------------------------------

<div align="center"><b>Official Arch Repo (Pacman)</b></div>

1. `sudo pacman -S zlib-ng zlib-ng-compat amd-ucode steam wine-staging winetricks wine-mono goverlay gamescope mangohud lib32-mangohud inputplumber tk libdecor lib32-libdecor scx-scheds python-pip python-pipx`
2. `sudo pacman -S jre-openjdk gstreamer lib32-gstreamer gst-plugin-va gst-plugins-base lib32-gst-plugins-base ffmpeg`
3. `sudo pacman -S gst-plugins-good lib32-gst-plugins-good gst-plugin-pipewire fontconfig lib32-fontconfig mpg123 lib32-mpg123 ttf-liberation vulkan-tools gamemode lib32-gamemode libva lib32-libva`
4. `sudo pacman -S libxslt lib32-libxslt lib32-gtk3 ocl-icd lib32-ocl-icd openal lib32-openal libjpeg-turbo lib32-libjpeg-turbo alsa-plugins lib32-alsa-plugins giflib lib32-giflib glfw python-glfw`
5. `sudo pacman -S gst-plugins-base-libs lib32-gst-plugins-base-libs python-setuptools python-virtualenv lib32-mesa dosfstools dolphin-plugins unrar 7zip gst-plugins-bad adobe-source-han-sans-jp-fonts adobe-source-han-sans-cn-fonts adobe-source-han-sans-hk-fonts`
6. `sudo pacman -S adobe-source-han-sans-kr-fonts adobe-source-han-sans-otc-fonts adobe-source-han-sans-tw-fonts adobe-source-sans-fonts ttf-nerd-fonts-symbols ttf-nerd-fonts-symbols-common ttf-nerd-fonts-symbols-mono` 

-----------------------------------------------------

**Install and Enable Bluetooth:**

1. `sudo pacman -S bluedevil bluez bluez-utils qt5-connectivity qt6-connectivity`
2. `sudo systemctl enable bluetooth.service`
3. `sudo systemctl start bluetooth.service`

-----------------------------------------------------

<div align="center"><b>AUR (Yay)</b></div>

1. `yay -S heroic-games-launcher-bin protonplus xpadneo-dkms vkbasalt lib32-vkbasalt faudio`

-----------------------------------------------------

<div align="center"><b>Fixes Section</b></div>

- Dualsense Controller Acting as a mouse (In KDE, but might work with other Desktop Enivronments):

Go to “Input & Output” in settings then clicked the tab “Mouse & Touchpad”. 
Select “Touchpad” and uncheck the box beside “Device enabled” at the top. 

-----------------------------------------------------

<div align="center"><b>Optional Section (Mostly Packages I Use)</b></div>

- **Pacman**

1. `sudo pacman -S vlc phonon-qt5-vlc phonon-qt6-vlc corectrl mission-center fastfetch kio-admin prismlauncher gwenview partitionmanager qbittorrent`

**Enabling Arch Update addon:**
1. `sudo pacman -S --needed pacman-contrib archlinux-contrib curl fakeroot htmlq diffutils hicolor-icon-theme python python-pyqt6 qt6-svg glib2`
2. `yay -S arch-update`
3. `arch-update --tray --enable`

- **Yay**

1. `yay -S librewolf-bin mullvad-vpn-bin jdownloader2 rustdesk-bin pince`

- **Other**

https://github.com/DeckCheatz/wemod-launcher
<br> <br> <br>
## <div align="center"><b>SPECIAL THANKS TO:</b></div>


<div align="center">
   <img src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/logos/cachyoslogo.png" style="vertical-align: middle; margin-right: 0px; height: 30px;">
<b>CachyOS Dev Team</b>
  
https://cachyos.org/
</b></div>  
<div align="center">
<img src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/logos/nobaralogo.png" style="vertical-align: middle; margin-right: 0px; height: 25px;">
<b>Nobara (Thomas Crider)</b>

https://nobaraproject.org/
</b></div>

<div align="center">
<img src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/logos/brodierobertsonlogo.png" style="vertical-align: middle; margin-right: 0px; height: 30px;">
<b>Brodie Robertson</b>

https://www.youtube.com/channel/UCld68syR8Wi-GY_n4CaoJGA

https://brodierobertson.xyz
</b></div>
<div align="center">
<img src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/logos/archupdatelogo.png" style="vertical-align: middle; margin-right: 0px; height: 27px;">
<b>Robin Candau (Antiz96)</b> 

https://antiz.fr/

https://github.com/Antiz96
</b></div>
