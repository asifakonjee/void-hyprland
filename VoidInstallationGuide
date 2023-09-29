sudo xbps-install git micro zip unzip bash-completion zsh figlet neofetch exa fontconfig
sudo xbps-install -y void-repo-multilib void-repo-multilib-nonfree void-repo-nonfree
sudo xbps-install -y intel-video-accel mesa-intel-dri mesa-vulkan-intel vulkan-loader
sudo xbps-install -y base-devel make cmake rust cargo rsync


# Insatll hyprland and xdg-desktop portal hyprland
git clone https://github.com/void-linux/void-packages.git
cd void-packages
./xbps-src binary-bootstrap
cd ..
git clone https://github.com/Makrennel/hyprland-void.git
cd hyprland-void
cat common/shlibs >> ../void-packages/common/shlibs
cat common/shlibs >> ../void-packages/common/shlibs
cp -r srcpkgs/* ../void-packages/srcpkgs
cd ~/void-packages
./xbps-src pkg hyprland
sudo xbps-install -R hostdir/binpkgs hyprland
./xbps-src pkg xdg-desktop-portal-hyprland
sudo xbps-install -R hostdir/binpkgs xdg-desktop-portal-hyprland




sudo xbps-install -y gvfs gvfs-mtp gzip ntp procps-ng udisks2 unzip zip ark wget curl plymouth bluez tlp tlp-rdw preload zstd htop grub-customizer ntfs-3g Thunar thunar-media-tags-plugin thunar-volman thunar-archive-plugin xfce-polkit ffmpeg ffmpegthumbs ffmpegthumbnailer xdg-user-dirs udiskie firefox libreoffice obs
sudo xbps-install -y pipewire wireplumber pulseaudio libpulseaudio libjack-pipewire libpipewire Waybar foot wezterm libsixel swaybg wl-clipboard dunst geany viewnior swayidle jq dunst qt5-wayland qt6-wayland qt5ct qt6ct kvantum mpv nwg-look swaylock evince octoxbps qbittorrent qutebrowser sddm


# Install Fonts and customized bash and zsh RC files
git clone https://github.com/asifakonjee/Fonts.git
cd Fonts/
mv .fonts/ ~/
sudo fc-cache -fv
cd
git clone https://github.com/asifakonjee/Void-RC-Files.git
cd Void-RC-Files/
mv -r * ~/
cd
cd .zsh/
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
cd
source .basrc
source .zshrc
add fcitx5 fcitx5-configtool
add libfcitx5-devel qt5-declarative-devel libzstd-devel qt5-devel cmake-devel
git clone --recursive https://github.com/OpenBangla/OpenBangla-Keyboard.git
cd OpenBangla-Keyboard\
git checkout develop
git submodule update
mkdir build && cd build
cmake .. -DENABLE_IBUS=OFF -DENABLE_FCITX=ON
make
sudo make install

sudo ln -s /etc/sv/sddm/ /var/service
sudo sv up sddm
sudo ln -s /etc/sv/NetworkManager /var/service/
 sudo sv up NetworkManager 

# How to configure HP printer in Void Linux:
# First start cupsd service:
sudo ln -s /etc/sv/cupsd /var/service
sudo sv up cupsd
## Add user to the lpadmin group
sudo usermod -aG lpadmin username ### Here username is your username!
## Install hplip and print-manager
add hplip print-manager
## Then open your system settings and add your printer.

