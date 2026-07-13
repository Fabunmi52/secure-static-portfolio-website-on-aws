# Command cheat sheet

## SSH

```bash
chmod 400 portfolioweb-key.pem
ssh -i portfolioweb-key.pem ubuntu@SERVER_PUBLIC_IP
```

## Files

```bash
mkdir -p ~/webcontent
unzip website.zip -d ~/webcontent
ls -la ~/webcontent
sudo rsync -av --delete ~/webcontent/ /var/www/html/
```

## Nginx

```bash
sudo nginx -t
sudo systemctl status nginx
sudo systemctl restart nginx
sudo systemctl reload nginx
sudo journalctl -u nginx --since '30 minutes ago'
```

## System

```bash
sudo apt update
sudo apt upgrade -y
df -h
free -h
ss -tulpn
```

## DNS and HTTPS

```bash
dig +short edwardfabunmi.online
curl -I http://edwardfabunmi.online
curl -I https://edwardfabunmi.online
sudo certbot renew --dry-run
```
