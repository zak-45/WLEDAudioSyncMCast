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

```
First time you run WLEDAudioSyncMCast-{OS},
this will create folder ./WLEDAudioSyncMCast and extract all files on it.

To save some space and time,
you can then delete WLEDAudioSyncMCast-* and run the app from created folder.
```

the IP address need to be the one of your active LAN interface otherwise you will get an error like :
```
OSError: [WinError 10049] Not valid address on this context
```

To check Multicast on Linux :

$**netstat --groups**
```
IPv6/IPv4 Group Memberships
Interface       RefCnt Group
--------------- ------ ---------------------
lo              1      all-systems.mcast.net
eth0            1      all-systems.mcast.net
```

on Win :

C:\\>**netsh interface ip show joins**
```


Interface 1 : Loopback Pseudo-Interface 1

Étendue     Références  Dern  Adresse
----------  ----------  ----  ---------------------------------
0                    0  Oui   224.0.0.251
0                    3  Oui   239.255.255.250

Interface 20 : Wi-Fi

Étendue     Références  Dern  Adresse
----------  ----------  ----  ---------------------------------
0                    0  Non   224.0.0.1
0                    1  Oui   224.0.0.251
0                    1  Oui   224.0.0.252
0                    0  Oui   239.0.0.1
0                    1  Oui   239.255.102.18
0                    2  Oui   239.255.255.250

Interface 11 : Ethernet

Étendue     Références  Dern  Adresse
----------  ----------  ----  ---------------------------------
0                    0  Oui   224.0.0.1
```

