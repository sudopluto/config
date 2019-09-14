# config
config for my machines, eventully going to script this (hopefullly)

---
- operating system
    - Fedora 30
    - default theme for most applications

- laptop: 
    - grub related fixes
        - grub location: /etc/default/grub
        - grub gen cmd: sudo grub2-mkconfig -o /boot/efi/EFI/fedora/grub.cfg
        - hardware:
            - faulty modules
                - modprobe.blacklist=nouveau
            - acpi profile
                - acpi_osi=\"!Windows 2015\"
    - ethernet 
        - add fix service to systemd
    - touchpad frozen
        - switch to free tty & switch back
    - optimus
        - nvida drivers: rpmfusion instructions
        - nvidia-xrun
            - install from copr and follow directions
                - blacklist in grub?
            - add bus id to xorg config
                - /etc/X11/nvidia-xorg.conf.d
                    - add 30-nvidia.conf
                    - or file directly
                    - BusID "PCI:2:0:0" 
            - verify that drm is not set in grub
            - setup the nvida-xrun config file
                - nvidia-xrun goes in /etc/default/
            - use script nvidia-gnome.sh to switch once in free tty
                - make sure logged out of all accounts
                - switch to free tty
                - login and run script
                - when done, logout 
                - switch back to gdm and login
            - lspci and glxgears should be as expected
    - screen tearing
        - enable intel driver and its tearfree option
            - add 20-intel.conf to /etc/X11/xorg.conf.d
    - vaapi
        - just try to find the same packages from arch wiki in rpmfusion
        - vainfo and vdpauinfo should just work
        - vaapi addon from gnome-software?
    - battery
        - install tlp
    - hardware
        - body near power port is weak, support w/ sheet metal
        - display and wifi cable can get freyed at hing

- desktop: nvidia gpu screen tearing fix
  - force full composition pipeline
    - normal: just use nvidia settings
    - lightdm: startup applications
      - add: nvidia-settings --assign CurrentMetaMode="nvidia-auto-select +0+0 { ForceCompositionPipeline = On }"

- horipad controller
    - append the steam controller udev rules with line in 60-steam-input.rules
        - located: /lib/udev/rules.d/60-steam-input.rules 

- bash:
  - consider adding aliases and vim mode from .bashrc located here
  - remember to use ctl-r for bash searching
  - use (jk) v to edit current command in editor

- vim:
    - just use the .vimrc located here

- gnome-extensions:
    - just install from gnome software
        - maybe considering using repository rather than gnome software?
    - extenions
        - dash-to-dock
        - Kstatusnotifier/appindicator

- vscode
    - vim extension
        - jk to escape 

- mpv
    - maybe use aliases
    - use the given config
        - put in ~/.config/mpv

