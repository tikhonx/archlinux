# archlinux


## install
sudo pacman -S xorg-server xorg-xinit i3-wm rxvt-unicode dmenu noto-fonts


## after install:
Configure sudo privileges:
/etc/sudoers

echo "exec i3" >> ⁓/.xinitrc 

⁓/.bash_profile


## finish
start x

## notes
change tty
ctrl + alt + f(1-12)
