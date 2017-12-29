# On-the-fly monitoring HTTP requests on a network interface


``` bash
tcpflow -p -c -i eth0 port 80 | grep -oE '(GET|POST|HEAD) .* HTTP/1.[01]|Host: .*'
# Or
httpry -i em1
```
https://unix.stackexchange.com/questions/6279/on-the-fly-monitoring-http-requests-on-a-network-interface

```
a2enmod headers
a2enmod expires
```
