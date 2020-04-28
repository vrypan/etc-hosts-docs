---
layout: default
title: ddclient
parent: clients
nav_order: 1
---

# How to configure ddclient
{: .no_toc }

The easiest way to configure [ddclient](https://github.com/ddclient/ddclient) 
with etc-hosts is to use the syndns2 protocol.

Set: 
- `protocol=dyndns2`
- `ssl=yes`
- `server=dyndns2.etc-hosts.com`
- `login=etc`
- `password=` the host API key

Example of /etc/ddclient.conf
```
# /etc/ddclient.conf

use=web

protocol=dyndns2
ssl=yes
server=dyndns2.etc-hosts.com
login=etc
password=235o-u3oy-724m-aa8d
test123456.etc-hosts.net
```