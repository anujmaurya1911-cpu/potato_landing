# 🥔 Potato Landing ☁️🚀

> **Automated Azure Infrastructure as Code (IaC) powered by Terraform** 🛠️✨

[![Terraform](https://img.shields.io/badge/Terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://azure.microsoft.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

---

## 📌 Table of Contents

- [📖 Overview](#-overview)
- [📂 Repository Structure](#-repository-structure)
- [⚙️ Prerequisites](#️-prerequisites)
- [🔐 Authentication & Setup](#-authentication--setup)
- [🚀 Quick Start / Usage Guide](#-quick-start--usage-guide)
  - [1️⃣ Initialize Terraform](#1️⃣-initialize-terraform)
  - [2️⃣ Format & Validate Code](#2️⃣-format--validate-code)
  - [3️⃣ Preview Plan](#3️⃣-preview-plan)
  - [4️⃣ Apply & Deploy](#4️⃣-apply--deploy)
  - [5️⃣ Destroy / Cleanup](#5️⃣-destroy--cleanup)
- [📦 Managed Resources](#-managed-resources)
- [🛡️ Security & Best Practices](#️-security--best-practices)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 📖 Overview

🌟 **Potato Landing** is an enterprise-ready Infrastructure as Code (IaC) repository built using **HashiCorp Terraform**. It streamlines and automates the provisioning, governance, and management of **Microsoft Azure** cloud landing zone infrastructure.

- ⚡ **Automated Provisioning:** Spin up consistent cloud environments in minutes.
- 🧱 **Modular Architecture:** Cleanly separated resource modules for high reusability.
- 🔒 **Secure by Default:** Designed adhering to cloud security best practices and state management.

---

## 📂 Repository Structure

```text
📁 potato_landing/
├── 📄 .gitignore          # 🚫 Git ignore rules (state files, secrets, lock files)
├── 📄 README.md           # 📘 Project documentation & setup guides
└── 📁 azurerm_rg/         # 📦 Azure Resource Group module & configurations
    └── 📄 main.tf         # 🏗️ Terraform resource definitions for Azure RGs
```

---

## ⚙️ Prerequisites

Ensure you have the following tools installed and ready on your machine:

- 🟪 **[Terraform](https://developer.hashicorp.com/terraform/downloads)** `v1.0.0+`
- 🟦 **[Azure CLI (az)](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)** `v2.0.0+`
- ☁️ **Azure Subscription** with permissions (*Contributor* / *Owner*)
- 💻 **Git** for version control

---

## 🔐 Authentication & Setup

Log in to your Azure tenant via the Azure CLI:

```bash
# 🔑 Sign in to Microsoft Azure
az login

# 🎯 Set your target Azure Subscription
az account set --subscription "<YOUR_SUBSCRIPTION_ID>"
```

---

## 🚀 Quick Start / Usage Guide

Navigate into the target configuration directory:

```bash
cd azurerm_rg
```

### 1️⃣ Initialize Terraform
Downloads the required provider plugins (`hashicorp/azurerm`) and sets up local working state:

```bash
terraform init
```

### 2️⃣ Format & Validate Code
Ensures syntax correctness and cleans up code formatting:

```bash
terraform fmt
terraform validate
```

### 3️⃣ Preview Plan
Generate and inspect an execution plan to verify changes before provisioning:

```bash
terraform plan
```

### 4️⃣ Apply & Deploy
Deploy the infrastructure directly into your Azure subscription:

```bash
terraform apply
```
> 💡 *Tip:* Use `terraform apply -auto-approve` inside CI/CD automation pipelines! 🤖

### 5️⃣ Destroy / Cleanup
Tear down all deployed resources when no longer needed:

```bash
terraform destroy
```

---

## 📦 Managed Resources

### 🌐 Azure Resource Groups (`azurerm_rg/`)

Resource groups organize and manage Azure infrastructure lifecycle:

| 🏷️ Resource Name | 🛠️ Type | 🌍 Region | 📝 Resource Group Name |
| :--- | :--- | :--- | :--- |
| `cool` | `azurerm_resource_group` | `centralindia` 🇮🇳 | `anujrg` |
| `cool1` | `azurerm_resource_group` | `centralindia` 🇮🇳 | `anujrg10` |
| `cool145` | `azurerm_resource_group` | `centralindia` 🇮🇳 | `anujrg10` |

---

## 🛡️ Security & Best Practices

- 🔒 **Zero Hardcoded Secrets:** Never commit `.tfvars`, credentials, or private keys to source control.
- 💾 **Remote State Storage:** Use Azure Blob Storage with state locking (`azurerm_storage_blob`) for production deployments.
- 🏷️ **Tagging Strategy:** Apply resource tags (Environment, Owner, Cost Center) for cost tracking and governance.
- 🔄 **Code Reviews:** Implement PR review requirements and automated validation pipelines before merges.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! 🎉

1. 🍴 **Fork the Project**
2. 🌿 **Create your Feature Branch** (`git checkout -b feature/AmazingFeature`)
3. 💾 **Commit your Changes** (`git commit -m '✨ Add new Azure service module'`)
4. 📤 **Push to the Branch** (`git push origin feature/AmazingFeature`)
5. 📬 **Open a Pull Request**

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more details. 📜

---

<p align="center">
  Made with ❤️ for DevOps & Cloud Automation 🚀
</p>