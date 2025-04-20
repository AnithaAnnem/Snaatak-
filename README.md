
 ![image](https://github.com/user-attachments/assets/f8d1e015-f9cb-4c1e-933e-22e6262b0c69)



|**Date**| **Version**| **Description**| **Changed By** |
|----------|---------|---------------|-----------------|
|**April 15** | v.1.0 | Initial Draft | Anitha Annem |
|**April 19** | v.1.1 | Updated sop_services.md | Anitha Annem |
|**April 20** | v.1.2 | Updated sop_services.md | Anitha Annem |


# Table of Contents
  1. [Introduction](#Introduction)

  2. [ Purpose](#-purpose)

  3. [ Prerequisites](#️-prerequisites)

  4. [ Definitions](#-definitions)

  5. [ Service Management Commands with systemctl](#-service-management-commands-with-systemctl)

  6. [ Troubleshooting](#troubleshooting)

  7.  [conclusion](#conclusion)

  8. [ Contact Information](#-contact-information)

  9. [ References](#-references)


# **Standard Operating Procedure (SOP): Managing Services on Ubuntu with systemctl**

# Introduction

In this documentation The SOP provides a clear and consistent process for managing services on Ubuntu using the systemctl command. 


# What is SOP ?

SOP stands for Standard Operating Procedure.
It is a written document that gives clear, step-by-step instructions on how to perform a specific task or process.

It's like a guide or manual that ensures things are done correctly, safely, and consistently every time.


# Why SOP ?

 - Ensures Consistency Across Operations
 - Improves Efficiency and Productivity
 - Enhances Safety and Reduces Risk



# Purpose

This SOP provides standardized procedures for managing services (start, stop, restart, enable, disable, check status) on Ubuntu OS.




# Prerequisites

To ensure the successful management of the service on Ubuntu, the following prerequisites must be met:


| Requirement       | Description                                                      |
|------------------|------------------------------------------------------------------|
| Ubuntu Version    | Ubuntu 16.04 or later (Recommended: 20.04, 22.04, or newer)      |
| systemd           | Must be installed (default from Ubuntu 15.04+)                   |
| Sudo Privileges   | User must have sudo access to manage services                    |
| Installed Services| The service (e.g., nginx, mysql) should be installed beforehand  |
| Terminal Access   | Access via SSH or local terminal                                 |











# Definitions



| Term     | Description                                           |
|----------|-------------------------------------------------------|
| systemd  | The system and service manager used in Ubuntu         |
| Service  | A background process (e.g., Apache, MySQL)            |






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


# conclusion 

This SOP provides a clear and consistent process for managing services on Ubuntu using the systemctl command. By following the outlined steps, users can efficiently start, stop, restart, enable, disable, and check the status of services, ensuring smooth operation of the system. The procedures promote consistency, improve productivity, and reduce the risk of errors during service management tasks.
With proper prerequisites met and troubleshooting tips in place, this SOP serves as a reliable guide for both new and experienced users to maintain and manage services on Ubuntu systems effectively.



# Contact Information

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|




# References

| Link                                                                 | Title / Description                             |
|----------------------------------------------------------------------|--------------------------------------------------|
| [https://www.linode.com/docs/guides/introduction-to-systemctl/](https://www.linode.com/docs/guides/introduction-to-systemctl/) | Introduction to systemctl and systemctl commands |
