cloudflared tunnel route dns 0daf7e99-69d0-4447-9696-5d0d9db2367c api.zatwasdead.my.id

nano /etc/cloudflared/config.yml

nano /etc/nginx/sites-available/pet

ss -tlnp | grep 8083

systemctl restart cloudflared
systemctl restart nginx
