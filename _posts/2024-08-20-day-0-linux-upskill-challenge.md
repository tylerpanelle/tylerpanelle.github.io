---
title: Linux Upskill Challenge Day 0
date: 2024-08-20 12:00:00 -500
categories: [homelab, linux]
tags: [homelab,linux,learn,challenge]
image:
  path: /assets/img/posts/LinuxUpskillDay0/Linux-Logo.png
---

# Linux Upskill Challenge - Day 0: Get Your Own Server

Welcome to the Linux Upskill Challenge! Before we dive into the lessons, you’ll need to set up your own server. This guide will help you get started with creating a server in the cloud, which is highly recommended to get the full experience.

## **Step 1: Choose Your Cloud VPS Provider**

First, decide which cloud provider you want to use for your server:

- **DigitalOcean**
- **Linode**
- **Vultr**
- **AWS**
- **Azure**
- **Google Cloud**

> **Note:** While these services generally require a credit card for signup, they often offer free trials or credits.

Be cautious when exploring other options online; there are many scammy and fraudulent sites. Stick to reputable providers.

## **Step 2: Setting Up Your Cloud VPS**

Once you've chosen your provider, follow these steps to set up your VPS:

### **DigitalOcean:**
- Create a new Droplet.
- Choose the latest Ubuntu LTS version.
- Configure with 1GB memory, 1 vCPU, and 25GB SSD storage.
- Use a strong password or SSH key for authentication.

### **Linode:**
- Create a new Linode.
- Choose the latest Ubuntu LTS version.
- Configure with 1GB memory, 1 vCPU, and 25GB SSD storage.
- Use a strong password or SSH key for authentication.

### **Vultr:**
- Deploy a new server instance.
- Choose the latest Ubuntu LTS version.
- Configure with 1GB memory, 1 vCPU, and 25GB SSD storage.
- Use SSH keys for authentication.

> **Tip:** Make sure to select a region close to you to optimize performance.

## **Step 3: Remote Access via SSH**

Once your server is set up, you’ll access it remotely via SSH:

- **For Windows 10/11:** Use the native SSH client.
- **For older Windows versions:** Use PuTTY or another third-party SSH client.
- **For Linux/MacOS:** Open a terminal and connect with:
  ```bash
  ssh username@ip_address
  ```


Or, if using an SSH key:

```bash
ssh -i private_key username@ip_address
```
## Step 4: Initial Setup and Updates

You’re now a sysadmin! Perform the following tasks:

### Update Your System:

```bash
sudo apt update
sudo apt upgrade -y
```
### Reboot if Necessary:

```bash
sudo reboot now
```
Your server is now ready for the challenge!

## Additional Notes:

- **Security:** Your server is now running and exposed to the Internet. Ensure you manage it securely.
- **Logout:** When done, you can logout with `logout` or `exit`.
- **Shutdown:** If needed, shut down your server with:

```bash
sudo shutdown now
```
## Next Steps:

Now that your server is set up, you’re ready to start Day 1 of the Linux Upskill Challenge! Let’s dive into learning and mastering Linux.
