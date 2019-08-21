## Squid

```bash
# copy config from image
docker run --rm --entrypoint cat sameersbn/squid /etc/squid/squid.conf > squid.conf

# test without password
curl -x http://localhost:3128  -L http://google.com

# create password
htpasswd -c -d conf/passwd john

# execute bash
docker run --rm -it  sameersbn/squid:3.5.27-2 bash

# test with password
docker-compmose up
curl -x http://john:1234@localhost:3128  -L http://google.com
```