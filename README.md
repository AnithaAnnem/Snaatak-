

![image](https://github.com/user-attachments/assets/73592ff1-ac7d-4181-ab9c-69b65b39ed33)

| Author        | Date       | Version | Review Level   | Reviewer Name        |
|---------------|------------|---------|----------------|----------------------|
| Anitha Annem  | April 20   | v1.1    | Pre-Reviewer   | Priyanshu            |
| Anitha Annem  | April 24   | v2.1    | L0             | Khushi Malothra      |
| Anitha Annem  |            |         | L1             | Rishabh Sharma       |
| Anitha Annem  |            |         | L2             | piyush Upadhyay      |




## Continuous Deployment (CD) Workflow with Ansible Playbook 


##  Table of Contents
- [Introduction](#introduction)
- [What is an Ansible Playbook?](#what-is-an-ansible-playbook)
- [What is a CD (Continuous Deployment) Workflow?](#what-is-a-cd-continuous-deployment-workflow)
- [CD Workflow Using Ansible Playbook – Step-by-Step](#cd-workflow-using-ansible-playbook--step-by-step)
  - [ Code Checkout and Branching](#code-checkout-and-branching)
  - [ Build and Package the Application](#build-and-package-the-application)
  - [ Deploying the Application to Staging](#deploying-the-application-to-staging)
  - [ Testing the Staging Environment](#testing-the-staging-environment)
  - [ Approval and Production Deployment](#approval-and-production-deployment)
- [Using tags with playbook](#using-tags-with-playbook)
- [Contact Information](#-contact-information)
- [References](#-references)

# Introduction 

This document provides an overview of setting up a Continuous Deployment (CD) Workflow using Ansible Playbooks.The playbooks also utilize tags to selectively run specific tasks, providing flexibility in managing the deployment pipeline. 


# **What is an Ansible Playbook?**  

An Ansible Playbook is a YAML file that defines a set of automation tasks to be run on remote systems. It tells Ansible what to do, where to do it, and how.

Introduction to Ansible Playbook

For more related to the Ansible Playbook Refer this link 
[Ansible Playbook](https://github.com/Cloud-NInja-snaatak/Documentation/blob/aditya_scrum49/commonstack/ansible/playbook/intro.md)


# **What is a CD (Continuous Deployment) Workflow?**  

Continuous Deployment (CD) is the process of automatically deploying every change that passes tests and builds into production. No human intervention is required after the CI (Continuous Integration) process.

#  **CD Workflow Using Ansible Playbook – Step-by-Step**  

Here’s how you can implement a CD pipeline using Ansible:

![image](https://github.com/user-attachments/assets/cf6db3ec-8578-4900-ae05-7231e45892e2)



##  Code Checkout and Branching

In this first stage, the goal is to get the latest version of the code from a repository (e.g., GitHub, GitLab) and place it in the correct environment.

### Tasks in this stage:
- **Checkout the Latest Code**: This is where you pull the latest changes from the appropriate branch (e.g., main, develop, or a feature branch).
  
- **Branch Handling**: Depending on the CD pipeline and your branching strategy (e.g., Git Flow or Trunk-based development), you may need to select the correct branch to deploy. Often, the staging branch is merged first into the main branch for production deployment.



##  Build and Package the Application

After checking out the latest code, the next step is to build or package the application. This could involve compiling code, building a frontend app, creating Docker images, or preparing deployment artifacts.

### Tasks in this stage:
- **Compile and Build**: If you're working with Java, Node.js, or another compiled language, you'll want to compile the source code.

- **Package**: Some applications need to be packaged into a deployable artifact, like a .tar.gz file, .deb, .rpm, Docker image, or .zip archive.

- **Install Dependencies**: This often includes installing libraries or tools the application needs to run (e.g., `npm install`, `pip install`, etc.).


##  Deploying the Application to Staging

Once the code is built and packaged, the next step is to deploy the application to the staging environment. The staging environment mimics production, but it’s a safe place for testing without affecting actual users.

### Tasks in this stage:
- **Deploying Artifacts**: This could involve copying files, Docker images, or any other form of deployment.
  
- **Service Restart**: If needed, you may need to restart web servers, background workers, or other services that serve the application.





##  Testing the Staging Environment

Once the application is deployed to the staging environment, you want to test it to ensure that everything is working as expected. This can be both automated tests (unit, integration) or manual tests.

### Tasks in this stage:
- **Automated Testing**: Running unit tests, integration tests, or end-to-end tests in staging.

- **Health Checks**: Ensuring that the application is up and running and accessible via the correct ports.

- **Smoke Tests**: These are simple checks to confirm that the basic functionality of the app is working, like checking if the homepage loads.



##  Approval and Production Deployment

Once the application passes all tests in the staging environment, the deployment can move to production. However, before deploying to production, there is often an approval step where a team member or the system itself approves the deployment.

### Tasks in this stage:
- **Approval Process**: A manual approval step (via a CI/CD tool interface or automatic based on conditions).
  
- **Production Deployment**: Deploy the application to the production servers after approval.

## Summary of Testing Workflow

| **Stage**                          | **Testing Type**             | **Purpose**                                               |
|-------------------------------------|------------------------------|-----------------------------------------------------------|
| **Code Checkout and Branching**     | Linting / Static Code Analysis | Ensure code style and structure are correct before proceeding |
|                                     | Unit Testing                 | Verify individual components/functions work as expected    |
|                                     | Dependency Audit             | Check for known vulnerabilities in packages                |
| **Build and Package Application**   | Build Verification           | Ensure code compiles/builds without errors                 |
|                                     | Integration Testing          | Validate interaction between modules or services           |
| **Deploying to Staging**            | Smoke Testing                | Confirm app runs and critical paths are working            |
|                                     | Service Validation           | Ensure Nginx, database, or backend APIs are responding correctly |
| **Testing the Staging Environment** | End-to-End (E2E) Testing     | Test complete flows from the user's perspective           |
|                                     | Regression Testing           | Confirm new changes don’t break existing features          |
|                                     | Health Checks                | Automated checks for uptime, response time, etc.           |
| **Approval & Prod Deployment**     | Final Sanity / Smoke Tests   | Lightweight manual or automated check before final deployment |





# Using tags with playbook



```yaml

- name: CD Workflow Playbook
  hosts: web_servers
  become: yes

  tasks:

    - name: Provision servers
      include_role:
        name: provision
      tags: provision

    - name: Configure system settings
      include_role:
        name: configure
      tags: configure

    - name: Deploy application
      include_role:
        name: deploy
      tags: deploy

    - name: Run post-deployment verification
      include_role:
        name: post_deploy
      tags: post-deploy

    - name: Rollback on failure
      include_role:
        name: rollback
      when: deploy_failed is defined and deploy_failed
      tags: rollback
  ```



#  Contact Information

| Name       | Email Address                |
|------------|------------------------------|
| Anitha     |anitha.annem.snaatak@mygurukulam.co|


#  References

| Link | Description |
|------|-------------|
| [https://faun.pub/5-ansible-playbooks-you-cant-live-without-in-your-ci-cd-pipeline-140549f3abcb](https://faun.pub/5-ansible-playbooks-you-cant-live-without-in-your-ci-cd-pipeline-140549f3abcb) | Documentation used from this link |




