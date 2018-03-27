# Configuration After Install
1. Enable RPM Fusion
2. Make Sure System is up to date
3. Install Driver VGA (NVIDIA)
  * Dependencies Install Requirment
  * Remove xorg-x11-drv-nouveua
  * Reboot to level 3
  * Install and RUN Nvidia Driver 
  * Install Nvidia Cuda
  * Back to Set Level 5
  * Enable video Acceleration
4. Remove Nvidia
5. Reinstall xorg and mesa packages

## Enable RPM Fusion
```java
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

## Make sure system is up to date
```java

```

## Install Driver VGA (NVIDIA)
Download and Install NVIDIA Driver
```java
http://www.nvidia.com/Download/index.aspx
```
cek VGA info and install
```java
uname -a

lspci |grep -E "VGA|3D"

chmod +x /path/to/NVIDIA-Linux-*.run
```
### Dependencies Install Requirment 
```java
## Fedora 27/26/25/24/23/22 ##
dnf install kernel-devel kernel-headers gcc dkms acpid libglvnd-glx libglvnd-opengl libglvnd-devel pkgconfig

## Fedora 21 ##
yum install kernel-devel kernel-headers gcc dkms acpid
```
### Remove xorg-x11-drv-nouveua
```java
## Fedora 27/26/25/24/23/22 ##
dnf remove xorg-x11-drv-nouveau

## Fedora 21 ##
yum remove xorg-x11-drv-nouveau
```

### Reboot to level 3
```java
systemctl set-default multi-user.target

reboot
```
### Install and RUN Nvidia Driver 
```java
./NVIDIA-Linux-*.run
```

### Install Nvidia Cuda
```java
dnf install xorg-x11-drv-nvidia-cuda
dnf install xorg-x11-drv-nvidia-cuda-libs
```

### Back to Set Level 5
```java
systemctl set-default graphical.target

reboot
```

### Enable Video Acceleration
```java
## Fedora 27/26/25/24/23/22 ##
dnf install vdpauinfo libva-vdpau-driver libva-utils

## Fedora 21 ##
yum install vdpauinfo libva-vdpau-driver libva-utils
```

## Remove Nvidia Driver
```java
nvidia-installer --uninstall
```

## Reinstall xorg and mesa packages
```java
## Fedora 27/26/25/24/23/22 ##
dnf reinstall xorg-\* mesa\*

## Fedora 21 ##
yum reinstall xorg-\* mesa\*
```
## Reference 
1. https://rpmfusion.org/Configuration
2. https://www.if-not-true-then-false.com/2015/fedora-nvidia-guide/
