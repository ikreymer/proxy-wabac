# wabac.js proxy mode demo

This proof-of-concept uses wabac.js to demonstrate a web archive loaded via service worker in 'proxy mode', without rewriting, running on a root domain.

The initial page installs the service worker, and then reloads, allowing the service worker to take over.

The main limitation is that iframes will not work in this mode. The demo does not add any banner, but can be added in the future.

This demo uses a WACZ file loaded from: https://dh-preserve.sfo2.cdn.digitaloceanspaces.com/webarchives/misc/derridas-margins.wacz

