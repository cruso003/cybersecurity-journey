# Commands Cheatsheet

## SSH & Server Management

```bash
# SSH into droplet (default)
ssh root@104.248.195.177
ssh cyberlab@104.248.195.177

# If your private key file is non-default, specify it explicitly (one-off):
# Replace the path with your private key (DO NOT share private key file)
ssh -i ~/.ssh/xpay_digitalocean cyberlab@104.248.195.177

# Or add the key to the ssh-agent for this session and connect normally:
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/xpay_digitalocean
ssh cyberlab@104.248.195.177

# Persistent config: add the following to ~/.ssh/config so SSH uses the
# correct identity automatically for this host.
##
# Host alias example (uncomment and adapt to enable)
Host do-droplet-cyberlab
	HostName 104.248.195.177
	User cyberlab
	IdentityFile ~/.ssh/xpay_digitalocean
	IdentitiesOnly yes

# After adding the Host entry, connect with the alias:
# ssh do-droplet-cyberlab
# You should see the Ubuntu welcome banner and an interactive shell like:
# "Welcome to Ubuntu 24.04.3 LTS (...)" if authentication succeeds.

# Update system
sudo apt update && sudo apt upgrade -y

# Install packages
sudo apt install PACKAGE_NAME -y
```

## Git Commands

```bash
# Add all changes
git add .

# Commit with message
git commit -m "Your message"

# Push to GitHub
git push origin main

# Check status
git status
```

_[Will expand as I learn more commands]_
