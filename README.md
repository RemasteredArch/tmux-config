# tmux-config

My personal tmux config.

## Setup

Replace `~/.config/` with your `$XDG_CONFIG_HOME` if you have an unusual one set
```
mkdir ~/.config/
cd ~/.config/
git clone https://github.com/RemasteredArch/tmux-config.git tmux/
mkdir tmux/plugins/
cd tmux/plugins/
git clone https://github.com/tmux-plugins/tpm
```
If your version of tmux does not autorun `~/.config/tmux/tmux.conf`, run:
```
ln -s tmux/tmux.conf ~/.tmux.conf
```
