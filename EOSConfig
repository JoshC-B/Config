#!/bin/bash
# minimal-endeavour.sh

# Update system
sudo pacman -Syu --noconfirm

# Install Xfce with EndeavourOS look
sudo pacman -S --noconfirm --needed \
    xfce4 xfce4-goodies lightdm lightdm-gtk-greeter \
    arc-gtk-theme papirus-icon-theme \
    firefox alacritty networkmanager \
    git base-devel

# Enable services
sudo systemctl enable lightdm NetworkManager

# Install yay
cd /tmp
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si --noconfirm

# Install EndeavourOS theme
yay -S --noconfirm eos-qogir-theme

# Get EndeavourOS wallpaper
mkdir -p ~/Pictures
wget -q -O ~/Pictures/endeavouros-wallpaper.jpg \
    "https://raw.githubusercontent.com/endeavouros-team/endeavouros-theming/main/wallpapers/eos_wallpapers_community/Endy_planet.png"

echo "Done! Reboot to start lightdm."
