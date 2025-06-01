# Ansible Linux Package Installer

This project uses **Ansible roles** to install common Linux packages on **multiple EC2 instances** (Ubuntu & Amazon Linux) in AWS Free Tier.

## 👤 Author

**Santosh Reddy**  
GitHub: [santoshreddy960-github](https://github.com/santoshreddy960-github)

---

## 📁 Project Structure

ansible-linux-packages/
├── inventory.ini
├── playbook.yaml
├── README.md
├── .gitignore
└── roles/
    └── common_packages/
        ├── tasks/
        │   ├── main.yml
        │   ├── ubuntu.yml
        │   └── amazon.yml
        ├── defaults/
        │   └── main.yml
        ├── vars/
        │   └── main.yml
        ├── meta/
        │   └── main.yml


---

## 🚀 How to Use

### 1. Clone the repo

```bash
git clone https://github.com/santoshreddy960-github/ansible-linux-packages.git
cd ansible-linux-packages

### 2. Update your inventory.ini

[all]
ubuntu ansible_host=<Ubuntu-EC2-IP> ansible_user=ubuntu ansible_ssh_private_key_file=~/Downloads/ansible-key.pem
amazon ansible_host=<Amazon-EC2-IP> ansible_user=ec2-user ansible_ssh_private_key_file=~/Downloads/ansible-key.pem

### 3. Run the playbook

ansible-playbook -i inventory.ini playbook.yaml

📦 Packages Installed

git

curl

unzip

htop

python3

python3-pip

🛠 Technologies Used
Ansible (role-based)

AWS EC2 (Free Tier)

YAML, SSH

📸 Sample Output

PLAY RECAP
amazon                     : ok=3    changed=1    failed=0
ubuntu                     : ok=3    changed=0    failed=0


📬 License
MIT License – free to use and modify.


