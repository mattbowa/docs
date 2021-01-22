#Setting Static IP on Ubuntu 18
cd into etc/netplan 
Inside is a file with name '00-installer-config.yaml' or similar

#Change its content from:
network:
  ethernets:
    enp0s3:
      dhcp4: true
  version: 2

#To:
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:
      dhcp4: no
      dhcp6: no
      addresses: [192.168.1.53/24]
      gateway4: 192.168.1.1
      nameservers:
         addresses: [8.8.8.8, 8.8.4.4]
		 
Once ready apply changes with:
$ sudo netplan apply
In case you run into some issues execute:
$ sudo netplan --debug apply

#Read more
https://linuxconfig.org/how-to-configure-static-ip-address-on-ubuntu-18-10-cosmic-cuttlefish-linux


