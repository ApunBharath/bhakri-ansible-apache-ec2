# 🛠️ bhakri-ansible-apache-ec2

This Ansible project installs Apache on a remote EC2 instance and serves a custom `index.html` page using roles.  
Great for DevOps practice or automation beginners.

---

## 📁 Project Structure

bhakri-ansible-apache-ec2/
├── host.ini # Inventory file with EC2 IP
├── site.yml # Main playbook
├── roles/
│ └── apache/
│ ├── tasks/
│ │ └── main.yml # Apache installation and copy task
│ └── files/
│ └── index.html # Custom web content

---

## 🚀 How to Use This Repository

### ✅ 1. Clone the Repository
```bash
git clone https://github.com/ApunBharath/bhakri-ansible-apache-ec2.git
cd bhakri-ansible-apache-ec2

✅ 2. Update the Inventory File (host.ini)
Replace the existing IP with your EC2 instance's public IP:

ini

[web]
<your-ec2-public-ip> ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/your-key.pem
ansible_user=ubuntu: default user for Ubuntu EC2

ansible_ssh_private_key_file: path to your PEM key

✅ 3. Install Ansible (if not installed)

sudo apt update
sudo apt install ansible -y

✅ 4. Run the Playbook

ansible-playbook -i host.ini site.yml

🌐 After Deployment
Visit http://<your-ec2-public-ip> in a browser.

You should see a custom HTML page:
"Hello from Ansible Role!"

⚠️ Notes
Make sure port 80 is open in your AWS Security Group for the EC2 instance.

Ensure your PEM file has secure permissions:

chmod 400 your-key.pem



📄 License
This project is for educational purposes. Feel free to fork and improve!

---
