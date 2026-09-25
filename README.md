# NETWORKWALKS-PASSWORD-CRACKING-REPORT

## Overview
This project documents a controlled cybersecurity lab focused on recovering passwords from protected PDF files by extracting
PDF hashes and performing dictionary attacks. The exercise compares a local John the Ripper (JTR)/Johnny workflow with the
Networkwalks web-based tools.

## Objectives
Demonstrate the process of recovering passwords from protected PDF files by extracting their hashes and using dictionary
attacks.
Compare the methodology of a local John the Ripper (JTR) installation with the web-based Networkwalks tools.

## Environment & Tools
Operating System: Windows
Hash Extraction: Online Hash Extractor (onlinehashcrack.com), Networkwalks Hash Calculator
Password Cracking: John the Ripper (JTR)/Johnny GUI, Networkwalks Password Cracker

## Methodology
### Module 1 — John the Ripper (JTR)
Hash Extraction: The online tool at onlinehashcrack.com was used to extract the $pdf$ hashes from the locked PDF files.
Preparation: The extracted hash values were saved into .txt files for local processing.
Cracking Process: The hash files were imported into the Johnny GUI, which provides a graphical interface for JTR, and a dictionary attack was executed to recover the passwords.
### Module 2 — Networkwalks Tools
Hash Extraction: The target PDF files were uploaded to the Networkwalks Hash Calculator to parse the files and extract their hashes within the web browser.
Cracking Process: The extracted hashes were supplied to the Networkwalks Password Cracker, where its built-in wordlist attack was executed to recover the passwords.

## Results
The dictionary attacks recovered the passwords for all three target PDF files and enabled the associated flags to be captured.
### Target 1 Evidence
#### Johnny result
<img width="960" height="564" alt="johnny1" src="https://github.com/user-attachments/assets/b7e8e10e-8186-49c4-9f3d-c3b9782800f4" />

#### Networkwalks password-cracker result
<img width="960" height="564" alt="nwpw1" src="https://github.com/user-attachments/assets/01ba9e65-f967-486f-9a72-7ff563ee8323" />

#### Captured flag
<img width="251" height="345" alt="flag1" src="https://github.com/user-attachments/assets/5e723c1b-4afd-47a2-88ac-55aaa5a83572" />


### Target 2 Evidence
#### Johnny result
<img width="960" height="564" alt="johnny2" src="https://github.com/user-attachments/assets/6a7294c8-eb2a-473d-be06-aa668e21fb70" />

#### Networkwalks password-cracker result
<img width="960" height="564" alt="nwp2" src="https://github.com/user-attachments/assets/e22c6508-d252-4427-9de8-3fcc00ec11f8" />

#### Captured flag
<img width="357" height="494" alt="flag2" src="https://github.com/user-attachments/assets/732d58ef-d8f3-4671-87db-26d21da51369" />


### Target 3 Evidence
#### Johnny result
<img width="960" height="564" alt="johnny3" src="https://github.com/user-attachments/assets/0fef6076-e746-4d09-8132-7ce749e1d4b7" />

#### Networkwalks password-cracker result
<img width="960" height="564" alt="nwpw3" src="https://github.com/user-attachments/assets/a1d7b0f2-f2fe-480f-ad0a-e39145d58860" />

#### Captured flag
<img width="367" height="470" alt="flag3" src="https://github.com/user-attachments/assets/958442c1-b60a-4d23-847e-5b886429de83" />

## Mitigation & Remediation Strategies
To reduce the likelihood of successful offline dictionary attacks, the following controls and policies should be implemented:

1. Enforce Strong Passphrases
Dictionary attacks rely heavily on common words and simple alphanumeric sequences. Long passphrases with high entropy make dictionary and brute-force attacks substantially more difficult.

2. Avoid Predictable Patterns
Users should avoid standard keyboard walks such as 1qaz2wsx or appending numbers to common words such as password1, because modern wordlists commonly test these patterns.

3. Use Strong Encryption Standards
Files should be secured using robust encryption algorithms such as AES-256 rather than legacy encryption methods, increasing the effort required for cracking attempts.

4. Consider Certificate-Based Security
For highly sensitive documents, certificate-based encryption can reduce reliance on human-selected passwords.

## Conclusion
The exercises demonstrated that predictable passwords such as password1 and 1qaz2wsx can be recovered using standard wordlists and readily available tools. The results reinforce the importance of strong password selection, avoidance of predictable patterns, and appropriate document-encryption controls when protecting files against offline hash-cracking attempts.

## Ethics & Scope
This report documents a controlled training exercise performed against designated lab files. Password-recovery and hash-cracking techniques should only be applied to systems, files, and accounts for which you have explicit authorization.

Project: PDF Hash Cracking Analysis

Training: Networkwalks Cybersecurity Internship

Author: Tawiah Prince Kodjo
