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



|  Number |  Meaning |
|----- | --------|
| 1 | General Commands |
| 2 | System Calls |
| 3 | Library functions, covering in particular the C standard library |
| 4 | Special files (usually devices, those found in /dev) and drivers |
| 5 | File formats and conventions |
| 6 | Games and screensavers |
| 7 | Miscellanea |
| 8 | System administration commands and daemons |
