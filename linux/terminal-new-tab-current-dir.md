# Terminal: Open new tab on current directory

## Solution

Add following line to `~/.bashrc` (or `~/.zshrc` or whatever unix shell is being used):
```bash
source /etc/profile.d/vte.sh
```
*Tested on Manjaro + Gnome Terminal*

## More info
- [unix.stackexchange - Spawn new terminal window with the same directory as the previous window](https://unix.stackexchange.com/a/511285)
- [unix.stackexchange - gnome-terminal: keep track of directory in new tab](https://unix.stackexchange.com/a/93477)
- [bugs.launchpad.net](https://bugs.launchpad.net/ubuntu-gnome/+bug/1193993)