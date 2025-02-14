# Docker-SmartDNS

SmartDNS in docker container, configurable via a simple WebUI.

## Software
- Alpine Linux: 3.21
- [SmartDNS](https://github.com/pymumu/smartdns): Release46
- [Webproc](https://github.com/jpillora/webproc): 0.4.0

## Usage
1. Run the container

   ```bash
   /Docker-Dnsmasq/bash $ sh up.sh
   ```

1. Visit `http://<docker-host>:5380`, authenticate with `foo/bar` and you should see.

    Example is the "Dnsmasq" WebUI interface.
   <img width="833" alt="screen shot 2017-10-15 at 1 41 21 am" src="https://user-images.githubusercontent.com/633843/31580966-baacba62-b1a9-11e7-8439-ca1ddfe828dd.png">
