# RaspberryPI

## Enable SSH when creating SD card
Just create a simple empty file named `ssh` on the Windows-accessible part of the SD card after writing Raspbian to it.

## Wifi/WLAN when creating SD card
Just create a simple file named `wpa_supplicant.conf` on the Windows-accessible part of the SD card after writing Raspbian to it.

```config
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=DE

network={
    ssid="<SSID>"
    psk="<KEY>"
    key_mgmt=WPA-PSK
}
```

**Verzeichnis `C:\USERS\<user>\Dokumente\RaspberryPi\<files for SD card>`**

## first login username/password
First login username `pi` and password `raspberry`.

## first steps after login
### ssh/key
```bash
```

### rename pi user

In `/etc/passwd` change `pi` to `newuser` and `/home/pi` to `/home/newuser`.

In `/etc/shadow` change `pi` to `newuser`.

In `/etc/group` change `pi` to `newuser` (all entries ^pi: and :pi for the sudoers).

In `/home` rename `pi` to `newuser`

EOF
