# Jenkins Vagrant VM Setup

This repository contains the necessary configuration to set up Jenkins inside a Virtual Machine (VM) managed by Vagrant. This allows you to create a reproducible environment to run Jenkins in a controlled, isolated manner.

## Prerequisites

- [Vagrant](https://www.vagrantup.com/downloads.html)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads) (or another provider supported by Vagrant)
- Git (optional, but recommended for cloning this repository)

## Setup Instructions

1. **Clone the Repository (Optional):**

   If you've decided to use Git:
   ```bash
   git clone https://your-repo-url.git
   cd your-repo-dir
   ```

2. **Start the VM:**

   From the root directory of the project, run:
   ```bash
   vagrant up
   ```

   This command will download the necessary base box (if not already downloaded), and provision the VM with Jenkins and any other necessary software.

3. **Access Jenkins:**

   Once the VM is up and running, Jenkins should be accessible from your host machine at:
   ```
   http://localhost:8080
   ```

   If you're asked for an initial admin password, you can find it in the VM at:
   ```bash
   sudo cat /var/lib/jenkins/secrets/initialAdminPassword
   ```

4. **SSH into the VM (Optional):**

   If you need to access the VM's terminal:
   ```bash
   vagrant ssh
   ```

5. **Stop the VM:**

   When you're done with Jenkins and want to shut down the VM:
   ```bash
   vagrant halt
   ```

6. **Destroy