## Nginx - Proxy
---
```shell
yum install -y nginx
```

```shell
systemctl enable --now nginx
```

```shell
vim /etc/nginx/nginx.conf
server {
        listen       80;
        listen       [::]:80;
        server_name  <WAS CIDR>;
        root         /usr/share/nginx/html;
        location / {
        	proxy_pass http://<WAS CIDR>:<Port>/<Path>;
        }
        # Load configuration files for the default server block.
        include /etc/nginx/default.d/*.conf;

        error_page 404 /404.html;
        location = /404.html {
        }
```

```shell
systemctl restart nginx
```