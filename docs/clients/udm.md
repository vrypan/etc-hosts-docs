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
- *Server* to `dyndns2.etc-hosts.com/\/nic/update?hostname=%h&myip=%i`

(If the last step seems unusual, the reason a bug in UDM.)

![screenshot](/assets/images/udm-screenshot.png)
