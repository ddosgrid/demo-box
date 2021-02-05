# demo-box
Demo: Snapshot of a box running DDoSGrid and DDoSDB 

:warning: This is a demo-snapshot and should be used in production. 

## Prerequisites
* Virtualbox
* Vagrant - If one wants to configure the VM without Vagrant one needs to replicate the config from the `Vagrantfile`
* Linux host OS: Tested on Debian 10 and Arch Linux
## Setup

First, download the virtual box image from the releases tab of this repo into the local copy:
``` 
cd /path/to/local/repo
curl -O TBD
```
Next, bring up the virtualbox with Vagrant. If you want to do this manually make sure that the guest OS has IP `10.0.1.2` and that it is reachable via port 80. This can be done via NAT or with a bridge interface.
```
sudo vagrant up
```

Finally, on your host OS (!), create a named alias to localhost:
```
sudo echo "127.0.0.1 ddos.grid" > /etc/hosts
```

Finally, login using your browser on the host OS by navigating to `http://ddos.grid/ddosgrid`. One may login with user `demo` and password `Tx6e#X4$f4Fs`.
