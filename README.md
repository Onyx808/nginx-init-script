# nginx init script for Ubuntu 16.04


Download this script to your server and place it at 
```
/etc/init.d/
```
Run the following commands
```
update-rc.d -f nginx defaults
```
```
echo "NGINX_CONF_FILE=/etc/nginx/nginx.conf" > /etc/default/nginx
```
```
echo "DAEMON=/usr/bin/nginx" >> /etc/default/nginx
```
Make sure you have the pid location before the http block in your nginx.conf located at /etc/nginx/nginx.conf
```
# pid of nginx process
pid /var/run/nginx.pid;
```
