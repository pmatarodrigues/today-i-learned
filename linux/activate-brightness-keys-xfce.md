Check if brightness keys are active:
```
xfconf-query -c xfce4-power-manager -p /xfce4-power-manager/handle-brightness-keys
```
Activate keys:
```
xfconf-query -c xfce4-power-manager -p /xfce4-power-manager/handle-brightness-keys --create -t bool -s true
```
