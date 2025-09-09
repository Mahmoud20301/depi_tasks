
# Docker Setup with Ansible on Remote Machine

![Docker](https://img.shields.io/badge/Docker-Aqua?logo=docker&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-Red?logo=ansible&logoColor=white)
![NGINX](https://img.shields.io/badge/Nginx-Orange?logo=nginx&logoColor=white)

## Overview
This project demonstrates how to **install Docker on a remote machine using Ansible** and **run an Nginx container**. It automates deployment and ensures consistent setup across servers.

## Prerequisites
- Local machine with Ansible installed  
- Remote machine accessible via SSH  
- User with `sudo` privileges on the remote machine
## SSH Setup
```bash
ssh-keygen -t rsa                          # Generate a new SSH key pair on your local machine
ssh-copy-id USER@REMOTE_IP                 # Copy your public key to the remote machine's ~/.ssh/authorized_keys

## Inventory File
