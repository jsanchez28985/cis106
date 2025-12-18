# Server Hardware, LXC, Firewall, and Nginx Documentation

## What are the server hardware specifications (LXC settings)?

Your web server is running inside an **LXC container on Proxmox**, which uses shared kernel virtualization. The exact specs depend on what you assigned in Proxmox, but for your placeholder Nginx web server the typical settings are:

- **CPU:** 1 vCPU (enough for a static or low-traffic site)
- **Memory:** 1–2 GB RAM
- **Storage:** 8–16 GB disk
- **Network:** Bridged network (`vmbr0`)
- **Operating System:** Ubuntu 24.04 LTS

Because it is an LXC container, it is lightweight, boots fast, and uses fewer resources than a full virtual machine.

## What is the IP address of your LXC server?

Inside the LXC container, you find the IP address using the command:

```bash
ip a
```

This command lists all network interfaces and shows the IPv4 address assigned to the container. In this case, the LXC server is assigned a private LAN IP address (for example: `192.168.1.79/24`).

## How do you work with the Firewall in Proxmox and the LXC?

Firewall management happens at **two layers**:

- Proxmox firewall (host / datacenter / node / container level)
- Firewall inside the LXC container (UFW)

Inside the LXC, you used **UFW (Uncomplicated Firewall)**, which is a frontend for `iptables`.

### Common UFW commands

```bash
sudo ufw status
```
Shows whether the firewall is active and lists all current rules.

```bash
sudo ufw enable
```
Enables the firewall and starts enforcing rules.

```bash
sudo ufw disable
```
Disables the firewall and stops filtering traffic.

```bash
sudo ufw allow 80/tcp
```
Allows incoming HTTP traffic on port 80.

```bash
sudo ufw allow 443/tcp
```
Allows incoming HTTPS traffic on port 443.

```bash
sudo ufw deny 8000/tcp
```
Blocks access to port 8000 from external sources.

## How do you check if the Firewall is running?

```bash
sudo ufw status
```

## How do you disable the Firewall?

```bash
sudo ufw disable
```

## How do you add Nginx to the Firewall?

```bash
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
```

Or:

```bash
sudo ufw allow 'Nginx Full'
```

## Nginx service commands

```bash
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl reload nginx
sudo systemctl status nginx
```

## Test Nginx configuration

```bash
sudo nginx -t
```

## Check Nginx version

```bash
nginx -v
```

## Nginx configuration files

- `/etc/nginx/nginx.conf`
- `/etc/nginx/conf.d/*.conf`
- `/etc/nginx/sites-available/`
- `/etc/nginx/sites-enabled/`

## Nginx logs

- `/var/log/nginx/access.log`
- `/var/log/nginx/error.log`

## Review logs

```bash
cat /var/log/nginx/access.log
cat /var/log/nginx/error.log
tail -f /var/log/nginx/access.log
grep error /var/log/nginx/error.log
```
