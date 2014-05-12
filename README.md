getdeps
======

A simple tool to download dependencies and verify them against a SHA256 hash

Uses a local cache to save network traffic and improve reliability in the face of network failures.

Depends on `curl` and `openssl`.

Use
---

```
getdeps dependenciesfile
```

Example dependencies file:

```
get http://code.jquery.com/jquery-2.1.1.min.js \
    vendor/jquery.js \
    874706b2b1311a0719b5267f7d1cf803057e367e94ae1ff7bf78c5450d30f5d4 \
    unpack=no
```

zip and tar files can be unpacked. tar files can strip leading path components with `strip=n` where n is the number of components to strip.

This will download and verify jquery, then put it in `vendor/jquery.js`
