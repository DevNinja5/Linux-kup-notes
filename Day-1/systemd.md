## Unit file for a services to run nginx server

**my-nginx-service.service**

```unit
[Unit]
Description=mynginx- server start

[Service]
type=forking
PIDFile=/run/nginx.pid
WorkingDirectory=/usr/sbin/
ExecStart=/usr/sbin/nginx
ExecReload=/usr/sbin/nginx -s reload
ExecStop=/bin/kill -s QUIT $MAINPID
PrivateTmp=true

[Install]
WantedBy=multi-user.target

```
