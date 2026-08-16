# Cross-Platform Configuration Management with Ansible

This project demonstrates how to use Ansible and AWX to manage and configure both Linux and Windows servers through reusable playbooks and roles.

## Project Overview

The project includes:

- A Linux playbook for configuring Linux servers.
- A Windows playbook for configuring Windows servers.
- Separate reusable roles for Linux and Windows.
- An inventory file containing Linux and Windows host groups.
- An Ansible configuration file for project settings.

## Project Structure

```text
awx-ansible-lab/
├── ansible.cfg
├── inventory/
│   └── hosts.ini
├── playbooks/
│   ├── linux.yml
│   └── windows.yml
└── roles/
    ├── linux_common/
    │   └── tasks/
    │       └── main.yml
    └── windows_common/
        └── tasks/
            └── main.yml



## Linux Automation

The Linux role performs the following tasks:

- Displays a test message.
- Creates a test file in `/tmp`.
- Confirms successful playbook execution.

## Windows Automation

The Windows role performs the following tasks:

- Displays a test message.
- Creates a folder on the Windows server.
- Creates a test file inside the folder.
- Retrieves and displays the Windows hostname.

## Technologies Used

- Ansible
- AWX
- Linux
- Windows
- WinRM
- YAML
- Git
- GitHub

## Syntax Validation

Validate the Linux playbook:

```bash
ansible-playbook --syntax-check playbooks/linux.yml
```

Validate the Windows playbook:

```bash
ansible-playbook --syntax-check playbooks/windows.yml
```

## Running the Playbooks

Run the Linux playbook:

```bash
ansible-playbook playbooks/linux.yml
```

Run the Windows playbook securely:

```bash
ansible-playbook playbooks/windows.yml --ask-pass
```

When using AWX, credentials should be stored securely in an AWX Machine Credential and attached to the Job Template.

## Security

Passwords and sensitive credentials are not stored in the repository. Credentials should be provided securely through AWX credentials, Ansible Vault, or runtime prompts.

## Author

Mariam Ashraf
