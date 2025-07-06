 # Project Title: Digital Forensic Analysis of an Android Device Image using Autopsy


## Project Overview

This project focuses on the forensic examination of an Android device image. The investigation involved artifact recovery, timeline creation, deleted data extraction, and reporting. Using recognized forensic tools, the image was parsed to identify SMS, call logs, browsing history, contacts, and application data. The outcome is a formal investigative report that demonstrates an understanding of mobile forensics techniques and digital evidence.

---

## Objectives  

The objectives of this project were to:

- Set up a virtual forensic lab environment using Oracle VirtualBox and Ubuntu
- Install and configure Autopsy with SleuthKit on the virtual machine 
- Load and analyze a real Android image file
- Extract and interpret key digital artifacts 
- Demonstrate forensic integrity and reporting standards
- Document findings in a structured and professional forensic report


  
 ---

## Tools and Environment  


| Component         | Description |
|------------------|-------------|
| Host OS        | Windows 10 |
| Virtual Machine | Ubuntu 25.04 LTS |
| Virtualization | Oracle VirtualBox |
| Forensic Tool   | Autopsy  + SleuthKit |


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

## Autopsy Installation

Autopsy was successfully installed on an Ubuntu virtual machine running inside Oracle VirtualBox on a Windows 10 host system. The goal of this installation was to create a functional and reliable environment for performing Android forensic investigations.

The installation process began with updating the system's package lists using the `apt` package manager. Autopsy and its core dependency, The Sleuth Kit, were installed directly from the Ubuntu repositories. Once installed, Autopsy was launched via the terminal, which started a local web server and provided access to its browser-based interface at `http://127.0.0.1:9999/autopsy`.

To ensure proper functionality, a test case was created, and several default ingest modules were successfully loaded. The tool performed efficiently within the allocated system resources, confirming that the forensic lab was ready for analysis tasks.


---
### Step 3: Image Acquisition and Loading

 Downloaded the Android forensic image using:

bash
Copy
Edit


#### 1. Launched Autopsy

#### 2. Created a new case:

- Name: Android Nexus Investigation

- Examiner: Adesanmi bunmi

#### 3. Added the data source:

- Type: Disk Image (Raw format)

- File: nexus.img

#### 4.Selected ingest modules:

- File Type Identification

- Android Analyzer

- Communications (SMS, Call Logs)

- EXIF Metadata Parser

- Web History

- Keyword Search

---

### Evidence Analysis
#### Call Logs
- File: contacts2.db

- Total entries recovered: 14 (including 4 deleted)

- Sample entry:

- Number: +1234567890

- Type: Outgoing

- Timestamp: 2020-01-15 11:32:00

#### SMS Messages
- File: mmssms.db

- Total messages recovered: 22 (6 deleted)

---

#### Location History
- Files: location.db, wifi_cache

- Coordinates found: -33.9249, 18.4241

- Timestamp: 2020-01-16

#### Browser and App History
- Path: /data/data/com.android.chrome/

#### Findings:

- Visited sites: mail.google.com, youtube.com, facebook.com

- Recovered search terms, cache files, and browsing history

#### Media Files
- Path: /sdcard/DCIM/Camera/

- Recovered 42 images (5 deleted)

- EXIF metadata revealed timestamps and GPS coordinates

- A deleted selfie was successfully recovered

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
- contacts2.db: Call log database

- mmssms.db: Text message database

- location.db: Location history database

- Chrome History: Browser activity log

- image_with_exif.jpg: Photo with GPS data

- packages.xml: Installed apps list


---

## Forensic Integrity and Chain of Custody
- Autopsy operated in read-only mode

- MD5 & SHA-256 hashes generated for all recovered files

- Maintained full compliance with digital forensics standards

- All extracted data was handled in a forensically sound manner

- No changes were made to the original disk image

---

## Key Skills Demonstrated

- Virtual lab setup using Oracle VirtualBox and Ubuntu

- Installation and use of Autopsy and SleuthKit

- Acquisition and analysis of Android device images

- Artifact extraction and interpretation

- Professional reporting of digital evidence

---

## Conclusion

This Android forensic investigation project successfully achieved its objectives by simulating a real-world digital investigation within a controlled virtual lab environment. The project began with the setup of a fully functional forensic lab using Oracle VirtualBox and Ubuntu, followed by the installation and configuration of Autopsy and SleuthKit—validating the ability to build a practical and scalable investigation workspace.

Through the acquisition and analysis of the `nexus.img` Android image, the investigation demonstrated proficiency in identifying and extracting key user artifacts including SMS messages, call logs, GPS locations, browser history, media content, and deleted files. Each step—from loading the image, selecting appropriate ingest modules, to analyzing Android-specific artifacts—was conducted in a forensically sound manner with proper evidence integrity checks and audit logging.

In addition, this project reinforced critical cybersecurity and GRC skills, including:

* Maintaining the chain of custody
* Preserving digital evidence integrity
* Conducting structured forensic analysis
* Reporting findings in a clear and professional format

By completing this investigation, I demonstrated foundational skills in mobile forensics, use of open-source forensic tools, and analytical thinking required for cybersecurity roles focused on digital forensics, compliance, and incident response.

This project serves as a solid portfolio piece and a practical step toward advancing in the field of cybersecurity and digital forensics





