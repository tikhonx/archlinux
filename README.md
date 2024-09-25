# archlinux
by running archinstall you can skip to section II.


## I. manual installation

pacstrap /mnt *package*  
  
base system:
base base-devel linux linux-firmware vim  

encryption starter pack:   
lvm2 cryptsetup grub  

other stuff:  
networkmanager  
efibootmgr   

runit (optional) 
pacstrap /mnt runit elogind-runit networkmanager-runit lvm-runit   




## II. after installation
sudo pacman -S *programm*

*programms:*  

vim (texteditor)   
git (github)    
xorg-server (display)  
xorg-xinit (display)   
i3-wm (desktop)  
i3status (statusbar for desktop)
i3blocks (better statusbar)
dmenu (menu for desktop)
kitty (terminal)   
noto-fonts (font collection)   
lxappearance (gui for system-themes)   
arc-gtk-theme (cool system-theme)  
feh (wallpaper)  
arandr (for display settings)  
pavucontrol (audio gui)  
   
### configs:

Configure sudo privileges:  
/etc/sudoers

Launch WM by *$ startx*
echo "exec i3" >> ⁓/.xinitrc   

### beauty  
apply theme in lxappearance and firefox extension  
  
### kitty
create config: ctrl+shift+f2  
edit ⁓/.config/kitty/kitty.conf  
background #404552  

### firefox  
  
Extentions:   
ublock  
I still dont care about cookies  
darkreader  

Themes:  
Arc Dark Theme  

Disable menu on alt:  
Set ui.key.menuAccessKey = 17 on the about:config page.  
This makes the menu bar work with Ctrl+Shift.   
  
    
### notes *(unrelated)*
change tty:
ctrl + alt + f(1-12)  

Keyboard issues:
sudo echo "KEYMAP=de" > /etc/vconsole.conf  
sudo mkinitcpio -P  

Keyboard issues 2:
echo "setxkbmap -layout de" >> ⁓/.bash_profile

remove loading cursor:  
$ cd ~/.icons/theme/cursors/  
$ rm watch left_ptr_watch
$ ln -s left_ptr watch  
$ ln -s left_ptr left_ptr_watch

Terminal not opening in i3:
bindsym $mod+Return exec dbus-launch gnome-terminal


