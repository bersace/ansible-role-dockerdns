dockerdns
=========

Setup docker container DNS resolution.

Run dnsdocker to resolve containers name with .docker TLD and setup local
dnsmasq as docker default nameserver.


Role Variables
--------------

- `iface`: name of the dummy network interface (default: `dockerdns0`).
- `network`: IPv4 range in which DNS servers will bind an address (default: 192.168.7.0/24).
- `domain`: Containers will be member of this domain (default: `docker`).


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - bersace.dockerdns


Copyright
-------

Licensed under BSD by Étienne BERSAC <@bersace>.
