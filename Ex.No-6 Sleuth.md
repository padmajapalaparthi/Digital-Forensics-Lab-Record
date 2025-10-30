#  **Experiment No. 06 — Digital Forensic Analysis using Sleuth Kit (TSK)**

## Aim
To perform digital forensic analysis using The Sleuth Kit (TSK) by examining a disk image, recovering deleted files, analyzing file system metadata, and extracting evidence to understand command-line based forensic investigation techniques.
## Procedure:

##  **Step 1: Installing Sleuth Kit**

1. **Download the Tool:**  
   - Head over to the official Sleuth Kit page or use this link:  
      [Download Sleuth Kit](https://drive.google.com/drive/u/1/folders/1ilSFY7Tqn2L7AjQGhq8yJ8kixc_xTU-v)  
   - Choose the latest stable **Windows-compatible** version.

2. **Installation Process:**  
   - Run the installer and follow the setup wizard .  
   - Once done, TSK will be ready to use on your system!

---

##  **Step 2: Acquire the Disk Image**

Before analysis, a **forensic disk image** (a perfect bit-by-bit copy) of the device is needed.

1. **Create Disk Image:**  
   - Use tools like **FTK Imager**  or **`dd`** to create an exact copy.  
   - Save it in a TSK-supported format: `.dd`, `.raw`, `.img`, or `.E01`.

2. **Sample Evidence Files:**  
   - For this lab, download the following from the provided link:  
      `4Dell Latitude CPi.E01`  
      `4Dell Latitude CPi.E02`

---

##  **Step 3: Mounting the Disk Image (Optional)**

Mounting lets you access the disk image as if it were a normal drive.

- Use **OSFMount**  to mount the image in **read-only mode**.  
-  *Note: This is optional but helps when browsing the file system.*

---

## **Step 4: File System Analysis with TSK**

Now let’s dive into Sleuth Kit tools to inspect the file system.

### Navigate to the TSK Directory

```bash
cd "C:\Program Files (x86)\sleuthkit-4.14.0-win32\bin"
```
  
<img width="400" alt="exp6 1" src="https://github.com/user-attachments/assets/ab629da5-77d5-478b-9a95-4edb64f6050f" />

---

###  Identify File System Type

```bash
.\fsstat.exe -o 63 "C:\Users\palap\Downloads\4Dell Latitude CPi.E01" 
```
<img width="600" alt="exp6 2" src="https://github.com/user-attachments/assets/e29e39f6-c5e9-405d-938a-b8bfab58ba6e" />

 *Displays key details about the file system type and structure.*

---

### View Partition Layout

```bash
.\mmls.exe "C:\Users\palap\Downloads\4Dell Latitude CPi.E01"
```
  

 *Lists all partitions and their respective start/end addresses.*

---

###  List Files and Directories

```bash
.\fls.exe -o 63 "C:\Users\palap\Downloads\4Dell Latitude CPi.E01" 
```


 *Recursively lists files and folders with their inode details.*

---

###  Recover Deleted Files

```bash
.\icat.exe -o 63 "C:\Users\palap\Downloads\4Dell Latitude CPi.E01" 119 > "C:\Users\knsha\Downloads\BOOTLOG_recovered.TXT"
```
 
<img width="1903" height="933" alt="exp6 4" src="https://github.com/user-attachments/assets/c469c0df-8080-43ef-93a8-68784f35841b" />



 *Recovers a deleted or existing file by its inode number.*

---

## **Step 5: Metadata Analysis**

To uncover file history and access details, view the file’s metadata.

```bash
.\istat.exe -o 63 "C:\Users\palap\Downloads\4Dell Latitude CPi.E01" 119 > "C:\Users\knsha\Downloads\BOOTLOG_recovered.TXT" 
```
 
<img width="600" alt="exp6 5" src="https://github.com/user-attachments/assets/7a5b9f31-59a1-4d8f-a1c8-41af9428256e" />


## **Step 6: Report Generation**

After completing your analysis:

1. **Compile All Outputs:**  
   Collect files like `filesystem_info.txt`, `partitions.txt`, `file_list.txt`, and `timeline.txt`.

2. **Interpret and Document:**  
   Write a clear summary explaining your findings, methods used, and any key recovered evidence.

---

## **Step 7: Evidence Preservation**

Ensuring the integrity of evidence is the final and most important step .

1. **Archive Evidence Securely:**  
   Use encryption  and hashing  to store your disk image and findings.

2. **Maintain Chain of Custody:**  
   Keep the evidence in a secure location following proper forensic protocols .

---
<br> <br> <br> <br> <br> <br> <br> <br> <br> <br> <br> <br> <br> <br> <br> <br> <br> <br>

## Rubrics 
<table style="width:50%; border-collapse:collapse;" border="1"> <tr> <th>Criteria</th> <th>Mark Allotted</th> <th>Mark Awarded</th> </tr> <tr> <td>1. GitHub Activity & Submission Regularity</td> <td style="text-align:center;">3</td> <td style="text-align:center;"></td> </tr> <tr> <td>2. Application of Forensic Tools & Practical Execution</td> <td style="text-align:center;">3</td> <td style="text-align:center;"></td> </tr> <tr> <td>3. Documentation & Reporting</td> <td style="text-align:center;">2</td> <td style="text-align:center;"></td> </tr> <tr> <td>4. Engagement, Problem-Solving & Team Collaboration</td> <td style="text-align:center;">2</td> <td style="text-align:center;"></td> </tr> <tr> <td><b>Total</b></td> <td style="text-align:center;"><b>10</b></td> <td style="text-align:center;"></td> </tr> </table>

## **Result**

Using the **Sleuth Kit (TSK)**, investigators can efficiently extract, analyze, and preserve digital evidence .  
It remains one of the most reliable and open-source forensic toolkits for digital investigation .
