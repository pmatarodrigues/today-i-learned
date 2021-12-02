# Output Microphone Audio

## Solution
### Activate
Install **pavucontrol** and load module for loopback device:
```bash
pactl load-module module-loopback latency_msec=1000
```


### Deactivate
```bash
pactl unload-module module-loopback
```

## More info
- [bytee](https://bytee.net/misc/listen-to-your-own-microphone-on-linux)
- [Modules - PulseAudio](https://www.freedesktop.org/wiki/Software/PulseAudio/Documentation/User/Modules/)
- [Stack Overflow - falconer](https://askubuntu.com/a/403454)
