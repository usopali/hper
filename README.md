
# HYPERLAND SETUP

setting up hyperland for newbie's and pro's alike


## Getting Started 
To get started you'll need few utilities and some basic things 
1. Adding Wayland & Xwayland 
2. Installing an AUR helper 
3. Installing hyprland and related dependencies
4. Setting up audio, vedio, Brightness, rofi & Screenshot
5. Installing and configuring app clients like Discord, Telegram



## Setup

A.  Setting Up Wayland and Xwayland 

If you are running something like Gnome, Kde, Sway, Qtile e.t.c you can skip this step and move to next one 
```bash
 sudo pacman -Sy wayland libdrm pixman libxkbcommon python2 libxml2 /
 llvm libpng gegl mtdev xorg-xwayland  qt5-wayland qt6-wayland 
 ```
These dependencies will setup the base required for proper functioning of hyprland or any other window manager based on wayland 

Xwayland is requied to run some xorg specific dependencies without it you might feel lag or sttuters while doing some task or some task might break

## About AUR Helper

Aur Helper is a tool which help you download apps and binaries stored and uploaded in Arch User Repository thus, giving you access to a large in no packages which are not avalible in official pacman repo's

There are a lots of aur helper out the but some common one are
1. Paru {written in rust and my personal favorite}
2. yay  {written in go and is quiet nice}
3. you can use anyone but replace it with paru while using cammands 

## Installing Paru

```bash
cd Downloads & 
git clone https://aur.archlinux.org/paru-bin 
```
```bash
cd paru-bin &
makepkg -si 
```

After installing PARU check for updates by using

```bash
paru -Syu
```
```bash
sudo pacman -Syu
```
making sure are repo's and all the packages are upto date

## Installing Hyprland & Stuff to Make Hyprland Functional 

[Hyprland](https://wiki.hyprland.org/) is a tiling window manager {To go and read its wiki click on hyprland}

```bash
paru -S hyprland-bin hyprpaper waybar-hyprland-git xdg-desktop-portal-wlr
wlroots xdg-desktop-portal polkit-kde-agent 
rofi-lbonn-wayland-git wezterm kitty pcmanfm-qt neovim gedit 
```
## Setting Up volume, Brightness & other useful Stuff

```bash
paru -S brightnessctl pavucontrol alsa-utils grim slurp mpv vvave brave-bin wlogout nm-applet 
```
if you are using my config files then,

Brighness & Volume is binded with thier Respective toggle keys for laptop users 
## App Clients that works smoothly in hyprland

you can find a compelete guide here on hyprland wiki

[App Client Links](https://wiki.hyprland.org/Useful-Utilities/App-Clients/)


## Installing Themes I Used

copy & paste
```bash
paru -S catppuccin-gtk-theme-mocha vimix-cursors  tela-icon-theme 
``` 
will make system a bit usable 
## Installation

To Install my configs 

```bash
cd Downloads &
git clone https://github.com/vs66388/hyprland.git
```
After cloning this repo you can paste file located in .config folder into you .config folder which is stores into your home dir {Hidden by default to see it Press Ctrl+H} mannually or use cmd given below

```bash
cp .config/ ~/.config/
```
after that cheack if all the folders are in ~/.config or not 

## Keybinds

```bash
bind = SUPER, W,      exec, brave
bind = SUPER, F,      exec, pcmanfm-qt
bind = SUPER, RETURN, exec, wezterm
bind = SUPER, X,      exec, wlogout
bind = SUPER, O,      exec, telegram-desktop
```
## Sample of Hyprland and Hyprpaper
[Hyprland](https://github.com/vs66388/hyprland/blob/main/hypr/hyprland.conf)

[Hyprpaper](https://github.com/vs66388/hyprland/blob/main/hypr/hyprpaper.conf)

## Wallpaper 

To setup wallpaper just paste you wallpaper into pictures folder and name it wallpaper.jpg
or replace image address in ~/.config/hypr/hyprpaper.conf




