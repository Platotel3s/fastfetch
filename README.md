# Fastfetch 

<h3 align="left">
Welcome to my fastfetch config presets repo :3
</h3>

[Fastfetch](https://github.com/fastfetch-cli/fastfetch) is a tool for fetching system information and displaying them in a pretty way. 
In this repo, I collect my config files that I designed for my [Arch Linux](https://archlinux.org/) [Hyprland](https://github.com/hyprwm/Hyprland) rice. 
Feel free to copy files and modify them or clone the complete repository.

<p align="center">
  <img src="./screenshots/floating-mode.png" style="width: 100%;">
</p>

## Usage

Clone the repository into ``~/.local/share``

```sh
cd ~/.local/share
git clone https://github.com/LierB/fastfetch
```
and execute your preferred files (e.g. ``groups.jsonc`` or ``minimal.jsonc``) with 

```sh
fastfetch --config groups
fastfetch --config minimal
```
OR

Copy your preferred config file (if necessary images/ascii-art files), rename it to ``config.jsonc``, move it to ``~/.config/fastfetch`` and execute it with 

```sh
fastfetch
# or with additional options e.g.
fastfetch --colors-block-range-start 9 --colors-block-width 3
```

## Fastfetch (2.40.0-1) 

If you upgrade your Fastfetch version to 2.40.0-1, there are some configuration differences from the previous version.
In this version, the commands fastfetch --config groups and fastfetch --config minimal no longer work, meaning you will encounter an error like the one below.

<img src="errors/image.png" style="width:60%;height:60%">

You need to add this line to your ~/.zshrc (if you are using Zsh) or ~/.bashrc (if you are using Bash):
```sh
    fastfetch -c $HOME/.local/share/fastfetch/presets/groups.jsonc
```
If you follow the tutorial provided earlier, everything should work fine. See the image below.

<img src="errors/image2.png" style="width:60%;height:60%">
