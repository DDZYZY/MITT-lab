# Standard Operating Procedure (SOP)

## Company Name

MITT IT Solutions

## Company Address

130 Henlow Bay, Winnipeg, MB, Canada

## Company Contact

* **Phone:** +1 204-555-1234
* **Email:** [support@mittitsolutions.ca](mailto:support@mittitsolutions.ca)

---

## Document Version and Approvals

| Version | Date       | Name          | Designation | Action   |
| ------- | ---------- | ------------- | ----------- | -------- |
| 1.0     | 2025-07-18 | Jack Liu      | Author      | Created  |
| 1.1     | 2025-07-19 | Felix Doe     | Reviewer    | Reviewed |
| 1.2     | 2025-07-20 | Marni Russell | Approver    | Approved |

---

## Purpose

This SOP describes the standardized steps required to set up a virtual Linux server specifically configured for web application testing environments. It ensures consistency, security, and readiness for developers and testers.

---

## Scope

This document applies to system administrators, DevOps teams, and QA engineers responsible for provisioning Linux-based virtual servers on VMware, VirtualBox, or cloud platforms (AWS, Azure).

### Objectives

* Define consistent server specifications.
* Standardize software packages necessary for web application testing.
* Establish secure network configurations.
* Provide a repeatable setup process for staging environments.

---

## Accountability Matrix

| Task                               | Responsible Team/Person  | Contact Info                                |
| ---------------------------------- | ------------------------ | ------------------------------------------- |
| Server Provisioning                | System Administrator     | [sysadmin@mitt.ca](mailto:sysadmin@mitt.ca) |
| OS & Software Installation         | DevOps Team              | [devops@mitt.ca](mailto:devops@mitt.ca)     |
| Network and Security Configuration | Network Admin            | [netadmin@mitt.ca](mailto:netadmin@mitt.ca) |
| Quality Assurance Testing          | QA Team                  | [qa@mitt.ca](mailto:qa@mitt.ca)             |
| Documentation                      | Documentation Specialist | [docs@mitt.ca](mailto:docs@mitt.ca)         |

---

## Definitions

* **VM:** Virtual Machine
* **LAMP Stack:** Linux, Apache, MySQL, PHP
* **UFW:** Uncomplicated Firewall
* **SSH:** Secure Shell

---

## Procedure Steps

### Step 1: Pre-setup Planning

1. **Define purpose:** Web Application Functional and Load Testing.
2. **Allocate resources:**

   * CPU: 4 Cores
   * Memory: 8GB RAM
   * Storage: 100GB SSD
   * Network: Bridged Adapter with Static IP
3. **Hostname:** `webtest-vm01`
4. **Select Linux Distribution:** Ubuntu Server 22.04 LTS.

### Step 2: VM Creation

1. Create a new VM on VMware or VirtualBox.
2. Set CPU, RAM, storage, and networking as defined.
3. Attach Ubuntu 22.04 ISO for installation.

### Step 3: OS Installation

1. Boot the VM and install Ubuntu Server.
2. Configure during setup:

   * Static IP: `192.168.1.50`
   * Hostname: `webtest-vm01`
   * Enable OpenSSH server
3. Set up the admin user (`webadmin`) with a strong password.

### Step 4: Essential Software Installation

**Update system:**

```bash
sudo apt update && sudo apt upgrade -y
```

**Install LAMP Stack and tools:**

```bash
sudo apt install apache2 mysql-server php libapache2-mod-php php-mysql php-cli php-curl php-gd php-mbstring php-xml php-zip -y
sudo apt install git curl wget ufw -y
```

**Install Node.js and npm:**

```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
```

**Install Python and Pip:**

```bash
sudo apt install python3 python3-pip -y
```

### Step 5: Network and Security Configuration

1. Enable UFW firewall:

```bash
sudo ufw allow OpenSSH
sudo ufw allow 'Apache Full'
sudo ufw enable
```

2. Verify network connectivity and firewall rules.

### Step 6: Optional Testing Tools Installation

* **Postman CLI:** API testing.
* **JMeter:** Load testing.
* **Docker:** Containerized app testing.

```bash
sudo apt install docker.io -y
sudo systemctl enable docker
```

### Step 7: Post-Setup Validation

1. Verify Apache:

```bash
sudo systemctl status apache2
```

2. Verify MySQL:

```bash
sudo systemctl status mysql
```

3. Confirm installations of Node.js, npm, and Python.
4. Test SSH and HTTP connectivity.

### Step 8: Documentation and Handover

* Document VM configurations, installed software versions, IP addresses.
* Share documentation and credentials securely with QA and Dev teams.

---

## References

* [Ubuntu Server Installation Guide](https://ubuntu.com/server/docs)
* [Apache HTTP Server Documentation](https://httpd.apache.org/docs/)
* [UFW Firewall Guide](https://help.ubuntu.com/community/UFW)

---

## Revision History

| Version | Date       | Author        | Changes               |
| ------- | ---------- | ------------- | --------------------- |
| 1.0     | 2025-07-18 | Jack Liu      | Initial draft         |
| 1.1     | 2025-07-19 | Felix Doe     | Reviewed, added tools |
| 1.2     | 2025-07-20 | Marni Russell | Final approval        |

---

*End of Document*
