# Catch Me if You Can – BEC Analysis

This project is part of the CodePath CYB102 course. Using Wireshark, I analyzed SMTP traffic in packet capture files to detect Business Email Compromise (BEC) phishing attempts. The investigation involved identifying malicious IPs, extracting fraudulent emails, and documenting the methodology.

---

## 🎯 Project Goals
- Inspect `.pcap` files for email traffic  
- Differentiate between legitimate and phishing emails  
- Identify the malicious actor’s IP address  
- Extract subject lines of phishing attempts  
- *(Optional)* Export `.eml` objects for deeper inspection  

---

## 🛠 Tools & Environment
- **Wireshark** – packet inspection & SMTP filters  
- **Kali Linux VM** – safe environment for malware traffic  
- **Command Line (Linux)** – handling `.zip` & file exports  

---

## 🔍 Methodology

### 1. Filtering SMTP Traffic
Applied filters like:
- `smtp`
- `smtp.data.fragment`

This isolated email content for inspection.

### 2. Email Reconstruction
Reassembled fragmented SMTP data to view full messages.

### 3. Phishing Indicators
Looked for:
- Suspicious subjects  
- Unusual sender addresses  
- External/malicious IP origins  

### 4. Malicious Actor Identification
Traced packet sources back to confirm the attacker’s IP.

---

## 📊 Key Findings
- **Malicious Actor IP:** `10.6.1.104`  
- **Phishing Email Subjects:**  
  - "Read carefully! - dayrit"  
  - "I can destroy everything! - 12345678"  
  - "Your password! - nafd111"  

---

## 📸 Screenshots
- Wireshark packet filter view  
- SMTP data pane showing phishing email  
- Exported IMF object → `.eml` file *(stretch goal)*  
<img width="1919" height="1080" alt="eml1" src="https://github.com/user-attachments/assets/b5ef3d46-e1a4-4a92-ae86-e68cff892758" />
<img width="1935" height="1080" alt="eml2" src="https://github.com/user-attachments/assets/5089e9c4-72e0-4503-b6b2-8af454fe2f1b" />
<img width="1908" height="1077" alt="eml3" src="https://github.com/user-attachments/assets/a6f0e2af-84cd-4ed3-ae58-2f2a891cbd86" />

---

## ⭐ Stretch Goal
Exported `.eml` objects (phishing emails) were saved and inspected in a safe environment.

---

## 💡 Reflection
This project demonstrated how real-world attackers exploit email protocols and how packet analysis tools like Wireshark can uncover fraud. It strengthened my skills in:
- Email forensics  
- Packet filtering & reassembly  
- Identifying malicious network traffic

---
