# archlinux


## install
sudo pacman -S xorg-server xorg-xinit i3-wm rxvt-unicode dmenu noto-fonts


## after install:
Configure sudo privileges:  
/etc/sudoers

echo "exec i3" >> ⁓/.xinitrc   

echo "setxkbmap -layout de" >> ⁓/.bash_profile

## finish
startx  

## notes
change tty  
ctrl + alt + f(1-12)  

sudo echo "KEYMAP=de" > /etc/vconsole.conf  
sudo mkinitcpio -P  

## beauty
sudo pacman -S lxappearance arc-gtk-theme  
apply in lxappearance and firefox extention
