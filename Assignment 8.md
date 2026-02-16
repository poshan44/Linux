# ASSIGNMENT 8 (Firewall)

In this assignment, I created a firewall for my linux server that starts automatically when the server boots.

## Firewall

I have use UFW as a host based firewall to protect the server.

## Define policies

1. Block All Incoming Traffic

```bash
sudo ufw default deny incoming
```

Purpose:

. Blocks all incoming connections by default.

. Only allowed services can receive traffic.

2. Allow Outgoing Traffic

```bash
sudo ufw default allow outgoing
```

Purpose:

. Allows the server to send outgoing connections.

. Needed for updates and normal communication.

## Allowed Services

### OpenSSH Server

```bash
sudo ufw limit ssh
```
Purpose:

. Allows SSH access on port 22.

. Used for remote server management.

### HTTP Server

```bash
sudo ufw allow http
```
Purpose:

. Opens port 80 (TCP).

. Allows users to access the website hosted on the server.

### HTTPS Server

```bash
sudo ufw allow https
```
Purpose:

. Enables firewall logging.

. Logs blocked connections and new connection attempts.

## Logging Configuration

```bash
sudo ufw logging medium
```
Purpose:

. Enables firewall logging.

. Logs blocked connections and new connection attempts.

Firewall logs are saved on:

```lua
/var/log/ufw.log
```

## SYN Flood Protection

```bash
sudo ufw limit ssh
```
Purpose:

. Limits the number of new TCP connection attempts.

. Protects the server from SYN flood attacks.

## Additional Protection 

### SSH Brute Force

```bash
sudo ufw limit ssh
```

Purpose:

. Prevents repeated login attempts from the same IP.

. If too many attempts happen in a short time, the firewall blocks that IP temporarily.

## Firewall Status Check

To check the firewall configuration, I used:

```bash
sudo ufw status verbose
```

Final configuration:

. Incoming: Denied

. Outgoing: Allowed

. SSH: Limited

. HTTP: Allowed

. HTTPS: Allowed

. Logging: Enabled (medium)