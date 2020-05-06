---
layout: default
title: UniFi UDM
parent: Clients and services
nav_order: 3
---

# How to configure UniFi Dream Machine
{: .no_toc }

To configure the UniFi Dream Machine to automatically update your host's IP, go to
settings (*Gateway > Dynamic DNS* or *Services > Dynamic DNS*) and add a new
service.

Set:

- *Service* to *dyndns*
- *Hostname* to your etc-hosts hostname
- *Username* to `etc`
- *Password* to your host's API key
- *Server* to `dyndns2.etc-hosts.com/\/nic/update?myip=%i&hostname=%h`. 
***Important:*** Make sure you copy and paste the value, 
without removing the backslash or altering the order of the variables: there is a known bug in UDM and
this exact value is probably the only way to get around it.

![screenshot](/assets/images/udm-screenshot.png)
