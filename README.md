# ansible-satellite-install
# Kevin Holmes
# kev@gokev.com

This playbook can be run on a freshly installed (unentitled) RHEL7 server and will result in a functioning WEBUI of Satellite Server.

Set your facts in **satellite_facts.yaml** for non-interactive install... 

The IP and hostname entered in the satellite_facts.yaml will be set statically.  The "target machine" ip can be the original DHCP assigned at new build.  My process:


1 - new RHEL build from latest RHEL7 ISO, basic packages
2 - power down the machine, snapshot the VM
3 - reboot, receiving DHCP and generic hostname
4 - run this playbook to the DHCP address of the machine
5 - when playbook completes, manually reboot.

Machine will come up to the IP you set and the webUI should be available with the credentials you set.


