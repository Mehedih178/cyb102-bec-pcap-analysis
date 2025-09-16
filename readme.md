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
- **Ubuntu VM** – safe environment for malware traffic  
- **Command Line (Linux/Mac)** – handling `.zip` & file exports  

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
- **Malicious Actor IP:** `X.X.X.X`  
- **Phishing Email Subjects:**  
  - "Urgent: Wire Transfer Request"  
  - "Payment Authorization Needed"  
  - "Action Required: Invoice Attached"  

*(Replace placeholders with your actual findings.)*

---

## 📸 Screenshots
- Wireshark packet filter view  
- SMTP data pane showing phishing email  
- Exported IMF object → `.eml` file *(stretch goal)*  

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
