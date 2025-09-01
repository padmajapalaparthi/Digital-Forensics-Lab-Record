# Ex.No.4   MHA (Mail Header Analyzer)
## Aim :
- The aim is to use a Mail Header Analyzer (MHA) to trace an email's origin and verify its authenticity by examining its header for signs of spoofing.
## Procedure
### Step 1: Get the Email Header
- First, you need to copy the full, raw header from the email.

- Gmail: Open the email, click the three dots (⋮), and select Show original.
<br>
<br>
<img width="958" height="562" alt="IMG 4(1)" src="https://github.com/user-attachments/assets/2939cb3f-5eae-436b-a88f-cee57785ccbd" />
<br>
<br>


- Select all the text in the header and copy it.

<br>
<img width="944" height="538" alt="image" src="https://github.com/user-attachments/assets/a89db48d-40c7-4129-8b95-649c2df4769f" />
<br>
<br>

### Step 2: Use a Mail Header Analyzer (MHA)
- The easiest way to analyze the header is with an online tool.

- Navigate to a site like MXToolbox Email Header Analyzer.
 <br>
<br>
<img width="957" height="535" alt="image" src="https://github.com/user-attachments/assets/00a9f9f0-2798-4ba9-b2b6-a1ed6c1865e9" />
<br>
<br>

- Paste the entire header you copied into the analysis box.
<br>
<br>

Click the "Analyze" button to get a parsed, easy-to-read report.
<br>
<br>
<img width="955" height="557" alt="IMG 4(3)" src="https://github.com/user-attachments/assets/7fa94efb-dcf5-4871-8ae7-c2d30ca00a3c" />
### Step 3: Analyze The Report
- This is the most critical step. In the analyzer's report, look for the SPF, DKIM, and DMARC results.
### Review the Overall Delivery Summary
- First, look at the high-level summary to get an immediate sense of the email's status.

- Check DMARC Compliance: The report shows the email is DMARC Compliant. This is the most important overall result.

- Check SPF Status: Both SPF Authenticated and SPF Alignment passed. This means the sending server was authorized.

- Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated failed (❌). This is a critical finding and indicates a problem with the email's digital signature.
<br>
<br>
<img width="953" height="540" alt="IMG 4(4)" src="https://github.com/user-attachments/assets/2a9cf79d-4694-4656-ad6c-922cc9a110b1" />
<br>
<br>

### Investigate the SPF Record and Email Path
- Next, verify why the SPF check passed.

- Examine the SPF Record: The SPF record for the domain is v=spf1 include:mailgun.org ~all. This record explicitly authorizes servers from Mailgun to send emails on its behalf.

- Trace the Relay Information: The delivery path shows the email was sent from m241-136.mailgun.net.

- Conclusion: Since the email came from a Mailgun server, which is authorized in the SPF record, the SPF check passed.
  <br>
  <br>
<img width="950" height="544" alt="IMG 4(5)" src="https://github.com/user-attachments/assets/75edc96a-903a-46f9-9ecc-1594a4fcecdf" />
<br>
<br>

### Analyze the DKIM Failure

<br>
<img width="950" height="511" alt="image" src="https://github.com/user-attachments/assets/f7b4a34b-e9f9-41ee-bdd5-aa0c8983ebac" />

