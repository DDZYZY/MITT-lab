# Request for Proposal (RFP)

### Wireless Infrastructure Deployment

---

### Issued by:

**Qijia Liu**
Network and Systems Administration Student
MITT, Manitoba, Canada
Email: [qijialiu@student.mitt.ca](mailto:qijialiu@student.mitt.ca)
Date: July 21, 2025

---

### Submitted to:

**Instructor:** Jibing Liang
Email: [jibing.liang@mitt.ca](mailto:jibing.liang@mitt.ca)

---

## 1. About Us

Our organization is an innovation-driven company focused on enhancing operational capabilities through robust technology solutions. We are seeking qualified vendors to design, deploy, and support a secure, high-performance wireless network across our premises to ensure seamless connectivity, security, and scalability for our growing operations.

---

## 2. Project Scope

### 2.1 Objectives

* Achieve complete wireless coverage throughout all office areas.
* Support the latest Wi-Fi 6 (802.11ax) standard for improved speed and capacity.
* Implement robust security measures, including WPA3 encryption and MAC address filtering.
* Ensure capacity for high-density device connectivity.
* Establish ongoing network monitoring and support.

### 2.2 Scope of Work (Detailed)

1. **Site Survey to Determine Optimal Access Point Placement:**

   * Conduct a comprehensive physical and environmental analysis of the entire office space.
   * Identify potential sources of interference, such as walls, electronic devices, and structural obstacles.
   * Use professional tools such as spectrum analyzers and heatmapping software to evaluate signal strength, coverage gaps, and optimal AP locations.
   * Document signal propagation maps and recommend specific placement strategies for each access point to ensure even and reliable coverage across all zones, including common areas, private offices, meeting rooms, and less frequented spaces like storage rooms.

2. **Installation and Configuration of Wireless Access Points:**

   * Procure and install enterprise-grade Wi-Fi 6 access points that support features like MU-MIMO, OFDMA, and beamforming for enhanced performance.
   * Configure APs with appropriate SSIDs, VLAN tagging for network segmentation, and QoS (Quality of Service) policies to prioritize critical applications like VoIP and video conferencing.
   * Perform channel planning to minimize co-channel and adjacent channel interference.
   * Conduct post-installation testing to verify coverage, connectivity, and throughput.

3. **Integration with Existing Wired Network:**

   * Establish secure and seamless integration with the organization's current wired network infrastructure.
   * Configure Layer 2 and Layer 3 network components to support VLANs, inter-VLAN routing, and proper subnetting.
   * Implement redundancy mechanisms and ensure compatibility with existing firewalls, switches, and network management systems.
   * Ensure proper network documentation and topology diagrams reflecting the integrated wireless-wired environment.

4. **Ongoing Maintenance and Support:**

   * Provide scheduled maintenance services, including firmware updates, security patches, and performance tuning.
   * Offer proactive monitoring services to detect and resolve network issues before they impact operations.
   * Establish a helpdesk or support line for troubleshooting and user support.
   * Deliver quarterly health reports detailing network performance, uptime statistics, and recommendations for improvements.

---

## 3. Requirements (Detailed)

1. **Coverage Throughout the Office Premises:**

   * Guaranteed 100% Wi-Fi coverage in all indoor office spaces, ensuring no dead spots.
   * Strong, stable signal in high-density areas such as conference rooms, open workspaces, and break rooms.
   * Coverage extends to semi-open or enclosed areas like hallways and storage areas.

2. **Support for Latest Wireless Standards (e.g., Wi-Fi 6):**

   * Full support for IEEE 802.11ax (Wi-Fi 6) standard, ensuring higher data rates, increased capacity, better performance in congested environments, and improved battery efficiency for connected devices.
   * Backward compatibility with legacy Wi-Fi standards such as 802.11ac/n.

3. **Robust Security Features, Including WPA3 and MAC Address Filtering:**

   * Implementation of WPA3 encryption to provide stronger security against brute-force and dictionary attacks.
   * MAC address filtering to restrict network access to authorized devices only.
   * Network segmentation through VLANs to isolate sensitive data and different user groups.
   * Regular vulnerability assessments and penetration testing.
   * Compliance with relevant data protection standards such as GDPR, HIPAA, and PCI DSS.

4. **Capacity to Handle High Number of Simultaneous Connections:**

   * Design and implementation must support a minimum of 200 concurrent devices without significant degradation of service.
   * Implement advanced load balancing and airtime fairness mechanisms to ensure equitable resource allocation.
   * Utilize APs with high client density capabilities and ensure proper placement to manage crowding in high-traffic areas.

5. **Network Monitoring and Management Capabilities:**

   * Deployment of a centralized network management system capable of providing real-time monitoring, historical analytics, and automated alerts.
   * Features should include traffic analysis, bandwidth usage monitoring, and device performance statistics.
   * Remote troubleshooting and configuration capabilities.
   * Access to a web-based or cloud-hosted dashboard for the internal IT team.

---

## 4. Network Topology Diagram

```
                       +------------------+
                       |     Internet     |
                       +--------+---------+
                                |
                       +--------v---------+
                       |     Firewall     |
                       +--------+---------+
                                |
                      +---------v----------+
                      |    Core Switch     |
                      +----+----------+----+
                           |          |
            +--------------+          +--------------+
            |                                        |
     +------v------+                         +-------v------+
     | Distribution|                         | Distribution |
     |    Switch   |                         |    Switch    |
     +------+------+                         +------+-------+
            |                                       |
   +--------v-------+                    +----------v---------+
   |  Wireless APs  |                    |    Wireless APs    |
   |  (Conference)  |                    |    (Workstations)  |
   +----------------+                    +--------------------+
```
<img width="2440" height="1686" alt="output" src="https://github.com/user-attachments/assets/6cfa5552-662e-4a54-a577-172800cccd0a" />

---

## 5. Deliverables

* Detailed site survey report.
* Comprehensive installation & configuration documentation.
* Security implementation report.
* User and administrator training materials.
* Maintenance schedule and support contacts.
* Network Monitoring Dashboard with access credentials.

---

## 6. Vendor Qualifications

* Minimum 2 years of experience in enterprise wireless deployments.
* Certifications such as:

  * Cisco Certified Network Professional (CCNP) Wireless
  * Certified Wireless Network Professional (CWNP)
  * CompTIA Network+
* Provide three references with similar project experience.
* Two innovative proposals for enhancing future network scalability.

---

## 7. Cost Estimation Table

| Item                         | Unit Cost | Quantity | Total Cost   |
| ---------------------------- | --------- | -------- | ------------ |
| Site Survey                  | \$2,000   | 1        | \$2,000      |
| Wi-Fi 6 Access Points        | \$300     | 12       | \$3,600      |
| Wireless Controller          | \$2,500   | 1        | \$2,500      |
| Switches                     | \$500     | 3        | \$1,500      |
| Installation & Configuration | \$4,000   | 1        | \$4,000      |
| Security Implementation      | \$1,500   | 1        | \$1,500      |
| Monitoring System Setup      | \$1,000   | 1        | \$1,000      |
| Annual Maintenance & Support | \$2,500   | 1/year   | \$2,500      |
| **Total Estimated Cost**     |           |          | **\$18,600** |

---

## 8. Service Level Agreement (SLA) Template

| Service Metric                      | Standard                |
| ----------------------------------- | ----------------------- |
| Uptime Guarantee                    | 99.9% per month         |
| Response Time for Critical Issues   | Within 2 hours          |
| Response Time for Minor Issues      | Within 8 business hours |
| Resolution Time for Critical Issues | Within 6 hours          |
| Preventative Maintenance            | Quarterly               |
| Security Audits                     | Semi-annually           |

---

## 9. Project Timeline

| Phase                        | Duration | Completion Date |
| ---------------------------- | -------- | --------------- |
| Site Survey                  | 1 Week   | \[07-21-2025]         |
| Equipment Procurement        | 2 Weeks  | \[07-29-2025]         |
| Installation & Configuration | 2 Weeks  | \[08-10-2025]         |
| Security Setup               | 1 Week   | \[08-22-2025]         |
| Monitoring Setup             | 1 Week   | \[08-31-2025]         |
| User Training                | 1 Week   | \[09-05-2025]         |
| Maintenance Start            | Ongoing  | \[10-01-2025]         |

---

## 10. Proposal Submission

* **Submission Deadline:** July 21, 2025, by 11:00 PM.
* **Format:** PDF
* **Submit To:** [jibing.liang@mitt.ca](mailto:jibing.liang@mitt.ca)

---

## 11. Terms and Conditions

* **Contract Duration:** 1 year with renewal option based on performance.
* **Confidentiality:** Strict confidentiality must be maintained for all organizational data.
* **Legal Compliance:** Vendors must comply with relevant data protection laws including GDPR and HIPAA.

---

We look forward to engaging with a capable vendor who can deliver a secure, reliable, and future-proof wireless infrastructure.

**Prepared by:**
**Qijia Liu**
Email: [qijialiu@student.mitt.ca](mailto:qijialiu@student.mitt.ca)
Date: July 21, 2025
