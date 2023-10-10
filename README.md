# Manual steps to be performed before running ansible-playbook
## 1. Copy your admin user's public ssh key to the node's authorized_key file
## 2. Make your admin user a passwordless sudoer
## 3. Configure sshd.service to permit key based authentication, only.
### 4. Test
## Do a dry run of the deploy-systems playbook.
`ansible-playbook deploy-system.yml -i inventory/private.yml -u <your-user> --check`

## Run the deploy-systems playbook as the target's admin user.
`ansible-playbook deploy-system.yml -i inventory/private.yml -u <your-user>`
