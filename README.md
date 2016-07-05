dockerdns
=========

Setup docker container DNS resolution.

Run dnsdocker to resolve containers name with .docker TLD and setup local
dnsmasq as docker default nameserver.


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

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
      - bersace.dockerdns


Copyright
-------

Licensed under BSD by Étienne BERSAC <@bersace>.
