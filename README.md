
# Ansible Playbook for Installing Node

This Ansible playbook automates the installation of Node on target machines. Node is a popular platform for developing, shipping, and running applications inside containers. This playbook simplifies the process of setting up Node, ensuring consistency across your infrastructure.

## Table of Contents

- [Ansible Playbook for Installing Node](#ansible-playbook-for-installing-node)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Prerequisites](#prerequisites)
  - [Usage](#usage)
  - [Example Inventory File](#example-inventory-file)
  - [Running the Playbook](#running-the-playbook)

## Introduction

This Ansible playbook simplifies the process of installing Node on target machines. Node provides a consistent environment for applications by packaging them in containers. This playbook uses Ansible roles to automate the installation steps, making it easy to manage Node installations across your infrastructure.

## Prerequisites

Before running this playbook, ensure you have the following prerequisites:

- Ansible installed on the machine where you'll run the playbook.
- SSH access to the target machines.
- A valid inventory file that lists the target machines where you want to install Node.

## Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/mohamedAhmed97/ansible-Node-install.git
   ```

2. Change into the project directory:

   ```bash
   cd ansible-Node-install
   ```

3. Customize the playbook variables in `vars/project-vars` to match your requirements (see Playbook Variables).

4. Create or update your Ansible inventory file with the target machine(s) where you want to install Node (see [Example Inventory File](#example-inventory-file)).

5. Run the playbook using the `ansible-playbook` command (see [Running the Playbook](#running-the-playbook)).



## Example Inventory File

Here's an example inventory file (`inventory.yml`) that lists the target machines:

```yaml
[Node_ec2_server]
192.168.154.221

[Node_ec2_server:vars]
ansible_ssh_private_key_file=~/.ssh/ansible-servers.pem
ansible_user=ubuntu
```

Ensure you replace `yourusername` and the IP addresses with your actual values.

## Running the Playbook

Use the `ansible-playbook` command to run the playbook and install Node on the target machines. Here's the command:

```bash
ansible-playbook -i ansilbe/hosts node-project.yaml
```

Replace `ansilbe/hosts` with your inventory file if it has a different name.


