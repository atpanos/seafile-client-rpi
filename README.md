# seafile-client_cli-gui_arm
Seafile CommandLine and GUI Client for ARM systems

Based on: https://manual.seafile.com/build_seafile/linux.html

Compiled on: `Linux armbian 4.8.4-sunxi #6 SMP Sun Oct 23 15:55:47 CEST 2016 armv7l GNU/Linux`

## Istallation

Download DEB files above.

### CommandLine only
```
dpkg -i libsearpc*.deb
dpkg -i ccnet*.deb
dpkg -i seafile-daemon*.deb
```

### with GUI
```
dpkg -i libsearpc*.deb
dpkg -i ccnet*.deb
dpkg -i seafile-daemon*.deb
dpkg -i seafile-client*.deb
```

## Uninstall
### libsearpc
```
dpkg -r libsearpc-3.0
```
### ccnet
```
dpkg -r ccnet-6.0.0
```
### seafile-daemon
```
dpkg -r seafile-daemon-6.0.0
```
### seafile-client
```
dpkg -r seafile-client
```

## Usage
https://seacloud.cc/group/3/wiki/seafile-cli-manual
