

![image](https://github.com/user-attachments/assets/57b80e28-7839-41e6-a2b7-a946fc02966c)


| Author        | Date       | Version | Review Level   | Reviewer Name        |
|---------------|------------|---------|----------------|----------------------|
| Anitha Annem  | April 20   | v1.1    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  | April 24   | v2.1    | L0             | Khushi Malothra      |
| Anitha Annem  |            |         | L1             | Rishabh Sharma       |
| Anitha Annem  |            |         | L2             | piyush Upadhyay      |


# Table of Contents 

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [What is Java?](#what-is-java?)
4. [Installing Java on macOS ](#installing-java-on-macos)
5. [Installing Java on Linux ](#installing-java-on-linux)
6. [Troubleshooting Java Installation Issues ](#troubleshooting-java-installation-issues)
7. [Conclusion](#conclusion)
8. [Contact Information](#contact-information)
9. [References ](#references)



# Introduction 
This document covers the stp by step installation of the java in different operating systems and configurig environment variables

# What is Java?
Java is a high-level object oriented programming language

For more related to java introduction refer this link  

[Java Introduction](https://github.com/Cloud-NInja-snaatak/Documentation/blob/aniruddh_scrum23/commonstack/applications/java/introduction/intro.md)



# Prerequisites 

Before installing Java, ensure that you have the following:

| **Requirement**                              | **Details**                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| **Operating System**                         | A computer running **Windows**, **macOS**, or **Linux**.       |
| **Administrator/Root Access**                | You need **administrator** or **root access** to install Java and set environment variables. |
| **Internet Connection**                      | An **internet connection** is required to download the JDK.    |





# Installing Java on macOS 

 ### 1. Check if Java is Already Installed

Before proceeding with the installation of Java, it's a good idea to first check if it's already installed on your system.

1. Open the **Terminal** application. You can find it under **Applications > Utilities**, or simply search for it using **Spotlight**.
2. In the Terminal window, type the following command and press **Enter**:

    ```bash
    java -version
    ```

3. If Java is installed, you'll see output displaying the installed version of Java. For example, you might see something like this:

    ```bash
    java version "1.8.0_261"
    Java(TM) SE Runtime Environment (build 1.8.0_261-b12)
    Java HotSpot(TM) 64-Bit Server VM (build 25.261-b12, mixed mode)
    ```

    If Java is not installed, you will receive a message indicating that the command is not recognized or that Java is not found on your system.

### 2. Install Java (JDK)

## Option 1. Install Java Using Homebrew (Recommended)

If you don't have Homebrew installed, you can install it by running the following command in Terminal:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

This installs Homebrew, a package manager that makes it easier to install software like Java.

## 2. Once Homebrew is installed, run the following command to install Java:

```bash
brew install openjdk@17
```

## 3. After installation is complete, you need to configure Java in your shell profile. 

Add the following lines to your `~/.zshrc` (or `~/.bash_profile` if you're using Bash) to set the Java environment variables:

```bash
export PATH="/usr/local/opt/openjdk@17/bin:$PATH"
export JAVA_HOME=$(/usr/libexec/java_home -v 17)
```

## 4.Apply the changes by running the following command:

```bash
source ~/.zshrc
```





# Installing Java on Linux 

### 1. Download JDK (Linux) 

For most Linux distributions, you can install Java directly using the system's package manager.

Alternatively, you can download the JDK manually from the official [Oracle JDK Download](https://www.oracle.com/java/technologies/javase-jdk-downloads.html) page.

### 2. Install JDK on Linux 

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

### 3. Set `JAVA_HOME` and `PATH` Environment Variables (Linux) 

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

# Troubleshooting Java Installation Issues 

| **Issue** | **Possible Causes** | **Solutions** |
|-----------|---------------------|--------------|
| **Java is Not Recognized**  | JAVA_HOME or PATH environment variables are not set correctly. | - Check if `JAVA_HOME` is set correctly.<br>- Ensure the `PATH` variable includes `%JAVA_HOME%\bin` (Windows) or `$JAVA_HOME/bin` (macOS/Linux). |
| **Permission Errors During Installation**  | Insufficient permissions for installing software. | - On Windows, ensure you are using an Administrator account to install.<br>- On macOS/Linux, use `sudo` for installation (e.g., `sudo apt install openjdk-11-jdk`). |
| **JDK Version Mismatch**  | An older version of Java might be installed. | - Download the latest version of the JDK from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-jdk-downloads.html).<br>- If using an older version, uninstall it and install the latest version. |
| **Java Not Running After Installation (Linux)**  | Incorrect `JAVA_HOME` path or `java` command location. | - Check the `JAVA_HOME` path to ensure it points to the correct JDK directory.<br>- Verify the location of `java` with the command: `which java` and ensure it's the correct version. |
| **Unable to Download JDK**  | Network issues, or Oracle website is down. | - Check your internet connection.<br>- Try downloading the JDK from a different network or use an alternative mirror for JDK downloads. |
| **Incompatible JDK Version**  | JDK version incompatible with your project requirements. | - Ensure the version of JDK you're installing matches the version needed for your project (e.g., Java 8 vs. Java 11).<br>- If you're working with legacy applications, consider installing Java 8 (JDK 1.8). |


# Conclusion

Java is a powerful, platform-independent programming language that continues to play a crucial role in software development across various domains—ranging from web and mobile applications to desktop software and embedded systems.


#  Contact Information 

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


# References 

| **Resource**                        | **Description**                                                                                     | **Link**                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **Oracle JDK Download Page**        | Download the latest version of the Java Development Kit (JDK).                                       | [Oracle JDK Download](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)       |
| **Official Java Documentation**     | Access the official Java documentation for in-depth details about Java API and usage.              | [Oracle Java Documentation](https://docs.oracle.com/en/java/)                                      |
| **OpenJDK**                         | Open-source implementation of the Java Platform, Standard Edition.                                  | [OpenJDK official website](https://openjdk.java.net/)                                             |




