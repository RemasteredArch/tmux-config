# tmux-config

My personal tmux config.

Made for tmux 3.0a on Ubuntu 20.04 and the default tmux version of Ubuntu 22.04.

## Setup

Replace `~/.config/` with your `$XDG_CONFIG_HOME` if you have an unusual one set
```
mkdir ~/.config/
cd ~/.config/
git clone https://github.com/RemasteredArch/tmux-config.git tmux/
mkdir tmux/plugins/
cd tmux/plugins/
git clone https://github.com/tmux-plugins/tpm
tmux # then press C-s I (ctrl-s, shift+i) to install plugins
```
If your version of tmux does not autorun `~/.config/tmux/tmux.conf`, run:
```
ln -s ~/.config/tmux/tmux.conf ~/.tmux.conf
```

## Known bugs
On tmux 3.0a on Ubuntu 20.04, the status bar renders incorrectly. Instead of the Cattpuccin status bar, it renders the default status bar with the Cattpuccin background color.
