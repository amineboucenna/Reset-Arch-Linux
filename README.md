# Reset-Arch-Linux

# First we need to start saving our important packages

```console
sudo pacman -D --asexplicit linux linux-firmware base base-devel networkmanager
```

# Now we need to login as sudo
```console
su -
```

# The next step is to remove all the packages excpet the important packages
```console
sudo pacman -Qttdq | pacman -Rns -
```

# Now reinstall your packages

```console
sudo pacman -S linux linux-firmware base base-devel networkmanager
```

# Reboot
```console
sudo reboot
````
