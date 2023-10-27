# WLEDAudioSyncMCast
Simple Python script to bind to a Multicast Group on specified NIC (IP address) and send a message.
This can solve problem with some software when try to bind to Multicast Group on OS with multiple NIC.

## Install

Take your release from : https://github.com/zak-45/WLEDAudioSyncMCast/releases
```
this is a portable version, just run it according your OS
```

## Use it

Windows example :
```
WLEDAudioSyncMCast-Windows.exe  --ip 192.168.1.12 --group 239.0.0.1 --port 19890
```
_options_
![image](https://github.com/zak-45/WLEDAudioSyncMCast/assets/121941293/b80a55eb-5177-4a63-be44-a843697991ed)

## Info

the IP address need to be the one of your active LAN interface otherwise you will get an error like :
```
OSError: [WinError 10049] Not valid address on this context
```
