# 🧠 WannaCry Memory Analysis (Volatility Forensics Project)

This project showcases a complete static memory forensics analysis of a sample infected with **WannaCry ransomware**, using Volatility and other forensic tools. It demonstrates real-world malware analysis techniques based on a `.vmem` memory dump.

## 📁 Project Overview

- **Target Malware:** WannaCry Ransomware
- **Memory Dump:** `VolpymeL1.vmem`
- **Tools Used:**  
  - Volatility 2.6 (memory analysis & process dumping)  
  - `strings` (extract readable strings from binary)  
  - HxD (hex inspection of PE binary)  
  - CFF Explorer (PE header and import table inspection)

---

## 🔍 Key Findings

- **Suspicious Process:** `@WanaDecryptor@` (PID 740)
- **Parent:** `tasksche.exe`, launched by `explorer.exe`
- **Extracted File:** `executable.740.exe`

### 📌 Indicators of Compromise (IOCs)

- **Ransom Strings:**  
  “Your payment has been checked!”, “Start decrypting now!”

- **Destructive Commands:**  
  `vssadmin delete shadows`, `wmic shadowcopy delete`, `bcdedit`, etc.

- **Bitcoin Address:**  
  `13AM4VW2dhxYgXeQepoHkHSQuy6NgaEb94`

- **URLs Found:**  
  `https://www.google.com/search?q=how+to+buy+bitcoin`

- **Import DLLs:**  
  `Kernel32.dll`, `Advapi32.dll`, `Shell32.dll`, `Urlmon.dll`

- **PE Header Timestamp:**  
  `May 12, 2017` (matches original WannaCry timeline)

---

## 📘 Report Includes

- Memory profile identification
- Process tree analysis and dumping
- String analysis (ransom messages, API calls, file extensions)
- PE header, import table, and section inspection
- Full summary and forensic conclusion

---

## 📄 Author

**Michael Helu**  
Cybersecurity Student | Malware Analysis & Memory Forensics Enthusiast  
📅 Date of Analysis: 29-06-2025  


---

