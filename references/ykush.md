---
creation date: 2024-11-04 13:30
tags:
  - dev/hardware
  - dev/usb
---
```yaml
os::*
command::pykush.py
desc::control usb device connectivity remotely
```


```cardlink
url: https://www.yepkit.com/products/ykush
title: "Yepkit USB Switchable Hub - YKUSH"
description: "The YEPKIT USB Switchable Hub (YKUSH) is more than just another USB Hub, it provides to the user unprecedented control over the power On/Off of the USB devices connected to the hub. And by On/Off we mean really powering up and down the USB ports, all this by software."
host: www.yepkit.com
```

---

```sh
sudo python pykush/pykush.py -d 1 # turn off power to port number 1
sudo python pykush/pykush.py -u 1 # turn on power to port number 1
```
