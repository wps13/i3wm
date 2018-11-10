# i3wm

Configuration files for i3wm.

### Necessary packages:

[Light](https://github.com/haikarainen/light)

Installation Process:

    sudo apt install dh-autoreconf
    Clone the Repository and open the folder
    ./autogen.sh && ./configure && make && sudo make install
    
i3blocks

    sudo apt install i3blocks 

[i3lock](https://github.com/i3/i3lock)

    sudo apt install i3lock
    
scrot

    sudo apt install scrot

feh

   sudo apt install feh

### Optional Packages:

pavucontrol

    sudo apt install pavucontrol

Place the files in the following paths:

    config -> ~/.config/i3/config
    
    i3blocks.conf -> ~/.i3blocks.conf
    
### Touchpad Configuration

Place the file in the path
    
    /etc/X11/Xsession.d
 
Enabling Tapping  
       
In the terminal:

Search for the device id:

    xinput

Search for some Tapping enabled related property (Ex.: libinput Tapping Enabled)

    xinput list-props id
    
 Use the property id to change its value to enabled(1)
    
    xinput set-prop deviceid propertyid 1 
   
 Place the command in the i3 config file to save permanently the config
    
    exec xinput set-prop deviceid propertyid 1
