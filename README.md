

![image](https://github.com/user-attachments/assets/57b80e28-7839-41e6-a2b7-a946fc02966c)


| Author          | Created On  | Version   | Last Updated By | Last Edited On |
|-----------------|-------------|-----------|------------------|----------------|
| Anitha   | 2025-04-17  | Version 1 |Anitha | 2025-04-18     |


# Table of Contents 📑

1. [Purpose of Java](#purpose-of-java)


2. [Key Uses of Java](#key-uses-of-java)
3. [Java Development Kit (JDK)](#java-development-kit-jdk)
4. [Prerequisites](#prerequisites)
5. [Checking Existing Java Installation ](#checking-existing-java-installation-)
6. [Installing Java on Windows ](#installing-java-on-windows-)
7. [Installing Java on macOS ](#installing-java-on-macos-)
8. [Installing Java on Linux ](#installing-java-on-linux-)
9. [Troubleshooting Java Installation Issues ](#troubleshooting-java-installation-issues-)
10. [Contact Information](#contact-information)
11. [References ](#references-)





# Purpose of Java 🌍

Java is one of the most popular and versatile programming languages, widely used for building cross-platform applications. Below are some key areas where Java is essential:

# Key Uses of Java

**Web Applications 🌐**

Java powers many server-side applications, including websites and web services. The Spring Framework is one of the most popular Java-based frameworks for web development.

 **Mobile Applications 📱**

Java is the primary language for developing Android applications, making it essential for mobile app development.

**Desktop Applications 🖥️**

With JavaFX and Swing, Java allows developers to create powerful desktop applications with rich user interfaces.

**Embedded Systems 🏠**

Java is used in embedded systems such as IoT devices, smart cards, and appliances, thanks to its portability and scalability.

---

# Java Development Kit (JDK)

The **JDK** is a set of tools that enables developers to create Java applications. It includes:

- **JRE (Java Runtime Environment):** For running Java programs.
- **Java Compiler (javac):** Compiles Java source code into bytecode.
- **JVM (Java Virtual Machine):** Executes Java bytecode on different platforms, providing cross-platform compatibility.
- **Development Tools:** Includes utilities like `javadoc` for documentation and `jdb` for debugging.

---

# Prerequisites ⚙️

Before installing Java, ensure that you have the following:

| **Requirement**                              | **Details**                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| **Operating System**                         | A computer running **Windows**, **macOS**, or **Linux**.       |
| **Administrator/Root Access**                | You need **administrator** or **root access** to install Java and set environment variables. |
| **Internet Connection**                      | An **internet connection** is required to download the JDK.    |


# Checking Existing Java Installation 🔍

**Windows:**

1. Press Win + R, type cmd, and press Enter to open Command Prompt.

2. Type:

```bash
java -version
```

**Output:**

```bash
openjdk version "11.0.10" 2021-01-19
OpenJDK Runtime Environment (build 11.0.10+9)
OpenJDK 64-Bit Server VM (build 11.0.10+9, mixed mode)

```

**macOS:**

1. Open Terminal.

2. Type:

```bash
java -version
```

**Output:**

```bash
openjdk version "11.0.10" 2021-01-19
OpenJDK Runtime Environment (build 11.0.10+9)
OpenJDK 64-Bit Server VM (build 11.0.10+9, mixed mode)

```

**Linux:**

1. Open Terminal.

2. Type:

```bash
java -version
```

**Output:**

```bash
openjdk version "11.0.10" 2021-01-19
OpenJDK Runtime Environment (build 11.0.10+9)
OpenJDK 64-Bit Server VM (build 11.0.10+9, mixed mode)

```


# Installing Java on Windows 🪟

### 1. Download JDK 📥

- Visit the official Oracle JDK download page: [Oracle JDK Download](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Select **Windows** as your operating system.
- Download the JDK installer (e.g., `jdk-11.x.x_windows-x64_bin.exe`).

### 2. Install JDK on Windows 🔧

- Once the `.exe` file is downloaded, run it to start the installation process.
- Follow the installation wizard:
  - Choose the installation directory (the default path is usually fine, like `C:\Program Files\Java`).
- After the installation is complete, click **Close**.

### 3. Set JAVA_HOME and PATH Environment Variables 🛠️

#### A. Set `JAVA_HOME` Variable

- Open the **Start Menu** and search for **Environment Variables**.
- Select **Edit the system environment variables**.
- In the **System Properties** window, click the **Environment Variables** button.
- Under **System Variables**, click **New**:
  - **Variable Name:** `JAVA_HOME`
  - **Variable Value:** The path to your JDK installation (e.g., `C:\Program Files\Java\jdk-11.x.x`)

#### B. Update the `PATH` Variable

- In the **System Variables** section, scroll down and find the `Path` variable, then click **Edit**.
- In the **Edit Environment Variables** window, click **New** and add:

  ```bash
  %JAVA_HOME%\bin
  ```

# Installing Java on macOS 🍎

### 1. Download JDK 📥

- Go to the official [Oracle JDK download page](https://www.oracle.com/java/technologies/javase-jdk-downloads.html).
- Select **macOS** and download the appropriate `.dmg` installer:
  - `jdk-17_macos-x64_bin.dmg` for **Intel-based Macs**
  - `jdk-17_macos-aarch64_bin.dmg` for **Apple Silicon (M1/M2)**

### 2. Install the JDK 🔧

- Open the downloaded `.dmg` file.
- Double-click the `.pkg` installer inside.
- Follow the steps in the installation wizard.
- Once the installation is complete, the JDK will typically be installed in:

  ```swift
  /Library/Java/JavaVirtualMachines/
  ```

### 3. Set `JAVA_HOME` and Update `PATH` 🛠️

Open your Terminal and follow these steps:

#### A. Find the installed JDK path

Run the following command to get the installed JDK path:

```bash
/usr/libexec/java_home
```

That command will output the path to the JDK, like:

```bash
/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home
```

#### B. Set `JAVA_HOME` and update your `PATH`

Add the following lines to your shell profile file:

- For **zsh** (default in macOS Catalina and later): `~/.zshrc`
- For **bash**: `~/.bash_profile`

```bash
export JAVA_HOME=$(/usr/libexec/java_home)
export PATH=$JAVA_HOME/bin:$PATH
```

Then run:

```bash
source ~/.zshrc  # or ~/.bash_profile
```

# Installing Java on Linux 🐧

### 1. Download JDK (Linux) 📥

For most Linux distributions, you can install Java directly using the system's package manager.

Alternatively, you can download the JDK manually from the official [Oracle JDK Download](https://www.oracle.com/java/technologies/javase-jdk-downloads.html) page.

### 2. Install JDK on Linux 🔧

#### For Ubuntu/Debian:

1. **Update the package index**:

   ```bash
   sudo apt update
   ```

2. **Install Java**:

   Run the following command to install **OpenJDK 11**:

   ```bash
   sudo apt install openjdk-11-jdk
   ```
#### For Fedora/CentOS/RHEL:

1. **Update the package index**:

   ```bash
   sudo dnf update
   ```

2. **Install Java**:

   Run the following command to install **OpenJDK 11**:

   ```bash
   sudo dnf install java-11-openjdk
   ```

### 3. Set `JAVA_HOME` and `PATH` Environment Variables (Linux) 🛠️

1. Open **Terminal**.

2. Add the following lines to your `~/.bashrc` or `~/.bash_profile` file:

   ```bash
   export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
   export PATH=$JAVA_HOME/bin:$PATH
   ```

3. **Apply the changes**:

   Run the following command to apply the changes:

   ```bash
   source ~/.bashrc   # Or `source ~/.bash_profile` depending on your shell
   ```

# Troubleshooting Java Installation Issues ⚠️

| **Issue** | **Possible Causes** | **Solutions** |
|-----------|---------------------|--------------|
| **Java is Not Recognized** ❌ | JAVA_HOME or PATH environment variables are not set correctly. | - Check if `JAVA_HOME` is set correctly.<br>- Ensure the `PATH` variable includes `%JAVA_HOME%\bin` (Windows) or `$JAVA_HOME/bin` (macOS/Linux). |
| **Permission Errors During Installation** 🔒 | Insufficient permissions for installing software. | - On Windows, ensure you are using an Administrator account to install.<br>- On macOS/Linux, use `sudo` for installation (e.g., `sudo apt install openjdk-11-jdk`). |
| **JDK Version Mismatch** 🔄 | An older version of Java might be installed. | - Download the latest version of the JDK from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-jdk-downloads.html).<br>- If using an older version, uninstall it and install the latest version. |
| **Java Not Running After Installation (Linux)** 🚫 | Incorrect `JAVA_HOME` path or `java` command location. | - Check the `JAVA_HOME` path to ensure it points to the correct JDK directory.<br>- Verify the location of `java` with the command: `which java` and ensure it's the correct version. |
| **Unable to Download JDK** 📥 | Network issues, or Oracle website is down. | - Check your internet connection.<br>- Try downloading the JDK from a different network or use an alternative mirror for JDK downloads. |
| **Incompatible JDK Version** ⚠️ | JDK version incompatible with your project requirements. | - Ensure the version of JDK you're installing matches the version needed for your project (e.g., Java 8 vs. Java 11).<br>- If you're working with legacy applications, consider installing Java 8 (JDK 1.8). |



# 📧 Contact Information

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


# References 📚

| **Resource**                        | **Description**                                                                                     | **Link**                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **Oracle JDK Download Page**        | Download the latest version of the Java Development Kit (JDK).                                       | [Oracle JDK Download](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)       |
| **Official Java Documentation**     | Access the official Java documentation for in-depth details about Java API and usage.              | [Oracle Java Documentation](https://docs.oracle.com/en/java/)                                      |
| **OpenJDK**                         | Open-source implementation of the Java Platform, Standard Edition.                                  | [OpenJDK official website](https://openjdk.java.net/)                                             |







