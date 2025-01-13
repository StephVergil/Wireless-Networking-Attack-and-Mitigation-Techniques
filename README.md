# Wireless Networking Attack and Mitigation Techniques

## Overview

This project delves into the vulnerabilities of wireless networks, exposing the risks posed by outdated encryption protocols such as WEP and WPA. By analyzing traffic, exploiting encryption weaknesses, and demonstrating mitigation techniques, it provides a comprehensive understanding of wireless security.

Using tools like **Wireshark**, **Aircrack-ng**, and **Kali Linux**, this project simulates real-world attack scenarios to illustrate how adversaries exploit wireless networks and how these threats can be mitigated effectively.

---

## Key Features

1. **Plain Text Traffic Analysis**:
   - Demonstrate the risks of unencrypted data transmission in wireless networks.
   - Recover sensitive information such as credentials, files, and images from intercepted traffic.

2. **WEP Encryption Exploitation**:
   - Analyze the inherent weaknesses of WEP encryption.
   - Execute dictionary and brute-force attacks to recover encryption keys.
   - Decrypt and analyze intercepted traffic for sensitive user data.

3. **WPA Encryption Exploitation**:
   - Explore vulnerabilities in WPA passphrase-based authentication.
   - Perform dictionary attacks to recover passphrases.
   - Analyze decrypted WPA traffic for DNS, HTTP, and FTP communication.

4. **Mitigation Strategies**:
   - Propose techniques for securing wireless networks using modern encryption protocols.
   - Highlight best practices to defend against common wireless attacks.

---

## Lab Steps Overview

### **1. Plain Text Traffic Analysis**
- **Objective**: Understand the risks of unencrypted wireless communication.
- **Steps**:
  - Open `.cap` files in Wireshark to inspect DNS queries and HTTP traffic.
  - Use the `Export Objects` feature in Wireshark to recover files (e.g., images or zip archives) from captured traffic.

### **2. Exploiting WEP Traffic**
- **Objective**: Demonstrate the vulnerabilities of WEP encryption.
- **Steps**:
  - Use Aircrack-ng to recover WEP keys:
    ```bash
    aircrack-ng ~/captures/WEP.cap -w /path/to/wordlist
    ```
  - Decrypt the traffic using Airdecap-ng:
    ```bash
    airdecap-ng -w <WEP_KEY> ~/captures/WEP.cap
    ```
  - Load decrypted `.cap` files in Wireshark to analyze DNS, HTTP, and FTP data.

### **3. Exploiting WPA Traffic**
- **Objective**: Explore weaknesses in WPA passphrase-based security.
- **Steps**:
  - Perform a dictionary attack to recover WPA passphrases:
    ```bash
    aircrack-ng ~/captures/WPA.cap -w /usr/share/wordlists/rockyou.txt
    ```
  - Decrypt the traffic using Airdecap-ng:
    ```bash
    airdecap-ng -p <PASSPHRASE> -e <SSID> ~/captures/WPA.cap
    ```
  - Analyze the decrypted traffic in Wireshark to extract HTTP objects and FTP transfers.

### **4. Mitigation Techniques**
- **Objective**: Evaluate strategies to secure wireless networks.
- **Steps**:
  - Implement WPA3 encryption to replace outdated protocols.
  - Enable network segmentation and VLANs to minimize attack surfaces.
  - Use strong passphrases and regularly update credentials.
  - Deploy intrusion detection systems to monitor suspicious wireless activity.

---

## Tools and Technologies

- **Wireshark**: Packet capture and analysis.
- **Aircrack-ng Suite**:
  - **Aircrack-ng**: Crack WEP/WPA encryption keys.
  - **Airdecap-ng**: Decrypt captured network traffic.
- **Kali Linux**: Penetration testing and network security platform.
- **Wordlists**: Predefined password lists (e.g., `rockyou.txt`) for dictionary attacks.

---

## Learning Objectives

1. **Traffic Analysis**:
   - Identify vulnerabilities in unencrypted wireless traffic.
   - Recover sensitive data from captured packets.

2. **Encryption Weaknesses**:
   - Analyze the limitations of WEP and WPA protocols.
   - Demonstrate how attackers exploit these vulnerabilities.

3. **Defensive Strategies**:
   - Learn how to implement modern encryption standards like WPA3.
   - Understand the importance of secure network configurations and monitoring.

---

## Real-World Applications

1. **Data Privacy**: Highlight the risks of unencrypted communication and the need for robust encryption protocols.
2. **Protocol Security**: Demonstrate why outdated protocols like WEP are unsuitable for modern networks.
3. **Incident Response**: Teach the tools and techniques required for monitoring, detecting, and mitigating network-based threats.

---

## Setup and Usage

### **Prerequisites**
- Install **Kali Linux** and ensure required tools (Wireshark, Aircrack-ng suite) are available.
- Download the provided `.cap` files for analysis.

### **Execution**
1. **Analyze Captured Traffic**:
   - Open `.cap` files in Wireshark to inspect DNS and HTTP traffic.
   - Use filtering options (e.g., `http`, `dns`) to narrow down results.

2. **Recover Encryption Keys**:
   - Use Aircrack-ng to crack WEP and WPA keys:
     ```bash
     aircrack-ng <capture_file> -w <wordlist>
     ```
   - Decrypt traffic with Airdecap-ng.

3. **Mitigation Testing**:
   - Implement secure encryption protocols (e.g., WPA3).
   - Deploy network monitoring and intrusion detection tools.

---

## Documentation

For detailed step-by-step instructions, refer to the full project documentation:  
[Wireless Networking Attack and Mitigation Techniques](https://github.com/StephVergil/Wireless-Networking-Attack-and-Mitigation-Techniques/blob/main/Wireless%20Networking%20Attack%20and%20Mitigation%20Techniques-Stephanie%E2%80%99s%20MacBook%20Pro.docx)

---

## References

1. **Wireshark Documentation**: [https://www.wireshark.org/docs/](https://www.wireshark.org/docs/)
2. **Aircrack-ng Documentation**: [https://www.aircrack-ng.org/documentation.html](https://www.aircrack-ng.org/documentation.html)
3. **Kali Linux**: [https://www.kali.org/](https://www.kali.org/)

---

## Disclaimer

This project was conducted in a controlled environment for educational purposes only. Unauthorized use of these techniques or tools outside of legal and ethical boundaries may result in violations of cybersecurity laws. Always seek proper permissions before conducting such activities.

---

