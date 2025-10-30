# Ex.No.1    FTK Imager: A Forensic Imaging Tool Overview

## Acquiring Volatile Memory (RAM) Using FTK Imager
<br>


### Steps to Capture RAM Using FTK Imager
<br>

### 1. Run as Administrator
- Open **FTK Imager** with administrative privileges.  
- Right-click the FTK Imager icon and select **Run as administrator**.

### 2. Initiate Memory Capture
- In the top menu bar, click **File → Capture Memory...** from the dropdown list.
  <br>
<br>
  <img width="952" height="494" alt="IMG 1(2)" src="https://github.com/user-attachments/assets/25066f07-cbe3-4633-b2a5-adb4db80f558" />
<br>
<br>

### 3. Configure Destination
A dialog box will appear where you configure where and how the memory will be saved.

- **Destination Path:**  
  Click **Browse** to select a folder on an **external drive** (not the system drive).  

- **Destination Filename:**  
  You can keep the default `memdump.mem` or assign a more descriptive name.

- **Optional: Include pagefile.sys**  
  Check this box to capture `pagefile.sys`, which is virtual memory stored on the disk.  
  > Note: This may increase capture size and duration, but can contain valuable artifacts.

- **Optional: Create AD1 file**  
  Saves the memory dump in an AccessData-specific container file.  
  > Generally not necessary if using tools like **Volatility** for analysis.



<br>
<br>
<br><img width="956" height="497" alt="IMG 1(3)" src="https://github.com/user-attachments/assets/2b7b1b66-2ecc-4e3f-82df-7b0eaca3368b" />
<br>

### 4. Start Capture
- Click the **Capture Memory** button to begin acquisition.
<br>
<br>
<img width="953" height="498" alt="IMG 1(4)" src="https://github.com/user-attachments/assets/b57ed391-68d4-423f-9c76-9ab43a2a5ada" />
<br>
<br>

### 5. Wait for Completion
- A progress bar will indicate the capture status.  
- Capture time depends on the system’s RAM size.  
- Once finished, the memory dump file will be available in the destination folder.
---
<br>
<br>

## Acquiring Non-Volatile Memory (Disk Image) Using FTK Imager


### 1. Start the Process
- In FTK Imager, go to the top menu bar: **File → Create Disk Image...**.

<br>
<br>
<img width="950" height="510" alt="IMG 1(5)" src="https://github.com/user-attachments/assets/8a6922c0-f0d3-4a70-8456-30342e932510" />
<br>
<br>

### 2. Select Source Evidence Type
A window will appear asking you to choose the source type:

- **Physical Drive:** Images the entire disk, including all partitions, unallocated space, and the Master Boot Record (MBR).  
- **Logical Drive:** Images a specific partition (e.g., C: drive).  
- **Image File:** Converts or copies an existing image file.  
- **Contents of a Folder:** Creates an image of a specific folder only.  

> **Tip:** For full forensic imaging, select **Physical Drive**.
<br>
<br>
<p align="center">
<img width="958" height="500" alt="IMG 1(6)" src="https://github.com/user-attachments/assets/2e049658-367f-4ce5-977f-4786eee5ec32" />
</p>
<br>
<br>

### 3. Select the Source Drive
- From the dropdown, choose the physical drive to image (connected via **write-blocker**).  
- Click **Finish**.
 <br>
<br>
<p align="center">
<img width="959" height="504" alt="IMG 1(7)" src="https://github.com/user-attachments/assets/0c4736b1-5194-4240-86ec-cdef8c52a889" />
</p>
<br>
<br>

### 4. Configure the Image Destination
- Click **Add...** in the "Create Image" window to define the image **format** and **destination**.
  <br>
<br>
<p align="center">
<img width="954" height="507" alt="IMG 1(8)" src="https://github.com/user-attachments/assets/6f84cfeb-e7f8-4c8b-934d-0b309f980cbf" />
<br>

#### Options:

- **Image Type:**  
  - **E01 (EnCase Format):** Recommended; includes compression, metadata, and error-checking.  
  - **Raw (DD):** Bit-for-bit copy with no extra features.
<br>
<br>
<p align="center">
<img width="953" height="505" alt="IMG 1(9)" src="https://github.com/user-attachments/assets/0d8e4316-08c8-4105-b2a6-6065e0304d2a" />
</p>
<br>
<br>

- **Fill in Evidence Item Information:**  
  - Enter case details, examiner name, and description.  
  - This information is stored in the image metadata (important for documentation).
 <p align="center">
<img width="955" height="500" alt="img 1(10)" src="https://github.com/user-attachments/assets/52fe1a03-796f-48a7-a025-6526d527d1aa" />
</p>
<br>
<br>

- **Choose Destination Folder:**  
  - Must be a different drive from the source.  
  - Name the image file (e.g., `Case001_SuspectHDD`).  

- **Image Fragment Size:**  
  - Set a value to split the image into multiple parts.  
  - Set to `0` for a single image file.
  <br>
  <br>
  
<p align="center">
<img width="957" height="502" alt="IMG 1(11)" src="https://github.com/user-attachments/assets/68c06591-e922-4cb9-9398-83e5fa3a87f1" />
</p>
<br>
<br>


### 5. Start the Imaging Process
- Click **Finish** to return to the "Create Image" screen.  
- **Check "Verify images after they are created"** to calculate hash values and ensure integrity.  
- Click **Start**.
  <br>
  <br>
  <p align="center">
<img width="959" height="513" alt="IMG 1(12)" src="https://github.com/user-attachments/assets/ba53f2aa-fe46-483c-a579-f88a0e2bdc1d" />
<img width="959" height="503" alt="IMG 1(13)" src="https://github.com/user-attachments/assets/7638673a-7b59-4d89-b917-043b90bc4f97" />
</p>
<br>
<br>

### 6. Completion and Hash Verification
- The imaging process may take time depending on the drive size.  
- After completion, FTK Imager verifies the hashes automatically.  
- A final window shows **MD5** and **SHA1** hashes for both the source drive and image.  
- Matching hashes confirm the forensic image’s integrity.

## Rubrics
<div style="display:flex; justify-content:center;">
<table style="width:50%; border-collapse:collapse; text-align:center;" border="1">
<tr>
<th>Criteria</th>
<th>Mark Allotted</th>
<th>Mark Awarded</th>
</tr>
<tr>
<td>1. GitHub Activity & Submission Regularity</td>
<td>3</td>
<td></td>
</tr>
<tr>
<td>2. Application of Forensic Tools & Practical Execution</td>
<td>3</td>
<td></td>
</tr>
<tr>
<td>3. Documentation & Reporting</td>
<td>2</td>
<td></td>
</tr>
<tr>
<td>4. Engagement, Problem-Solving & Team Collaboration</td>
<td>2</td>
<td></td>
</tr>
<tr>
<td><b>Total</b></td>
<td><b>10</b></td>
<td></td>
</tr>
</table>
</div>



## Result

Successfully captured RAM and disk images using FTK Imager, verified integrity with matching MD5 & SHA1 hashes.  
The acquired forensic images are ready for analysis using tools like Autopsy, FTK Toolkit, or Volatility.
