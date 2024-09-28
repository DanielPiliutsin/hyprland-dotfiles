<i><h1>Minimal Blue</h1></i>
<img src="https://raw.githubusercontent.com/DanielPiliutsin/hyprland-dotfiles/refs/heads/main/git/assests/ezgif.com-animated-gif-maker.gif">
<p>⚠️ Nvidia Only! ⚠️</p>
<h2>Desktop Packages:</h2>
<ul>
  <li>App Launcher ~> Rofi 🐶</li>
  <li>Terminal Emulator ~> Kitty 😺 (with Fish 🐟)</li>
  <li>Top-bar ~> Waybar ⏲</li>
  <li>Logout Screen ~> Wlogout 🖥️</li>
  <li>Lock Screen ~> Swaylock 🔒</li>
  <li>Wallpaper Daemon ~> SWWW 🌆</li>
  <li>File Manager ~> Thunar ⚡</li>
</ul>

<h2>Installation:</h2>
<h3>Install Hyprland:</h3>
<p><i>WARNING: This step assumes you are booted into arch linux ISO with a single blank drive. Follow a seperate tutorial when messing with the drive(s) selection if this is not applicable to you! I am not responisble for any damages caused by improper drive setup!</i></p>

```
archinstall
```
<p><b>follow the setup instructions and select the following: </b></p>
<ul>
 <li>Drive(s) - ...use a best-effort defualt partition layout | READ WARNING!</li> 
 <li>Profile - Desktop - Hyprland - Nvidia (Proprietary)</li>
 <li>Audio - Pipewire</li>
 <li>Network Configuration - Network Manager</li>
 <li>Optional Repositories - Multilib</li>
 <li>For the other options, they are up to you</li>
</ul>
<p>Then Click Install!</p>
<h3>Install yay:</h3>

```
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

<h3>Install the dependencies:</h3>

```
yay -Syu git python swww thunar kitty waybar rofi rofi-emoji fish udiskie swaylock wlogout playerctl nerd-fonts qt5ct neofetch btop
```

<h3>Copy the configuration files:</h3>

```
git clone https://github.com/DanielPiliutsin/hyprland-dotfiles
cd hyprland-dotfiles
cp .config $HOME/.config
```

<h3>Reboot:</h3>

```
reboot
```
