# tmux-config

My personal tmux config.

Made for tmux 3.0a on Ubuntu 20.04 and the default tmux version of Ubuntu 22.04.

## Setup

Replace `~/.config/` with your `$XDG_CONFIG_HOME` if you have an unusual one set. You will also have to do this within [`tmux.conf`](./tmux.conf).
```bash
mkdir ~/.config/
cd ~/.config/
git clone https://github.com/RemasteredArch/tmux-config.git tmux/
mkdir tmux/plugins/
cd tmux/plugins/
git clone https://github.com/tmux-plugins/tpm
tmux # then press C-s I (ctrl-s, shift+i) to install plugins
```
If your version of tmux does not autorun `~/.config/tmux/tmux.conf`, create a symlink with:
```
ln -s ~/.config/tmux/tmux.conf ~/.tmux.conf
```

### Enable custom shell configurations only while in tmux

Add this to `~/.bashrc`:
```bash
if [[ -n $TMUX ]]; then
  # your commands here
fi
```
For example, do this to only enable a [starship](https://starship.rs/) prompt whilst in tmux:
```bash
if [[ -n $TMUX ]]; then
  eval "$(starship init bash)"
fi
```

## Known bugs
On tmux 3.0a on Ubuntu 20.04, the status bar renders incorrectly. Instead of the Catppuccin status bar, it renders the default status bar with the Cattpuccin background color. This bug bothers me, but my limited attempts to fix it have be fruitless, so I have chosen to simply ignore it until I update to Ubuntu 24.04.

# License

tmux-config is licensed under the GNU General Public License version 3, or (at your option) any later version. You should have received a copy of the GNU General Public License along with tmux-config, found in [LICENSE](./LICENSE). If not, see <[https://www.gnu.org/licenses/](https://www.gnu.org/licenses/)>.
