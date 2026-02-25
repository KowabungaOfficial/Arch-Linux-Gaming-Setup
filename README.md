# <img style="width: 52px; height: 52px;" src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/logos/ArchLinuxLogo.png"> Arch Linux Gaming Setup

> [!IMPORTANT]
> Run These When Booting Into Desktop Environment (i.e. KDE)
> 
> (I Don't Include Feral Gamemode Because Of Performance Related Issues. i.e. Stutters & FPS Loss In Some Games)

-----------------------------------------------------
- **Main Step**

**Enabling use of AUR:**
1. `sudo pacman -Syu`
2. `sudo pacman -S --needed base-devel git`
3. `git clone https://aur.archlinux.org/yay.git`
4. `cd yay`
5. `makepkg -si`
-----------------------------------------------------
- **Second Step (Backup Kernels)**

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
- **Fourth Step (No Password Automount HDD's/SSD's)**

>For when you have multiple game drives or other drives

1. Run this in your ternminal: `lsblk -f`
2. open fstab file located in etc folder
3. In the console take note of the UUID of your drive in "UUID" section, and where your drives are mounted in the "MOUNTPOINTS" section, and the Format type in "FSTYPE"
4. open fstab file located in etc folder
5. As for # add it and you can name it to whatever you want to indentify the drive
6. See example bellow to see what it will look like

Example:

<img style="" src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/misc/AUTOMOUNTDRIVE.png">

-----------------------------------------------------

- **Final Step**

1. Edit pacman.conf in `/etc/`
2. Find the [multilib] section and remove the # from the two lines:
```
[multilib]
Include = /etc/pacman.d/mirrorlist
```
>(Optional Section) 

[Enables Color and Pacman Video Game Loading/Downloading Bar In Terminal]

3. In Misc options section remove # before color
4. Add ILoveCandy after CheckSpace

-----------------------------------------------------
<div align="center"><b>Gaming Packages</b></div>

-----------------------------------------------------

<div align="center"><b>Official Arch Repo (Pacman)</b></div>

1. `sudo pacman -S zlib-ng zlib-ng-compat amd-ucode steam wine-staging winetricks wine-mono wine-gecko wine-nine goverlay gamescope mangohud lib32-mangohud inputplumber tk libdecor lib32-libdecor scx-scheds python-pip python-pipx`
2. `sudo pacman -S jre-openjdk gstreamer lib32-gstreamer gst-plugin-va gst-plugins-base lib32-gst-plugins-base ffmpeg`
3. `sudo pacman -S gst-plugins-good lib32-gst-plugins-good gst-plugin-pipewire fontconfig lib32-fontconfig mpg123 lib32-mpg123 ttf-liberation vulkan-tools libva lib32-libva`
4. `sudo pacman -S libxslt lib32-libxslt lib32-gtk3 ocl-icd lib32-ocl-icd openal lib32-openal libjpeg-turbo lib32-libjpeg-turbo alsa-plugins lib32-alsa-plugins giflib lib32-giflib glfw lib32-pipewire`
5. `sudo pacman -S gst-plugins-base-libs lib32-gst-plugins-base-libs python-setuptools python-virtualenv lib32-mesa dosfstools dolphin-plugins unrar 7zip gst-plugins-bad adobe-source-han-sans-jp-fonts adobe-source-han-sans-cn-fonts adobe-source-han-sans-hk-fonts`
6. `sudo pacman -S adobe-source-han-sans-kr-fonts adobe-source-han-sans-otc-fonts adobe-source-han-sans-tw-fonts adobe-source-sans-fonts ttf-nerd-fonts-symbols ttf-nerd-fonts-symbols-common ttf-nerd-fonts-symbols-mono ffmpegthumbs kdegraphics-thumbnailers` 

-----------------------------------------------------

**Install and Enable Bluetooth:**

1. `sudo pacman -S bluedevil bluez bluez-utils qt6-connectivity`
2. `sudo systemctl enable bluetooth.service`
3. `sudo systemctl start bluetooth.service`

-----------------------------------------------------

<div align="center"><b>AUR (Yay)</b></div>

1. `yay -S heroic-games-launcher-bin protonplus xpadneo-dkms vkpost lib32-vkpost faudio python-glfw ttf-ms-fonts`

-----------------------------------------------------

<div align="center"><b>Fixes Section</b></div>

- Dualsense Controller Acting as a mouse (In KDE, but might work with other Desktop Enivronments):

Go to “Input & Output” in settings then clicked the tab “Mouse & Touchpad”. 
Select “Touchpad” and uncheck the box beside “Device enabled” at the top. 

-----------------------------------------------------

<div align="center"><b>Optional Section (Mostly Packages I Use)</b></div>

- **Pacman**

1. `sudo pacman -S android-tools mpv vlc phonon-qt6-vlc corectrl mission-center fastfetch kio-admin prismlauncher gwenview partitionmanager qbittorrent`

2. `sudo pacman -S --needed sof-firmware alsa-firmware alsa-utils pipewire pipewire-alsa pipewire-pulse pipewire-jack wireplumber plasma-pa pavucontrol linux-firmware`

3 (Laptops Only). `sudo pacman cups cups-pdf system-config-printer avahi nss-mdns hplip gutenprint foomatic-db foomatic-db-ppds foomatic-db-nonfree foomatic-db-nonfree-ppds foomatic-db-engine foomatic-db-gutenprint-ppds splix cups-filters ghostscript gsfonts ipp-usb power-profiles-daemon`

**Enabling Arch Update addon:**
1. `sudo pacman -S --needed pacman-contrib archlinux-contrib curl fakeroot htmlq diffutils hicolor-icon-theme python python-pyqt6 qt6-svg glib2`
2. `yay -S arch-update`
3. `arch-update --tray --enable`

- **Yay**

1. `yay -S mullvad-vpn-bin jdownloader2 rustdesk-bin floorp-bin harmony2`
   
2 (Laptops Only). `yay -S alsa-ucm-conf-git epson-inkjet-printer-escpr epson-inkjet-printer-escpr2 cnijfilter2 brother-dcp7065dn brother-hll2340dw brother-mfc7360n brother-dcp1610w brother-hl1210w`

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
