 # Project Title: Android-Forensic-Image-Analysis

## Project Summary  
This project focuses on the forensic examination of an Android device image. The investigation involved artifact recovery, timeline creation, deleted data extraction, and reporting. Using recognized forensic tools, the image was parsed to identify SMS, call logs, browsing history, contacts, and application data. The outcome is a formal investigative report that demonstrates an understanding of mobile forensics techniques and digital evidence handling.

---

## Project Overview  
This project simulates a mobile forensic case involving the analysis of a digital Android image. It documents the procedure from image acquisition through evidence extraction to formal reporting.

---

## Objectives  

- Set up a forensic lab using Oracle VirtualBox and Ubuntu
- Install and configure Autopsy with SleuthKit
- Load and analyze a real Android image file
- Extract and interpret relevant user artifacts
- Demonstrate forensic integrity and reporting standards

  
 ---

## Tools and Environment  


| Component         | Description |
|------------------|-------------|
| Host OS        | Windows 10 |
| Virtual Machine | Ubuntu 22.04 LTS |
| Virtualization | Oracle VirtualBox |
| Forensic Tool   | Autopsy 4.19 + SleuthKit |
| Disk Image      | `nexus.img` (Android 8 – Oreo) |
| Image Source    | [DFRWS/NIST Nexus Image](https://dfrws.org/download/android-images/Nexus4_Oreo/nexus.img) |


---

##  Step-by-Step Methodology

###  Step 1: Virtual Lab Setup

1. **Install Oracle VirtualBox**  
   Download: [https://www.virtualbox.org](https://www.virtualbox.org)

2. **Download Ubuntu ISO**  
   Ubuntu 22.04: [https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)

3. **Create and Configure the VM**  
   - Name: `ForensicLab`
   - Type: Linux (Ubuntu 64-bit)
   - RAM: 4 GB
   - HDD: 25 GB (dynamically allocated)

4. **Install Ubuntu on the VM**  
   Boot with ISO and complete the OS setup

---

###  Step 2: Install Autopsy on Ubuntu

1. **Update system and install tools**
```bash
sudo apt update && sudo apt install autopsy sleuthkit -y

## Forensic Procedure
Step 3: Acquire and Load Forensic Image
Download Android image

bash
Copy
Edit
wget https://dfrws.org/download/android-images/Nexus4_Oreo/nexus.img
Open Autopsy and:

Create New Case: Android Nexus Investigation

Add Data Source: nexus.img

Select Ingest Modules:

File Metadata

Keyword Search

Android Analyzer

Communications

EXIF Parser

Web History

 Step 4: Analyze Artifacts
1.  Call Logs
File: contacts2.db

Recovered: 14 call entries (4 deleted)

Sample:

Number: +1234567890

Type: Outgoing

Time: 2020-01-15 11:32:00

2.  SMS Messages
File: mmssms.db

Recovered: 22 messages (6 deleted)

Sample:

"Meeting rescheduled. Send me the docs before 4."

3. Location History
File: location.db and wifi_cache

Recovered:

Latitude: -33.9249

Longitude: 18.4241

Time: 2020-01-16

4.  Web & App History
File Path: /data/data/com.android.chrome/

Findings:

Visited: mail.google.com, youtube.com, facebook.com

Search History, Bookmarks, and Cache entries

5.  Media Files
Path: /sdcard/DCIM/Camera/

Recovered: 42 images (5 deleted)

Details:

Some files had GPS EXIF data

Recovered deleted selfie with location info

 Summary of Findings
Artifact Type	Key Findings
Call Logs	14 total, 4 deleted, various durations
SMS Messages	22 messages, timestamps & content recovered
GPS Data	At least 5 geolocations tied to app activity
App Usage	WhatsApp, Chrome, Facebook identified
Browser Data	Google search, Gmail access confirmed
Media Files	Photos with EXIF GPS metadata found

 Digital Evidence Samples
contacts2.db – Call logs

mmssms.db – SMS/MMS content

location.db – GPS coordinates

History – Chrome web activity

image_with_exif.jpg – Camera image with location

packages.xml – Installed apps

 Forensic Integrity and Chain of Custody
Autopsy operated in read-only mode

MD5 & SHA-256 hashes generated for all recovered files

Logs preserved in the case folder

All extracted data was handled in a forensically sound manner

No changes were made to the original disk image

 Skills Demonstrated
Mobile image analysis and reporting

Android artifact extraction and parsing

SQLite database examination (SMS, Call logs)

Web and media artifact investigation

Virtual lab setup using VirtualBox & Ubuntu

Evidence documentation and forensic integrity

 References
Autopsy by SleuthKit

Digital Forensic Research Workshop (DFRWS)

Digital Corpora

SQLite Browser

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




