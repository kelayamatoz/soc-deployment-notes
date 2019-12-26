# Getting DHCP working on DE1SoC board
- On the Ubuntu side, use: 
  - nm-connection-editor.
  - Make sure that the interface wired to the ethernet port of DE1SoC is configured to "Shared to other computers" under the IPv4 Settings.
- On the board side, use: 
  - ifconfig eth0.
    - If eth0 doesn't show any IPv4 addresses, then we need to restart the dhclient. Run:
    ```bash 
    sudo dhclient -v eth0 
    ```
  - Make sure that eth0 is not searching on 255.255.255.255..