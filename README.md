# Reset-Arch-Linux

# Setting all packages as dependencies

```console
sudo pacman -D --asdeps $(pacman -Qqe)
```

# We need to start saving our important packages

```console
sudo pacman -D --asexplicit linux linux-firmware base base-devel networkmanager grub efibootmgr
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
sudo pacman -S linux linux-firmware base base-devel networkmanager grub efibootmgr
```

# Reboot
```console
sudo reboot
````
