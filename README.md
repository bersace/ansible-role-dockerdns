[![Build Status](https://travis-ci.org/bersace/ansible-role-dockerdns.svg?branch=master)](https://travis-ci.org/bersace/ansible-role-dockerdns)

dockerdns
=========

Setup docker container DNS resolution.

Run dnsdocker to resolve containers name with .docker TLD and setup local
dnsmasq as docker default nameserver.


```
LAN      local dnsmasq     Docker Engine            dnsdock                   container
 |              |                |                     |                          |
 |              |                *----- set local dnsmasq as nameserver --------->*
 |              |                |                     |                          |
 |              *<--------------------- DNS queries ------------------------------*
 |              |                |                     |                          |
 |              *---------- delegate .docker --------->*                          |
 |              |                |                     |                          |
 *<- delegate --*                |                     |                          |
 |              |                |                     |                          |
```

Role Variables
--------------

    # Name of the dummy network interface.
    iface: dockerdns0
    # IPv4 range in which DNS servers will bind an address.
    network: 192.168.7.0/24
    # Containers will be member of this domain:
    domain: docker


Example Playbook
----------------

    - hosts: localhost
      roles:
      - bersace.dockerdns


Copyright
-------

Licensed under BSD by Étienne BERSAC <@bersace>.
