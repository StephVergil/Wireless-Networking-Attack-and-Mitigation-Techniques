# Wireless Networking Attack and Mitigation Techniques

## Overview

This project explores methods to analyze wireless network traffic, extract data from unencrypted and encrypted transmissions, and evaluate the vulnerabilities of different wireless security protocols like WEP and WPA. Using tools such as Wireshark and Aircrack-ng, this lab demonstrates the risks of weak encryption and highlights techniques to mitigate potential threats.

---

## Key Features

1. **Plain Text Traffic Analysis**:
   - View unencrypted wireless traffic to identify data vulnerabilities.
   - Extract files, images, and sensitive information (e.g., credentials) from captured packets.

2. **Exploiting and Analyzing WEP Traffic**:
   - Decrypt WEP traffic using Aircrack-ng to recover encryption keys.
   - Analyze decrypted traffic for DNS queries, HTTP objects, and file transfers.

3. **Exploiting and Analyzing WPA Traffic**:
   - Use dictionary attacks to crack WPA passphrases.
   - Decrypt WPA traffic and analyze DNS queries, HTTP objects, and FTP file transfers.

---

## Lab Steps Overview

### 1. Examining Plain Text Traffic
- **View Wireless Traffic**: Use Wireshark to load `httpcapture.cap` and filter for DNS queries to inspect unencrypted traffic.
- **Extract Files**:
  - Use the "Export Objects" feature in Wireshark to recover HTTP files like images or zip files.
  - Save and open extracted files for further inspection.

### 2. Exploiting WEP Traffic
- **Decrypt Traffic**:
  - Use Aircrack-ng to recover WEP keys:
    ```bash
    aircrack-ng ~/Desktop/captures/WEP.cap
    ```
  - Decrypt traffic with Airdecap-ng:
    ```bash
    airdecap-ng -w <WEP_KEY> ~/Desktop/captures/WEP.cap
    ```
- **Analyze Decrypted Traffic**:
  - Load decrypted traffic in Wireshark and filter for DNS, HTTP, or FTP data.
  - Export and review recovered files such as images and zip archives.

### 3. Exploiting WPA Traffic
- **Crack WPA Passphrases**:
  - Perform a dictionary attack with Aircrack-ng:
    ```bash
    aircrack-ng ~/Desktop/captures/WPA.cap -w /usr/share/john/password.lst
    ```
- **Decrypt Traffic**:
  - Use Airdecap-ng to decrypt WPA traffic:
    ```bash
    airdecap-ng ~/Desktop/captures/WPA.cap -e <SSID> -p <PASSPHRASE>
    ```
- **Analyze Decrypted Traffic**:
  - Inspect decrypted packets in Wireshark and filter for DNS, HTTP, or FTP data.
  - Export and review transferred files.

---

## Tools Used

1. **Wireshark**: For capturing and analyzing wireless network traffic.
2. **Aircrack-ng Suite**:
   - **Aircrack-ng**: To crack WEP/WPA encryption keys.
   - **Airdecap-ng**: To decrypt wireless network traffic.
3. **Kali Linux**: The operating system used for executing wireless network attacks and analysis.

---

## Key Learning Objectives

1. **Traffic Analysis**:
   - Understand the risks of unencrypted data transmission over wireless networks.
   - Learn how to extract sensitive information from network traffic.

2. **Encryption Vulnerabilities**:
   - Explore the weaknesses of WEP encryption and how they are exploited.
   - Perform dictionary attacks to crack WPA passphrases.

3. **Mitigation Techniques**:
   - Highlight the importance of strong encryption and secure file transfer protocols (e.g., SFTP over FTP).
   - Learn strategies for securing wireless networks against common attacks.

---

## Real-World Relevance

This lab simulates realistic wireless networking scenarios to teach key cybersecurity concepts:
1. **Data Privacy**: Demonstrates the importance of encrypting wireless traffic to protect sensitive information.
2. **Protocol Vulnerabilities**: Highlights the weaknesses in outdated encryption protocols like WEP and older WPA implementations.
3. **Incident Response**: Provides hands-on experience in analyzing and responding to compromised network traffic.

---

## Documentation

For detailed instructions and step-by-step guidance, refer to the [Wireless Networking Attack and Mitigation Techniques](https://github.com/StephVergil/Wireless-Networking-Attack-and-Mitigation-Techniques/blob/main/Wireless%20Networking%20Attack%20and%20Mitigation%20Techniques-Stephanie’s%20MacBook%20Pro.docx)

---

### Disclaimer
This project was conducted in a controlled environment. Unauthorized use of these techniques or tools outside such an environment may violate ethical guidelines and legal regulations.
