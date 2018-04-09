# Useful Application 
## Session
1. Install Google Chrome
2. Install Theme MACOS

### Install Google Chrome
Open terminal 
```java
cat << EOF > /etc/yum.repos.d/google-chrome.repo
[google-chrome]
name=google-chrome
baseurl=http://dl.google.com/linux/chrome/rpm/stable/x86_64
enabled=1
gpgcheck=1
gpgkey=https://dl.google.com/linux/linux_signing_key.pub
EOF

dnf install google-chrome-stable
```

### Install Theme MacOS
* Package Icon
  * read more : https://github.com/keeferrourke/la-capitaine-icon-theme
  * Installation
```command
sudo dnf copr enable tcg/themes
sudo dnf install la-capitaine-icon-theme
```
  
* Theme 
  * read more : https://github.com/vinceliuice/Sierra-gtk-theme
  * Installation
```command
## git clone 
root@localhost theme]# cd Sierra-gtk-theme/
[root@localhost Sierra-gtk-theme]# in
in             infotocap      install        instperf       
info           init           install-info   invprofcheck   
infocmp        insmod         installkernel  
[root@localhost Sierra-gtk-theme]# ./Install 
   Installing Sierra-light ...
   Installing Sierra-dark ...
   Installing Sierra-light-solid ...
   Installing Sierra-dark-solid ...
   Installing Sierra-compact-light ...
   Installing Sierra-compact-dark ...
   Installing Sierra-compact-light-solid ...
   Installing Sierra-compact-dark-solid ...
[root@localhost Sierra-gtk-theme]# 
```

Reference : 
1. https://www.if-not-true-then-false.com/2010/install-google-chrome-with-yum-on-fedora-red-hat-rhel/
