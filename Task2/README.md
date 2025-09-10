

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
```
## Get IP of remote VM
<img width="1400" height="900" alt="Screenshot 2025-09-09 224244" src="https://github.com/user-attachments/assets/7720bc3e-b52c-4e59-9fca-d5a6456027c7" />

## Inventory File
```bash
[install-docker]
vm1 ansible_host=192.168.1.17 ansible_user=ansible  #Defines remote hosts for Ansible.
```

## Ansible Playbook
- Automates Docker installation on remote hosts  
- Ensures Docker service is started and enabled  
- Deploys Nginx container automatically  
- Provides a repeatable and consistent setup for all servers
## Running the Playbook
Execute the playbook from your local machine with:

```bash
ansible-playbook -i inventory.ini docker-play.yaml
```
<img width="1920" height="1080" alt="Screenshot 2025-09-09 223346" src="https://github.com/user-attachments/assets/05a788b5-e9f9-4f90-a9db-e31e1275b811" />

<img width="1920" height="1080" alt="Screenshot 2025-09-09 223256" src="https://github.com/user-attachments/assets/0cc3c2ae-812e-430f-8567-869c09860eeb" />


