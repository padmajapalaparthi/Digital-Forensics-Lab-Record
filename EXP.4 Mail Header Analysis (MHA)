# Ex.No.4   MHA (Mail Header Analyzer)
## Aim :
- The aim is to use a Mail Header Analyzer (MHA) to trace an email's origin and verify its authenticity by examining its header for signs of spoofing.
## Procedure
### Step 1: Get the Email Header
- First, you need to copy the full, raw header from the email.

- Gmail: Open the email, click the three dots (⋮), and select Show original.
<br>
<br>
<img width="1951" height="1096" alt="image" src="https://github.com/user-attachments/assets/684d3ca9-e73e-4658-9cff-bca5639be3ad" />
<br>
<br>


- Select all the text in the header and copy it.

<br>
<img width="1913" height="1147" alt="image" src="https://github.com/user-attachments/assets/3ca951b6-d1a8-40b8-8e53-9593d9bf10e8" />
<br>
<br>

### Step 2: Use a Mail Header Analyzer (MHA)
- The easiest way to analyze the header is with an online tool.

- Navigate to a site like MXToolbox Email Header Analyzer.
 <br>
<br>

  <img width="1919" height="1053" alt="image" src="https://github.com/user-attachments/assets/43254222-09b5-4a21-9aae-6f1705bb23aa" />
<br>
<br>

- Paste the entire header you copied into the analysis box.
<br>
<br>

Click the "Analyze" button to get a parsed, easy-to-read report.
<br>
<br>

<img width="1919" height="1054" alt="image" src="https://github.com/user-attachments/assets/ddd00744-08ab-42fb-bdb6-7cc06702d5f8" />

### Step 3: Analyze The Report
- This is the most critical step. In the analyzer's report, look for the SPF, DKIM, and DMARC results.
### Review the Overall Delivery Summary
- First, look at the high-level summary to get an immediate sense of the email's status.

- Check DMARC Compliance: The report shows the email is DMARC Compliant. This is the most important overall result.

- Check SPF Status: Both SPF Authenticated and SPF Alignment passed. This means the sending server was authorized.

- Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated failed (❌). This is a critical finding and indicates a problem with the email's digital signature.
<br>
<br>

<img width="1918" height="909" alt="image" src="https://github.com/user-attachments/assets/eb5fb84a-2ef3-444a-a15c-65009272d68d" />
<br>
<br>

### Investigate the SPF Record and Email Path
- Next, verify why the SPF check passed.

- Examine the SPF Record: The SPF record for the domain is v=spf1 include:mailgun.org ~all. This record explicitly authorizes servers from Mailgun to send emails on its behalf.

- Trace the Relay Information: The delivery path shows the email was sent from m241-136.mailgun.net.

- Conclusion: Since the email came from a Mailgun server, which is authorized in the SPF record, the SPF check passed.
  <br>
  <br>
<img width="1917" height="874" alt="image" src="https://github.com/user-attachments/assets/9d3277b3-89e8-423a-a351-095dcef1f0a6" />
<br>
<br>

### Analyze the DKIM Failure

<br>
<img width="1917" height="989" alt="image" src="https://github.com/user-attachments/assets/8c62253c-68c6-42cc-b30e-d5581f4494ab" />
