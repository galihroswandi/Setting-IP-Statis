
## Tutorials

Check the IP address used

```bash
  ip a
```

Create configuration on cat /etc/netplan/01-network-manager-all.yaml and paste code here

```bash
  # Let NetworkManager manage all device on this system

  network:
    version: 2
    renderer: NetworkManager
    ethernets:
        0xxxxxxxxxxx:
            dhcp4: no
            addresses:
                - <choose-ip>/24
            routes:
                - to: default
                  via: <your-gateway4>
            nameservers:
                addresses:
                    - 8.8.8.8
                    - 8.8.4.4
```

Apply configuration with command

```bash
  sudo netplan apply
```
    
