# Terraform-installation-playbook
Terraform installation on linux servers
# Directory Structure

ansible-terraform-playbook/

├── roles/

│   └── terraform/

│       ├── tasks/

│       │   └── main.yml

│       ├── vars/

│       │   └── main.yml

│       └── handlers/

│           └── main.yml

├── playbook.yml

└── inventory

# Explanation

playbook.yml: The main playbook that references the Terraform role.

## Role Structure:
  
  tasks/main.yml: Contains the tasks for installing Terraform, including installing dependencies, downloading Terraform, and verifying the installation.
        vars/main.yml: Contains the variable terraform_version, which allows you to set or change the Terraform version easily.
        handlers/main.yml: Can be used to trigger actions like service restarts or notifications (though not needed for Terraform installation).

This playbook structure follows Ansible best practices by using roles to modularize the installation process. You can easily extend or reuse this role in other playbooks.

# Running the Playbook

Save the Playbook and Roles: Save your playbook in the directory structure outlined above.

Run the Playbook: Run the playbook using the following command:

```
ansible-playbook -i inventory playbook.yml
```
