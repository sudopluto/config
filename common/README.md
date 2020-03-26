# software config
config for software 

---

- git
    - install libsecret: sudo dnf install git-credential-libsecret

- horipad controller
    - append the steam controller udev rules with line in 60-steam-input.rules
        - located: /lib/udev/rules.d/60-steam-input.rules 

- bash:
  - consider adding aliases and vim mode from .bashrc located here
  - remember to use ctl-r for bash searching
  - use (jk) v to edit current command in editor
  - color theme: dracula

- vim:
    - just use the .vimrc located here

- neovim:
    - copy over the .vimrc and the init.vim
    - init.vim location: ~/.config/nvim/init.vim

- vscode
    - vim extension
        - jk to escape 
    - located: ~/.config/Code/User/settings.json
    - color theme: dracula

- mpv
    - maybe use aliases in .bashrc
    - use the given config
    - located: ~/.config/mpv
    - for intel cpus
        - install libva-utils (vainfo)
        - install libva-intel-driver (actual driver)

- tlp
    - disable bluetooth on startup
