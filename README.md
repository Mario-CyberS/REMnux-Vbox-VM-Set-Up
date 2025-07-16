# REMnux Virtual Machine Setup – Malware Analysis Lab  
This project documents how to import and configure a REMnux Linux VM inside VirtualBox to simulate a fake internet environment and provide essential reverse engineering tools for malware analysis. This lab pairs perfectly with FLARE-VM in an isolated malware testing setup.

---

## 🎯 Objective  
To deploy a hardened REMnux VM inside VirtualBox and prepare it to act as a DNS/web sinkhole and malware analysis endpoint in an offline lab. This enables safe execution and analysis of malicious code while maintaining system isolation.

---

## 🔍 Why Use REMnux in a Malware Lab?  
REMnux provides a ready-made Linux distribution preloaded with:
- Static and dynamic malware analysis tools  
- Built-in support for INetSim to simulate internet services  
- A trusted, isolated reverse engineering environment  
- Compatibility with FLARE-VM Windows malware analysis workflows  
- Easy import as a VirtualBox OVA

---

## 📚 Skills Learned  
- VirtualBox VM importation and configuration  
- Linux terminal navigation and root escalation  
- Installing VirtualBox Guest Additions  
- Host-only network setup and routing principles  
- Preparing an offline Linux VM for malware triage  

---

## 🛠️ Tools Used  
<div>
  <img src="https://img.shields.io/badge/-VirtualBox-183A61?style=for-the-badge&logo=VirtualBox&logoColor=white"/>
  <img src="https://img.shields.io/badge/-REMnux-cc0000?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/-INetSim-darkblue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/-Ubuntu-E95420?style=for-the-badge&logo=Ubuntu&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Linux Terminal-black?style=for-the-badge"/>
</div>

---

## 📝 Deployment Steps  

### 1. Download the REMnux OVA  
- Visit: [REMnux Official Site](https://remnux.org)  
- Click **Download**, locate the **VirtualBox OVA**  
- Download the `.ova` file from Box (approx. 5 GB)  
- While downloading, create a working directory:
```bash
C:\Users\<You>\Documents\MalwareLab\REMnux


