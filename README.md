# ansible
1/ création de la présente branche : second
2/ modification  en entrant ce texte points 1 & 2 
3/ s  line from ansible master 
4/ update add line 4
5/ after fix pb keys
----   notes
ip addr show dev ens3
edit file /etc/netplan/01-netcfg.yaml
----------------
network:
  version: 2
  renderer: networkd
  ethernets:
    ens3:
      dhcp4: no
      addresses:
        - 192.168.121.221/24
      gateway4: 192.168.121.1
      nameservers:
          addresses: [8.8.8.8, 1.1.1.1]
----------------
When editing Yaml files, make sure you follow the YAML code indent standards. If the syntax is not correct, the changes will not be applied.

Once done, save the file and apply the changes by running the following command:
---------------------
sudo netplan apply
--------------
Verify the changes by typing:

ip addr show dev ens3
