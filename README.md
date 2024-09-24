# archlinux



## maunual installation

pacstrap /mnt *package*  
  
### base system:
base base-devel linux linux-firmware vim  

### encryption starter pack:   
lvm2 cryptsetup grub  

### other stuff:  
networkmanager  
efibootmgr   

### runit (optional) 
pacstrap /mnt runit elogind-runit networkmanager-runit lvm-runit   
  
## after installation
sudo pacman -S *programm*

programms:
vim (texteditor)   
git (github)    
xorg-server (display)  
xorg-xinit (display)   
i3-wm (desktop)   
kitty (terminal)   
noto-fonts (font collection)   
lxappearance (gui for system-themes)   
arc-gtk-theme (cool system-theme)  
feh (wallpaper)  
arandr (for display settings)  
  
  
## after install:
Configure sudo privileges:  
/etc/sudoers

echo "exec i3" >> ⁓/.xinitrc   

echo "setxkbmap -layout de" >> ⁓/.bash_profile

## finish
startx  
 
## beauty
apply theme in lxappearance and firefox extension
edit ⁓/.config/kitty/kitty.conf
background #404552

## notes
change tty:
ctrl + alt + f(1-12)  

Keyboard issues:
sudo echo "KEYMAP=de" > /etc/vconsole.conf  
sudo mkinitcpio -P  

arc-dark color Palette:
#404552
#383c4a
#4b5162
#5294e2
#7c818c

remove loading cursor:  
$ cd ~/.icons/theme/cursors/  
$ rm watch left_ptr_watch
$ ln -s left_ptr watch  
$ ln -s left_ptr left_ptr_watch

Terminal not opening in i3:
bindsym $mod+Return exec dbus-launch gnome-terminal

