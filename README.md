Couple of scripts for setting up WOL on a linux server

Steps to take (assuming network interface supports wake-on-lan):

1. Install `ethtool` to inspect network interface (e.g. `sudo ethtool eno1`)
2. Change the `Wake-on` state to `g` with `sudo ethtool --change eno1 wol g`
3. Create a new service
4. Enable the service:

```
sudo systemctl daemon-reload
sudo systemctl enable wol.service
```
