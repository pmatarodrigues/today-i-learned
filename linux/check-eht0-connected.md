# Check if ethernet cable is physically connected (and more)


```bash
cat /sys/class/net/eth0/carrier
```
Returns "1" if it's connected and "0" if it's not.


```bash
sudo ethtool eth0
```
Returns a list of information related to the selected interface.
At the bottom we can see "Link detected" to check if the cable is connected or not.
