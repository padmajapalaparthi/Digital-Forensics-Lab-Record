#  Digital Forensics Lab – Experiment 3  
**Password Capturing using Wireshark**  

---

## Introduction  
Wireshark is a network packet capture and analysis tool.  
It can capture sensitive information such as:  
- Usernames  
- Passwords  
- Email addresses  
- Session cookies  
- Other transmitted data  

Protocols like **HTTP, FTP, Telnet** often transmit unencrypted credentials.  
This makes Wireshark useful both for **network troubleshooting** and, if misused, for unauthorized access.  

In this experiment, we capture HTTP login credentials using Wireshark.  

---

##  Steps  

### Step 1 – Start Wireshark Capture  
- Open Wireshark in Windows/Linux.  
- Start capturing packets (e.g., Wi-Fi traffic).  

<p align="center">
 <img width="956" height="561" alt="Image 3(1)" src="https://github.com/user-attachments/assets/217c5ca2-042e-481c-903a-5044ee7ffc31" />
</p>  

---

### Step 2 – Perform Login on a Website  
- Visit a test website.  
- Enter login credentials (username + password).  
- These will be sent over the network in plain text (if HTTP is used).  

<p align="center">
<img width="959" height="565" alt="Image 3(2)" src="https://github.com/user-attachments/assets/2e20117a-2af7-44d4-9d42-e6ee4dc21da2" />
</p>  

---

### Step 3 – Apply HTTP Filter in Wireshark  
- After login, filter packets to show only HTTP traffic.  
- Enter the following in the **Display Filter Bar**:  


<p align="center">
  <img width="937" height="548" alt="Image 3(3)" src="https://github.com/user-attachments/assets/60a213e0-0051-4681-b59b-e2e33540a8d8" />
</p>  

---

### Step 4 – Form Submission Methods  
Web forms use two methods to send login data:  
- **GET:** Data appended in the URL (rare for login forms).  
- **POST:** Data sent in the request body (commonly used).  

---

### Step 5 – Check GET Requests  
- Apply filter:  


- Result: Only page requests are shown.  
- **No login data captured in GET requests.**  

<p align="center">
 <img width="957" height="568" alt="image" src="https://github.com/user-attachments/assets/46e10feb-812c-4f55-bed1-ebe51b8da633" />
</p>  

---

### Step 6 – Check POST Requests  
- Apply filter:  
<p align="center">
<img width="937" height="551" alt="IMG 3(5)" src="https://github.com/user-attachments/assets/a5e3f5ea-3e73-4ac8-98e5-445362038dff" />
</p>  

---

<br>







## Rubrics
<table style="width:50%; border-collapse:collapse;" border="1">
<tr>
<th>Criteria</th>
<th>Mark Allotted</th>
<th>Mark Awarded</th>
</tr>
<tr>
<td>1. GitHub Activity & Submission Regularity</td>
<td style="text-align:center;">3</td>
<td style="text-align:center;"></td>
</tr>
<tr>
<td>2. Application of Forensic Tools & Practical Execution</td>
<td style="text-align:center;">3</td>
<td style="text-align:center;"></td>
</tr>
<tr>
<td>3. Documentation & Reporting</td>
<td style="text-align:center;">2</td>
<td style="text-align:center;"></td>
</tr>
<tr>
<td>4. Engagement, Problem-Solving & Team Collaboration</td>
<td style="text-align:center;">2</td>
<td style="text-align:center;"></td>
</tr>
<tr>
<td><b>Total</b></td>
<td style="text-align:center;"><b>10</b></td>
<td style="text-align:center;"></td>
</tr>
</table>


##  Result
The experiment successfully intercepted login credentials in plaintext (captured POST), confirming that **HTTP** transmits sensitive data openly and is trivially interceptable by an attacker.



