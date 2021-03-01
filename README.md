<html>
<p align="center">
    <img src="https://cdn.iconscout.com/icon/free/png-256/linux-13-532188.png">
</p>
<h2 align="center">Archlinux Installer</h2>
    <p align="center">
   
 [![Contributors][contributors-shield]][contributors-url] [![Forks][forks-shield]][forks-url] [![Stargazers][stars-shield]][stars-url] [![Issues][issues-shield]][issues-url]


[![Project Status: Active - The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/0.1.0/active.svg)](http://www.repostatus.org/#active)

 # Table of Contents

- [Introduction](#introduction)
- [Screenshots](#screenshots)
- [Detail](#detail)
- [Usage](#usage)
- [MyChanges](#mychanges)
- [Credits](#credits)
- [License](#license)

# Introduction 

After installing arch for the first time by manually typing every commands
carefully. I realized that those commands will be forgotten soon enough and I
have to do the hard work again when reinstalling arch. Unfortunately I did not
know shell script very well at that time to automate stuff like that

That's why I wrote this script now. This is the wizard that help installing
arch less painful because I do not reinstall my system regularly, I use arch
for that reason as I don't want to install or update my OS again, just use it
and move on with my life, but if I have to someday then it should not be much
of a chore as right now

This script is heavily inspired from [aui][1], many functions and logic is copied
from there, you should use that one instead as this one is customized to my
machine and setup and not guarantee to work on your computer. [aui][1] is more
customizable, well maintained and have more options than my script anyway

# Screenshot 

Here, the lightdm theme that you will get : 

<img src=https://raw.githubusercontent.com/lassipulkkinen/lightdm-webkit2-theme/master/screenshots/screenshot1.png width="960"/>

Currently, the desktop look like this : 

<img src=https://raw.githubusercontent.com/DraGiuS/arch_installer/master/screenshot.jpg width="960"/>

# Detail

* This script will only run on UEFI systems
* At the beginning you have to choose 4 partitions for: root, home, boot and swap
* After that it will format boot partition as fat32, /home in xfs (better for data), / in btrfs w/ a subvolume named storage
* Please have 35G minimum for the root partition
* I currently use KDE so the code installing i3 and xfce4 is not tested yet

#  Usage

* Download arch ISO file from [here][2]
* Use [rufus][3] (most stable to me) to make a bootable USB using the arch image
* Reboot to the usb
* Get the script and run it

**Note:** You should install in the correct order from 1-n because I did not
check all cases

```bash 

# if you use wifi, if not, then check out the next part

https://wiki.archlinux.org/index.php/Iwd

```

```bash


pacman -Sy git

git clone https://github.com/DraGiuS/arch_installer

cd arch_installer

it's recommended to edit the "common" file

./install

```

* After installing the base system choose finish to reboot. Clone the repo then go to it and run the other script

```bash
git clone -b postinstall https://github.com/DraGiuS/arch_installer

cd arch_installer

./postinstall
```

# MyChanges

* Support of bumblebee and vulkan with primus-vk

* Kde unstable option

* Added some packages, aur or not.. 

* You can set up your android development easily 

* Default setup of zsh with powerlevel9k

* Pamac

* Keyboard layout support

* Support of translation for main apps

* Conky

* Colorscheme for konsole

* Some applets by default

* Changed default gtk theme

* Alternative kernel (Xanmod Kernel...)

* GOG Games

* Choose your own version of firefox 

* Nano synthax highlighting

* MacOS Virtualization with qemu

* Spotify themed with spicetify 

#  Credits

* [aui][1]
* https://github.com/webbrandon/Surface-Boot-Themes
* https://github.com/bhilburn/powerlevel9k
* https://github.com/jsalatas/plasma-pstate
* https://github.com/Polunom/mac-inline-battery
* https://github.com/Zren/plasma-applet-volumewin7mixer
* https://github.com/zren/plasma-applet-tiledmenu
* https://github.com/divinae/uswitch
* https://github.com/DraGiuS/conky-spoclo
* https://github.com/arcticicestudio/nord-konsole
* https://github.com/Jazqa/kwin-quarter-tiling
* https://github.com/NearHuscarl/arch_installer
* https://github.com/robbyrussell/oh-my-zsh
* https://github.com/Sude-/lgogdownloader
* https://github.com/DraGiuS/linux-precompiled
* http://repo.steampowered.com/arch/valveaur/
* https://github.com/foxlet/macOS-Simple-KVM
* https://github.com/TheTeamByte/Spotify-Themes
* Archlinux team
* ME ('cause i love me)
# License

[**BSD 3-Clauses**](../master/LICENSE.md)

[1]: https://github.com/helmuthdu/aui
[2]: https://www.archlinux.org/download/
[3]: https://rufus.akeo.ie/


[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FDraGiuS%2Farch_installer.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FDraGiuS%2Farch_installer?ref=badge_large)



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/Dragius/arch_installer.svg?style=social&logo=appveyor
[contributors-url]: https://github.com/Dragius/arch_installer/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Dragius/arch_installer.svg?style=social&logo=appveyor
[forks-url]: https://github.com/Dragius/arch_installer/network/members
[stars-shield]: https://img.shields.io/github/stars/Dragius/arch_installer.svg?style=social&logo=appveyor
[stars-url]: https://github.com/Dragius/arch_installer/stargazers
[issues-shield]: https://img.shields.io/github/issues/Dragius/arch_installer.svg?style=social&logo=appveyor
[issues-url]: https://github.com/Dragius/arch_installer/issues
