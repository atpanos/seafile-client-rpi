# Seafile Client for Raspberry Pi (CommandLine and/or GUI)

Based on: https://manual.seafile.com/build_seafile/linux.html

Compiled on: `Linux ARMbian 4.8.4-sunxi #6 SMP Sun Oct 23 15:55:47 CEST 2016 armv7l GNU/Linux`

## Istallation

### Install Seafile client dependencies

```
sudo apt update && sudo apt install qt5-default libqtcore4
```

### Download Seafile client

Download DEB files archive and md5 checksum for file integrity check. For Seafile client version `6.0.0` you can download the archive to your current directory via:

```
pwd
wget wget https://github.com/saljut7/seafile-client-rpi/blob/master/seafile-client_6.0.0_rpi.tar.gz?raw=true -O seafile-client_6.0.0_rpi.tar.gz
wget wget https://github.com/saljut7/seafile-client-rpi/blob/master/seafile-client_6.0.0_rpi.tar.gz.md5?raw=true -O seafile-client_6.0.0_rpi.tar.gz.md5
md5sum -c seafile-client_6.0.0_rpi.tar.gz.md5
```

If output is...

```
$ md5sum -c seafile-client_6.0.0_rpi.tar.gz.md5 
seafile-client_6.0.0_rpi.tar.gz: OK
```

...extract the file archive to your current directory with:

```
tar xvf seafile-client_6.0.0_rpi.tar.gz
```

Now you can install only the CommandLine client or the client with GraphicalUserInterface from your current directory.

### CommandLine client

The command line client is just what is called "seafile-daemon" so you just need to install the daemon if you don't need a graphical user interface.

```
sudo dpkg -i seafile-client_6.0.0_rpi/libsearpc-3.0-latest_rpi.deb
sudo dpkg -i seafile-client_6.0.0_rpi/ccnet-6.0.0_rpi.deb
sudo dpkg -i seafile-client_6.0.0_rpi/seafile-daemon_6.0.0_rpi.deb
```

### GUI client

```
sudo dpkg -i seafile-client_6.0.0_rpi/libsearpc-3.0-latest_rpi.deb
sudo dpkg -i seafile-client_6.0.0_rpi/ccnet_6.0.0_rpi.deb
sudo dpkg -i seafile-client_6.0.0_rpi/seafile-daemon_6.0.0_rpi.deb
sudo dpkg -i seafile-client_6.0.0_rpi/seafile-client_6.0.0_rpi.deb
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

### seafile-daemon (command line client)

```
sudo dpkg -r seafile-daemon-6.0.0
```

### seafile-client (gui client)

```
sudo dpkg -r seafile-client
```

## Usage

Follow official tutorial: https://seacloud.cc/group/3/wiki/seafile-cli-manual
