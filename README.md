

 ![image](https://github.com/user-attachments/assets/f8d1e015-f9cb-4c1e-933e-22e6262b0c69)


| Author        | Date       | Version | Review Level   | Reviewer Name        |
|---------------|------------|---------|----------------|----------------------|
| Anitha Annem  | April 20   | v1.1    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  | April 24   | v2.1    | L0             | Khushi Malothra      |
| Anitha Annem  |            |         | L1             | Rishabh Sharma       |
| Anitha Annem  |            |         | L2             | piyush Upadhyay      |


# Table of Contents
  1. [Introduction](#Introduction)
  2. [ Purpose](#purpose)
  3. [ Prerequisites](#️prerequisites)
  4. [ Service Management Commands with systemctl](#service-management-commands-with-systemctl)
  5. [ Troubleshooting](#troubleshooting)
  6.  [Conclusion](#conclusion)
  7. [ Contact Information](#contact-information)
  8. [ References](#references)


#  SOP for  Managing Services On Ubuntu With systemctl

# Introduction

In this documentation The SOP provides a clear and consistent process for managing services on Ubuntu using the systemctl command. 




# Prerequisites

To ensure the successful management of the service on Ubuntu, the following prerequisites must be met:


| Requirement       | Description                                                      |
|------------------|------------------------------------------------------------------|
| Ubuntu Version    | Ubuntu 16.04 or later (Recommended: 20.04, 22.04, or newer)      |
| systemd           | Must be installed (default from Ubuntu 15.04+)                   |
| Sudo Privileges   | User must have sudo access to manage services                    |
| Installed Services| The service (e.g., nginx, mysql) should be installed beforehand  |
| Terminal Access   | Access via SSH or local terminal                                 |




# Service Management Commands with systemctl





- **Check Status of a Service**  
  - Displays whether the service is active (running) or inactive.  
  - **Command**:  
    ```bash
    systemctl status <service_name>
    ```  
  - **Example**:  
    ```bash
    systemctl status nginx
    ```

- **Start a Service**  
  - Starts the service immediately.  
  - **Command**:  
    ```bash
    sudo systemctl start <service-name>
    ```  
  - **Example**:  
    ```bash
    sudo systemctl start nginx
    ```

- **Stop a Service**  
  - Stops the running service immediately.  
  - **Command**:  
    ```bash
    sudo systemctl stop <service-name>
    ```  
  - **Example**:  
    ```bash
    sudo systemctl stop nginx
    ```

- **Restart a Service**  
  - Stops and then starts the service, useful when changes are made to configuration files.  
  - **Command**:  
    ```bash
    sudo systemctl restart <service-name>
    ```  
  - **Example**:  
    ```bash
    sudo systemctl restart nginx
    ```

- **Enable a Service**  
  - Configures the service to start automatically at system boot.  
  - **Command**:  
    ```bash
    sudo systemctl enable <service-name>
    ```  
  - **Example**:  
    ```bash
    sudo systemctl enable nginx
    ```

- **Disable a Service**  
  - Prevents the service from starting automatically at boot.  
  - **Command**:  
    ```bash
    sudo systemctl disable <service-name>
    ```  
  - **Example**:  
    ```bash
    sudo systemctl disable nginx
    ```








# Troubleshooting


| Issue                | Solution                                                           |
|----------------------|--------------------------------------------------------------------|
| Service won't start  | Use `journalctl -xe` to check logs                                 |
| Permission denied    | Ensure the command is run with `sudo`                              |
| Service not found    | Confirm the service is installed (`systemctl list-unit-files`)     |
| Changes not applied  | Use `systemctl daemon-reexec` or `systemctl daemon-reload`         |


# Conclusion 

This SOP provides a clear and consistent process for managing services on Ubuntu using the systemctl command. By following the outlined steps, users can efficiently start, stop, restart, enable, disable, and check the status of services, ensuring smooth operation of the system. 


# Contact Information

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|




# References

| Link                                                                 | Title / Description                             |
|----------------------------------------------------------------------|--------------------------------------------------|
| [https://www.linode.com/docs/guides/introduction-to-systemctl/](https://www.linode.com/docs/guides/introduction-to-systemctl/) | Introduction to systemctl and systemctl commands |
