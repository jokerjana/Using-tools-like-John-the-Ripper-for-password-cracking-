# Using-tools-like-John-the-Ripper-for-password-cracking
# NAME: JANARTHANAN B
# REG NO : 212223100014
## AIM:
To crack password hashes using John the Ripper in Kali Linux.
## REQUIREMENTS:
- **Operating System:** Kali Linux / Ubuntu / Windows (with JtR binaries)
- **Tools:**
    - John the Ripper (Community/Pro version)
    - Hash generating tools (e.g., openssl, unshadow)
- **Test Data:**
    - /etc/shadow file (Linux hashed passwords)
    - Custom password-protected file (ZIP, RAR, etc.)
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Password Protected File / Hash] --> B[John the Ripper]
    B --> C[Select Attack Mode: Dictionary or Brute Force]
    C --> D[Load Wordlist / Charset Rules]
    D --> E[Password Cracking Process]
    E --> F[Recovered Passwords]
```
## DESIGN STEPS:
### Step 1: Install John the Ripper
```bash
sudo apt update
sudo apt install john -y
```

### Step 2: Prepare Hash File
- Extract hashes (Linux example):
```
unshadow /etc/passwd /etc/shadow > myhashes.txt
```
- For a ZIP file:
```
zip2john secret.zip > ziphash.txt
```
### Step 3: Run John the Ripper
- Dictionary Attack:
```
john --wordlist=/usr/share/wordlists/rockyou.txt myhashes.txt
```
- Brute Force (Incremental Mode):
```
john --incremental myhashes.txt
```
### Step 4: Show Cracked Passwords
```
john --show myhashes.txt
```
## PROGRAM:
1. **Hash Extraction** – Obtain password hashes from system files or encrypted archives.
2. **Attack Mode Selection** – Choose between dictionary, brute force, or hybrid.
3. **Cracking Phase** – John the Ripper runs through candidate passwords.
4. **Password Recovery** – Successfully cracked passwords are displayed.

## OUTPUT:
Cracked Passwords from Hash File
<img width="787" height="599" alt="Screenshot 2026-03-24 103859" src="https://github.com/user-attachments/assets/e6207b0a-c7c4-4d3a-a871-11ba476afaa5" />
<img width="796" height="603" alt="Screenshot 2026-03-24 103954" src="https://github.com/user-attachments/assets/bf6bd80a-5bcf-43e0-b9c2-b40f1c11fe9e" />
<img width="804" height="605" alt="Screenshot 2026-03-24 104259" src="https://github.com/user-attachments/assets/0643bd0d-58c5-4cde-952e-ac9c0c9b351b" />
<img width="798" height="595" alt="Screenshot 2026-03-24 104410" src="https://github.com/user-attachments/assets/dc601513-f3f7-4017-8c18-096c884e7dd9" />
<img width="797" height="598" alt="Screenshot 2026-03-24 104644" src="https://github.com/user-attachments/assets/23782251-41c8-4a2f-ae46-9ad62247dfaa" />


## RESULT:
The password hashes were successfully cracked using John the Ripper.

