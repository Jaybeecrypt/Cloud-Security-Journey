# Linux System Administration Lab

## Project Objective
The objective of this lab is to demonstrate foundational Linux administration skills, including user management, file permissions, SSH, log monitoring, and cron job automation. These skills are essential for system administration and security monitoring.

## Environment
- OS: Ubuntu 22.04 LTS (via WSL2)
- Tools: Terminal, nano/vim, sudo privileges

## Skills Demonstrated
- User and group management
- File permissions and access control
- SSH configuration and monitoring
- System log monitoring
- Automating tasks with cron

## Tasks & Commands
1. Create Users and Groups
sudo adduser analyst
sudo adduser devops
sudo groupadd security
sudo usermod -aG security analyst
