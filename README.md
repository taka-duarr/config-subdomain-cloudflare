nano /etc/cloudflared/config.yml

nano /etc/nginx/sites-available/pet

ss -tlnp | grep 8083

systemctl restart cloudflared
systemctl restart nginx
