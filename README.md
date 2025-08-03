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
  <a href="https://www.virtualbox.org/" target="_blank">
    <img src="https://img.shields.io/badge/-VirtualBox-183A61?style=for-the-badge&logo=VirtualBox&logoColor=white"/>
  </a>
  <a href="https://remnux.org/" target="_blank">
    <img src="https://img.shields.io/badge/-REMnux-AA0000?style=for-the-badge&logo=Linux&logoColor=white"/>
  </a>
  <a href="https://www.inetsim.org/" target="_blank">
    <img src="https://img.shields.io/badge/-INetSim-darkblue?style=for-the-badge"/>
  </a>
  <a href="https://ubuntu.com/" target="_blank">
    <img src="https://img.shields.io/badge/-Ubuntu-E95420?style=for-the-badge&logo=Ubuntu&logoColor=white"/>
  </a>
  <a href="https://man7.org/linux/man-pages/man1/bash.1.html" target="_blank">
    <img src="https://img.shields.io/badge/-Linux Terminal-black?style=for-the-badge"/>
  </a>
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
```

### 2. Import REMnux into VirtualBox
- Once the OVA is downloaded, move it into the folder you created (e.g., MalwareLab\REMnux).
- Right-click the OVA file → Choose Open With → VirtualBox.
- VirtualBox will launch the Import Virtual Appliance wizard.
- Change the VM name to something recognizable:
Example: PMAT-REMnux
- (Optional) Adjust RAM or CPU cores as needed (recommended: 2 GB RAM minimum).
- Click Import and wait a few minutes for the process to complete.

### 3. Launch the REMnux VM
- In VirtualBox, select the new PMAT-REMnux VM and click Start.
- REMnux will boot directly into the desktop environment (no installer needed).
- A terminal window should automatically open upon login.

### 4. Install VirtualBox Guest Additions (Optional)
This improves display scaling, clipboard sharing, and mouse integration.
- In VirtualBox top menu, click:
```bash
Devices → Insert Guest Additions CD Image...
```
- In the terminal inside REMnux:
```bash
sudo mkdir -p /media/cdrom
sudo mount /dev/cdrom /media/cdrom
cd /media/cdrom
sudo -s    # Elevate to root
./autorun.sh
```
- Wait for the Guest Additions install script to complete.
- When prompted with:
```bash
Press return to close this window
```
– hit Enter.
- Reboot the VM:
```bash
reboot
```

### 5. Expand the REMnux Display (if needed)
- If your REMnux desktop is still in a small window:
- Click the Minimize window button on the top right of the REMnux VM window.
- Then click Maximize window.
- The VM should now resize to match your host screen.

### Final Result
Your REMnux VM is now:
- Imported and configured in VirtualBox
- Ready for simulated malware traffic and reverse engineering
- Integrated with future host-only networking or INetSim
Pair with FLARE-VM (in next sub-project) for a complete isolated lab setup.

---

### 👨‍💻 Author
Mario Tagaras | Cyber Security Specialist



