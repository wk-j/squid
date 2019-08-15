## Squid

```bash
docker run --rm --entrypoint cat sameersbn/squid /etc/squid/squid.conf > squid.conf

curl -x http://localhost:3128  -L http://google.com

htpasswd -c -d conf/passwd john

docker run --rm -it  sameersbn/squid:3.5.27-2 bash

curl -x http://john:1234@localhost:3128  -L http://google.com
```