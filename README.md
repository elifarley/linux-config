# linux-config
Mostly configuration files from /etc

# pacman tips
See https://wiki.archlinux.org/index.php/Pacman/Tips_and_tricks#Listing_all_changed_files_from_packages
```bash
pacman -Qii | awk '/^MODIFIED/ {print $2}' # Shows modified backup files
pacman -Qkk # Shows problems on installed packages like wrong file permissions
pacman -Qdt # List unneeded packages
```
