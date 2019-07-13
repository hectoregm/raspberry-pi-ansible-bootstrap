# Raspberry Pi Networking Setup

When you plug a fresh new Raspberry Pi into your network, the default configuration tells the Pi to use DHCP to dynamically request an IP address from your network's router. Typically this is a pretty random address, and it can make configuration annoying.

# TBD

* Place the current IP of the Pis to provision in the `inventory` file
* Use the helper script `get-ip-from-mac-addr.sh` to get the current IPs of your Pis
  * Script requires `arp-scan`
  * `sudo apt-get install arp-scan`
  * `brew install arp-scan`
* Update `vars.yml` to mac addresses of your Pis and set each `hostname` and `ip` to the desired values
* Run playbook: `ansible-playbook -i inventory main.yml -k`