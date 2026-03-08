# Linux System Administration Lab

## About This Project

In this lab, I practiced some basic Linux system administration tasks. The goal was to get comfortable with managing users, controlling file permissions, monitoring system logs, and automating simple tasks.

This project is a part of my journey learning Linux, networking, and cloud security.

I used environment like Ubuntu (WSL2), Bash terminal and sudo privileges

## User Management
Here, I created a few users and a group to understand how Linux handles access control.

The Commands I used are:
sudo adduser analyst_intern
sudo adduser devops_intern
sudo adduser analyst
sudo adduser devops
sudo groupadd security
sudo usermod -aG security analyst

The lessons I learnt were:
Users represent individual accounts on the system.
It is easier to manage permissions for multiple user by adding all of them to a group.
The principle of least privilege means users should only have access to what they actually need(Limiting access).

## I moved on to File Permissions
I gave directory permissions using chmod to limit access to files.
Commands used:
mkdir secure_data
chmod 700 secure_data

mkdir shared_logs
chmod 770 shared_logs

What I learned here:
4 - gives read permission
2 - gives write permission
1 - gives execute permission
4 + 2 + 1 = 7
`700` means only the owner can access the folder.
`770` allows both the owner and group members to access it.
`777` allows both the owner, group members and others to access it.
File permissions are one of the main ways Linux controls security.

## Log Monitoring
To see how system activity is recorded, I monitored authentication logs in the log folders.
The command i used:
sudo tail -f /var/log/auth.log
I combined the tail command + -f with the log file location.
This allowed me to watch login events and authentication activity in real time.

Logs are extremely important in security because they help detect suspicious activity.

## Cron Job Automation
Finally, I created a simple cron job to understand how scheduled tasks work in Linux.

I used a Command: crontab -e

Live cron job example:

0 * * * * echo "System check running" >> /home/ajibola/system_check.log

This job runs every hour and writes a message to a log file.

What I learned:
Cron is useful for automating repetitive administrative tasks.
The cron format uses time fields (minute, hour, day, month, weekday).

## What I Learned From This Lab

My Work and practices through this lab taught me and helped me to understand:
How Linux manages users and groups
How file permissions protect system resources
How logs can be used to monitor system activity
- how cron can automate simple tasks

These are foundational skills for system administration, cloud environments, and cybersecurity.
