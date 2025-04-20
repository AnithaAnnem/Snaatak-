![image](https://github.com/user-attachments/assets/394cd790-db18-404a-93b7-7885f63b727d)

|**Date**| **Version**| **Description**| **Changed By** |
|----------|---------|---------------|-----------------|
|April 16 | v.1.0 | Initial Draft | Anitha Annem |
|April 19 | v.1.1 | Updated documentation.md | Anitha Annem |
|April 20 | v.1.2 | Updated documentation.md | Anitha Annem | 


# Table of Contents
1. [Introduction](#Introduction)
2. [ What is a Virtual Environment?](#1--what-is-a-virtual-environment)
3. [ Why Use a Virtual Environment?](#2--why-use-a-virtual-environment)
4. [ Purpose](#3--purpose)
5. [ Prerequisites](#4--prerequisites-with-system-requirements)
6. [ Setting Up a Virtual Environment](#5--setting-up-a-virtual-environment)
7. [ Best Practices](#7--best-practices)
8. [ Common Issues & Troubleshooting](#8-common-issues--troubleshooting)
9. [conclusion](#conclusion)
10. [Contact](#Contact)
11. [ References](#9--references)


# Introduction


# 1.  What is a Virtual Environment?

A virtual environment is a self-contained directory that contains a Python interpreter and all required libraries for a specific project. It helps avoid global package installation and conflicts between projects.

For example:

- Project A needs Django 3.2

- Project B needs Django 4.0

A virtual environment allows both versions to coexist separately.


# 2. Why Use a Virtual Environment?

   - **Dependency Isolation** : Keep dependencies for each project separate.
   - **Avoid Conflicts** : Prevent version clashes between projects.
   - **Reproducibility** : Share exact project environments.
   - **Cleaner Setup** : Install only necessary dependencies.
   - **Easy Cleanup** : Remove environments when done.
   - **Enhanced Collaboration** : Share consistent setups with others.


# 3. Purpose

The purpose of a Python virtual environment is to:

- Provide an isolated space for Python projects.

- Prevent package version conflicts across different projects.

- Facilitate reproducibility and portability.

- Simplify development and deployment.






## 4.  Prerequisites (with System Requirements)

Before setting up a Python virtual environment, make sure your system meets the following requirements:

| **Component**             | **Requirement**                  | **How to Install / Check**                                                                                                                                           |
|--------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operating System**     | Windows / macOS / Linux          | Any OS that supports Python 3.3+                                                                                                                                     |
| **Python Version**       | Python 3.3 or newer              | 🔹 **Check**: `python --version` or `python3 --version`  <br> 🔹 **Install**: [Download from python.org](https://www.python.org/downloads/)                          |
| **pip (Python Installer)**| Comes with Python 3.4+ or install manually | 🔹 **Check**: `pip --version` <br> 🔹 **Install (if missing)**: `python -m ensurepip --upgrade` or follow the [Pip Installation Guide](https://pip.pypa.io/en/stable/installation/) |
| **venv module**          | Included with Python 3.3+        | 🔹 No extra install needed if Python 3.3+ is installed                                                                                                               |
| **Terminal / CLI**       | Any terminal (cmd, bash, PowerShell, etc.) | Default with all OS. Use: <br> - **Command Prompt / PowerShell** (Windows) <br> - **Terminal** (macOS/Linux)                                                        |
| **Text Editor or IDE** *(Optional)* | VS Code, PyCharm, Sublime, etc. | 🔹 [VS Code](https://code.visualstudio.com/) <br> 🔹 [PyCharm](https://www.jetbrains.com/pycharm/)  

##  Summary of Installation Commands
    here are the key installation/check commands:

  **Check if Python is Installed**
  ```bash
  python --version
  # or
  python3 --version
   ```

   **Example Output:**
   ```bash
   Python 3.10.12

   ```

   If you get a "command not found" error, Python is likely not installed.


   ** Install pip (if missing)**
   ```bash
    python -m ensurepip --upgrade
   ```


   **Example Output:**

   ```bash
   Looking in links: ...
   Installing collected packages: pip
   Successfully installed pip-23.2.1

   ```

  **Upgrade pip (Recommended)**

Before installing dependencies, it's recommended to upgrade `pip` to the latest version:

```bash
python -m pip install --upgrade pip
```

**Example Output:**
   ```bash
 Successfully installed pip-24.0

   ```

**Install Python on Linux (Ubuntu/Debian)**
```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip
```
**Check Installation:**
```bash
python3 --version
pip3 --version
```

**Optional: Install Python on macOS via Homebrew**
Requires Homebrew. Install Homebrew if not already installed.
```bash
brew install python
```

**Check Installation:**
```bash
python3 --version
pip3 --version
```
## 5. Setting Up a Virtual Environment

**Step 1: Create a Virtual Environment**
```bash
python -m venv venv
```
This will create a folder called venv/ in your project directory.

**Example:**
Once you run the above command, your project directory will look like this:

```bash
myproject/
│
├── venv/                # This is the virtual environment folder
├── requirements.txt     # Example of a file where you can list your dependencies
└── app.py               # Your main Python file (or any other files for your project)
```


You can rename venv to anything, but venv is a common convention.

**Step 2: Activate the Environment**

**Windows:**
```bash
venv\Scripts\activate
```
**macOS / Linux:**
```bash
source venv/bin/activate
```

**Example:**

Once activated, your terminal prompt will change to show the name of the virtual environment, like this:
```bash
(venv) user@machine:~/myproject$
```
This indicates that you are now working within the venv virtual environment. The (venv) part shows that the virtual environment is active.

**Step 3: Deactivate the Environment**

To leave the virtual environment:

```bash
deactivate
```



## 6. Best Practices

 **Create one virtual environment per project**
Keep dependencies isolated to prevent conflicts and ensure reproducibility.

 **Add `venv/` to your `.gitignore` file**
Avoid committing the virtual environment to version control.

 **Use `requirements.txt` to track dependencies**
Generate it with `pip freeze > requirements.txt` and share it with your team or use for deployment.

 **Avoid installing unnecessary packages globally**
Always install project-specific packages inside the virtual environment.

 **Delete unused environments to free space**
Clean up environments for old or completed projects to save disk space.

 **Use `deactivate` when switching contexts**
Don’t forget to deactivate the current environment before activating another.


# 7. Common Issues & Troubleshooting

| Issue                             | Solution                                                                 |
|----------------------------------|--------------------------------------------------------------------------|
| `command not found: python`      | Use `python3` instead                                                    |
| `pip not recognized`             | Ensure Python and pip are added to your system's PATH                   |
| Activation doesn’t work on macOS | Use `chmod +x` to give execution permission to the activate script       |
| Can't activate on Windows        | Use PowerShell and run:<br>`Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` |



# conclusion

 virtualenv is an invaluable tool for Python development, providing a simple yet effective way to manage project-specific dependencies. By isolating each project into its own virtual environment, you can avoid conflicts between different package versions and ensure that each project remains reproducible and portable. This not only helps with version control but also streamlines collaboration and deployment.




# Contact 

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


# 8. References

| Link                                                         | Description                              |
|--------------------------------------------------------------|------------------------------------------|
| [Python venv documentation](https://docs.python.org/3/library/venv.html) | Creation of virtual environments         |
| [Python venv tutorial](https://docs.python.org/3/tutorial/venv.html) | Documentation followed for this guide    |
