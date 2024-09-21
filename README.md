# archlinux


### install
sudo pacman -S xorg-server xorg-xinit i3-wm kitty dmenu noto-fonts


### terminal  
edit ⁓/.config/i3/config
bindsym $mod+Return exec kitty

alternative: bindsym $mod+Return exec dbus-launch gnome-terminal

### after install:
Configure sudo privileges:  
/etc/sudoers

echo "exec i3" >> ⁓/.xinitrc   

echo "setxkbmap -layout de" >> ⁓/.bash_profile

### finish
startx  

### notes
change tty  
ctrl + alt + f(1-12)  

sudo echo "KEYMAP=de" > /etc/vconsole.conf  
sudo mkinitcpio -P  

### beauty
sudo pacman -S lxappearance arc-gtk-theme feh  
apply in lxappearance and firefox extension
remove loading cursor:  
$ cd ~/.icons/theme/cursors/
$ rm watch left_ptr_watch
$ ln -s left_ptr watch
$ ln -s left_ptr left_ptr_watch
