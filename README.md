# docker-afraid-dyn-updater

Super simple curl-bot.

- `UPDATE_URL` is the URL that dynamically sets your new IP - Get from here: http://freedns.afraid.org/dynamic/
- `UPDATE_INTERVAL` is the frequency at which to check/update 1800 is probably reasonable

### Simple Build and Run:
```
docker build -t url-test https://raw.githubusercontent.com/sover02/docker-afraid-dyn-updater/master/Dockerfile
docker run -dit --restart always -e UPDATE_URL="http://freedns.afraid.org/dynamic/update.php?< AFRAID API KEY >" -e UPDATE_INTERVAL="300" dynamic-updater
```

#### Simple Logging

```
# docker logs -f dde6f20a2a621f6a9f12b5f9cd4cf1300a4d9571ea63973cb020d3a1b491110f
Fri Jan  4 03:20:43 UTC 2019 ERROR: Address 78.124.2.61 has not changed.
Fri Jan  4 03:20:47 UTC 2019 ERROR: Address 78.124.2.61 has not changed.
Fri Jan  4 03:20:50 UTC 2019 ERROR: Address 78.124.2.61 has not changed.
Fri Jan  4 03:20:53 UTC 2019 ERROR: Address 78.124.2.61 has not changed.
Fri Jan  4 03:20:56 UTC 2019 ERROR: Address 78.124.2.61 has not changed.
Fri Jan  4 03:21:00 UTC 2019 ERROR: Address 78.124.2.61 has not changed.
Fri Jan  4 03:21:03 UTC 2019 ERROR: Address 78.124.2.61 has not changed.
^C
```
