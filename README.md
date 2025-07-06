 # Project Title: Digital Forensic Analysis of an Android Device Image using Autopsy


## Project Overview
This project focuses on the forensic examination of an Android device image. The investigation involved artifact recovery, timeline creation, deleted data extraction, and reporting. Using recognized forensic tools, the image was parsed to identify SMS, call logs, browsing history, contacts, and application data. The outcome is a formal investigative report that demonstrates an understanding of mobile forensics techniques and digital evidence.
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
1. Installed Oracle VirtualBox from [https://www.virtualbox.org](https://www.virtualbox.org)  
2. Downloaded Ubuntu ISO from [https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)  
3. Created a new VM:
   - Name: `ForensicLab`
   - OS Type: Ubuntu (64-bit)
   - RAM: Minimum 4 GB
   - Storage: 25 GB (dynamically allocated)
4. Installed Ubuntu in the VM and completed the setup

---
### Step 2: Autopsy Installation

Opened a terminal in Ubuntu and ran:

```bash
sudo apt update && sudo apt install autopsy sleuthkit -y
autopsy

---

### Step 3.Image Acquisition and Loading

 Downloaded the Android forensic image using:

bash
Copy
Edit
wget https://dfrws.org/download/android-images/Nexus4_Oreo/nexus.img

#### 1. Launched Autopsy

#### 2. Created a new case:

-Name: Android Nexus Investigation

-Examiner: Adesanmi bunmi

#### 3. Added the data source:

-Type: Disk Image (Raw format)

-File: nexus.img

#### 4.Selected ingest modules:

-File Type Identification

-Android Analyzer

-Communications (SMS, Call Logs)

-EXIF Metadata Parser

-Web History

-Keyword Search

---

### Evidence Analysis
#### Call Logs
-File: contacts2.db

-Total entries recovered: 14 (including 4 deleted)

-Sample entry:

-Number: +1234567890

-Type: Outgoing

-Timestamp: 2020-01-15 11:32:00

#### SMS Messages
-File: mmssms.db

-Total messages recovered: 22 (6 deleted)

---

#### Location History
-Files: location.db, wifi_cache

-Coordinates found: -33.9249, 18.4241

-Timestamp: 2020-01-16

#### Browser and App History
-Path: /data/data/com.android.chrome/

#### Findings:

-Visited sites: mail.google.com, youtube.com, facebook.com

-Recovered search terms, cache files, and browsing history

#### Media Files
-Path: /sdcard/DCIM/Camera/

-Recovered 42 images (5 deleted)

-EXIF metadata revealed timestamps and GPS coordinates

-A deleted selfie was successfully recovered

## Artifact Summary
| Artifact Type   |   Description                                
| --------------- | ------------------------------------------- |
| Call Logs       | 14 records with caller ID and duration      |
| SMS Messages    | 22 total messages (6 deleted)               |
| GPS Coordinates | 5 accurate locations with timestamps        |
| App Usage       | WhatsApp, Facebook, Chrome identified       |
| Browser History | Full Chrome web history and cache           |
| Media Files     | Photos and deleted files with EXIF metadata |


---

## Digital Evidence Collected
-contacts2.db: Call log database

-mmssms.db: Text message database

-location.db: Location history database

-Chrome History: Browser activity log

-image_with_exif.jpg: Photo with GPS data

-packages.xml: Installed apps list

## Forensic Integrity
-Operated on nexus.img in read-only mode

-Generated MD5 and SHA-256 hashes for validation

-Made no modifications to the original image

-Captured an automatic audit trail through Autopsy

-Maintained full compliance with digital forensics standards

---

## Forensic Integrity and Chain of Custody
-Autopsy operated in read-only mode

-MD5 & SHA-256 hashes generated for all recovered files

-Logs preserved in the case folder

-All extracted data was handled in a forensically sound manner

-No changes were made to the original disk image

---

## Key Skills Demonstrated
Virtual lab setup using Oracle VirtualBox and Ubuntu

Installation and use of Autopsy and SleuthKit

Acquisition and analysis of Android device images

Artifact extraction and interpretation

Professional reporting of digital evidence


---

## Conclusion
This Android forensic investigation project demonstrated the ability to simulate real-world incident response using publicly available tools. The analysis of call logs, messages, locations, browser history, and app usage highlighted the effectiveness of Autopsy in recovering both live and deleted digital evidence.

The investigation validated skills in setting up a virtual lab, using forensic tools, and adhering to chain of custody principles. It served as a strong foundation for further work in cybersecurity, governance, risk, compliance, and digital forensics.




