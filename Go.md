https://gowebexamples.com
https://github.com/teh-cmc/go-internals

Pointer
https://nathanleclaire.com/blog/2014/08/09/dont-get-bitten-by-pointer-vs-non-pointer-method-receivers-in-golang/


## server

```
[Unit]
Description=Go server

[Service]
ExecStart=/var/www/binary
# WorkingDirectory=/www/myapp
# EnvironmentFile=-/www/myapp/config/myapp.env
StandardOutput=journal
StandardError=inherit
SyslogIdentifier=myapp
User=www-data
Group=www-data
Type=simple
Restart=on-failure

[Install]
WantedBy=multi-user.target

```

systemctl start myapp
systemctl status myapp
systemctl enable myapp

```
