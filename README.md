# Ansible Jenkins Website with Docker on AWS

This repository contains the code and configurations for deploying a website using Ansible, Jenkins, and Docker on AWS.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project aims to automate the deployment of a website using Ansible for configuration management, Jenkins for continuous integration, and Docker for containerization. The deployment is targeted to run on Amazon Web Services (AWS).

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- AWS account with appropriate credentials
- Ansible installed locally
- Jenkins server accessible
- Docker installed on target servers
- AWS CLI configured with necessary credentials

## Setup

1. Clone this repository:

    ```bash
    git clone https://github.com/bonao99/ansible-jenkins.git
    ```

2. Navigate to the project directory:

    ```bash
    cd ansible-jenkins
    ```

3. Configure AWS credentials:

    ```bash
    aws configure
    ```

    Ensure your AWS credentials have the necessary permissions for EC2 instances, S3 buckets, and other resources.

4. Update Ansible inventory with your AWS instance details:

    Edit `ansible/inventory/aws_inventory.yml` with your AWS instance details.

5. Configure Jenkins:

    Set up a Jenkins job to trigger the Ansible playbook. Refer to `jenkins/README.md` for detailed instructions.

6. Execute the Ansible playbook:

    ```bash
    ansible-playbook -i ansible/inventory/aws_inventory.yml ansible/site.yml
    ```

## Usage

Describe how to use the deployed website and any additional steps required for maintenance or updates.

## Folder Structure

- `ansible/`: Ansible playbooks and roles
- `jenkins/`: Jenkins job configuration and scripts
- `docker/`: Docker configurations and Dockerfile
- `website/`: Source code and assets for the website
- `scripts/`: Additional scripts for deployment or automation
- `LICENSE`: Project license file
- `README.md`: This file

## Contributing

If you find any issues or have suggestions for improvement, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
