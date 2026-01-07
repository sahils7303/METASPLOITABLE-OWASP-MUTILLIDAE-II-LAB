# METASPLOITABLE-OWASP-MUTILLIDAE-II-LAB

## Objective

To set up Metasploitable and fix the Mutillidae II database error and demonstrate OWASP Top 10 vulnerabilities.

## Tools used 🚀
- VMware Workstation Pro
- Metasploitable 2
- Kali Linux
- OWASP Mutillidae II

## Steps Performed
1. Created a new Linux user in Metasploitable as 'Sahil1'.
2. Configured MySQL using init scripts.
3. Fixed Mutillidae II database error.
4. Then, Verified Mutillidae II running successfully in browser.
5. Tested OWASP Top 10 vulnerabilities.

## Screenshots
Screenshots are provided in the screenshots folder.

# Now follow these steps to build your project

## Step 1: Login as Admin User
```bash
login: msfadmin
password: msfadmin
```
## step 2: Switch to Root (Admin privileges)
```bash
sudo su
```
## Step3: Navigate to Mutillidae Configuration Directory
```bash
cd /var/www/mutillidae
```
## Step4: List all the files
```bash
ls
```
## Step5: Open Configuration File in Nano Editor
```bash
sudo nano config.inc
```
## Step6: Change the database name from ‘metasploit’ to ‘owasp10’ :

<img width="729" height="185" alt="Image" src="https://github.com/user-attachments/assets/c84356fd-8aad-4f3f-b08f-a6d1300c7b30" />

After change it will look like

<img width="214" height="74" alt="Image" src="https://github.com/user-attachments/assets/bf9429b4-cc2a-409a-b7d4-643dc72934d0" />

## Step7: Save and Exit Nano Editor

CTRL + O  → Enter
CTRL + X

## Step8: Start / Restart Apache Server
```bash
/etc/init.d/apache2 restart
```

## Step9: Start MySQL Server (Required for Mutillidae)
```bash
/etc/init.d/mysql start
```
## Step10: Check MySQL service status
```bash
/etc/init.d/mysql status
```
## Step11: Verify Network & Get IP Address
```bash
ifconfig
```
Note down the IP address (example: 192.168.92.128)

## Step12: Open Mutillidae in Browser

http://metasploitable-IP/mutillidae

Example: 
http://192.168.92.128/mutillidae

## Step13: Reset Mutillidae Database (First Time Only)

From the Mutillidae web interface:
 - Click on Reset DB
 - Confirm database reset

## Final Result
- OWASP Mutillidae II loaded successfully
- OWASP Top 10 enabled
- Application running using admin (msfadmin) user
- Apache & MySQL services running properly

## Disclaimer

This lab is for educational and ethical hacking practice only.
