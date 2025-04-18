

![image](https://github.com/user-attachments/assets/57b80e28-7839-41e6-a2b7-a946fc02966c)


## 📂 Document Info

| Author   | Created on | Version  | Last Edited On | Internal-Reviewer | L0-Reviewer  | L1-Reviewer | L2-Reviewer  | 
|----------|------------|----------|----------------|-------------------|--------------|-------------|--------------|
| Anitha  | 16-04-25   | version 1| 18-04-25       | priyanshu     | Khushi| mukul joshi | Piyush upadyay |


# Table of Contents 📑

1. [Purpose of Java](#purpose-of-java)
2. [Key Uses of Java](#key-uses-of-java)
3. [Java Development Kit (JDK)](#java-development-kit-jdk) 
4. [Prerequisites](#prerequisites)
5. [Checking Existing Java Installation ](#checking-existing-java-installation-)
6. [Installing Java on macOS ](#installing-java-on-macos-)
7. [Installing Java on Linux ](#installing-java-on-linux-)
8. [Troubleshooting Java Installation Issues ](#troubleshooting-java-installation-issues-)
9. [Contact Information](#contact-information)
10. [References ](#references-)





# Purpose of Java 

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




# Prerequisites 

Before installing Java, ensure that you have the following:

| **Requirement**                              | **Details**                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| **Operating System**                         | A computer running **Windows**, **macOS**, or **Linux**.       |
| **Administrator/Root Access**                | You need **administrator** or **root access** to install Java and set environment variables. |
| **Internet Connection**                      | An **internet connection** is required to download the JDK.    |










# Installing Java on macOS 🍎

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

## 3. After installation is complete, you need to configure Java in your shell profile. Add the following lines to your `~/.zshrc` (or `~/.bash_profile` if you're using Bash) to set the Java environment variables:

```bash
export PATH="/usr/local/opt/openjdk@17/bin:$PATH"
export JAVA_HOME=$(/usr/libexec/java_home -v 17)
```

## 4.Apply the changes by running the following command:

```bash
source ~/.zshrc
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



#  Contact Information 

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


# References 📚

| **Resource**                        | **Description**                                                                                     | **Link**                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **Oracle JDK Download Page**        | Download the latest version of the Java Development Kit (JDK).                                       | [Oracle JDK Download](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)       |
| **Official Java Documentation**     | Access the official Java documentation for in-depth details about Java API and usage.              | [Oracle Java Documentation](https://docs.oracle.com/en/java/)                                      |
| **OpenJDK**                         | Open-source implementation of the Java Platform, Standard Edition.                                  | [OpenJDK official website](https://openjdk.java.net/)                                             |




