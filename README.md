# Seafile Client for Raspberry Pi (CommandLine and/or GUI)

Based on: https://manual.seafile.com/build_seafile/linux.html

Compiled on: `Linux ARMbian 4.8.4-sunxi #6 SMP Sun Oct 23 15:55:47 CEST 2016 armv7l GNU/Linux`

## Istallation

Download DEB files above (and MD5 files if you want to check file integrity), example for download `ccnet-6.0.0_armhf.deb` to your current directory:

```
pwd
wget https://github.com/saljut7/seafile-client-rpi/blob/master/ccnet-6.0.0_armhf.deb
```

### Optional: MD5 check

Example:
```
$ md5sum -c libsearpc*.md5 
libsearpc-3.0-latest_armhf.deb: OK
```
### Install Seafile client dependencies

```
sudo apt update && sudo apt install qt5-default libqtcore4
```
### CommandLine only
```
sudo dpkg -i libsearpc*.deb
sudo dpkg -i ccnet*.deb
sudo dpkg -i seafile-daemon*.deb
```

### with GUI
```
sudo dpkg -i libsearpc*.deb
sudo dpkg -i ccnet*.deb
sudo dpkg -i seafile-daemon*.deb
sudo dpkg -i seafile-client*.deb
```

## Uninstall
### libsearpc
```
sudo dpkg -r libsearpc-3.0
```
### ccnet
```
sudo dpkg -r ccnet-6.0.0
```
### seafile-daemon
```
sudo dpkg -r seafile-daemon-6.0.0
```
### seafile-client
```
sudo dpkg -r seafile-client
```

## Usage
https://seacloud.cc/group/3/wiki/seafile-cli-manual
