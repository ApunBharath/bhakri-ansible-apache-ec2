# Apache Web Server Deployment using Ansible Roles

This project automates the setup of an Apache web server on an AWS EC2 instance using Ansible roles.

## 🚀 Features

- Installs Apache on remote EC2 (Ubuntu)
- Deploys a custom `index.html`
- Uses Ansible best practices with roles
- Role-based directory structure

## 📁 Project Structure

apache-role-project/
├── host.ini
├── site.yml
└── roles/
└── apache/
├── tasks/
│ └── main.yml
├── handlers/
│ └── main.yml
└── files/
└── index.html

## 🧪 How to Run

1. SSH into your control EC2 (EC2-1).
2. Update `host.ini` with EC2-2 IP and correct key path.
3. Run the playbook:

##cmd
ansible-playbook -i host.ini site.yml
#Visit EC2-2's public IP in browser to see the result.
http://<ip.pub of target server>

✅ Example Output in Browser:

Hello from Ansible Role!
