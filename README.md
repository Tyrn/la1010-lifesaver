## An Arch Linux emergency procedure for Kingst LA1010 and PulseView

- Install PulseView from AUR
```
$ yay -S pulseview-git
```
- [Get](http://www.qdkingst.com/en/vis-old) KingstVIS_v3.5.4.tar.gz

- Untar it
```
$ tar -zxf KingstVIS_v3.5.4.tar.gz
```
- To deploy firmware to `~/.local/share/sigrok-firmware/kingst` just run
```
$ python fwextractor.py KingstVIS/KingstVIS
```
- Replace the `pulseview-git` dependency `libsigrok-git` with `libsigrok-git-0.2.1.r3900.g4002c5c7-1-x86_64.pkg.tar.zst` (1254770 Bytes)
```
ᐅ yay -U libsigrok-git-0.2.1.r3900.g4002c5c7-1-x86_64.pkg.tar.zst
```

Good luck!

- In case you no longer need LA1010
```
$ yay -Rsn pulseview-git
$ yay -S pulseview-git
```
