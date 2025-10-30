</head>
<body>

<h1>Experiment 9: Using Process Explorer to Identify Suspicious Processes</h1>

<h2>Aim</h2>
<p>To use Process Explorer to identify and analyze suspicious processes running on a Windows system.</p>

<h2>Objective</h2>
<ul>
  <li>Monitor running processes and their resource usage.</li>
  <li>Verify digital signatures of executables.</li>
  <li>Detect hidden or unauthorized processes.</li>
</ul>
<h2>Procedure </h2>

<h3>Step1: Launch Process Explorer</h3>
<p>Open <code>procexp.exe</code>. The Process Explorer window displays a hierarchical view of all running processes, showing their CPU usage, memory usage, and parent–child relationships.</p>
<img width="1915" height="1125" alt="Screenshot 2025-10-28 110503" src="https://github.com/user-attachments/assets/0aa6a2d6-58e1-4eb5-b014-7afd567baa8f" />


<h3>Step 2: Viewing Process Details</h3>
<p>Right-click on any process and choose <strong>Properties</strong>. The “Image” tab shows the process file path, command line, and creation time. This helps verify if the process is legitimate or suspicious.</p>
<img width="1892" height="1114" alt="Screenshot 2025-10-28 110524" src="https://github.com/user-attachments/assets/66c2a6dd-1ff8-4f23-a1a3-ca638d032f3b" />

<h3>Step 3: Analyzing Process Properties</h3>
<p>Explore the other tabs such as <strong>Performance</strong> and <strong>Threads</strong> to view real-time CPU usage, thread activity, and memory statistics for the selected process.</p>
<img width="1826" height="861" alt="Screenshot 2025-10-28 110807" src="https://github.com/user-attachments/assets/019e5f49-523c-4408-bca0-861aa29053fd" />

<h3>Step 4: Viewing Thread and Performance Tabs</h3>
<p>In the Threads tab, you can inspect all threads started by the process and their CPU consumption. The Performance tab shows graphs of resource usage.</p>
<img width="1575" height="862" alt="Screenshot 2025-10-28 110827" src="https://github.com/user-attachments/assets/ee15ead0-1246-41b8-97da-a37d97248050" />

<h3>Step 5: Checking Loaded DLLs</h3>
<p>Go to <strong>View → Lower Pane View → DLLs</strong> to see the list of DLLs loaded by the process. This helps in identifying injected or malicious modules.</p>
<img width="1680" height="1107" alt="Screenshot 2025-10-28 110914" src="https://github.com/user-attachments/assets/c4a2af56-12dd-4283-9736-88379b057425" />


<h3>Step 6: Verifying Process Signatures</h3>
<p>Hover over or check the <strong>Verified Signer</strong> column to confirm the authenticity of each process. A missing or invalid signature might indicate a potentially malicious file.</p>
<img width="1446" height="1006" alt="Screenshot 2025-10-28 111015" src="https://github.com/user-attachments/assets/1597588a-041f-4694-bd15-3c78b64aa2e7" />

<h3>Step 7: Handling Suspicious Processes</h3>
<p>If a suspicious process is detected, right-click on it and choose <strong>Kill Process</strong> or <strong>Suspend</strong> to stop its execution. Always confirm its path and digital signature before taking action.</p>
<img width="1903" height="1044" alt="Screenshot 2025-10-28 111045" src="https://github.com/user-attachments/assets/d1e7e1d2-778b-4e89-82d1-12aa972abae1" />


















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
 **Hence, the analysis of suspicious processes using Process Explorer was performed successfully.**

 
  
  






  
