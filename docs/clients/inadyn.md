---
layout: default
title: inadyn
parent: Clients and services
nav_order: 2
---

# How to configure ddclient
{: .no_toc }

To configure [inadyn](https://github.com/troglobit/inadyn) 
with etc-hosts setup a custom configuration.

Set: 
- `hostname =` your host name.
- `username = "etc"`
- `password =` your host API key
- `ddns-server = "dyndns2.etc-hosts.com"`
- `ddns-path = "v3/update?hostname=%h&myip=%i"`

Example of /etc/inadyn.conf 

```
# /etc/inadyn.conf 

iface = ppp0
custom dyndns2.etc-hosts.com {
    hostname = "test123456.etc-hosts.net"
    username = "etc"
    password = "abcd-a9pi-6ulx-ftmc"
    ddns-server = "dyndns2.etc-hosts.com"
    ddns-path = "nic/update?hostname=%h&myip=%i"
}
```