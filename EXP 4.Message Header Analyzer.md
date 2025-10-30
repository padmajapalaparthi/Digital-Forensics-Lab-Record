# Ex.No.4   MHA (Mail Header Analyzer)
## Aim :
- The aim is to use a Mail Header Analyzer (MHA) to trace an email's origin and verify its authenticity by examining its header for signs of spoofing.
## Procedure
### Step 1: Get the Email Header
- First, you need to copy the full, raw header from the email.
- Gmail: Open the email, click the three dots (⋮), and select Show original.
<img width="400" alt="IMG 4(1)" src="https://github.com/user-attachments/assets/0fb53133-c020-46a2-8f49-9335e899fdf6" />

- Select all the text in the header and copy it.
<img width="952" height="565" alt="image" src="https://github.com/user-attachments/assets/ad8ceb60-d6c3-4e67-910c-e69be79edff7" />

### Step 2: Use a Mail Header Analyzer (MHA)
- The easiest way to analyze the header is with an online tool.
- Navigate to a site like MXToolbox Email Header Analyzer.
<img width="1892" height="1023" alt="Screenshot 2025-09-01 213915" src="https://github.com/user-attachments/assets/f8665802-39ae-432d-bfff-8d39b04110be" />

- Paste the entire header you copied into the analysis box.
Click the "Analyze" button to get a parsed, easy-to-read report.
<img width="955" height="557" alt="IMG 4(3)" src="https://github.com/user-attachments/assets/75eb2b44-47db-4b88-b1bb-01a3791c7bd7" />

### Step 3: Analyze The Report
- This is the most critical step. In the analyzer's report, look for the SPF, DKIM, and DMARC results.
### Review the Overall Delivery Summary
- First, look at the high-level summary to get an immediate sense of the email's status.

- Check DMARC Compliance: The report shows the email is DMARC Compliant. This is the most important overall result.

- Check SPF Status: Both SPF Authenticated and SPF Alignment passed. This means the sending server was authorized.

- Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated failed (❌). This is a critical finding and indicates a problem with the email's digital signature.
<img width="953" height="540" alt="IMG 4(4)" src="https://github.com/user-attachments/assets/6648985d-5c19-4ad9-8129-d1f793c8af51" />

### Investigate the SPF Record and Email Path
- Next, verify why the SPF check passed.
- Examine the SPF Record: The SPF record for the domain is v=spf1 include:mailgun.org ~all. This record explicitly authorizes servers from Mailgun to send emails on its behalf.
- Trace the Relay Information: The delivery path shows the email was sent from m241-136.mailgun.net.
- Conclusion: Since the email came from a Mailgun server, which is authorized in the SPF record, the SPF check passed.

<img width="947" height="514" alt="image" src="https://github.com/user-attachments/assets/23ff84e9-e21e-4910-bf46-e172d00c572d" />

<br>

### Analyze the DKIM Failure
<img width="600" alt="image" src="https://github.com/user-attachments/assets/47029e6f-dda0-4473-b547-1e2be4c18d60" />

## Rubrics
<table style="width:50%; border-collapse:collapse;" border="1"> <tr> <th>Criteria</th> <th>Mark Allotted</th> <th>Mark Awarded</th> </tr> <tr> <td>1. GitHub Activity & Submission Regularity</td> <td style="text-align:center;">3</td> <td style="text-align:center;"></td> </tr> <tr> <td>2. Application of Forensic Tools & Practical Execution</td> <td style="text-align:center;">3</td> <td style="text-align:center;"></td> </tr> <tr> <td>3. Documentation & Reporting</td> <td style="text-align:center;">2</td> <td style="text-align:center;"></td> </tr> <tr> <td>4. Engagement, Problem-Solving & Team Collaboration</td> <td style="text-align:center;">2</td> <td style="text-align:center;"></td> </tr> <tr> <td><b>Total</b></td> <td style="text-align:center;"><b>10</b></td> <td style="text-align:center;"></td> </tr> </table>

## Result
Successfully analyzed the email header using an MHA tool. SPF and DMARC passed, confirming legitimate sender origin, while DKIM failed, indicating a possible signature issue. The experiment demonstrated how header analysis helps verify email authenticity.


