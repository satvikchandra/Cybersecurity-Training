This repository contains my college project demonstrating John the Ripper for educational password cracking simulations.

# John the Ripper(JtR) password cracker.

John the Ripper is a fast password cracker, currently available for many flavors of Unix, macOS, Windows, DOS, BeOS, and OpenVMS (the latter requires a contributed patch). Its primary purpose is to detect weak Unix passwords. Besides several crypt(3) password hash types most commonly found on various Unix flavors, supported out of the box are Kerberos/AFS and Windows LM hashes, as well as DES-based tripcodes, plus hundreds of additional hashes and ciphers in "-jumbo" versions.


## How to install
Go to the official website: 
```bash
openwall.com/john.
```
Download the community edition (free):

For Windows: Download the ZIP file, extract it, and run the installer. No admin rights needed usually.

For Linux (e.g., Ubuntu): Open a terminal and run:
```bash
sudo apt update
sudo apt install john
```
For Mac: Use Homebrew if you have it installed: brew install john. Otherwise, download the source code and compile it (quick guide on the site).

Verify installation: Open a command prompt or terminal and type john --version. It should display the version number. If not, double-check your download or search for "John the Ripper installation troubleshooting" on their site.

## How to use John the Ripper

- Firstly, we will use JtR to crack password for an account we have but don't remeber the password. So, open the kali linux operating system. Here, we add a user, for example, david. We set the password for this david user. 
```bash
sudo adduser david
```
<img width="711" height="409" alt="Screenshot 2025-10-15 235402" src="https://github.com/user-attachments/assets/3b72f1fa-ad90-47bf-baa8-a5b9af719243" />

- Then we find the shadow file which contains the hash password of the david user. It is located in etc folder. We extract the contents of this shadow file using:
```bash
sudo cat shadow
```
<img width="849" height="589" alt="openshadow" src="https://github.com/user-attachments/assets/b71e6fa0-8cdf-4b56-8621-41dbb07efe7b" />

- Then we copy the hash password, create a text file on desktop and paste the hash password in the text file. To create a new file:
```bash
nano hash.txt
```
- Now we need to get a worlist file- a wordlist file contains millions of hash password. In kali linux, a file named rockyou.txt can be used as a wordlist file. Its located in wordlist folder. We need to unzip the file using
```bash
sudo gunzip rockyou.txt.gz
```
- Finally, using John the Ripper we are going to crack the password. For this, we use the syntax
```bash
sudo john -format=crypt --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
```
The password will be successfully cracked!
<img width="718" height="537" alt="crackpass" src="https://github.com/user-attachments/assets/f26c9b1b-9c8a-4516-8e1a-122f52a211f6" />

