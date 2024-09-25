# Automated Deployment and Configuration for Boilerplate

## Overview

This project involves the automated deployment and configuration of a Java boilerplate application using Ansible. The playbook performs the following tasks:

- **Clone**: Clones the devops branch of the boilerplate repository to a remote Linux server (Ubuntu 22.04).
- **Install Dependencies and Deploy**: Installs all necessary dependencies and deploys the application.
- **Setup PostgreSQL**: Configures a PostgreSQL database and stores the credentials.
- **Messaging Queue**: Sets up any required messaging queue (e.g., RabbitMQ).
- **Application Configuration**: Configures the application to run on port 3000 and sets up Nginx to reverse proxy to port 80.
- **Logging**: Configures logging to specific files with proper ownership.

## Prerequisites

- An Ubuntu 22.04 server
- Python 3.12 installed on the server
- Ansible 2.9 or later installed
- An SSH private key file for access to the server

## Directory Structure

- `main.yaml`: Main Ansible playbook for deployment.

## Inventory File

The Ansible playbook requires an inventory file to specify the target host.

## Running the Playbook

```sh

ansible-playbook main.yaml -b -i inventory.cfg
```

## Verify the Deployment

### Check the status of the application service:

```sh
sudo systemctl status stage_5b
```
