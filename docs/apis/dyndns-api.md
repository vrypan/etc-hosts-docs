---
layout: default
title: Support for the Dyn API
parent: APIs
nav_order: 2
---

# Support for the Dyn API
{: .no_toc }

etc-hosts supports a subset of the popular [Dyn Perform Update (RA-API)](https://help.dyn.com/remote-access-api/perform-update/). (Sometimes also refered to as DynDNS.org API.)

If you use this API, you must set:

- `hostname` to your full etc-hosts hostname, for example `test12345.etc-hosts.net`. Only one hostname is supported.
- `myip` to your IP.
- `user` to `etc`.
- `password` to the API key that corresponds to this host.

The endpoint for the DynDNS API is `https://dyndns2.etc-hosts.com/v3/update`. In some tools this is refered to as the *server*. 
- Both HTTPS and HTTP are supported.
- the legacy `/nic/update` endpoint is also supported.

So, the generic URL is

```bash
https://{user}:{API key}@dyndns2.etc-hosts.com/v3/update?hostname={hostname}&myip={IP Address}
```

Example:

```bash
curl 'http://etc:qmqo-a9pi-4ulx-abmc@dyndns2.etc-hosts.com/v3/update?hostname=test12345.etc-hosts.com&myip=10.0.1.1'
```
