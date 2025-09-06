# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.
<img width="1919" height="1067" alt="Screenshot 2025-09-06 142412" src="https://github.com/user-attachments/assets/c42feb2b-8507-4b6e-8b69-3af42d2e9f53" />
<img width="1919" height="1004" alt="Screenshot 2025-09-06 142620" src="https://github.com/user-attachments/assets/a52c1352-38c7-4049-b806-2ac0abef9e86" />
<img width="1919" height="994" alt="Screenshot 2025-09-06 133349" src="https://github.com/user-attachments/assets/63deb7c9-3085-4520-9f30-f2247331225b" />


### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.
<img width="1919" height="1000" alt="Screenshot 2025-09-06 133643" src="https://github.com/user-attachments/assets/65b1a1e5-f4da-4f62-8314-ee5831364004" />
<img width="1919" height="989" alt="Screenshot 2025-09-06 134236" src="https://github.com/user-attachments/assets/47f5a7b1-f4ec-49c4-a89b-58d1efda5fa2" />
<img width="1919" height="1066" alt="Screenshot 2025-09-06 134340" src="https://github.com/user-attachments/assets/a867afb1-e916-4b59-ad42-f80233568398" />
<img width="1475" height="826" alt="Screenshot 2025-09-06 134429" src="https://github.com/user-attachments/assets/bdc85528-d5aa-487b-9687-bc62c5efec42" />


### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.
<img width="1919" height="1007" alt="image" src="https://github.com/user-attachments/assets/50c1fd9c-ac4b-482a-978c-1b48a43c7b44" />


## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1919" height="1007" alt="image" src="https://github.com/user-attachments/assets/a2151ae1-f9f5-41b3-8f74-690843a6e6aa" />
<img width="1919" height="995" alt="image" src="https://github.com/user-attachments/assets/2158e74c-eaad-4fc4-879a-1d9fc9b6e648" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
