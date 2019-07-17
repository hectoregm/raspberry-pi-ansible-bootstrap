# Headless Raspberry Pi Setup with Ansible

## Current automations

* Boot: enable cgroups, disable WiFi, disable Bluetooth, disable IPv6, disable HDMI, disable audio
* Network: Set static IP, set DNS servers, set hostname, set hosts DNS names, use legacy IP tables
* System: upgrade system, upgrade packages, install common packages, set timezone, disable swap
* User: install and activate neofetch

## What do

* Place the current IP of the Pis to provision in the `inventory` file
* Use the helper script `get-ip-from-mac-addr.sh` to get the current IPs of your Pis
  * Script requires `arp-scan`
  * `sudo apt-get install arp-scan`
  * `brew install arp-scan`
* Update `vars.yml` to mac addresses of your Pis and set each `hostname` and `ip` to the desired values
* Run playbook: `ansible-playbook -i inventory main.yml -k`
