# service-worker-example

Based on https://www.youtube.com/watch?v=ksXwaWHCW6k since the repo was removed.

Full cred to https://github.com/bradtraversy/

## Two ways of caching a website

### Specifying resources and caching _on service worker install_

When visiting the site all of the specified static files (.html .css .js etc...) will be cached as soon as the service worker installs. See `sw_cached_pages.js` and register it in `main.js`.

### Caching the response on every fetch "as you go"

If you want to cache everything and not deal with specifying what resources to store, then you can just cache the entire response on every fetch. But bear in mind that pages that have yet to be visited will not be cached, as well as their associated assets. See `sw_cached_site.js` and register it in `main.js`.
