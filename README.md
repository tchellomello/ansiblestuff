# ansiblestuff
This repository contains some fun Ansbile stuff that uses *vagrant* as backend with *libvirt* by default.

Currently *Docker* support is being developed.


## How to use it

### Installing dependencies on CentOS7

```
yum install qemu libvirt libvirt-devel ruby-devel \
            gcc qemu-kvm  libxslt-devel libxml2-devel \
            libguestfs-tools-c ruby-devel gcc

vagrant plugin install vagrant-libvirt vagrant-dns
```
