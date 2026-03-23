# Using-tools-like-John-the-Ripper-for-password-cracking
## AIM:
To crack password hashes using John the Ripper in Kali Linux.

## DESIGN STEPS:
### Step 1:
Install John the Ripper using the command:

### Step 2:
Prepare the password hash file (e.g., using unshadow for Linux password and shadow files).


### Step 3:
Use John the Ripper to crack the hashes:

## PROGRAM:
Password Cracking with John the Ripper

## OUTPUT:
- Create an txt file 
![image](https://github.com/user-attachments/assets/e7328b13-1938-444d-bb77-6be3377f430e)

-  Create a Password-Protected ZIP File 
![image](https://github.com/user-attachments/assets/46f87c52-2b2c-48a3-916f-aaaa53cc687d)

### OR
```
zip -e secret.zip file.txt
```

- Open John-The-Ripper Tool
- 
![image](https://github.com/user-attachments/assets/fae39a60-9f20-474e-b7a1-9132d5d1d88a)

![435692993-333966f0-b113-4cca-b707-9f2d1c20a572](https://github.com/user-attachments/assets/7a69d91f-a92c-4b5d-86ec-99fa6682c2b1)

- Generate Hash Using zip2john
 
![Screenshot 2025-04-21 200236](https://github.com/user-attachments/assets/2a9a53f8-f51e-462c-979e-6d346b720280)

- cat hash.txt

![image](https://github.com/user-attachments/assets/18aa5639-556a-4a63-b983-7e6d674aac6b)

![image](https://github.com/user-attachments/assets/10c4fe4f-e04d-4d44-829d-036cf0d7f34f)


## RESULT:
The password hashes were successfully cracked using John the Ripper.
