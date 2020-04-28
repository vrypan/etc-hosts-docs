---
layout: default
title: Hostnames
nav_order: 1
---

# Hostnames in etc-hosts.com
{: .no_toc }

etc-hosts allows you to associate your IP with a hostname like `your-fancy-hostname.etc-hosts.net`.

`.etc-hosts.net` it the domain and it's up to you to pick `your-fancy-hostname` based on your needs and likes but:

- it must be between 7-63 characters long 
- it may contain only digits, letters and the symbols "." and "-".
- it has to be available, i.e. not used by someone else.

Examples of valid hostnames:
- `test123456.etc-hosts.net`
- `01.myhost.etc-hosts.net`
- `router.myhost.etc-hosts.net`

Right now, you are only given the option to select hostnames under the `.etc-hosts.net` domain (please note the .net tld),
but I intend to offer more options in the future.

Also note that each hostname can have an A (i.e. IPv4), an AAAA (i.e. IPv6) and a TXT value.