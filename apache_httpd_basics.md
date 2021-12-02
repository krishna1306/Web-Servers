```bash
yum install httpd

service httpd start

service httpd restart
```

```bash
firewall-cmd --permanent --add-service=http
```

```
/var/log/httpd/access_log

/var/log/httpd/error_log
```

```
/etc/httpd/conf/httpd.conf
```

- Which port it listens on - 80

- On which IPs it listens on - All

- Document root `/var/www/html` . All static content stored here

  - HTML
  - CSS
  - JS

- Which server to talk to (not mandatory though)

  `ServerName www.houses.com:80`

### Virtual Hosts

To support hosting multiple web apps through one server, you can use virtual hosts

```
<VirtualHost *:80>
	ServerName www.houses.com
	DocumentRoot /var/www/houses
</VirtualHost>

<VirtualHost *:80>
	ServerName www.oranges.com
	DocumentRoot /var/www/oranges
</VirtualHost>
```

Each virtual host configuration can also be separated

```
Include conf/houses.conf
Include conf/oranges.conf
```

```
/etc/httpd/conf/houses.conf

<VirtualHost *:80>
	ServerName www.houses.com
	DocumentRoot /var/www/houses
</VirtualHost>
```

Similarly for `oranges.conf` 