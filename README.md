
<div align="center" class="tip" markdown="1" style>

![screenshot](images/Screenshot.png)

![GitHub repo size](https://img.shields.io/github/license/Gictorbit/photoshopCClinux?style=flat) ![Tested on arch](https://img.shields.io/badge/Tested%20on-Archlinux-brightgreen)
![GitHub stars](https://img.shields.io/github/stars/Gictorbit/photoshopCClinux?style=sad) ![rep size](https://img.shields.io/github/repo-size/gictorbit/photoshopCClinux) ![bash](https://img.shields.io/badge/bash-5.0.11-yellowgreen)
</div>

# photohop CC v19 installer for linux
This bash script installs Photoshop CC version 19 on your Linux machine using wine behind the scene
and sets some necessary component up for best performance

## :rocket: Features
* downloads necessary component and installs them (`vcrun`,`atmlib`,`msxml`...)
* downloads photoshop.exe installer and installs it automatically
* creates photoshop commands and desktop entry
* configures wine for dark mode
* detects various graphic cards like (`intel`, `Nvidia`...)
* saves the downloaded files in your cache directory
* It's free and you will not need any license key
* works on any Linux distributions

## :warning: Requirements
1- use 64bit edition of your distro <br>
2. make sure installed wine,if you get something error on wine fix before install photosop cc but this important for successfully install photoshop <br>
3. make sure below packages are already installed on your Linux distro
* `wine`
* `winetricks`
* `aria2`

if they are not already installed you can install them using your package manager for example in arch Linux
```bash
sudo pacman -S wine aria2 winetricks
``` 
or
```bash

sudo apt-get install wine
sudo apt-get install aria2 winetricks
```
3- make sure you have enogh storage in your `/home` partition about `5 GiB`
> 1 GiB will be free after installation

4- make sure you have internet connection and about 1.5 Gib traffic for downloading photoshop and its components at first time

## :computer: Installation
you can easily run `setup.sh` script to install photoshop cc on your linux distro

```bash
chmod +x setup.sh
./setup.sh
```
recommendation  number 1 use with winetricks
<div align="center" class="tip" markdown="1" style>

![setup-screenshot](images/setup-screenshot.png)
</div>

during installation please pay attention to script messages

> **NOTE :** make sure OS version in wine is on windows 7



## :wine_glass: wineprefix Configuration
if you need to configure wineprefix of photoshop you can use `winecfg.sh` script just run below command
```bash
chmod +x winecfg.sh
./winecfg.sh
```
## :hammer: Tools

<details>
<summary>:sparkles: Liquify Tools</summary>
as you know photoshop has many useful tools like `Liquify Tools`.</br>

if you get some errors during working with these tools
It may because of the graphics card.</br>

photoshop uses the `GPU` to process these tools so before using these tools make sure that your graphics card `(Nvidia, AMD)` is configured correctly in your Linux machine.
</br>The other solution is you can configure photoshop to use `CPU` for image processing. to do that, follow the below steps:

* go to edit tab and open `preferences` or `[ctrl+K]`
* then go to the `performance` tab
* in the graphics processor settings section, uncheck `Use graphics processor`

![](https://user-images.githubusercontent.com/34630603/80861998-117b7a80-8c87-11ea-8f56-079f43dfafd9.png)
</details>

---
<details>
<summary>:camera: Adobe Camera Raw</summary>

another useful adobe software is `camera raw` if you want to work with it beside photoshop you must install it separately to do this, after photoshop installation run `cameraRawInstaller.sh` script with below commands:
```bash
chmod +x cameraRawInstaller.sh
./cameraRawInstaller.sh
```
then restart photoshop.you can open it from 
`Edit >>Preferences >> Camera Raw`

> **_NOTE1:_** the size of camera raw installation file is about 400MB


> **_NOTE2:_** camera raw performance depends on your graphic card driver and its configuration

</details>

## :hotsprings: Uninstall
for uninstall photoshop you can use uninstaller script with below commands

```bash
chmod +x uninstaller.sh
./uninstaller.sh
```


## :bookmark: License
![GitHub](https://img.shields.io/github/license/Gictorbit/photoshopCClinux?style=for-the-badge)
