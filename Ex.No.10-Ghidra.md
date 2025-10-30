# Ex.No.10 — Malware Disassembly and Analysis using Ghidra

---

## Aim
To perform static analysis of a suspicious binary file using **Ghidra**, understand its internal structure, and identify possible indicators of malicious behavior through disassembly and decompilation.

---
## Procedure

### Step 1 — Setting Up the Environment
- Launch your **virtual machine** to create a secure workspace.  
- Install and configure **Ghidra**, ensuring JDK is properly linked.  
- Prepare the binary sample to be analyzed.  

<img width="600" alt="exp10 1" src="https://github.com/user-attachments/assets/7ce1a376-46a0-4560-8f59-b8e487d858ee" />


---

### Step 2 — Loading and Initial Analysis
- Open Ghidra → Create a new project → Import the binary file.  
- Run **Auto Analysis** and select the necessary analyzers.  
- Identify the **entry point** and inspect the disassembled code.

<img width="600" alt="exp10 2" src="https://github.com/user-attachments/assets/585799ba-9095-49b7-8795-17846a95f205" />

---

### Step 3 — Function Analysis
- Use the **Decompiler** to convert assembly into C-like code for readability.  
- Rename and document key functions to better understand the program’s logic.  
- Use **Cross-References (XREF)** to track function calls and variable usage.

<img width="600" alt="exp10 4" src="https://github.com/user-attachments/assets/6050677c-dee1-41db-8b26-66a5fe67dd8e" />


---

### Step 4 — String and Import Analysis
- Explore the **Defined Strings** section to locate readable strings (e.g., IPs, file paths, registry entries).  
- Examine the **Import Table** for system API calls like `CreateFileA`, `URLDownloadToFile`, or `RegSetValueEx` which hint at malware capabilities.

<img width="600" alt="exp10 5" src="https://github.com/user-attachments/assets/a3785a35-bfb3-40e1-b581-30acd7d6b29b" />

<img width="600" alt="exp10 6" src="https://github.com/user-attachments/assets/eaa18d51-417c-44f4-a389-e717e001942f" />

---

### Step 5 — Advanced (Optional)
- Visualize the **Control Flow Graph (CFG)** to trace code execution paths.  
- Write custom scripts in Python/Java using Ghidra’s API for automated analysis.

---

## Automation Scripts (Optional Section)

| Script Name | Description |
| :----------- | :----------- |
| `extract_strings.py` | Lists all unique string references found in the binary. |
| `network_trace.py` | Detects functions using networking APIs such as `connect`, `send`, or `recv`. |
| `auto_label.py` | Automatically labels known malicious patterns like registry changes or file manipulation. |

---

## Sample Files
A collection of harmless binaries used for demonstration:

- **Example File:** `binary.txt` — a small test executable designed for disassembly practice only.  

<img width="600" alt="exp10 7" src="https://github.com/user-attachments/assets/02f82d65-a57f-4de6-8f8e-6fa9029cf3a2" />

<img width="600"  alt="exp10 8" src="https://github.com/user-attachments/assets/66fbee67-9e4f-4f19-a18a-13803d499b9b" />


<img width="600" alt="exp10 9" src="https://github.com/user-attachments/assets/239d4407-8d3c-4aca-8c31-d6eddd3366f0" />

---

## Report Format
Use this structure to document your findings:

1. **Overview:** Description of the sample and purpose of analysis.  
2. **Disassembly Observations:** List of key functions and their interpreted purpose.  
3. **Indicators of Compromise (IOCs):** Suspicious strings, network activity, or persistence behavior.  
4. **Conclusion & Recommendations:** Mitigation steps or further analysis suggestions.

---

## Result
The analysis was successfully completed using **Ghidra**.  
The binary file was disassembled, examined, and its functions and strings were analyzed.  
Thus, the objective of performing malware analysis using Ghidra was achieved.
