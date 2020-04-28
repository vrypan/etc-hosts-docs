---
layout: default
title: The etc-hosts.com API
nav_order: 1
---

# The etc-hosts.com API
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Update host IP

The endpoint to update your host's IP is `https://etc-hosts.com/api/ping?hostname=<HOSTNAME>&api_key=<API_KEY>&ip=<IP>`

Where:
- `HOSTNAME` is your hostname. For example `test12345.etc-hosts.net`.
- `API_KEY` is the API key that corresponds to this host.
- `IP` is the IPv4 or IPv6 you want to assign to this hostname. If `ip` is ommited, etc-hosts will automaticlly use the IP that was 
used to make the request. Depending on the IP version (IPv4 or IPv6) a A or AAAA records will be generated/updated.

You can use both GET and POST methods. The following are equal: 
`curl 'https://etc-hosts.com/api/ping?hostname=test12345.etc-hosts.com&api_key=6b7n-58h8-q8mx-2g0l&ip=10.0.1.1'`

`curl https://etc-hosts.com/api/ping \
--data "hostname=test12345.etc-hosts.net" \
--data "api_key=6b7n-58h8-q8mx-2g0l" \
--data "ip=10.0.1.1"`

## Update a TXT record

The endpoint to update (or create) a TXT record is `https://etc-hosts.com/api/ping?hostname=<HOSTNAME>&api_key=<API_KEY>&txt=<TEXT>`

Where:

- `HOSTNAME` is your hostname. For example `test12345.etc-hosts.net`.
- `API_KEY` is the API key that corresponds to this host.
- `TEXT` is the value of the TXT record.

Again, both GET and POST methods can be used. Since TEXT must be URL encoded, it is probably easier to use the POST version in this case: 

`curl https://etc-hosts.com/api/ping \
--data 'hostname=test12345.etc-hosts.net' \
--data 'api_key=6b7n-58h8-q8mx-2g0l' \
--data 'txt=Hello World. This is a sample TXT record.'`

## Check your IP

You can check the IP etc-hosts would automatically assign to your host, by calling `https://etc-hosts.com/api/whatsmyip`.

For example: `curl -4 https://etc-hosts.com/api/whatsmyip` will return your IPv4 address and `curl -6 https://etc-hosts.com/api/whatsmyip` will return your IPv6 address (*if* you are using IPv6).
