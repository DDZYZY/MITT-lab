# 📘 Title: Build a Home Lab PC for MITT NSA Students


### 👥 Audience:

Beginners with no PC building experience, especially students in the MITT Network and Systems Administrator program, seeking a hands-on virtual lab environment at home.

---



## 🟩 Part 1: Define Needs & Choose Hardware

### 🎯 Goal:

Design and select components for a high-performance desktop PC capable of supporting multiple virtual machines, network experiments, and remote services, all within a **\$3000 CAD budget**.

### 📋 Key Requirements

![1 1 3](https://github.com/user-attachments/assets/5d35c706-d04d-47d8-8649-375362dbe375)

| 🧪 Use Case                    | 📌 Requirement Description                     |
| ------------------------------ | ---------------------------------------------- |
| Virtual Machines (e.g. VMware) | `>= 64GB RAM`, `>= 12-core CPU`                |
| File & ISO Storage             | `1TB NVMe SSD + 2TB HDD`                       |
| Network Simulation (pfSense)   | `Multi-port NIC` or PCIe expandability         |
| Linux + Windows Dual-Boot      | BIOS must support `virtualization` + dual boot |
| Upgradeable & Quiet            | Reliable PSU, cooler, and case                 |

![1 1](https://github.com/user-attachments/assets/68ccd21f-13ce-4ae2-a1db-9c76fba1e46a)
<img width="317" height="159" alt="1 1 2" src="https://github.com/user-attachments/assets/13d74016-2292-47c9-8a2c-86ac8553100f" />




### 🧰 Recommended Hardware List

| 🔧 Component | 💡 Model                   | 📝 Reason                                                  | 💵 Price (CAD) |
| ------------ | -------------------------- | ---------------------------------------------------------- | -------------- |
| CPU          | AMD Ryzen 9 7900X          | 12-core/24-thread, efficient for VMs, better value than i9 | \$520          |
| Motherboard  | ASUS TUF B650-PLUS WIFI    | PCIe 5.0, Wi-Fi 6, durable, user-friendly BIOS             | \$240          |
| RAM          | DDR5 64GB (2x32GB) 5600MHz | High-capacity & speed for multi-VM workloads               | \$270          |
| SSD          | Samsung 990 PRO 1TB NVMe   | Super fast, reliable for OS + VM storage                   | \$180          |
| HDD          | Seagate Barracuda 2TB      | For ISOs, snapshots, backups                               | \$85           |
| Cooler       | DeepCool AK620             | Silent, powerful air cooling                               | \$80           |
| PSU          | Corsair RM750x 750W Gold   | Stable power, future-proof                                 | \$130          |
| NIC          | Intel i350-T4 Quad Port    | Essential for labs, widely supported in pfSense            | \$150          |
| Case         | Fractal North Mid Tower    | Quiet, clean airflow, good cable management                | \$140          |
| Monitor      | LG 27" QHD IPS             | Large workspace for multitasking & labs                    | \$350          |
| Others       | Mouse, Keyboard, USB, HDMI | Basic peripherals                                          | \$100          |
| **Total**    |                            |                                                            | **\~\$2345**   |

![22](https://github.com/user-attachments/assets/a77a9d04-0193-457a-be2b-f96bc9af60f0)

💡 *Reserve \~\$600 for UPS, 2nd SSD, or a backup drive.*

Additional Notes:

* Compatibility between CPU, RAM, and motherboard is validated via [PCPartPicker](https://ca.pcpartpicker.com).
* All parts selected ensure future scalability, allowing for upgrades like additional storage or a dedicated GPU if needed.

---




## 🟨 Part 2: 🛠️ Assemble the Computer

### 🧭 Goal:

Assemble all components into a fully functioning machine ready for operating system installation.

### ✅ Step-by-Step Instructions



🔹 **Step 2.1: Preparation**

<img width="1920" height="1080" alt="21" src="https://github.com/user-attachments/assets/bc416238-4e22-42ab-8ecd-3a3508753975" />

* Clear your desk and wear an anti-static wrist strap
* Prepare a Phillips screwdriver, zip ties, and the motherboard manual

📎 *Suggested visual: component layout on desk*


🔹 **Step 2.2: Install CPU onto Motherboard**

![24](https://github.com/user-attachments/assets/8ad518fd-8b60-4a32-8521-5a36565aab8e)

* Open CPU socket lever (AM5 platform)
* Align gold triangle → gently place → close the latch

⚠️ Caution:

* Never apply pressure! If it doesn’t fit, check the orientation
* Do not touch the CPU contacts


🔹 **Step 2.3: Install CPU Cooler**

![25](https://github.com/user-attachments/assets/1c207f76-1f09-42fe-826c-83c1874bd743)

* Apply a pea-sized amount of thermal paste
* Attach the cooler base → tighten screws → connect CPU\_FAN cable to motherboard

⚠️ Caution:

* Make sure the CPU\_FAN is connected to the correct header, or the system won’t boot!


🔹 **Step 2.4: Install RAM**

![26](https://github.com/user-attachments/assets/df33bd93-da21-4bdb-a85d-16c70e41b667)

* Use A2 + B2 slots
* Align the notch → press firmly until you hear a “click”

⚠️ If it won’t go in, don’t force it — recheck alignment!


🔹 **Step 2.5: Install SSD & HDD**

![30](https://github.com/user-attachments/assets/5d29fa76-ce2f-44ab-9c5b-54d3f8506e66)

* Insert M.2 SSD into designated motherboard slot → secure with screw
* Mount HDD into tray, connect SATA data cable to motherboard


🔹 **Step 2.6: Install Motherboard into Case**

![28](https://github.com/user-attachments/assets/58615abb-342e-426d-a2c2-0d8dd1ed861b)

* First insert the I/O shield → position motherboard → fasten with 9 screws

📎 *Suggested diagram: I/O shield and screw alignment*


🔹 **Step 2.7: Install Power Supply & Connect Cables**

![27](https://github.com/user-attachments/assets/51231648-cde6-4344-ba37-770f101eb849)

* Place PSU in power chamber, secure with screws
* Connect 24-pin ATX power, 8-pin CPU power
* Connect GPU (if any), fans, USB front panel, HD\_AUDIO, power/reset switch

📎 *Refer to motherboard manual for front panel header layout*


🔹 **Step 2.8: Install NIC & Cable Management**

* Insert Intel i350 NIC into PCIe x4 slot
* Route cables cleanly → tie with zip ties → ensure airflow


🔹 **Step 2.9: Power-On Test**

* Connect monitor, keyboard, and power cable → turn on → enter BIOS

✅ If successful, BIOS should recognize CPU, RAM, and SSD

🆘 No display?

* Check if 24-pin and 8-pin cables are securely plugged
* Verify RAM is fully seated
* Ensure CPU cooler is connected to CPU\_FAN header

---




## 🟦 Part 3: 💽 Install Operating Systems & Set Up Virtual Lab


### 🧭 Goal:

Install Windows and Linux OS, configure virtualization platform (Hyper-V), and prepare a home lab with multiple virtual machines and remote access.


### 🖥️ Step 3.1: BIOS Setup

<img width="1200" height="720" alt="31" src="https://github.com/user-attachments/assets/814b4814-b62e-4b7f-94cc-94e4af9656cf" />
* On first boot, press `DEL` or `F2` to enter BIOS.
* Enable virtualization: `SVM` or `Intel VT-x`
* Set boot order: First device should be USB or the desired OS install disk
* Optional: Enable XMP profile for RAM performance

📎 *Visual suggestion: Screenshot of BIOS virtualization & boot menu*


### 💿 Step 3.2: Install Windows 11

* Download official ISO: [https://www.microsoft.com/en-us/software-download/windows11](https://www.microsoft.com/en-us/software-download/windows11)
* Create bootable USB using [Rufus](https://rufus.ie)
* Follow on-screen prompts: Custom install → Delete all partitions → Select NVMe SSD
* Create a **local account** (avoid Microsoft login for lab control)
* Skip TPM checks using Rufus pre-config (if needed)

⚠️ Important:

* Do not enable BitLocker or device encryption for VM labs


### 🐧 Step 3.3: Install Ubuntu (Dual Boot Optional)

* Download ISO: [https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)
* Flash USB using Rufus or BalenaEtcher
  <img width="768" height="461" alt="3 31_BALENAeTCHER" src="https://github.com/user-attachments/assets/c2787f17-cb12-49c9-af08-8379ebf5160a" />
* BIOS → Boot from USB → Select “Try Ubuntu”
* Install alongside Windows OR manual partitioning
* Update packages after install:

```bash
sudo apt update && sudo apt upgrade -y
```


### 🧪 Step 3.4: Enable Hyper-V for Virtualization

In Windows Terminal (Admin):

```powershell
dism /online /enable-feature /featurename:Microsoft-Hyper-V -All /norestart
```

* Reboot → Search “Hyper-V Manager”
* Create a Virtual Switch: Internal + External (for pfSense)

📎 *Tip: Always name your VMs clearly: “Win11-ITLab”, “pfSense-Test”, etc.*


### 🧰 Step 3.5: Create Virtual Machines

| VM Name     | OS           | RAM  | CPU | Disk | Purpose                  |
| ----------- | ------------ | ---- | --- | ---- | ------------------------ |
| Win11-ITLab | Windows 11   | 8 GB | 4   | 80GB | Primary workstation      |
| Ubuntu-Test | Ubuntu 22.04 | 4 GB | 2   | 40GB | Linux shell & practice   |
| DC-Server   | Win Server   | 6 GB | 2   | 60GB | Domain Controller (AD)   |
| Kali-Lab    | Kali Linux   | 6 GB | 2   | 40GB | Pen-testing environment  |
<img width="1037" height="659" alt="3 5" src="https://github.com/user-attachments/assets/0536b660-4219-4000-a7b4-664c8929bd2a" />

💡 Reserve 10–20% host RAM for system stability.


### 🌐 Step 3.6: Remote Access & Services

* Enable RDP (Windows) and SSH (Linux)

```powershell
sudo apt install openssh-server -y
sudo systemctl start sshd
sudo systemctl enable sshd
```

* Open firewall ports:

```powershell
New-NetFirewallRule -DisplayName "SSH" -Direction Inbound -Protocol TCP -LocalPort 22 -Action Allow
```



* For WAN access:
<img width="1200" height="989" alt="3 6" src="https://github.com/user-attachments/assets/978488e5-cf2f-4c6e-9bc7-e6c184c1faed" />

  * Use DuckDNS + Port Forwarding
  * Optional: Use Tailscale / ZeroTier for secure tunneling



### 📎 References & Troubleshooting

| Issue                  | Solution / Resource                                 |
| ---------------------- | --------------------------------------------------- |
| Hyper-V not listed     | BIOS → Enable virtualization (SVM/VT-x)             |
| Ubuntu freezes on boot | Add `nomodeset` in GRUB boot options                |
| Windows Update fails   | Run `sfc /scannow` or `DISM /Online /Cleanup-Image` |
| Need VM images         | [https://osboxes.org/](https://osboxes.org/)        |

✅ All setup is now complete. You're ready to begin your NSA labs and real-world IT practice at home!

---


## 📚 Additional References & Learning Resources


### 🖥️ Hardware & PC Building

* [PCPartPicker - Build Compatibility Checker](https://ca.pcpartpicker.com/)
* [How to Install a CPU](https://www.intel.com/content/www/us/en/gaming/resources/how-to-install-a-cpu.html)
* [Installing RAM Guide](https://www.crucial.com/articles/about-memory/installing-memory)


### 🧰 Operating System Installation

* [Microsoft Windows 11 Official ISO Download](https://www.microsoft.com/en-us/software-download/windows11)
* [Ubuntu Desktop Download](https://ubuntu.com/download/desktop)
* [Rufus USB Tool](https://rufus.ie/)


### 🧪 Virtualization & Networking

* [Hyper-V Documentation (Microsoft)](https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/)
* [pfSense Documentation](https://docs.netgate.com/pfsense/en/latest/)
* [Tailscale Setup Guide](https://tailscale.com/kb/)


### 🧑‍💻 VM Images & Practice Labs

* [OSBoxes – Prebuilt VM Images](https://www.osboxes.org/)
* [Kali Linux – Offensive Security](https://www.kali.org/get-kali/)
* [Windows Server Evaluation](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server)


### 🔧 Troubleshooting Forums & Communities

* [Tom’s Hardware Forums](https://forums.tomshardware.com/)
* [Microsoft Community](https://answers.microsoft.com/)
* [Ask Ubuntu](https://askubuntu.com/)
* [Reddit: r/homelab](https://www.reddit.com/r/homelab/)

💡 *Bookmark these pages for quick access during lab experiments or system troubleshooting!*
