 # Project Title: Android-Forensic-Image-Analysis

## Project Summary  
This project focuses on the forensic examination of an Android device image. The investigation involved artifact recovery, timeline creation, deleted data extraction, and reporting. Using recognized forensic tools, the image was parsed to identify SMS, call logs, browsing history, contacts, and application data. The outcome is a formal investigative report that demonstrates an understanding of mobile forensics techniques and digital evidence handling.

---

## Project Overview  
This project simulates a mobile forensic case involving the analysis of a digital Android image. It documents the procedure from image acquisition through evidence extraction to formal reporting.

---

## Objectives  
- Analyze an Android image using forensic tools  
- Extract digital artifacts such as messages and app data  
- Create a timeline of user activity  
- Compile a structured and professional forensic report
  
 ---

## Tools and Environment  
- Forensic analysis software  
- SQLite database viewer  
- Device bridge and file extractors  
- Hashing utility for integrity checks

---

## Forensic Procedure  

1. Acquisition and Verification  
- Acquired Android disk image in standard format  
- Verified image using hash comparison to ensure integrity

2. Image Loading  
- Loaded image into forensic analysis tool  
- Automatically parsed SMS, contacts, call logs, and app data

3. Artifact Extraction  
Artifact Type      Source                Description  
SMS                Message databases     Sent and received texts  
Call Logs          Log databases         Incoming and outgoing calls  
Contacts           Address book file     Contact names and numbers  
App Data           App directories       User activity in mobile apps  
Browser History    History database      URLs and timestamps

4. Database Analysis  
- Opened SQLite databases  
- Identified deleted rows and hidden entries  
- Converted timestamps for timeline building

5. Timeline Reconstruction  
- Consolidated data across apps and system logs  
- Ordered activities chronologically to identify behavior patterns

6. Report Compilation  
- Created a structured PDF report  
- Included methodology, tools, evidence, screenshots, and analysis  
- Noted data integrity methods used throughout

---

### Report Document  
Filename: Android_Forensic_Investigation_Report.pdf  
Content Includes:  
- Summary and objectives  
- Investigation procedure  
- Extracted artifacts  
- Timeline and observations  
- Appendices with hashes and screenshots

---

### Screenshots  
Insert screenshot of recovered SMS in forensic tool  
Insert screenshot of call log database in SQLite viewer  
Insert screenshot of browsing history timeline

---

### conclusion 
- Recovered multiple mobile artifacts for analysis  
- Produced a professional investigative report  
- Applied proper evidence handling practices  
- Demonstrated core mobile forensics competence


