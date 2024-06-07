# Step-1:
ping the google so you will getting the information that the ISO connect with internet or not.😅😅
## Wi-Fi:
```sh
# ------------------------------
# |             iwctl          |
# ------------------------------

$ iwctl 
# ...
$ device list  # show the list of devices
# ...
$ station wlan0 show # showing the device wlan0 status
# ...
$ station wlan0 scan  # start scanning with the device wlan0
# ...
$ station wlan0 connect YourWifiSSID
# ...
$ quit # to leave iwctl
```

## Keys
```shell
# ------------------------------
# |  Refresh the package keys  |
# ------------------------------

# Reinitialize files & folders for keys
$ sudo pacman-key --init

# Repopulate keys
$ sudo pacman-key --populate archlinux

# Reinstall latest keyrings
$ sudo pacman -Sy gnupg archlinux-keyring

# Refresh the signature keys
$ sudo pacman-key --refresh-keys

# Clear out the software packages downloaded during aborted installations (optional):
sudo pacman -Sc
```

## Set Fastest mirror:
```shell
sudo pacman -S rate-mirrors

rate-mirrors --disable-comments-in-file --entry-country=IN --protocol=https arch --max-delay 7200 | sudo tee /etc/pacman.d/mirrorlist

sudo pacman -Syu
```

