# dnsmasq

this is forked from andyshinn/docker-dnsmasq

# replace systemd-resolved with dnsmasq

+ disable systemd-resolved

   ```shell
   sudo systemctl disable systemd-resolved
   ```

+ set **dns=none** in */etc/NetworkManager/NetworkManager.conf*

   ```shell
   [main]
   dns=none
   ```

+ the */etc/resolv.conf* contents:

   ```shell
   nameserver 127.0.0.1
   ```

+ start dnsmasq with docker-compose
