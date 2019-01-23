# Detec and Install Wifi Driver

```command
sudo dnf install -y https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-25.noarch.rpm https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-25.noarch.rpm
sudo dnf install -y broadcom-wl kernel-devel
sudo akmods --force --kernel `uname -r` --akmod wl
sudo modprobe -a wl

sudo dnf install -y kernel-devel
sudo akmods --force --kernel `uname -r` --akmod wl
```
