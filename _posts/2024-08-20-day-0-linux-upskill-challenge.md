---
title: Linux Upskill Challenge Day 0
date: 2024-08-20 12:00:00 -500
categories: [homelab, linux]
tags: [homelab,linux,learn,challenge]
image:
  path: /assets/img/posts/LinuxUpskillDay0/Linux-Logo.png
---

# Introduction

Before you can dive into Linux server administration, you need a server. Today, we'll set up your very own server—completely free!

Thanks to advances in Linux and virtualization technology, you can now create and rent a Virtual Private Server (VPS) almost instantly and at minimal cost. This VPS will be hosted in a data center, where a single physical server running Linux is split into multiple virtual servers using KVM (Kernel-based Virtual Machine) technology.

We'll also need to choose the right "flavor" of Linux to install on your server. With numerous Linux distributions available, it can be a bit overwhelming for beginners. For this course, we'll be using the latest LTS (Long Term Support) version of Ubuntu Server, which is a popular and reliable choice.

Now, let's get started with setting up your AWS server!

## Setting Up Your Server in AWS

*In this guide, we'll walk through setting up a cloud server using AWS (Amazon Web Services). If you'd prefer to use a different cloud provider like DigitalOcean, Linode, or Google Cloud, you can find detailed instructions [here](https://linuxupskillchallenge.org/00/).*

## Why Choose AWS?

AWS offers a free-tier option that allows you to explore and test various services for 12 months at no cost, provided you stay within the usage limits. This makes it an excellent choice for beginners looking to get started with cloud computing without a significant upfront investment.

### Step 1: Sign Up for AWS

1. Visit the [AWS website](https://aws.amazon.com/).
2. Click on "Create an AWS Account" and provide your email address, a password, and a phone number for two-factor authentication.
3. You'll also need to provide credit card information, but you won’t be charged as long as you stay within the free tier limits.
4. Choose the “Basic Plan/Free” for support.

### Step 2: Launch Your EC2 Instance

1. After logging in, navigate to the **EC2** service from the top menu.
2. Click on **Launch Instance**.
3. Choose an image with “Ubuntu Server LTS” for the operating system.
4. For the instance type, select **t2.micro**—this is eligible for the free tier.
5. Under **Security Groups**, configure the firewall settings:
    - Add a rule to allow **All traffic** from **Anywhere**.
    - This setup is ideal for learning, but note that it's not recommended for production environments due to security concerns.

### Step 3: Generate SSH Keys

1. When prompted, create a new key pair.
2. Download the private key file to your local machine—this is crucial for accessing your server via SSH.

### Step 4: Access Your Server

1. Navigate to **Services > EC2 > Running instances** and locate your instance.
2. Find the **IPv4** address listed for your instance; this is the IP you'll use to connect via SSH.
3. If you're on Linux or macOS, open a terminal and use the following command:
    ```bash
    ssh -i /path/to/private_key ubuntu@your_ip_address
    ```
   For Windows users, you can use PuTTY to connect using the generated SSH key.

### Step 5: Initial Setup

1. Once logged in, confirm you can perform administrative tasks:
    ```bash
    sudo apt update
    sudo apt upgrade -y
    ```
2. If there are any kernel updates, reboot your server:
    ```bash
    sudo reboot now
    ```

Your server is now set up and ready for use!

## Important Notes

- **Responsibility**: Your server is now live and exposed to the Internet, meaning you're responsible for its security and management.
- **Regular Maintenance**: Keep your system updated regularly to ensure it remains secure.
- **Stopping vs. Terminating**: You can stop the instance at any time, but it will still incur charges. To avoid charges after you're done, make sure to terminate the instance.

For more options or if you prefer to use a different cloud provider, be sure to check out the [Linux Upskill Challenge Day 0](https://linuxupskillchallenge.org/00/) for detailed instructions.