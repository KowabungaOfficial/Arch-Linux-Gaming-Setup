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

For inspiration: https://youtu.be/xTqOKMJdP5c https://youtu.be/r6SUBZAO5SM https://youtu.be/d3KfkKXRDzk

add driving wheel drivers: https://youtu.be/HKaB5fAucTU

<details>
<summary>CHECK ON THESE!!!</summary>

Audio:

pipewire: A modern audio and video server.   
pipewire-alsa: ALSA plugin for PipeWire.  
pipewire-pulse: PulseAudio compatibility layer for PipeWire.  
lib32-pipewire: 32-bit PipeWire libraries.  
alsa-utils: ALSA utilities for managing sound devices.  

Libraries and Dependencies:

lib32-gcc-libs: 32-bit GNU Compiler Collection libraries (needed for many 32-bit games).
lib32-libx11: 32-bit X11 libraries.
lib32-libxext: 32-bit X11 extension libraries.
lib32-libxi: 32 bit X input library
lib32-libxrandr: 32 bit X randr library  
lib32-libxrender: 32 bit X render library  
lib32-libxfixes: 32 bit X fixes library
lib32-libxcursor: 32 bit X cursor library  
lib32-libxinerama: 32 bit X inerama library
lib32-libxft: 32 bit X font library
lib32-libxpm: 32 bit X pixmap library  
lib32-libxtst: 32 bit X test library
lib32-libxxf86vm: 32 bit X vga library  
lib32-libxxf86misc: 32 bit X misc library
lib32-libxcomposite: 32 bit X composite library  
lib32-libxdamage: 32 bit X damage library
lib32-libdrm: 32-bit Direct Rendering Manager library.
lib32-zlib: 32 bit zlib library
lib32-sdl2: 32 bit Simple DirectMedia Layer  
lib32-openal: 32 bit Open Audio Library  
lib32-v4l-utils: 32 bit Video4Linux Utilities  
lib32-libpulse: 32 bit PulseAudio Library  
lib32-lcms2: 32 bit LittleCMS2 Library
lib32-libogg: 32 bit Ogg Library
lib32-libvorbis: 32 bit Vorbis Library  
lib32-libflac: 32 bit FLAC Library
lib32-libtheora: 32 bit Theora Library
lib32-libopus: 32 bit Opus Library
lib32-libpng: 32 bit PNG Library
lib32-freetype2: 32 bit FreeType2 Library  
lib32-fontconfig: 32 bit Fontconfig Library  
lib32-glib2: 32 bit GLib2 Library
lib32-gdk-pixbuf2: 32 bit GDK Pixbuf2 Library
lib32-gtk3: 32 bit GTK3 Library
lib32-pango: 32 bit Pango Library  
lib32-cairo: 32 bit Cairo Library
lib32-libjpeg-turbo: 32 bit libjpeg-turbo Library
lib32-libtiff: 32 bit TIFF Library
lib32-libwebp: 32 bit WebP Library  
lib32-libgudev: 32 bit libgudev Library
lib32-systemd: 32 bit systemd Library  
lib32-libudev: 32 bit libudev Library
lib32-libusb: 32 bit libusb Library
lib32-libxkbcommon: 32 bit libxkbcommon Library
lib32-libxshm: 32 bit libxshm Library
lib32-libxt: 32 bit libxt Library
lib32-libxmu: 32 bit libxmu Library
lib32-libxaw: 32 bit libxaw Library
lib32-libxkbfile: 32 bit libxkbfile Library  
lib32-libxrender: 32 bit libxrender Library  
lib32-libxcb: 32 bit libxcb Library
lib32-libxdmcp: 32 bit libxdmcp Library
lib32-libxau: 32 bit libxau Library  
lib32-libxft: 32 bit libxft Library
lib32-libxpm: 32 bit libxpm Library  
lib32-libxtst: 32 bit libxtst Library
lib32-libxxf86vm: 32 bit libxxf86vm Library  
lib32-libxxf86misc: 32 bit libxxf86misc Library
lib32-libxcomposite: 32 bit libxcomposite Library  
lib32-libxdamage: 32 bit libxdamage Library
lib32-libdrm: 32-bit Direct Rendering Manager library.
lib32-zlib: 32 bit zlib library
lib32-sdl2: 32 bit Simple DirectMedia Layer
</details>

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
