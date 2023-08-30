# Vagrant environment for a standalone kubernetes cluster
> This procedure was performed on Apple M2 chip. [More info](https://www.unixarena.com/2022/09/virtual-machine-on-apple-mac-chip-m1-m2-fusion-vagrant.html/)

This repository contains a Vagrantfile to spin up a standalone kubernetes cluster using [kubeadm](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/).
The environment is based on [Vagrant](https://www.vagrantup.com/) and [VMwarefusion](https://www.vmware.com/au/products/fusion.html). 

## Prerequisites
- [Vagrant cloud account](https://app.vagrantup.com/)
- [VMware account] (https://customerconnect.vmware.com/home)
- [VMware fusion] (https://customerconnect.vmware.com/downloads/get-download?downloadGroup=FUS-PUBTP-22H2)
- [Vagrant VMware utitity] (https://developer.hashicorp.com/vagrant/docs/providers/vmware/vagrant-vmware-utility)

> After you download the vmware-utility you're going to need to registry it on your VMware account to download a personal use license key.

## Getting Started

1. Clone this repository to your local machine and then:

```bash
brew install vagrant
vagrant plugin install vagrant-vmware-desktop
vagrant plugin install vagrant-hostmanager
vagrant box add bento/ubuntu-20.04-arm64```

2.

```bash
vagrant up
```

> The CNI used in this lab was [calico](https://docs.tigera.io/calico/latest/getting-started/kubernetes/self-managed-onprem/onpremises#install-calico-with-etcd-datastore)