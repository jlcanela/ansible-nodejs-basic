# Troubleshooting

## vagrant unable to start

```
There was an error while executing `VBoxManage`, a CLI used by Vagrant
for controlling VirtualBox. The command and stderr is shown below.

Command: ["dhcpserver", "add", "--ifname", "vboxnet0", "--ip", "172.28.128.2", "--netmask", "255.255.255.0", "--lowerip", "172.28.128.3", "--upperip", "172.28.128.254", "--enable"]

Stderr: VBoxManage: error: DHCP server already exists
```
found https://github.com/mitchellh/vagrant/issues/3083

solution : 
```
VBoxManage dhcpserver remove --netname HostInterfaceNetworking-vboxnet0
```

## optimize nginx config

have a look at:
https://gist.github.com/carlessistare/6417055
