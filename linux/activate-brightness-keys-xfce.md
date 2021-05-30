# Activate Brightness Keys on XFCE (bug solving)
## Check if brightness keys are active:
```bash
xfconf-query -c xfce4-power-manager -p /xfce4-power-manager/handle-brightness-keys
```
## Activate keys:
```bash
xfconf-query -c xfce4-power-manager -p /xfce4-power-manager/handle-brightness-keys --create -t bool -s true
```
