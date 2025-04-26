![image](https://github.com/user-attachments/assets/b66a9e29-b167-4e32-bd6e-b33c8e8ab444)

| Author        | Date       | Version | Review Level   | Reviewer Name        |
|---------------|------------|---------|----------------|----------------------|
| Anitha Annem  | April 20   | v1.1    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  | April 24   | v2.1    | L0             | Khushi Malothra      |
| Anitha Annem  |            |         | L1             | Rishabh Sharma       |
| Anitha Annem  |            |         | L2             | piyush Upadhyay      |


# Table of Contents
1. [Introduction](#1-Introduction)
2. [ What is a Virtual Environment?](#2-what-is-a-virtual-environment)
3. [ Why Use a Virtual Environment?](#3-why-use-a-virtual-environment)
4. [ Purpose](#4-purpose)
5. [ Setting Up a Virtual Environment](#5-setting-up-a-virtual-environment)
6. [ Best Practices](#6-best-practices)
7. [Virtual Environment Set UP](#-virtual-environment-set-up)
8. [Conclusion](#7-conclusion)
9. [Contact Information](#8-Contact-information)
10. [ References](#9-references)


# 1. Introduction
This document covers what is virtual environment and why we are using and showing how to setup a virtual environment using python and some best practices 


# 2. What is a Virtual Environment?

A virtual environment is a self-contained directory that contains a Python interpreter and all required libraries for a specific project. It helps avoid global package installation and conflicts between projects.

For example:

- Project A needs Django 3.2

- Project B needs Django 4.0

A virtual environment allows both versions to coexist separately.


# 3. Why Use a Virtual Environment?

   - **Dependency Isolation** : Keep dependencies for each project separate.
   - **Avoid Conflicts** : Prevent version clashes between projects.
   - **Reproducibility** : Share exact project environments.
   - **Cleaner Setup** : Install only necessary dependencies.
   - **Easy Cleanup** : Remove environments when done.
   - **Enhanced Collaboration** : Share consistent setups with others.


# 4. Purpose

The purpose of a Python virtual environment is to:

- Provide an isolated space for Python projects.

- Prevent package version conflicts across different projects.

- Facilitate reproducibility and portability.

- Simplify development and deployment.


# 5. Setting Up a Virtual Environment

| Step  | Description                                | Command / Example                                                                 |
|-------|--------------------------------------------|------------------------------------------------------------------------------------|
| **1** | **Create a Virtual Environment**           | `python -m venv venv`                                                              |
|       | This creates a folder named `venv/`.       |                                                                                    |
|       | **Example Directory Structure:**           | ```myproject/ ├── venv/ ├── requirements.txt └── app.py```                         |
|       | You can rename `venv/`, but it's standard. |                                                                                    |
| **2** | **Activate the Environment (Windows)**     | `venv\Scripts\activate`                                                             |
|       | **Activate the Environment (macOS/Linux)** | `source venv/bin/activate`                                                          |
|       | **Example Terminal Prompt:**               | `(venv) user@machine:~/myproject$`                                                 |
|       | Shows you're inside the virtual environment.|                                                                                   |
| **3** | **Deactivate the Environment**             | `deactivate`                                                                       |
|       | Returns you to the system Python environment. |                                                                                   |



# 6. Best Practices 

| Best Practice                                      | Description                                                                                     |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Create one virtual environment per project         | Keep dependencies isolated to prevent conflicts and ensure consistent builds.                   |
| Add `venv/` to your `.gitignore` file              | Prevent committing environment files to version control.                                         |
| Use `requirements.txt` to track dependencies       | Use `pip freeze > requirements.txt` to list dependencies for sharing or deployment.              |
| Avoid installing unnecessary packages globally     | Always install project-specific packages inside a virtual environment.                          |
| Delete unused environments to free up space        | Clean up environments from old or unused projects to save disk space.                           |
| Use `deactivate` when switching contexts           | Deactivate the current environment before activating another to avoid conflicts.                |


# 7. Virtual Environment Set UP
 For setting UP Virtual environment Please refer this document.

[Python Virtual Environment](https://github.com/Cloud-NInja-snaatak/Documentation/blob/himanshu_scrum16/commonstack/applications/python/virtualenv/sop.md)






# 8. Conclusion

 virtualenv is an invaluable tool for Python development, providing a simple yet effective way to manage project-specific dependencies. By isolating each project into its own virtual environment, you can avoid conflicts between different package versions and ensure that each project remains reproducible and portable.



# 9. Contact Information

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


# 10. References

| Link                                                         | Description                              |
|--------------------------------------------------------------|------------------------------------------|
| [Python venv documentation](https://docs.python.org/3/library/venv.html) | Creation of virtual environments         |
| [Python venv tutorial](https://docs.python.org/3/tutorial/venv.html) | Documentation followed for this guide    |
