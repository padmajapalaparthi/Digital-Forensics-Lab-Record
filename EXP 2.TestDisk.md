#  Digital Forensics Lab – Experiment 2  
**Recover Deleted or Damaged Files from a Storage Device using TestDisk**  

##  Aim  
To use **TestDisk** step by step to recover a missing partition and repair a corrupted one.  

### 1. Log Creation & Disk Detection  
When TestDisk starts, it creates a log file.  
All connected hard drives are detected and listed with their correct size.  
 Use the arrow keys to select the drive with the lost partition.  

<p align="center">
 <img width="956" height="512" alt="IMG 2(1)" src="https://github.com/user-attachments/assets/f2dabce3-708f-42d0-a27a-cd6a8b8f0aa5" />
</p>  

---

### 2. Partition Table Type Selection  
TestDisk auto-detects the **partition table type**.  
- Usually, the default value is correct.  
- Press **Enter** to proceed.  

<p align="center">
 <img width="955" height="561" alt="IMG 2(2)" src="https://github.com/user-attachments/assets/485858d6-f1fd-4958-8ca1-fbdb6c3d4466" />
</p>  

---

### 3. Analyse Current Partition Structure  
Choose **Analyse** → TestDisk displays the current partition structure.  
- The first partition is listed twice → indicates corruption.  
- “Invalid NTFS boot” → faulty NTFS boot sector.  
- One logical partition is missing.  

Press **Quick Search** to continue.  

<p align="center">
  <img width="959" height="562" alt="IMG 2(3)" src="https://github.com/user-attachments/assets/62b6c670-6d23-48c7-9b4c-9329d1cd7469" />
</p>  

---

### 4. Quick Search for Partitions  
Quick Search begins and TestDisk lists results in real-time.  
- Missing logical partition (Partition 3) is detected.  
- Press **p** to list files inside the partition.  
- Files in **red** are deleted entries.  

<p align="center">
<img width="956" height="536" alt="IMG 2(4)" src="https://github.com/user-attachments/assets/c323dc9a-58c9-46e0-aced-fe78b22431a9" />
</p>  

---


<br>



### 5. Deeper Search (If Needed)  
If a partition is still missing → run **Deeper Search**.  
- TestDisk scans cylinder by cylinder.  
- It can detect FAT32, NTFS, ext2/ext3 backup boot sectors.  
- Some partitions may appear as **D (Deleted)** and overlap.  
- Use **p** to preview files in each partition to decide which is correct.  

<p align="center">
  <img width="958" height="566" alt="IMG 2(5)" src="https://github.com/user-attachments/assets/2ab79dd1-38f2-4f7f-8ffa-c55eaa40d247" />
</p>  

 If files are visible → mark the correct partition as **L (Logical)** or **P (Primary)**.  

---

### 6. Partition Table Recovery  
Once the correct partitions are identified:  
- Go to **Write** → Save the partition table.  
- Confirm with **Enter → Y → OK**.  
- TestDisk updates the partition structure.  

<p align="center">
<img width="959" height="528" alt="IMG 2(6)" src="https://github.com/user-attachments/assets/90fa915b-ebaa-4cc3-9671-52f87d8c8a0e" />
</p>  

---

### 7. NTFS Boot Sector Recovery  
If the NTFS boot sector is damaged but the backup is valid:  
- Choose **Backup BS** → copy backup boot sector over the corrupted one.  
- Now both boot sector and backup are identical → filesystem recovered.  

<p align="center">
<img width="958" height="540" alt="IMG 2(7)" src="https://github.com/user-attachments/assets/15539082-52e9-4052-aa62-dd0f7202a502" />
</p>  

 Finally, TestDisk prompts: **“Restart your Computer to access your data.”**  

---
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
- Successfully recovered deleted and formatted files using **Wondershare Recoverit**.  
- Both **Quick Scan** and **Deep Scan** modes worked effectively.  
- Recovered files were saved safely and verified for integrity.
