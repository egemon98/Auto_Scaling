# Auto_Scaling
Azure VM auto scaling


Here’s a professional and informative `README.md` file for your **Azure VMSS Auto-Scaling Terraform Project**. You can place this in your GitHub repository root.

---

## Azure VM Scale Set with Auto-Scaling using Terraform

This project deploys an **Azure Virtual Machine Scale Set (VMSS)** using **Terraform**, with **auto-scaling enabled based on CPU usage**. It demonstrates how to configure scalable infrastructure in Azure using Infrastructure as Code (IaC) principles.

---

## Features

* ✅ Deploys a VMSS with Ubuntu instances
* ✅ Installs and runs **NGINX** on each instance
* ✅ Auto-scales based on average CPU utilization
* ✅ Configures virtual network, subnet, and load balancer
* ✅ Modular and reusable Terraform code

---

## Technologies Used

* [Terraform](https://www.terraform.io/)
* [Microsoft Azure](https://azure.microsoft.com/)
* Azure Resources:

  * VM Scale Sets
  * Load Balancer
  * Network Security Groups
  * Virtual Network & Subnet
  * Auto-scale Rules

---

## Infrastructure Diagram

```txt
+---------------------+
|  Azure Load Balancer|
+---------------------+
         |
+---------------------------+
|  VM Scale Set (Ubuntu)   |
|  - NGINX                 |
|  - Auto-scaling (CPU >70%)|
+---------------------------+
         |
+---------------------+
| Virtual Network/Subnet |
+---------------------+
```

---

## ⚙️ Setup Instructions

### 1️⃣ Prerequisites

* Terraform installed (`v1.5+`)
* Azure CLI installed and authenticated:

  ```bash
  az login
  ```
* An active Azure subscription

---

### 2️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/azure-vmss-autoscale.git
cd azure-vmss-autoscale
```

---

### 3️⃣ Initialize Terraform

```bash
terraform init
```

---

### 4️⃣ Apply Terraform Plan

```bash
terraform apply
```

When prompted, type `yes` to confirm.

---

### 5️⃣ Destroy Resources

To remove all created infrastructure:

```bash
terraform destroy
```

---

## 📈 Auto-Scaling Rules

This VM Scale Set will:

* **Scale out** (add 1 VM) when average CPU > 70% for 5 minutes
* **Scale in** (remove 1 VM) when average CPU < 30% for 10 minutes
* Maintain a **minimum of 1** and a **maximum of 3** instances

---

## 📁 Project Structure

```
.
├── main.tf            # Main configuration
├── variables.tf       # Input variables
├── outputs.tf         # Outputs
├── terraform.tfvars   # User-defined variable values
└── README.md          # Project documentation
```

---

## 📃 License

This project is licensed under the [MIT License](LICENSE).

---

## ✍️ Author

Md Emdadul Gani
💼 Cloud & Database Engineer
🌐 [LinkedIn](https://linkedin.com/in/md-emdadul-gani) | 📧 [Email](mailto:md.emdadulgani@gmail.com)

