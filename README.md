# Wireless Networking Attack and Mitigation Techniques

## Overview

This project investigates the vulnerabilities of wireless networks by analyzing traffic, exploiting encryption weaknesses, and proposing mitigation strategies. It focuses on exposing the risks of outdated security protocols such as WEP and WPA, while emphasizing the importance of adopting strong encryption and secure configurations.

Using tools like **Wireshark** and **Aircrack-ng**, this project demonstrates how attackers exploit wireless networks and highlights practical measures to defend against such attacks.

---

## Key Features

1. **Plain Text Traffic Analysis**:
   - Examine unencrypted wireless traffic for vulnerabilities.
   - Extract sensitive data, such as files, credentials, and images, from intercepted packets.

2. **WEP Encryption Exploitation**:
   - Crack WEP encryption keys using dictionary and brute-force attacks.
   - Decrypt captured traffic to reveal user activities and data.

3. **WPA Encryption Exploitation**:
   - Perform dictionary attacks to recover WPA passphrases.
   - Decrypt and analyze WPA traffic for DNS, HTTP, and FTP data.

4. **Mitigation Techniques**:
   - Outline strategies for strengthening wireless network security.
   - Demonstrate the importance of transitioning from insecure protocols to robust encryption mechanisms.

---

## Lab Steps Overview

### **1. Examining Plain Text Traffic**
- **Task**: Analyze unencrypted traffic to uncover vulnerabilities.
- **Steps**:
  - Use Wireshark to inspect DNS queries and HTTP objects.
  - Export and view sensitive files like images and ZIP archives from traffic captures.

### **2. Exploiting WEP Traffic**
- **Task**: Crack WEP encryption and analyze decrypted traffic.
- **Steps**:
  - Use Aircrack-ng to recover WEP keys and decrypt traffic with Airdecap-ng.
  - Analyze DNS, HTTP, and FTP data in Wireshark to extract sensitive information.

### **3. Exploiting WPA Traffic**
- **Task**: Crack WPA passphrases and analyze decrypted traffic.
- **Steps**:
  - Perform dictionary attacks with Aircrack-ng.
  - Decrypt traffic using Airdecap-ng and analyze HTTP and FTP data in Wireshark.

---

## Tools and Technologies

1. **Wireshark**: For capturing and analyzing network traffic.
2. **Aircrack-ng Suite**:
   - **Aircrack-ng**: To crack WEP/WPA keys.
   - **Airdecap-ng**: To decrypt captured wireless traffic.
3. **Kali Linux**: An essential platform for executing network attacks and analyses.

---

## Learning Objectives

1. **Traffic Analysis**:
   - Understand the risks of transmitting unencrypted data.
   - Learn how attackers extract sensitive information from network traffic.

2. **Encryption Vulnerabilities**:
   - Explore the weaknesses of WEP and WPA protocols.
   - Gain hands-on experience with tools used to exploit these vulnerabilities.

3. **Mitigation Techniques**:
   - Learn how to secure wireless networks using modern encryption standards.
   - Understand best practices for preventing unauthorized access and data breaches.

---

## Real-World Applications

This project simulates real-world scenarios to educate on cybersecurity fundamentals:
- **Data Privacy**: Highlights the need for encrypted communication to safeguard sensitive data.
- **Protocol Evolution**: Demonstrates why older protocols like WEP are obsolete and insecure.
- **Incident Response**: Provides insights into monitoring, detecting, and mitigating network attacks.

---

## Setup and Usage

### **Prerequisites**
- Install **Kali Linux** with the required tools (Wireshark, Aircrack-ng suite).
- Download the traffic capture files used for analysis.

### **How to Run the Lab**
1. **Inspect Captured Traffic**:
   - Open `.cap` files in Wireshark and use filters like `dns`, `http`, and `ftp` to explore data.
   - Export files using Wireshark's `Export Objects` feature.

2. **Crack WEP/WPA Keys**:
   - Use Aircrack-ng to recover encryption keys:
     ```bash
     aircrack-ng <capture_file> -w <wordlist>
     ```
   - Decrypt traffic using Airdecap-ng:
     ```bash
     airdecap-ng -w <key> <capture_file>
     ```

3. **Analyze Decrypted Traffic**:
   - Load decrypted `.cap` files into Wireshark for further inspection.
   - Extract and analyze data to understand user activities.

---

## Documentation

For step-by-step guidance, refer to the detailed project documentation:
[Wireless Networking Attack and Mitigation Techniques](https://github.com/StephVergil/Wireless-Networking-Attack-and-Mitigation-Techniques/blob/main/Wireless%20Networking%20Attack%20and%20Mitigation%20Techniques-Stephanie%E2%80%99s%20MacBook%20Pro.docx)

---

### Disclaimer

This project was conducted in a controlled environment for educational purposes. Unauthorized use of these techniques or tools outside of ethical and legal guidelines may lead to violations of cybersecurity laws and regulations.

---

## References

1. **Wireshark Documentation**: [https://www.wireshark.org/docs/](https://www.wireshark.org/docs/)
2. **Aircrack-ng Documentation**: [https://www.aircrack-ng.org/documentation.html](https://www.aircrack-ng.org/documentation.html)
3. **Kali Linux**: [https://www.kali.org/](https://www.kali.org/)

---

