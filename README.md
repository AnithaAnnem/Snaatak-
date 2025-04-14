# Snaatak

**Standard Operating Procedure (SOP): Managing Services on Ubuntu with systemctl**


**1. Purpose**

This SOP provides standardized procedures for managing services (start, stop, restart, enable, disable, check status) on Ubuntu OS.

**2. Prerequisites**


| Requirement       | Description                                                      |
|------------------|------------------------------------------------------------------|
| Ubuntu Version    | Ubuntu 16.04 or later (Recommended: 20.04, 22.04, or newer)      |
| systemd           | Must be installed (default from Ubuntu 15.04+)                   |
| Sudo Privileges   | User must have sudo access to manage services                    |
| Installed Services| The service (e.g., nginx, mysql) should be installed beforehand  |
| Terminal Access   | Access via SSH or local terminal                                 |





**3. Definitions**



| Term     | Description                                           |
|----------|-------------------------------------------------------|
| systemd  | The system and service manager used in Ubuntu         |
| Service  | A background process (e.g., Apache, MySQL)            |



**4.Service Management Commands with systemctl**

**Check Status of a Service**
It will displays us whether the service active (running)or inactive 
systemctl status <service_name>
**Example**: systemctl status nginx

**Start a Service**
It will start the service immediately
sudo systemctl start <service-name>
**Example**:systemctl status nginx

**Stop a Service**
It will stop the running process
sudo systemctl stop <service-name>
**Example**:sudo systemctl stop nginx

**Restart a Service**
It is useful to Restart(Stops and then starts) the service and it is very useful command to use whenever we have done any configuration changes
sudo systemctl restart <service-name>
**Example**:sudo systemctl restart nginx

**Enable a Service**
It Enables a service to start automatically on system boot.
sudo systemctl enable <service-name>
**Example**: sudo systemctl enable nginx

**Disable a Service**
Prevents a service from starting at boot.
sudo systemctl disable <service-name>
**Example**: sudo systemctl disable nginx


**5.Troubleshooting**


| Issue                | Solution                                                           |
|----------------------|--------------------------------------------------------------------|
| Service won't start  | Use `journalctl -xe` to check logs                                 |
| Permission denied    | Ensure the command is run with `sudo`                              |
| Service not found    | Confirm the service is installed (`systemctl list-unit-files`)     |
| Changes not applied  | Use `systemctl daemon-reexec` or `systemctl daemon-reload`         |





