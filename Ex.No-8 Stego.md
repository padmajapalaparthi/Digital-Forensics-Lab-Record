#  Ex.No.8 — Detect Hidden Data in Images Using StegExpose
---
##  Aim

To detect hidden data in image files using **StegExpose**, a steganography analysis tool.

---
##  Step 1 — Compile the Source Code

Compile the Java files with the required dependency:

javac -cp commons-math3-3.1.1.jar -source 1.8 -target 1.8 *.java

<img width="400" alt="exp8 1" src="https://github.com/user-attachments/assets/0a35f66b-fd82-4cca-9ef3-88eee8c54139" />

 Note: Ignore warnings like `RSAnalysis.java uses unchecked or unsafe operations`. Compilation is successful if `.class` files are generated.

---

##  Step 2 — Create the Executable JAR
By using Notepad
Create a file named `manifest.mf` in the same folder:

```
Main-Class: StegExpose
```
<img width="1712" height="162" alt="exp8 4" src="https://github.com/user-attachments/assets/ede74e26-efa2-4727-8124-21acfb21d570" />

Build the JAR:

```bash
jar cfm StegExpose.jar manifest.mf *.class
```

<img width="1836" height="660" alt="exp8 2" src="https://github.com/user-attachments/assets/4116a087-0040-4f14-80a7-ee04a3866935" />



 You now have `StegExpose.jar` ready to use.

---

##  Step 3 — Run StegExpose

```bash
java -jar StegExpose.jar "C:\Users\palap\Downloads\StegExpose-master\StegExpose-master\testFolder"
```

---

##  Step 4 — Example Output

<img width="1716" height="214" alt="exp8 3" src="https://github.com/user-attachments/assets/39904131-568a-4911-bb9d-9f98149521c6" />



| Hidden Bytes   | Meaning                             |
| -------------- | ----------------------------------- |
| < 10,000       | Likely clean (no hidden data)       |
| 10,000–100,000 | Possibly contains hidden data       |
| > 100,000      | Highly likely steganography present |

---

## Step 5 — Analyze and Verify Results

The tool lists images with potential hidden data and estimates the approximate size. Further validation can be done using tools such as:

* StegSolve
* OpenStego
* zsteg
* Binwalk

---

##  Optional — Export Results Automatically

Generate a results file for easier review:

```bash
java -jar StegExpose.jar "C:\Users\palap\Downloads\StegExpose-master\StegExpose-master\testFolder" fast 0.3 results.csv

```
<img width="600" alt="exp8 4" src="https://github.com/user-attachments/assets/0c75cac4-c396-4ff7-a16b-0a7bc0df88bb" />

<img width="600"  alt="exp8 5" src="https://github.com/user-attachments/assets/27adfc08-776c-4692-92aa-61bba7a5f662" />
<br> <br>

## Rubrics
<table style="width:50%; border-collapse:collapse;" border="1"> <tr> <th>Criteria</th> <th>Mark Allotted</th> <th>Mark Awarded</th> </tr> <tr> <td>1. GitHub Activity & Submission Regularity</td> <td style="text-align:center;">3</td> <td style="text-align:center;"></td> </tr> <tr> <td>2. Application of Forensic Tools & Practical Execution</td> <td style="text-align:center;">3</td> <td style="text-align:center;"></td> </tr> <tr> <td>3. Documentation & Reporting</td> <td style="text-align:center;">2</td> <td style="text-align:center;"></td> </tr> <tr> <td>4. Engagement, Problem-Solving & Team Collaboration</td> <td style="text-align:center;">2</td> <td style="text-align:center;"></td> </tr> <tr> <td><b>Total</b></td> <td style="text-align:center;"><b>10</b></td> <td style="text-align:center;"></td> </tr> </table>

##  Result

* Successfully compiled and executed StegExpose
* Detected images containing potential hidden data
* Interpreted results and exported findings

Hidden data in image files was successfully detected using StegExpose.
