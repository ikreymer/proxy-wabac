# wabac.js proxy mode demo

This proof-of-concept uses wabac.js to demonstrate a web archive loaded via service worker in 'proxy mode', without rewriting, running on a root domain.

The initial page installs the service worker, and then reloads, allowing the service worker to take over.

With the 404 fallback (see below), this should work for any page.

The main limitation is that iframes will not work in this mode. The demo does not add any banner, but can be added in the future.

This demo uses a WACZ file loaded from: https://dh-preserve.sfo2.cdn.digitaloceanspaces.com/webarchives/misc/derridas-margins.wacz

The system can be deployed as static files on nginx with a 404 fallback to index page, for example:

```
    location / {
      alias /path/to/proxy-wabac;

      error_page 404 /index.html;
    }
```
