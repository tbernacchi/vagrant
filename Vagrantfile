# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
# A CentOS 7 virtual machine with 7 disks.
Vagrant.configure(2) do |config|
config.vm.define "zfs" do |zfs|
  zfs.vm.box = "insaneworks/centos7"
  zfs.vm.hostname = "zfs"
  zfs.vm.network :private_network, ip: "192.168.33.102"
  zfs.vm.provider "virtualbox" do |vb|
  unless File.exist?('./secondDisk.vdi')
    vb.customize ['createhd', '--filename', './secondDisk.vdi', '--variant', 'Fixed', '--size', 10 * 1024]
  end
  unless File.exist?('./thirdDisk.vdi')
    vb.customize ['createhd', '--filename', './thirdDisk.vdi', '--variant', 'Fixed', '--size', 10 * 1024]
  end
  unless File.exist?('./thirdDisk.vdi')
      vb.customize ['createhd', '--filename', './fourthDisk.vdi', '--variant', 'Fixed', '--size', 10 * 1024]
  end
  unless File.exist?('./thirdDisk.vdi')
    vb.customize ['createhd', '--filename', './fifthDisk.vdi', '--variant', 'Fixed', '--size', 10 * 1024]
  end
  unless File.exist?('./thirdDisk.vdi')
    vb.customize ['createhd', '--filename', './sixthDisk.vdi', '--variant', 'Fixed', '--size', 10 * 1024]
  end
  unless File.exist?('./thirdDisk.vdi')
    vb.customize ['createhd', '--filename', './seventhDisk.vdi', '--variant', 'Fixed', '--size', 10 * 1024]
  end
  unless File.exist?('./thirdDisk.vdi')
    vb.customize ['createhd', '--filename', './eighth.vdi', '--variant', 'Fixed', '--size', 10 * 1024]
  end
  vb.memory = "1024"
  vb.customize ["storagectl", :id, "--name", "SAS Controller3", "--add", "sas", '--portcount', 7]
  vb.customize ['storageattach', :id,  '--storagectl', 'SAS Controller3', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', './secondDisk.vdi']
  vb.customize ['storageattach', :id,  '--storagectl', 'SAS Controller3', '--port', 2, '--device', 0, '--type', 'hdd', '--medium', './thirdDisk.vdi']
  vb.customize ['storageattach', :id,  '--storagectl', 'SAS Controller3', '--port', 3, '--device', 0, '--type', 'hdd', '--medium', './fourthDisk.vdi']
	vb.customize ['storageattach', :id,  '--storagectl', 'SAS Controller3', '--port', 4, '--device', 0, '--type', 'hdd', '--medium', './fifthDisk.vdi']
	vb.customize ['storageattach', :id,  '--storagectl', 'SAS Controller3', '--port', 5, '--device', 0, '--type', 'hdd', '--medium', './sixthDisk.vdi']
	vb.customize ['storageattach', :id,  '--storagectl', 'SAS Controller3', '--port', 6, '--device', 0, '--type', 'hdd', '--medium', './seventhDisk.vdi']
	vb.customize ['storageattach', :id,  '--storagectl', 'SAS Controller3', '--port', 7, '--device', 0, '--type', 'hdd', '--medium', './eighth.vdi']
  end
end
end
