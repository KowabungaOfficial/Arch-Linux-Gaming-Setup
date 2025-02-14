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

1. Install LTS Kernel just in case (Here is a list of lts kernels: https://www.kernel.org/category/releases.html)
-----------------------------------------------------
- **Third Step**

**Install These (Enables CachyOS Kernel, ROCm Support, and Mesa Vulkan):**
1. yay -S linux-cachyos
2. yay -S opencl-amd
3. sudo pacman -S vulkan-mesa-layers lib32-vulkan-mesa-layers
-----------------------------------------------------
- **Fourth Step**

**Enabling Arch Update addon:**
1. sudo pacman -S --needed pacman-contrib archlinux-contrib curl fakeroot htmlq diffutils hicolor-icon-theme python python-pyqt6 qt6-svg glib2
2. yay -S arch-update
-----------------------------------------------------
- **Final Step**

1. Use performance mode in KDE power settings, fixes some issues.
-----------------------------------------------------

<div align="center"><b>Needed Packages (Includes personal Gaming and other Packages as well)</b></div>

-----------------------------------------------------
<div align="center"><b>AppImages (AppImageLauncher)</b></div>
Goverlay Beta (AppImage Beta, more up to date): https://github.com/benjamimgois/goverlay/releases

Wemod: https://github.com/DeckCheatz/wemod-launcher

-----------------------------------------------------

<div align="center"><b>Official Arch Repo (Pacman)</b></div>

1. sudo pacman -S appimagelauncher corectrl vlc phonon-qt5-vlc phonon-qt6-vlc steam mission-center winetricks pince-git
2. sudo pacman -S gamescope mangohud lib32-mangohud inputplumber fastfetch tk libdecor lib32-libdecor kio-admin prismlauncher
3. sudo pacman -S python-pip python-pipx python-setuptools python-virtualenv scx-scheds gstreamer lib32-gstreamer wine-staging wlroots
4. sudo pacman -S alsa-plugins lib32-alsa-plugins giflib lib32-giflib glfw python-glfw gst-plugins-base-libs lib32-gst-plugins-base-libs
5. sudo pacman -S lib32-gtk3 lib32-libjpeg-turbo ocl-icd lib32-ocl-icd openal lib32-openal libjpeg-turbo libva lib32-libva libxslt lib32-libxslt
6. sudo pacman -S mpg123 lib32-mpg123 ttf-liberation vulkan-tools gamemode lib32-gamemode fontconfig lib32-fontconfig gst-plugin-pipewire
7. sudo pacman -S gst-plugin-va gst-plugins-base lib32-gst-plugins-base gst-plugins-good lib32-gst-plugins-good wine-mono

-----------------------------------------------------

**Notes For Myself:**
**(figure out if this is already included when using ArchInstall) xorg-xwayland, gwenview, partitionmanager, amd-ucode, mesa, lib32-mesa**

**ALSO CHECK TO SEE WHAT NEEDS TO BE INSTALLED ON THE AMD SIDE WHEN USING ARCHINSTALL**

-----------------------------------------------------

<div align="center"><b>AUR (Yay)</b></div>

1. yay -S librewolf-bin mullvad-vpn-bin heroic-games-launcher-bin jdownloader2 protonplus rustdesk-bin xpadneo-dkms protontricks

-----------------------------------------------------

<div align="center"><b>Fixes Section</b></div>

- Dualsense Controller Acting as a mouse (In KDE, but might work with other Desktop Enivronments):

Go to “Input & Output” in settings then clicked the tab “Mouse & Touchpad”. 
Select “Touchpad” and uncheck the box beside “Device enabled” at the top. 

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
