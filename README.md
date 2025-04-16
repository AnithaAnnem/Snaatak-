![image](https://github.com/user-attachments/assets/394cd790-db18-404a-93b7-7885f63b727d)

## 📂 Document Info

| Author          | Created On  | Version   | Last Updated By | Last Edited On |
|-----------------|-------------|-----------|------------------|----------------|
| Annem Anitha | 2025-04-16  | Version 1 |Annem Anitha | 2025-04-16     |


## 📖 Table of Contents


1. **Purpose**
2. **What is a Virtual Environment?**
3. **Why Use a Virtual Environment**
4. **Prerequisites**
5. **Setting Up a Virtual Environment**
6. **Managing Dependencies**
7. **Best Practices**
8. **Common Issues & Troubleshooting**
9. **References**



## 1. 🎯 Purpose

The purpose of a Python virtual environment is to:

- Provide an isolated space for Python projects.

- Prevent package version conflicts across different projects.

- Facilitate reproducibility and portability.

- Simplify development and deployment.


## 2. 📦 What is a Virtual Environment?

A virtual environment is a self-contained directory that contains a Python interpreter and all required libraries for a specific project. It helps avoid global package installation and conflicts between projects.

For example:

- Project A needs Django 3.2

- Project B needs Django 4.0

A virtual environment allows both versions to coexist separately.

## 3. ✅ Why Use a Virtual Environment?

   - **Dependency Isolation** 🧩: Keep dependencies for each project separate.
   - **Avoid Conflicts** 🚫: Prevent version clashes between projects.
   - **Reproducibility** 🔄: Share exact project environments.
   - **Cleaner Setup** 🧹: Install only necessary dependencies.
   - **Easy Cleanup** 🗑️: Remove environments when done.
   - **Enhanced Collaboration** 🤝: Share consistent setups with others.


## 4. ⚙️  Prerequisites (with System Requirements)

Before setting up a Python virtual environment, make sure your system meets the following requirements:

| **Component**             | **Requirement**                  | **How to Install / Check**                                                                                                                                           |
|--------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operating System**     | Windows / macOS / Linux          | Any OS that supports Python 3.3+                                                                                                                                     |
| **Python Version**       | Python 3.3 or newer              | 🔹 **Check**: `python --version` or `python3 --version`  <br> 🔹 **Install**: [Download from python.org](https://www.python.org/downloads/)                          |
| **pip (Python Installer)**| Comes with Python 3.4+ or install manually | 🔹 **Check**: `pip --version` <br> 🔹 **Install (if missing)**: `python -m ensurepip --upgrade` or follow the [Pip Installation Guide](https://pip.pypa.io/en/stable/installation/) |
| **venv module**          | Included with Python 3.3+        | 🔹 No extra install needed if Python 3.3+ is installed                                                                                                               |
| **Terminal / CLI**       | Any terminal (cmd, bash, PowerShell, etc.) | Default with all OS. Use: <br> - **Command Prompt / PowerShell** (Windows) <br> - **Terminal** (macOS/Linux)                                                        |
| **Text Editor or IDE** *(Optional)* | VS Code, PyCharm, Sublime, etc. | 🔹 [VS Code](https://code.visualstudio.com/) <br> 🔹 [PyCharm](https://www.jetbrains.com/pycharm/)                                                                   |

  ## 📜 Summary of Installation Commands
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
  
   **📦 Install pip (if missing)**
    ```bash
    python -m ensurepip --upgrade
    ```
   **Example Output:**
   ```bash
   Looking in links: ...
   Installing collected packages: pip
   Successfully installed pip-23.2.1
   ```

  **⬆️ Upgrade pip (Recommended)**
Before installing dependencies, it's recommended to upgrade `pip` to the latest version:

```bash
python -m pip install --upgrade pip
```

**Example Output:**
   ```bash
 Successfully installed pip-24.0

   ```

**🐧 Install Python on Linux (Ubuntu/Debian)**
```bash
sudo apt update
sudo apt install python3 python3-venv python3-pip
```
**Check Installation:**
```bash
python3 --version
pip3 --version
```

**🍎 Optional: Install Python on macOS via Homebrew**
Requires Homebrew. Install Homebrew if not already installed.
```bash
brew install python
```

**Check Installation:**
```bash
python3 --version
pip3 --version
```
## 5. 🧪 Setting Up a Virtual Environment

**🔹 Step 1: Create a Virtual Environment**
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

**🔹 Step 2: Activate the Environment**

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

**🔹 Step 3: Deactivate the Environment**

To leave the virtual environment:

```bash
deactivate
```

## 6. 📦 Managing Dependencies

🔸 **Install Packages**
  You're demonstrating how to install Python packages inside the virtual environment using pip. Any package installed while the virtual environment is active will only be available within that environment, keeping your global Python environment clean and free from project-specific packages.

```bash
pip install flask
```
**What you're doing here:** You're installing the Flask package within the virtual environment. The Flask framework will be available only in this environment and won’t interfere with other projects.

🔸 **Freeze Installed Packages**
 This step shows how to create a list of the exact versions of all installed packages within your virtual environment. The command pip freeze generates a list of installed packages and their specific versions, which can then be saved to a file called requirements.txt.

```bash
pip freeze > requirements.txt
```

**What you're doing here:** You’re saving the current state of all installed packages and their versions to a requirements.txt file. This ensures that anyone else working on the project can install the exact same dependencies with the exact same versions, making your environment reproducible.

🔸 **Install from requirements.txt**
 If you have a requirements.txt file (e.g., shared with others or stored in version control), this command will install all the dependencies listed in that file. This is especially useful when setting up the project on a new machine or environment.

```bash
pip install -r requirements.txt
```
**What you're doing here:** You’re using the requirements.txt file to install all the dependencies that are required for the project. This command ensures that the exact versions of the packages specified in the file are installed.

## 7. 🧭 Best Practices

✅ **Create one virtual environment per project**  
Keep dependencies isolated to prevent conflicts and ensure reproducibility.

📁 **Add `venv/` to your `.gitignore` file**  
Avoid committing the virtual environment to version control.

📌 **Use `requirements.txt` to track dependencies**  
Generate it with `pip freeze > requirements.txt` and share it with your team or use for deployment.

📦 **Avoid installing unnecessary packages globally**  
Always install project-specific packages inside the virtual environment.

🧹 **Delete unused environments to free space**  
Clean up environments for old or completed projects to save disk space.

🧪 **Use `deactivate` when switching contexts**  
Don’t forget to deactivate the current environment before activating another.

## 8.❗ Common Issues & Troubleshooting

| Issue                             | Solution                                                                 |
|----------------------------------|--------------------------------------------------------------------------|
| `command not found: python`      | Use `python3` instead                                                    |
| `pip not recognized`             | Ensure Python and pip are added to your system's PATH                   |
| Activation doesn’t work on macOS | Use `chmod +x` to give execution permission to the activate script       |
| Can't activate on Windows        | Use PowerShell and run:<br>`Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` |

## 📧 Contact Information

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


## 9. 📚 References

| Link                                                         | Description                              |
|--------------------------------------------------------------|------------------------------------------|
| [Python venv documentation](https://docs.python.org/3/library/venv.html) | Creation of virtual environments         |
| [Python venv tutorial](https://docs.python.org/3/tutorial/venv.html) | Documentation followed for this guide    |


















  






