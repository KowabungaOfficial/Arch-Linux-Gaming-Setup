# <img style="width: 52px; height: 52px;" src="https://kowabungaofficial.github.io/Arch-Linux-Gaming-Setup/ArchLinuxLogo.png"> Arch Linux Gaming Setup

# Work in progress! Currently moving to Arch.


**IMPORTANT: RUN THESE FIRST ON SYSTEM STARTUP (Booting into KDE)**

-----------------------------------------------------
- **Main Step**

**Enabling use of AUR:**
1. sudo pacman -Syu
2. sudo pacman -S --needed base-devel git
3. git clone https://aur.archlinux.org/yay.git
4. cd yay
5. makepkg -si
-----------------------------------------------------
- **Second Step**

1. sudo pacman -S linux-lts linux-lts-headers
-----------------------------------------------------
- **Third Step**

**Install These (Enables CachyOS Kernel and Mesa Layers):**
1. yay -S linux-cachyos linux-cachyos-headers
2. sudo pacman -S vulkan-mesa-layers lib32-vulkan-mesa-layers
-----------------------------------------------------
- **Fourth Step**

**Enabling Arch Update addon:**
1. sudo pacman -S --needed pacman-contrib archlinux-contrib curl fakeroot htmlq diffutils hicolor-icon-theme python python-pyqt6 qt6-svg glib2
2. yay -S arch-update
-----------------------------------------------------
- **Final Step**

1. Use performance mode in KDE power settings, fixes some issues.
-----------------------------------------------------

<div align="center"><b>Gaming Packages</b></div>

-----------------------------------------------------

<div align="center"><b>Official Arch Repo (Pacman)</b></div>

1. sudo pacman -S amd-ucode steam wine-staging winetricks wine-mono goverlay gamescope mangohud lib32-mangohud inputplumber tk libdecor lib32-libdecor scx-scheds wlroots python-pip python-pipx
2. sudo pacman -S jre-openjdk jre-openjdk-headless jre21-openjdk jre21-openjdk-headless jre11-openjdk jre11-openjdk-headless gstreamer lib32-gstreamer gst-plugin-va gst-plugins-base lib32-gst-plugins-base
3. sudo pacman -S gst-plugins-good lib32-gst-plugins-good gst-plugin-pipewire fontconfig lib32-fontconfig mpg123 lib32-mpg123 ttf-liberation vulkan-tools gamemode lib32-gamemode libva lib32-libva
4. sudo pacman -S libxslt lib32-libxslt lib32-gtk3 lib32-libjpeg-turbo ocl-icd lib32-ocl-icd openal lib32-openal libjpeg-turbo alsa-plugins lib32-alsa-plugins giflib lib32-giflib glfw python-glfw
5. sudo pacman -S gst-plugins-base-libs lib32-gst-plugins-base-libs python-setuptools python-virtualenv

-----------------------------------------------------

**Notes For Myself:**
**(figure out if this is already included when using ArchInstall) xorg-xwayland, lib32-mesa**

**ALSO CHECK TO SEE WHAT NEEDS TO BE INSTALLED ON THE AMD SIDE WHEN USING ARCHINSTALL**

wemodlauncher later

For inspiration: https://youtu.be/xTqOKMJdP5c https://youtu.be/r6SUBZAO5SM https://youtu.be/d3KfkKXRDzk

add driving wheel drivers: https://youtu.be/HKaB5fAucTU

-----------------------------------------------------

<div align="center"><b>AUR (Yay)</b></div>

1. yay -S heroic-games-launcher-bin protonplus xpadneo-dkms protontricks vkbasalt lib32-vkbasalt

-----------------------------------------------------

<div align="center"><b>Fixes Section</b></div>

- Dualsense Controller Acting as a mouse (In KDE, but might work with other Desktop Enivronments):

Go to “Input & Output” in settings then clicked the tab “Mouse & Touchpad”. 
Select “Touchpad” and uncheck the box beside “Device enabled” at the top. 

-----------------------------------------------------

<div align="center"><b>Optional Section (Mostly Packages I Use)</b></div>

- Pacman

sudo pacman -S vlc phonon-qt5-vlc phonon-qt6-vlc corectrl mission-center pince-git fastfetch kio-admin prismlauncher gwenview partitionmanager

- Yay

yay -S librewolf-bin mullvad-vpn-bin jdownloader2 rustdesk-bin

- Other

https://github.com/DeckCheatz/wemod-launcher
-----------------------------------------------------
<div align="center"><b>SPECIAL THANKS TO:</b></div>

<div align="center">CachyOS Dev Team 
  
  https://cachyos.org/
</b></div>  
<div align="center">Nobara (Thomas Crider)

https://nobaraproject.org/
</b></div>

<div align="center">Brodie Robertson

https://www.youtube.com/channel/UCld68syR8Wi-GY_n4CaoJGA

https://brodierobertson.xyz
</b></div>
