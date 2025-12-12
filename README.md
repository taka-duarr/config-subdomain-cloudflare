cloudflared tunnel route dns 0daf7e99-69d0-4447-9696-5d0d9db2367c api.zatwasdead.my.id

nano /etc/cloudflared/config.yml

        server {
            listen 8084;
            server_name your subdomain.zatwasdead.my.id;
            
            root /var/www/html/your file location;
            index index.html index.htm;
        
            location / {
                try_files $uri $uri/ =404;
            }
            }

nano /etc/nginx/sites-available/pet

    server {
        listen 8084;
        server_name api.zatwasdead.my.id;
    
        root /var/www/html/tarik_tambang_server;
        index index.html index.htm;
    
        location / {
            try_files $uri $uri/ =404;
        }
    }
ln -s /etc/nginx/sites-available/api /etc/nginx/sites-enabled/

ss -tlnp | grep 8083

nginx -t
systemctl restart nginx


systemctl restart cloudflared
systemctl restart nginx
