# 🧠 Ansible-Project-Monitoring

## 📌 Project Overview  
This project automates **VM monitoring using Ansible**.  
It helps deploy, configure, and collect system metrics (CPU, memory, disk, etc.) from Linux virtual machines — all through automated playbooks.  
You can easily extend it to integrate with dashboards or alerting systems.

---

## ✅ Key Features  
- 🧩 **Inventory-based host management** — define target servers in `inventory/`  
- ⚙️ **Group variables** stored in `group_vars/`  
- 📊 **Metrics collection playbook** → `collect_metrics.yaml`  
- 📨 **Report generation playbook** → `send_report.yaml`  
- 🧱 Modular and reusable Ansible configuration (`ansible.cfg`)  
- 💻 Shell scripts for automation → `key.sh`, `tag.sh`  
- 🔐 **MIT Licensed** project — open for reuse and customization  

---

## 🎯 Use Case  
This project is ideal for:
- Small or medium service-based companies needing quick monitoring setup  
- DevOps/DevSecOps engineers wanting to automate VM health checks  
- Teams looking to standardize their infrastructure monitoring through code  
- Freelancers building monitoring-as-a-service solutions  

---

## 🛠️ Prerequisites  
Before you start, ensure you have:
- 🐧 Linux servers or VMs accessible via SSH  
- 🧰 Ansible installed (`v2.9+` recommended)  
- 🔑 SSH keys properly configured  
- 🐍 Python installed (for automation scripts)  
- 🗂️ Inventory file configured (`inventory/hosts.ini`)  

---

## 🚀 Setup Instructions  

1. **Clone this repository**  
   ```bash
   git clone https://github.com/Saeedullahshaikh/Ansible-project-monitoring.git
   cd Ansible-project-monitoring
   ```

2. **Configure your inventory**  
   - Open `inventory/hosts.ini`  
   - Add your target machines (for example):  
     ```ini
     [monitoring]
     server1 ansible_host=192.168.1.10 ansible_user=ubuntu
     server2 ansible_host=192.168.1.11 ansible_user=ubuntu
     ```

3. **Set group variables**  
   Edit files under `group_vars/` to define thresholds or environment-specific variables.

4. **Run the metrics collection playbook**  
   ```bash
   ansible-playbook -i inventory/hosts.ini collect_metrics.yaml
   ```

5. **Run the report generation playbook**  
   ```bash
   ansible-playbook -i inventory/hosts.ini send_report.yaml
   ```

---


## 📚 Directory Structure  
```
/
├─ inventory/              # Target host inventories  
├─ group_vars/             # Group-specific variables  
├─ ansible.cfg             # Ansible configuration file  
├─ collect_metrics.yaml    # Playbook for collecting VM metrics  
├─ send_report.yaml        # Playbook for generating/sending reports  
├─ key.sh                  # Helper script for SSH key setup  
├─ tag.sh                  # Helper script for tagging VMs  
└─ LICENSE                 # MIT License  
```

---

## 📝 License  
This project is licensed under the **[MIT License](LICENSE)** — feel free to use and modify.
---


## Author

**Saeedullah Shaikh**
- GitHub: [@Saeedullahshaikh](https://github.com/Saeedullahshaikh)

---
