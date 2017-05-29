# On-the-fly monitoring HTTP requests on a network interface


``` bash
tcpflow -p -c -i eth0 port 80 | grep -oE '(GET|POST|HEAD) .* HTTP/1.[01]|Host: .*'
# Or
httpry -i em1
```
