# Secure Hybrid Infrastructure (Azure)

This project deploys a secure hybrid infrastructure on Azure with one Windows Server (acting as a domain controller) and one hardened Linux VM.

## 🌐 Infrastructure Overview

- Azure Resource Group and VNet
- 2 Subnets: Windows & Linux
- NSGs for secure RDP/SSH access
- Windows VM with AD + DNS auto-setup
- Linux VM hardened via CIS-style script

## 🔧 Technologies Used

- Terraform
- Azure Virtual Machines
- PowerShell / Bash
- Azure Custom Script Extensions
- Azure Blob Storage (for script delivery)

## 🛡️ Hardening Includes

- UFW enabled
- Fail2ban configured
- Root SSH login disabled
- AIDE integrity checker
- Automatic updates
- CIS compliance alignment

## 🚀 How to Use

1. Update Terraform variables and your Blob Storage URLs in `main.tf`
2. Run:

```bash
terraform init
terraform plan
terraform apply
```

## 📜 Output

- Public IPs for RDP and SSH
- Logs stored at `/var/log/harden.log` on Linux VM

## ✅ Next Steps

- Add Azure Key Vault for secrets
- Set up Azure Monitor or Defender
