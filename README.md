## Ansible + Dockerized Nginx Deployment

###  Project Overview
This project demonstrates how to automate the deployment of a Dockerized Nginx web server using **Ansible**.  
The same Ansible playbook is used to provision both **Dev** and **Prod** environments with minimal manual intervention.

---

###  Goals
- Implement **Infrastructure as Code** principles
- Use Ansible to **install Docker** remotely
- Deploy a **custom HTML landing page** into an Nginx container
- Maintain a single codebase for both Dev and Prod environments

---

###  What I Learned
Through this project I have:
- Configured **Ansible inventory** for multiple environments
- Automated **Docker installation** and container deployment
- Mounted custom content into containers via **volumes**
- Ensured reproducible deployments across environments

---

###  Project Structure

```
ansible-nginx-deploy/
├── inventory.ini      you have create inventory file by yourself with your data
├── playbook.yml
├── files/
│   └── index.html
├── .gitignore
├── README.md
```

---

### Technologies Used
- **Ansible** – automation & configuration management
- **Docker** – containerized Nginx web server
- **Linux (Ubuntu)** – target servers
- **AWS EC2** – hosting Dev & Prod environments

---

##  How to Use

###  Configure Inventory
```
git clone ...
Create  inventory.ini and set your server IPs, SSH user, and private key path
Check conection...!
Remember to load Ansible onto the control machine.
Run Deployment:
ansible-playbook playbook.yml -i inventory.ini --limit dev
ansible-playbook playbook.yml -i inventory.ini --limit prod

Verify Deployment:
Open your pub ip... or curl http://<server-ip>
```
If something does not work or does not start, try to find the error and fix it, learn how to do it and solve errors, and you will never repeat it again.


**Good luck!** 😊










