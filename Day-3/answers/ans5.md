# Que 5: Can we block a website by its domain name only?

Yes we can use domain name or IP.

`iptables -A INPUT -s facebook.com -j DROP`
